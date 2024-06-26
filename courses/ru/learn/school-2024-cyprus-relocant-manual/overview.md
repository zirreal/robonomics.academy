---
title: "Robonomics School 2024 / Курс релоканта на Кипр: Умный дом"
lastUpdate: 
description: "Курс релоканта на Кипр: Умный дом"
metaOptions: [Learn, "Robonomics School 2024 / Курс релоканта на Кипр: Умный дом"]
defaultName: "Robonomics School 2024 / Cyprus Relocant Manual: Smart Home"
---

<LessonImages imageClasses="mb"  src='school-2024-cyprus-relocant-manual/Setup_SmartHome-Academy.jpg' alt="Cyprus Relocant Manual Cover" />

Изменение страны проживания всегда приносит не только новые возможности, но и вызовы. Так случилось, что в моем случае новой страной стал Кипр, куда я приехал строить компанию. Последние 10 лет до переезда я жил в большом городе, где успел привыкнуть к определенным благам в виде центрального отопления от города, горячего водоснабжения, дешевому электричеству. На Кипре каждый дом и каждая квартира гораздо более автономный в плане жизнеобеспечения, но заботы о поддержании комфортной жизни ложатся на владельца. Взять, например, горячую воду. В холодные месяцы приходится самостоятельно включать бойлер, чтобы её нагреть. Квартиру тоже нужно отапливать самостоятельно. Зимой включаем/выключаем термоодеяло и бойлер, а летом кондиционер и средство от комаров. Это требует не только времени и энергии, но и денег.

Моя первая зима на Кипре вылилась в астрономические счета за электричество. Это был серьезный удар по моему бюджету. Одно из возможных решений: изменить свои привычки и подстроиться под новые условия. Но после переезда у вас и так будет достаточно забот. Будучи инженером, я начал искать решения, которые помогли бы мне контролировать расходы и сделать жизнь комфортнее, и хочу поделиться с вами опытом.

## Выбор оборудования

