---
title: "Feecc演示"
description: 本课程主要介绍Feecc系统及其所有组件。
metaOptions: [学习，熟悉Feecc]
defaultName: Getting Used to Feecc
---

<RoboAcademyText fWeight="500">
在本课程中，您将使用虚拟测试平台测试Feecc的基本功能，该平台以生产跟踪系统的实例为例进行模拟，类似于真实生产跟踪系统。
</RoboAcademyText>

为了演示目的，它缺少一些典型功能，如标签打印或视频录制，但它包含了这种系统的主要概念。

## 先决条件

要运行演示，您需要:

- 类UNIX系统（在[Ubuntu 22.04.2](https://releases.ubuntu.com/jammy/)上测试通过）
- [Docker](https://docs.docker.com/engine/install/ubuntu/)和[Docker compose](https://docs.docker.com/compose/)
- Web浏览器（在Google Chrome和Mozilla Firefox上测试通过）

## 安装

执行以下命令:

<LessonCodeWrapper language="bash">
git clone https://github.com/Multi-Agent-io/feecc-academy
cd feecc-academy
sudo docker compose up -d --build
</LessonCodeWrapper>

要检查工作容器，请运行以下命令:

<LessonCodeWrapper language="bash">
sudo docker ps -a
</LessonCodeWrapper>

您应该看到以下输出:

<LessonCodeWrapper language="bash" codeClass="big-code" noLines noCopyIcon>
CONTAINER ID   IMAGE                               COMMAND                  CREATED          STATUS                             PORTS     NAMES
0db8382bb271   feecc-academy-workbench-daemon      "uvicorn app:app --h…"   19 seconds ago   Up 7 seconds (healthy)                       feecc_academy_workbench_daemon
0dbc7bb977d1   feecc-academy-workbench-frontend    "node nodeServer.js"     20 seconds ago   Up 19 seconds (health: starting)             feecc_academy_workbench_frontend
a74fa229eb90   robonomics/robonomics:sha-bd71a23   "robonomics --dev --…"   20 seconds ago   Up 19 seconds (health: starting)             feecc_academy_robonomics_node
0c9e8022658a   mongo:jammy                         "docker-entrypoint.s…"   20 seconds ago   Up 19 seconds (healthy)                      feecc_academy_mongoDB
6b0748904d0f   ipfs/go-ipfs:v0.17.0                "/sbin/tini -- /usr/…"   20 seconds ago   Up 19 seconds (healthy)                      feecc_academy_ipfsnode
814e6f489a77   nyurik/alpine-python3-requests      "tail -f /dev/null"      20 seconds ago   Up 19 seconds                                feecc_academy_hid_emulator
</LessonCodeWrapper>

## 启动演示

1. 在浏览器中转到http://localhost:3000/，您应该看到一个欢迎屏幕。

2. 在此阶段，系统应提示员工将其RFID卡放在扫描仪上进行授权。在演示中，您可以使用`hid-emulator.py`进行授权。要执行此操作，请运行一个单独的Docker容器:

<LessonCodeWrapper language="bash">
sudo docker exec -ti feecc_academy_hid_emulator sh
python3 hid-emulator.py
</LessonCodeWrapper>

它能够模拟两个功能: 提供RFID卡和扫描条形码; 您需要第一个功能，请输入`1`。

<LessonCodeWrapper language="bash" codeClass="big-code" noLines noCopyIcon>
> Select emulated action (1/2): 
>  1. Put ID card on the RFID扫描仪.
>  2. Scan a sample barcode with a barcode scanner.
> 1
> INFO:2023-03-21 21:42:05,370:Event relayed to endpoint http://127.0.0.1:5000/workbench/hid-event
</LessonCodeWrapper>

3. 选择组合类型的屏幕将显示，选择`单个设备`。

<LessonImages src="feecc-course/menu.png" alt="Feecc start menu"/>

4. 通知将出现在左下角，指示为其创建唯一ID的设备开始工作。蓝色通知还将显示虚拟打印机的活动；在实际设置中，此时将打印带有设备ID的条形码。

<LessonImages src="feecc-course/single_device.png" alt="Single device composition"/>

5. 点击`开始组合`开始记录设备组装过程。您将被提示完成所有必要的组装步骤；每当员工完成一步时，他们应单击`下一步`按钮，之后视频将保存到IPFS。还可以暂停组装（`暂停`）以稍后返回或完全停止该过程（`停止`）。

6. 当所有组装阶段完成后，`完成`按钮将出现，之后Feecc建议保存设备的证书。但是，在执行此操作之前，请在浏览器中打开[本地Robonomics节点](https://polkadot.js.org/apps/?rpc=ws%3A%2F%2F127.0.0.1%3A9944#/explorer)，稍后会用到。之后，返回到Feecc并单击`保存护照`。
    
    您将在屏幕角落看到新的通知：证书已上传到Robonomics和IPFS，以及两条关于打印封条标签和指向证书的QR码的蓝色消息。

<LessonImages src="feecc-course/single_certificate.png" alt="Cetrificate of single composition"/>

7. 在Robonomics本地节点屏幕的`链信息`部分下，您应该看到`最近事件`列下的新事件`datalog.NewRecord`。如果展开它，将显示与设备证书文件对应的IPFS CID在`字`字段中。

<LessonImages src="feecc-course/single_datalog.png" alt="Datalog of single composition"/>

打印的QR码包含指向此CID的链接，可在浏览器中打开证书文件。由于您的本地IPFS节点可能无法发现该文件，您可以通过`localhost:8080/ipfs/CID`在本地访问该文件。证书的内容看起来像：

<LessonCodeWrapper language="json" codeClass="big-code" noLines noCopyIcon>
Unit Unique Code: 423d3c1b42f6427e80cc881a16e07451
Unit Model Name: Single Device
Total Assembly Time: 0:05:37
Production Stages:
- Name: Prepare Tools (not finished.)
  Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
  Start Time: 26-06-2023 17:38:47
  Finish Time: 26-06-2023 17:40:28
  Assembly data in IPFS: This is a place for any production data, let it be video
    record, some sensor data or any other data collection representing the production
    process.
- Name: Prepare Tools (not finished.)
  Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
  Start Time: 26-06-2023 17:40:30
  Finish Time: 26-06-2023 17:42:06
  Assembly data in IPFS: This is a place for any production data, let it be video
    record, some sensor data or any other data collection representing the production
    process.
- Name: Prepare Tools
  Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
  Start Time: 26-06-2023 17:42:16
  Finish Time: 26-06-2023 17:43:00
  Assembly data in IPFS: This is a place for any production data, let it be video
    record, some sensor data or any other data collection representing the production
    process.
- Name: Saw Through the Single Device
  Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
  Start Time: 26-06-2023 17:43:00
  Finish Time: 26-06-2023 17:43:51
  Assembly data in IPFS: This is a place for any production data, let it be video
    record, some sensor data or any other data collection representing the production
    process.
- Name: Stack Tools
  Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
  Start Time: 26-06-2023 17:43:51
  Finish Time: 26-06-2023 17:44:36
  Assembly data in IPFS: This is a place for any production data, let it be video
    record, some sensor data or any other data collection representing the production
    process.
</LessonCodeWrapper>

8. 现在让我们尝试为由多个设备组成的复合组装创建证书。在类型选择菜单中，点击`复合设备`，然后`示例设备`。复制其单元ID（位于组合编号字段中），稍后会用到。然后，继续执行组装设备的标准步骤。

9. 组装完成后，返回到`复合设备`并按`最终组装`以完成复合组装。系统将要求您提供已组装设备的单元ID，员工必须扫描其条形码。为模拟此过程，返回到`hid-emulator.py`并选择条形码扫描的功能`2`，然后将保存的单元ID插入其中。

10. 接下来，系统将提示您通过复合组装的必要阶段并为其生成证书：

<LessonCodeWrapper language="json" codeClass="big-code" noLines noCopyIcon>
Unit Unique Code: d08101feae7c4efbb5529885c9ad544b
Unit Model Name: Composite Device
Total Assembly Time: 0:00:03
Production Stages:
- Name: Prepare Tools
  Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
  Start Time: 26-06-2023 18:18:25
  Finish Time: 26-06-2023 18:18:26
  Assembly data in IPFS: This is a place for any production data, let it be video
    record, some sensor data or any other data collection representing the production
    process.
- Name: Tape the Sample Device to the base plate
  Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
  Start Time: 26-06-2023 18:18:26
  Finish Time: 26-06-2023 18:18:27
  Assembly data in IPFS: This is a place for any production data, let it be video
    record, some sensor data or any other data collection representing the production
    process.
- Name: Stack Tools
  Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
  Start Time: 26-06-2023 18:18:27
  Finish Time: 26-06-2023 18:18:28
  Assembly data in IPFS: This is a place for any production data, let it be video
    record, some sensor data or any other data collection representing the production
    process.
Unit Components:
- Unit Unique Code: b165b382c3674127a6aaf5817c5a7040
  Unit Model Name: Sample Device
  Total Assembly Time: 0:00:03
  Production Stages:
  - Name: Prepare Tools
    Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
    Start Time: 26-06-2023 18:17:45
    Finish Time: 26-06-2023 18:17:46
    Assembly data in IPFS: This is a place for any production data, let it be video
      record, some sensor data or any other data collection representing the production
      process.
  - Name: Assemble Sample Device
    Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
    Start Time: 26-06-2023 18:17:46
    Finish Time: 26-06-2023 18:17:47
    Assembly data in IPFS: This is a place for any production data, let it be video
      record, some sensor data or any other data collection representing the production
      process.
  - Name: Stack Tools
    Employee Code: e9b69b302f72d82ca47964196536aab3f36e367910aff06d2be30888f9ad4234
    Start Time: 26-06-2023 18:17:47
    Finish Time: 26-06-2023 18:17:48
    Assembly data in IPFS: This is a place for any production data, let it be video
      record, some sensor data or any other data collection representing the production
      process.
Total Assembly Time (Including Components): 0:00:06
</LessonCodeWrapper>

11. 要删除演示，请输入命令：

<LessonCodeWrapper language="bash">
sudo docker compose down --rmi all && docker builder prune -f
</LessonCodeWrapper>

<RoboAcademyText fWeight="500">
在下一课中，我们将继续进行Feecc系统所有必要组件的实际部署。
</RoboAcademyText>