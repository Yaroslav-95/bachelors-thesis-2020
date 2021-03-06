---
title: Доклад по ВКР
author: Yaroslav de la Peña Smirnov
output: pdf_document
fontsize: 12pt
header-includes:
  \usepackage[english,russian]{babel}
  \usepackage[margin=3cm]{geometry}
---

Добрый вечер уважаемые председатель комиссии и члены комиссии. Представляю вам
выпускную квалификационную работу на тему: Разработка программы
автоматизированного построения полётного задания для управления группой БПЛА.

## Цель

Цель данной работы является разработка прототипа программного обеспечения для
автоматизированного построения полётного задания группы БПЛА.

## Задачи

* исследовать и изучить предметную область и теоретические основы темы;
* определить общие требования к ПО;
* выбрать и изучить оптимальные компоненты и библиотеки для реализации ПО;
* выбрать оптимальный язык программирования для реализации ПО;
* спроектировать и разработать архитектуру для взаимодействия разных
  компонентов;
* разработать прототип ПО для построения полётного задания для управления
  группой БПЛА.

## Актуальность

Данная тема является актуальной по ряду причин, среди которых

* рост спроса БПЛА, который продолжает увеличивается с каждым годом; глобальный
  объем коммерческого рынка БПЛА на 2018 год был оценен в 25,59 млрд. долларов и
  ожидается его рост до 70,28 млрд. долларов к 2029 году;
* появления новых задач с применением БПЛА и применение БПЛА в большей
  количество сфер
* новые требования к повышенной автономности БПЛА, в том числе способность БПЛА
  летать и координировать свои действия в групповом полёте;
* развитие технологий и новые разработки в сфере информационных технологий,
  которые открывает новые возможности для дальнейшего развития беспилотных
  систем.

## Обзор предметной области

Большинство гражданских беспилотных систем состоят из удалённо пилотируемого ЛА,
человеческого фактора, полезного груза, подсистемы управления, и архитектуры и
канала передачи данных и коммуникаций. В военных системах могут присутствовать и
другие элементы, как например оружейные системы.

* БПЛА --- летательный аппарат управляемый без прямого вмешательства человека
  внутри или на борту данного аппарата
* Подсистемы управления --- делятся на
  * Автопилот --- система управления на борту ЛА, которая обеспечивает
  определённый уровень автономности.
  * НСУ --- предоставляет средства для управления БПЛА человеком, могут быть
  разных размеров.
* Канал передачи данных --- этот термин определяет способ связи между НСУ и
  автопилотом. Это могут быть обычная радиосвязь прямой видимости или такие
  коммуникации вне прямой видимости как спутниковая связь.
* Полезный груз --- большинство задач, выполняемые БПЛА требует наличие
  определённого полезного груза, как например, камеры, коммуникационные системы
  или доставляемый груз.
* Человеческий фактор --- состоит их оператора и вспомогательной наземной
  команды. В зависимости от сложности системы, роли могут занимать несколько
  человек или объединить несколько ролей в одну.

На сегодняшний день, БПЛА применяются в множество разных сфер и индустрий.
Большинство заданий, в которых участвуют БПЛА, визуального характера, то есть,
те в которых применяется видео или фотосъёмка. В последние годы также начинают
набирать популярность полётные задания для доставки небольших грузов на малые
и средние расстояния.

Примеры сфер где применяются БПЛА:

* Дистанционное зондирование --- в том числе:
  * Фотограмметрические задания
  * Управление природными ресурсами
  * Сельско хозяйственные задания
* Промышленное обследование
* Воздушная фотография и видеосъёмка --- например в:
  * Маркетинг
  * Кинематография
  * Журнализм
* Разведка --- например для:
  * Обеспечение правопорядка
  * Поисково-спасательные работы
* Метеорология
* Доставка грузов

## Обзор архитектуры системы управления БПЛА

(Объяснить схемы)

## Требования к ПО

* Данная программа должна быть совместимой с ОС Linux и/или UNIX-подобными
  системами;
* Выбранный язык программирования должен обладать развитой экосистемой, то есть
  большой базой сторонних библиотек и модулей;
* Компоненты, стороннее ПО и библиотеки должны обладать свободной лицензией с
  открытым исходным кодом;
* Протоколы коммуникаций должны использовать существующие сетевые стеки,
  например TCP/IP