Первое с чего хочется начать - выбор экосистемы. Проводные системы сразу отпадают, так как требуют больших бюджетов и серьезного вмешательства в инфраструктуру квартиры/дома. Из беспроводных существует огромное количество устройств под брендами Sonoff и Tyua, но все они работают через интернет, который не всегда стабильно работает на острове. Это не говоря уже про вопрос приватности и сохранности ваших персональных данных на чужих серверах. Я рекомендую строить свой умный дом на основе домашнего сервера с [Home Assistant](https://www.home-assistant.io) на борту. Из плюсов: может работать без доступа во внешний интернет; есть возможность забрать с собой при переезде и развернуть на новом месте, не потеряв настройки; поддержка огромного количества устройств, в том числе умные телевизоры, пылесосы, и многое другое.

Самые популярные протоколы беспроводного подключения устройств это Wi-Fi, Zigbee, Bluetooth. В одной квартире могут встретиться все три вида подключения сразу, но что касается устройств, делающих из обычных вещей умные, удобнее работать с протоколом Zigbee. В этом случае нам не нужно заботиться об их адресах и зоне покрытия, плюс они могут работать от батарейки. Wi-Fi устройства требуют постоянного подключения к питанию, и они зависимы от уровня сигнала Wi-Fi. Даже в небольшой квартире, где есть пару стен между роутером и вашей спальней, порой приходится ставить Wi-Fi Extender. В случае с Zigbee, устройства сами выполняют роль ретрансляторов.

Возвращаясь на Кипр, мой необходимый минимум устройств получился следующим:

## Компьютер - домашний сервер

Конечная задача для сервера - это обслуживать умный дом под управлением Home Assistant. Проще всего взять уже преднастроенный [Home Assistant Green](https://www.home-assistant.io/green/). Стоимость [€70 без налога](https://thepihut.com/products/home-assistant-green).

<LessonImages  src="school-2024-cyprus-relocant-manual/home-assistant-green.png" alt="Home Assistant green"/>

Вариант чуть продвинутей, но зато можно иметь контроль даже над операционной системой, это найти/купить [Raspberry Pi](https://www.raspberrypi.com). Стоимость [€90 без налога](https://https://thepihut.com/products/raspberry-pi-5-starter-kit). На странице [Installation](https://www.home-assistant.io/installation/) приведено много вариантов на все вкусы.

<LessonImages imageClasses="small" src="school-2024-cyprus-relocant-manual/raspberry-pi.png" alt="Raspberry Pi"/>

В качестве Zigbee Coordinator берем [Sonoff Zigbee Dongle P или E](https://sonoff.tech/product/gateway-and-sensors/sonoff-zigbee-3-0-usb-dongle-plus-p/), они практически всегда в наличии на острове. Стоимость около [€35](https://www.amazon.de/-/en/dp/B09KXTCMSC/). Так же можно подобрать себе стик из [этого списка](https://www.zigbee2mqtt.io/guide/adapters/).

<LessonImages imageClasses="small" src="school-2024-cyprus-relocant-manual/sonoff-zigbee-stick.png" alt="Sonoff Zigbee USB Stick"/>

Очень рекомендую закрепить статический локальный IP адрес для домашнего сервера. Если нет возможности попасть в настройки роутера, то дополнительно можно поставить второй роутер (у меня [MikroTik](https://mikrotik.com/product/hap_ax2), примерно [€80](https://www.mstronics.com/c/337_1345_485/networking-devices-routers.html?filter_id=154)), и настроить интернет на нем. Да и вообще всем умным Wi-Fi устройствам лучше закреплять статичный IP. Это зачастую важно для нормальной работы интеграций Home Assistant.

## Бойлерная кнопка

Бойлер потребляет 3-3.5 kWh и обычный умный выключатель не подойдет. При выборе обязательно обращайте внимание на допустимый ток, он должен быть минимум 16А, а лучше 20А. Быстро найти Zigbee выключатель на самом острове сложно, я заказывал из [китая](https://vi.aliexpress.com/item/1005006833309900.html), вышло примерно €20.

<robo-academy-grid :columns="2" textAlign="center">
    <robo-academy-grid-element>
        <LessonImages src="school-2024-cyprus-relocant-manual/boiler-switch-dimension.png" alt="Boiler Switch"/>
    </robo-academy-grid-element>
    <robo-academy-grid-element>
        <LessonImages src="school-2024-cyprus-relocant-manual/boiler-switch-wiring.png" alt="Boiler Switch Wiring"/>
    </robo-academy-grid-element/>
</robo-academy-grid>

Первая и наиболее важная автоматизация - отключение кнопки через N минут после любого включения. Настраиваем и больше не думаем о том, забыли ли вы выключить кнопку или она уже третий день работает. Пример автоматизации для Home Assistant, нужно заменить на свои `device_id` и `entity_id`:

<LessonCodeWrapper language="yaml" noCopyIcon>
    alias: Boiler turn off after 30 min
    description: ""
    trigger:
    - platform: device
        type: turned_on
        device_id: a7ee4b26ec5b9e36d959f7b4b8490c42
        entity_id: 61230c7b5528330e3b60ee38c5fe1f12
        domain: switch
        for:
        hours: 0
        minutes: 30
        seconds: 0
    condition: []
    action:
    - type: turn_off
        device_id: a7ee4b26ec5b9e36d959f7b4b8490c42
        entity_id: 61230c7b5528330e3b60ee38c5fe1f12
        domain: switch
    mode: single
</LessonCodeWrapper>

В течение года можно менять время. Например, в феврале мне нужно греть воду час, а в апреле достаточно 30 мин. Из полезного, стоит добавить отправку уведомления на телефон, когда вода нагрелась.


<robo-academy-note type="note" title="Домашнее задание">
  Сделать автоматизацию, которая будет выключать бойлер через заданные Х минут. Чтобы задать время как переменную, посмотрите на <a href="https://www.home-assistant.io/integrations/input_number/">эту интеграцию</a>
</robo-academy-note>

## ИК пульты для кондиционеров и ТВ

Пульты бывают с подключением по Wi-Fi (требуют постоянного питания) и по Zigbee (работают от батарейки).

Wi-Fi вариант, испробованный мной, от производителя [Broadlink](https://www.ibroadlink.com/productinfo/762674.html), покупал на [Amazon](https://www.amazon.de/-/en/dp/B07ZSG9Y67/), около €30. Для первоначальной настройки придется установить себе их приложение на телефон и создать аккаунт, но после этого ИК пульт будет работать в локальной сети, подключение к HA выполняется с помощью [интеграции](https://www.home-assistant.io/integrations/broadlink/). Для дальнейшей настройки пульта под ваши нужды рекомендую посмотреть на репозиторий [SmartIR](https://github.com/smartHomeHub/SmartIR) - это большая библиотека уже готовых команд для разных кондиционеров и ТВ.

<robo-academy-note type="note" title="Совет">
  Если не нашлось конкретно вашей модели кондиционера, попробуйте другие модели от того же производителя. Вероятно, команды будут те же самые и вы сможете подключить свой кондиционер.
</robo-academy-note>

<LessonImages src="school-2024-cyprus-relocant-manual/broadlink-ir.png" alt="Broadlink IR Remote Control"/>

Пример конфигурации для Broadlink IR Remote:

<LessonCodeWrapper language="yaml" noCopyIcon>
    climate:
    - platform: smartir
        name: Living Room AC
        unique_id: living_room_ac
        device_code: 1390
        controller_data: remote.living_room_ir_remote_control
        temperature_sensor: sensor.0xa4c138b6ad623598_temperature
        humidity_sensor: sensor.0xa4c138b6ad623598_humidity 
</LessonCodeWrapper>

Пульты, работающие на Zigbee, не требуют постоянного подключения к питанию, а работают от батареек. С одной стороны, это плюс, т.к. можно разместить устройство в любом удобном месте комнаты. С другой, батарейки нужно будет менять по мере необходимости. Процесс настройки таких пультов тоже может отличаться от Broadlink. Если не получится воспользоваться библиотекой SmartIR, то пульт нужно будет обучить каждой команде отдельно и сохранить в конфигурации Home Assistant.

Программируемые пульты очень просты в установке и настройке, не требуют монтажа на стену или подключению к шине кондиционера. Однако, есть небольшое ограничение, связанное с отсутствием обратной связи между устройствами. Мы не можем проверить, что кондиционер включился и исполняет именно ту команду, которую мы отправили. Однако мы же делаем быстро и без ущерба для квартиры. Чтобы дать немного больше информации пульту, можно установить любой Zigbee датчик температуры и влажности, например [такой](https://vi.aliexpress.com/item/1005005595631552.html) за €10, и привязать показания к пульту. Таким образом у нас появляется простая обратная связь, а количество интересных сценариев увеличивается.

## Электромониторинг

Существуют полуинвазивные измерители потребленного электричества, такие как на изображении ниже:

<LessonImages imageClasses="small" src="school-2024-cyprus-relocant-manual/energy-meter.png" alt="Energy Meter"/>

Их необходимо запитать, подав L и N на вход. С другой стороны к измерителю подключается индукционное кольцо, которое вешаем на фазу или линию потребления для измерения. В большинстве домов и квартир заходит 3 фазы, значит нужно установить 3 таких модуля. Покупал на [Amazon](https://www.amazon.de/gp/product/B0C37DJXVD/) по €60, по одному на каждую из фаз. В более старых домах может встречаться всего одна фаза.

## Заключение

Для меня умный дом — это не роскошь, а необходимость. Это место, где я хочу отдыхать и проводить время с семьей, не тратя силы на решение бытовых вопросов. Стоимость вышеописанного комплекта в моем случае составила около €500 и пару вечеров. Результат - неоценим!
