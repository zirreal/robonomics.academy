---
title: "Introducción a la solución de código abierto para hogares inteligentes privados"
lastUpdate: Tue May 09 2023 13:56:49 GMT+0400 (Samara Standard Time)
description: Aprenderás cómo integrar soluciones de código abierto con dispositivos inteligentes económicos para hacer que tu hogar inteligente esté orientado de forma privada y no dependa de la nube en su funcionamiento.
metaOptions: [Aprender]
defaultName: Introduction to open source solution for private smart homes
---

<LessonImages src="smart-home-intro/open-source-private-smart-home-intro.png" imageClasses="mb full" />

<RoboAcademyText>
  ¡Hola a todos! Hoy quiero llevarlos a una conversación sobre un hogar inteligente, cuándo se necesita, de qué se compone y qué puede ofrecer.
</RoboAcademyText>

## Hogares inteligentes: Solucionando problemas de calefacción y agua caliente

En 2022, me mudé a Chipre y tuve que acostumbrarme rápidamente a las condiciones de vida en un lugar nuevo. Después de Rusia, la diferencia en la actitud hacia el uso de los recursos energéticos se siente especialmente agudamente. Por ejemplo, en Chipre no hay calefacción central. Y hasta diciembre, no podías pensar en ello. Y luego resultó que la temperatura de mi dormitorio es la misma que la temperatura fuera de la ventana. Para ser honesto, es incómodo dormir a +10 °C ... ¡brrr!

## Potencia tus ahorros con el monitoreo del hogar inteligente

Además, tampoco hay suministro central de agua caliente. Hay calentadores que se instalan en el techo y se calientan con el sol. Pero en invierno el sol no es suficiente para calentar el tanque de agua. El apartamento tiene un interruptor que enciende el elemento calefactor dentro del tanque. Lo primero que resulta incómodo es que necesitas encenderlo con anticipación. Media hora a una hora antes de ducharte. Por la noche, este escenario sigue siendo aceptable, pero por la mañana nunca tendrás agua caliente. En segundo lugar, puedes olvidar fácilmente apagarlo. Como resultado: un elemento calefactor quemado y una factura de electricidad.

Por cierto, la electricidad es muy cara aquí, y debes pagarla cada 2 meses. Es imposible, en este momento, determinar el consumidor principal. Sería bueno tener estadísticas sobre los principales consumidores eléctricos, como el aire acondicionado, la calefacción por suelo radiante, la iluminación, etc. Teniendo datos en tiempo real sobre el consumo de energía a mano, al menos puedes comenzar a analizar en qué se gasta.

## Componentes esenciales de un hogar inteligente: interruptores, sensores y medidores inteligentes

Resulta que los primeros candidatos para dispositivos inteligentes son varios interruptores y monitoreo del consumo de energía. Luego, probablemente pensarás en controlar el aire acondicionado y la calefacción por suelo radiante según un horario o según las lecturas de temperatura. Esto significa que necesitaremos sensores de temperatura y humedad, relés para controlar la calefacción por suelo radiante y controles remotos por infrarrojos para los aires acondicionados. Cada casa también tiene ventanas, y las ventanas suelen tener cortinas: sería genial que al acostarte las cortinas caigan automáticamente. Así, los interruptores, sensores y medidores inteligentes forman la base de un hogar inteligente. Y luego puedes soñar en función de necesidades específicas.

## Elegir la solución adecuada para el hogar inteligente: KNX vs. Sonoff vs. Xiaomi

¿Qué soluciones de hogar inteligente y automatización hay en el mercado? Podemos pensar en KNX, que hoy es una de las soluciones más comunes para su uso en sistemas de automatización medianos y grandes para hogares, oficinas y locales comerciales. Ha estado en el mercado durante más de veinte años y ahora es compatible con muchos fabricantes importantes de equipos eléctricos. Sin embargo, para ensamblar una solución KNX, se necesita hacer mucho trabajo de ingeniería. La lógica principal se ensambla, por lo general, en un cuadro de interruptores separado. Si no se previó originalmente, la instalación en un apartamento existente puede ser difícil o imposible, sin realizar cambios apropiados en la distribución. Además, las soluciones basadas en KNX son bastante caras.

Otro enfoque podría ser comprar dispositivos de fabricantes chinos como Sonoff o Xiaomi. Su principal ventaja es el precio, la facilidad de instalación y configuración. Cualquiera podrá instalar la mayoría de los sensores y dispositivos en sus hogares. En algún lugar puede que necesites un electricista, por ejemplo, para instalar interruptores inteligentes, pero ocuparán el lugar de los antiguos y no tendrás que hacer cambios en la distribución del apartamento. El fabricante ofrece una sola aplicación para gestionar los dispositivos. Sin embargo, siempre debes recordar que tus datos se envían a algún servidor, y toda comunicación con los dispositivos es imposible sin una conexión a Internet.


## Hogar inteligente DIY: Construyendo un servidor doméstico para un control total

Y otro enfoque para construir un hogar inteligente se basa en el segundo, es decir, utilizar dispositivos disponibles de los mismos fabricantes chinos, pero además instalar un servidor doméstico en tu apartamento/casa para deshacerte de las nubes. Este es el camino que tomamos en nuestra solución de hogar inteligente. En las siguientes partes, hablaré en detalle sobre el montaje de nuestro stand de demostración y sus capacidades.

<RoboAcademyText fWeight="500">
  ¡Eso es todo por ahora! En la próxima lección, profundizaremos en el lado práctico de la construcción de un hogar inteligente y te mostraremos cómo ensamblar un Tablero de Hogar Inteligente. ¡Mantente atento y prepárate para dar tu primer paso hacia la creación de un hogar completamente funcional y automatizado.
</RoboAcademyText>