## Компоненты для реализации ПО

После исследования и анализа существующих модулей и библиотек были выбранные
следующие компоненты:

* Язык программирования JavaScript, так как является де факто стандартом веба
делая его самым распространённым языком программирования;
* В качестве ОС был выбран дистрибутив Linux Ubuntu 18.04, в связи с
доступностью программных решений для разработки робототехнических систем;
* Автопилот PX4, так как обладает свободной лицензией и режимом SIL;
* Протокол MAVLink для общения между ПО и автопилотом;
* Библиотека React для разработки ГПИ;
* Библиотека Redux для управления состоянием программы;
* Фреймворк Electron в качестве оболочки над программой для запуска в нативной
среде ОС
* Платформа Cesium для визуализации объектов на трёхмерной карте мира.

## Архитектура системы управления и ПО

Далее представлена схема архитектуры управления группой БПЛА в режиме
программного обеспечения в контуре (SIL).

(Объяснить схему)

Далее представлена схема архитектуры разрабатываемого ПО.

(Объяснить схему)

## Разработка ПО

Все файлы с исходным кодом программы находятся в папке `src/` в корневой папке
репозитория. Структура файлов в данной папке выглядит следующим образом:

* `actions/` --- в данной папке содержатся Redux-действия по
  изменению состояния программы;
* `components/` --- здесь содержатся React-компоненты, которые
  являются частью ГРИ
* `mavlink/` --- здесь находится код для коммуникации с БПЛА по
  протоколу MAVLink;
* `reducers/` --- папка в которой находятся функции для изменения
  состояния программы посредством Redux, называемые «функции-редукторы», в
  данных функциях находится основная бизнес-логика программы;
* `app.js` --- файл с которого начинается сама программа;
* `index.js` --- файл с основным React-компонентом, который содержит
  всех остальные компонентов, импортируя их с папки `components`;
* `main.js` --- файл, являющийся отправной точкой для фреймворка
  Electron.

Далее в папках `actions` и `reducers` находятся следующие файлы, которые
содержат действия и функции-редукторы соответственно:

* `uav-connect.js` --- событие по подключению БПЛА к ПО;
* `uav-disconnect.js` --- событие по отключению БПЛА от ПО;
* `waypoint-add.js` --- событие по добавлению путевой точки в ГПИ;
* `waypoint-del.js` --- событие по удалению путевой точки в ГПИ;
* `waypoint-edit.js` --- событие по удалению путевой точки в ГПИ;
* `uav-location-update.js` --- событие по получению новой информации
  о геолокации БПЛА от автопилота, оно нужно чтобы уведомить вьюер cesium о
  новой локации БПЛА в реальном времени;
* `mavlink-message-rcv.js` --- событие по получению любого сообщения
  от автопилота по протоколу MAVLink;
* `mavlink-message-send.js` --- событие по отпарвлению любого
  сообщения автопилоту по протоколу MAVLink.

Далее React-компоненты, которые содержаться в папке `components` и являются
частью графического интерфейса:

* `<CesiumViewer />` --- этот компонент показывает спутниковую карту
  мира посредством платформы Cesium;
* `<Panel />` --- через данный компонент пользователь программы
  управляет полётным заданием каждого БПЛА, редактируя путевые точки, и
  запуская, завершая, загружая или сохраняя задание на диск; состоит из
  следующих под-компонентов:
  * `<Aircraft />` --- содержит все путевые точки полётного задания
    БПЛА и позволяет запустить, или посадить его отдельно от остальной группы;
  * `<Waypoint />` --- содержит одну из путевых точек определённого
    БПЛА.

Для запуска программы и произведения теста, запускается сначала необходимое
количество инстанций автопилота PX4 в режиме SIL вместе с симулятором Gazebo.
Затем сама программа запускается и подключается ко всем инстанциям автопилота
через UDP.

## Заключение

В ходе данной выпускной работы были получены следующие результаты:

* определены основные применения и направления систем беспилотных
  летательных аппаратов;
* были анализированы перспективы развития систем БПЛА;
* определены основные элементы систем БПЛА;
* выбраны необходимые элементы для разработки ПО;
* спроектирована архитектура системы и ПО;
* разработан прототип программы автоматизированного построения полётного
  задания для управления группой БПЛА.

**Зе энд**
