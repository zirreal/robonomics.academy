---
title: Proyectos basados en ROS para espacios inteligentes
lastUpdate: Thu May 04 2023 12:53:19 GMT+0400 (Samara Standard Time)
description: Proyectos basados en ROS para espacios inteligentes
metaOptions: [Aprender]
defaultName: ROS-based projects for smart spaces
---

A lo largo de sus 15 años de desarrollo, el marco del Sistema Operativo de Robots se integró con docenas de [dispositivos robóticos diversos](https://robots.ros.org/), e incluso hay más paquetes con algoritmos y herramientas desarrolladas por la comunidad. A decir verdad, ahora hay tantos proyectos, y el caos del estilo de descripción de sus repositorios ha crecido tanto que actualmente es bastante problemático encontrar proyectos dedicados a un tema específico. 

Aquí encontrarás una lista modesta de proyectos basados en ROS que están dedicados a robots y dispositivos IoT destinados para su uso en un entorno doméstico u oficina. Este tema es uno de los pilares de la plataforma Robonomics. Nuestro objetivo es intentar llevar estos proyectos a la par con Robonomics, tanto desde un punto de vista de integración técnica como desde la perspectiva de una aplicación interesante de estos dispositivos en una economía robótica. Siéntete libre de utilizar esta lista en tu búsqueda de ideas e inspiración.

Puedes ver algunos ejemplos de proyectos ROS integrados con Robonomics en nuestra sección de [Aprender](/learn).

<!-- En este momento (**Abril 2021**), Robonomics está orientado hacia las versiones de ROS **Melodic** y **Noetic**. Las versiones anteriores también pueden funcionar, pero puede ser necesario realizar trabajo adicional de integración. En el futuro, se añadirá soporte para la versión 2 de ROS. -->

Los principales recursos para buscar repositorios y paquetes de ROS se pueden acceder [aquí](https://index.ros.org/).

## Simulación

Antes de centrar nuestra atención únicamente en dispositivos, vale la pena recordar que para una gran cantidad de proyectos de ROS, existe la opción de probarlos en una simulación. La herramienta más popular para el modelado 3D de varios robots bajo ROS es el simulador [Gazebo](http://gazebosim.org/) y su proyecto derivado, [Ignition](https://index.ros.org/r/ros_ign/). Ambos simuladores permiten modelar dispositivos en diversos entornos interiores y exteriores difíciles, modificar el modelo y el entorno en sí, probar algoritmos de control y depurar antes de pasar al dispositivo real. Además, esta es una excelente herramienta para entrenamiento y situaciones en las que no se dispone de un dispositivo real.

En general, esta es una de las mejores opciones para intentar integrar Robonomics con un dispositivo ROS sin ningún gasto en absoluto. Un escenario real simplemente requeriría modificaciones de código ligeras. Para Gazebo, Robonomics tiene una guía detallada que consta de dos partes que cubren [configuraciones](https://wiki.robonomics.network/docs/en/connect-any-ros-compatible-robot-under-robonomics-parachain-control-1/) e [integraciones](https://wiki.robonomics.network/docs/en/connect-any-ros-compatible-robot-under-robonomics-parachain-control-2/) (usando un dron como ejemplo). El principal desafío está en encontrar un modelo listo (por ejemplo, [aquí](https://github.com/osrf/gazebo_models)) para Gazebo o intentar crear tu propio modelo utilizando el [SDFormat](http://sdformat.org/) desarrollado para simuladores. 

## Computadoras de placa única y otras placas

Estas placas actúan como un componente base para conectar otros dispositivos a ROS, principalmente sensores y dispositivos de grabación (grabadoras de audio, foto y video, cámaras, sensores de temperatura, presión y concentración de sustancias) porque el concepto de un espacio inteligente implica la creación de un [gemelo digital](https://gateway.pinata.cloud/ipfs/QmNNdLG3vuTsJtZtNByWaDTKRYPcBZSZcsJ1FY6rTYCixQ/Robonomics_keypoint_March_2021.pdf) de objetos de infraestructura. Además, las placas pueden actuar como el dispositivo informático principal y controlador para construir un dispositivo móvil robótico. A continuación se presenta una lista de placas que admiten ROS:

| Name and link                                                                                         |                                    Description                                  | ROS version | Last update |
|:-----------------------------------------------------------------------------------------------------:|---------------------------------------------------------------------------------|:-----------:|:-----------:|
|  [Raspberry Pi](http://wiki.ros.org/ROSberryPi/Installing%20ROS%20Melodic%20on%20the%20Raspberry%20Pi)| single board computer; RaspPi versions 2, 3 and 4 are available                 |   melodic   |     2020    |
|    [Arduino](http://wiki.ros.org/rosserial_arduino)                                                   | single board computer                                                           |    noetic   |     2021    |
|    [Phidgets](http://wiki.ros.org/phidgets)                                                           | sets of boards, various sensors and devices: Ph sensor, LED, RFID, motor control|    noetic   |     2020    |
|   [Sense HAT](https://wiki.ros.org/sensehat_ros)                                                      | shield for RaspPi with a set of sensors and LED                                 |    noetic   |     2020    |
|     [Navio2](https://navio2.emlid.com/)                                                               | autopliot shield for RaspPi 2,3,4                                               |    noetic   |     2020    |
|     [OpenCR](http://wiki.ros.org/opencr)                                                              | robot controller                                                                |    noetic   |     2021    |

<br/>

## Dispositivos para el hogar inteligente y robots domsticos

Aquí se presentan dispositivos ROS cuyo uso inicial fue para hogares inteligentes u oficinas. La lista varía ampliamente, desde aspiradoras y asistentes robóticos hasta sistemas de control del hogar.

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

## Plataformas móviles y manipuladores

En primer lugar, ROS es conocido por apoyar la robótica móvil, desde drones hasta manipuladores industriales, para los cuales se crearon muchos paquetes que realizan la localización y mapeo simultáneos ([SLAM](http://wiki.ros.org/rtabmap_ros)), resuelven la tarea directa e inversa de cinemática, [planificación de trayectorias](https://moveit.ros.org/), y más. La robótica móvil está penetrando gradualmente en la vida cotidiana, por lo que es ciertamente interesante probar los robots ROS existentes en su uso dentro de un espacio inteligente. La lista general de plataformas móviles basadas en ROS es bastante grande, por lo que aquí hemos seleccionado aquellas que son potencialmente convenientes para operar en un espacio doméstico u oficina. 

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