---
title: Проекти на основі ROS для розумних просторів
lastUpdate: Thu May 04 2023 12:53:19 GMT+0400 (Samara Standard Time)
description: Проекти на основі ROS для розумних просторів
metaOptions: [Вчитися]
defaultName: ROS-based projects for smart spaces
---

Протягом своїх 15 років розвитку фреймворк Robot Operating System був інтегрований з десятками [різних робототехнічних пристроїв](https://robots.ros.org/), і є ще більше пакетів з алгоритмами та інструментами, розробленими спільнотою. Правду кажучи, зараз існує так багато проектів, і хаотичність стилю опису їх репозиторіїв зросла настільки, що в даний момент досить проблематично знайти проекти, присвячені конкретній темі. 

Тут ви знайдете скромний список проектів на основі ROS, які присвячені роботам та Інтернету речей, призначених для використання в домашньому або офісному середовищі. Ця тема є однією з основних складових платформи Robonomics. Нашою метою є спроба привести ці проекти на шлях з Robonomics, як з точки зору технічної інтеграції, так і з точки зору цікавого застосування цих пристроїв в роботизованій економіці. Вільно використовуйте цей список у своєму пошуку ідей та натхнення.

Ви можете переглянути деякі приклади проектів на основі ROS, інтегрованих з Robonomics у нашому [розділі Навчання](/learn).

<!-- На даний момент (**квітень 2021 року**), Robonomics орієнтований на версії ROS **Melodic** та **Noetic**. Старіші версії також можуть працювати, але може знадобитися додаткова робота з інтеграції. У майбутньому буде додана підтримка версії ROS 2. -->

Основні ресурси для пошуку репозиторіїв та пакетів ROS можна знайти [тут](https://index.ros.org/).

## Симуляція

Перш ніж звертати увагу виключно на пристрої, варто пам'ятати, що для великої кількості проектів ROS існує можливість тестування їх у симуляції. Найпопулярнішим інструментом для 3D-моделювання різних роботів під управлінням ROS є симулятор [Gazebo](http://gazebosim.org/) та його проект-нащадок, [Ignition](https://index.ros.org/r/ros_ign/). Обидва симулятори дозволяють моделювати пристрої в різних складних внутрішніх та зовнішніх середовищах, змінювати модель та саме середовище, тестувати алгоритми керування та відлагоджувати перед переходом до реального пристрою. Крім того, це відмінний інструмент для навчання та ситуацій, коли реальний пристрій відсутній.

Загалом, це один з найкращих варіантів спроби інтегрувати Robonomics з пристроєм ROS без будь-яких витрат. Реальний сценарій потребуватиме лише незначних змін у коді. Для Gazebo Robonomics має докладний посібик, який складається з двох частин, що охоплюють [налаштування](https://wiki.robonomics.network/docs/en/connect-any-ros-compatible-robot-under-robonomics-parachain-control-1/) та [інтеграції](https://wiki.robonomics.network/docs/en/connect-any-ros-compatible-robot-under-robonomics-parachain-control-2/) (з використанням дрона як прикладу). Основний виклик полягає в пошуку готової моделі (наприклад, [тут](https://github.com/osrf/gazebo_models)) для Gazebo або спробі створити власну модель за допомогою [SDFormat](http://sdformat.org/), розробленого для симуляторів. 

## Одноплатні комп'ютери та інші плати

Такі плати виступають як базовий компонент для підключення інших пристроїв до ROS, в основному сенсорів та пристроїв запису (аудіо, фото та відеокамер, камер, датчиків температури, тиску та концентрації речовини), оскільки концепція розумного простору передбачає створення [цифрового двійника](https://gateway.pinata.cloud/ipfs/QmNNdLG3vuTsJtZtNByWaDTKRYPcBZSZcsJ1FY6rTYCixQ/Robonomics_keypoint_March_2021.pdf) об'єктів інфраструктури. Крім того, плати можуть виступати як основний обчислювальний пристрій та контролер для побудови роботизованого мобільного пристрою. Нижче наведений список плат, які підтримують ROS:

| Name and link                                                                                         |                                    Description                                  | ROS version | Last update |
|:-----------------------------------------------------------------------------------------------------:|---------------------------------------------------------------------------------|:-----------:|:-----------:|
|  [Raspberry Pi](http://wiki.ros.org/ROSberryPi/Installing%20ROS%20Melodic%20on%20the%20Raspberry%20Pi)| single board computer; RaspPi versions 2, 3 and 4 are available                 |   melodic   |     2020    |
|    [Arduino](http://wiki.ros.org/rosserial_arduino)                                                   | single board computer                                                           |    noetic   |     2021    |
|    [Phidgets](http://wiki.ros.org/phidgets)                                                           | sets of boards, various sensors and devices: Ph sensor, LED, RFID, motor control|    noetic   |     2020    |
|   [Sense HAT](https://wiki.ros.org/sensehat_ros)                                                      | shield for RaspPi with a set of sensors and LED                                 |    noetic   |     2020    |
|     [Navio2](https://navio2.emlid.com/)                                                               | autopliot shield for RaspPi 2,3,4                                               |    noetic   |     2020    |
|     [OpenCR](http://wiki.ros.org/opencr)                                                              | robot controller                                                                |    noetic   |     2021    |

<br/>

## Пристрої для розумного дому та побутові роботи

Тут представлені пристрої ROS, призначені спочатку для розумних домів або офісів. Список різноманітний, від пилососів та роботизованої допомоги до систем управління домом.

| Name and link                                             | Description                                                 |          ROS version          | Last update |
|:---------------------------------------------------------:|-------------------------------------------------------------|:-----------------------------:|:-----------:|
|  [Care-O-bot 4](http://wiki.ros.org/care-o-bot)           | household robot-assistant; a simulation is available        |            melodic            |     2021    |
|     [Kobuki](http://wiki.ros.org/kobuki)                  | mobile platform with different use cases (e.g. a waiter)    |            melodic            |     2020    |
|    [QTrobot](http://wiki.ros.org/Robots/qtrobot)          | humanoid social robot                                       | kinetic (melodic can be used) |     2020    |
|      [Nao](http://wiki.ros.org/nao)                       | humanoid robot; a simulation is available                   |            Melodic            |     2020    |
|     [TIAGo](http://wiki.ros.org/Robots/TIAGo)             | service robot with a manipulator; a simulation is available |            kinetic            |     2020    |
|     [Roomba](https://github.com/AutonomyLab/create_robot) | robot vacuum cleaner                                        |            melodic            |     2020    |
|    [OpenHAB](http://wiki.ros.org/iot_bridge)              | home automation system                                      |            kinetic            |     2017    |
|     [Sesame](https://index.ros.org/p/sesame_ros/)         | smart lock                                                  |            melodic            |     2021    |

<br/>

## Мобільні платформи та маніпулятори

Перш за все, ROS відомий підтримкою мобільної робототехніки, від дронів до промислових маніпуляторів, для яких було створено багато пакетів, які реалізують одночасну локалізацію та картографування ([SLAM](http://wiki.ros.org/rtabmap_ros)), вирішують пряму та обернену задачу кінематики, [планування траєкторії](https://moveit.ros.org/), тощо. Мобільна робототехніка поступово проникає в повсякденне життя, тому цікаво випробувати існуючі ROS-роботи у їх використанні в розумному просторі. Загальний список мобільних платформ на основі ROS досить великий, тому тут ми вибрали ті, які потенційно зручно використовувати в домашньому або офісному просторі. 

| Name and link                                             | Description                                | ROS version | Last update |
|:---------------------------------------------------------:|--------------------------------------------|:-----------:|:-----------:|
|   [turtlebot](http://wiki.ros.org/turtlebot3)             | mobile platform tailored for ROS           |    noetic   |     2020    |
|    [GoPiGo3](http://wiki.ros.org/Robots/gopigo3)          | mobile robot based on RaspPi               |   melodic   |     2020    |
|    [LoCoBot](http://wiki.ros.org/locobot)                 | mobile manipulator                         |   kinetic   |     2020    |
|   [ROSbot 2.0](http://wiki.ros.org/Robots/ROSbot-2.0)     | mobile platform; a simulation is available |    noetic   |     2021    |
|     [VOLTA](http://wiki.ros.org/Robots/Volta)             | mobile platform; a simulation is available |   melodic   |     2021    |
|    [evarobot](http://wiki.ros.org/Robots/evarobot)        | mobile platform; a simulation is available |    noetic   |     2020    |
|    [Freight](http://wiki.ros.org/Robots/freight)          | mobile platform; a simulation is available |   melodic   |     2021    |
|      [PR2](http://wiki.ros.org/Robots/PR2)                | mobile platform; a simulation is available |   melodic   |     2021    |