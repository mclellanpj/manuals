# Руководство по построению TJBotCZ и подключению аппаратных средств

---
![exclamation](https://raw.githubusercontent.com/tjbotcz/manuals/master/images/exclamation.png) _**УВЕДОМЛЕНИЕ ПЕРЕД НАЧАЛОМ**_ 

 1. БУДЬТЕ ВНИМАТЕЛЬНЫ ПРИ СКЛАДЫВАНИИ КАРТОНА. ЕСЛИ СЛОЖИТЬ НЕВЕРНО, ВАМ ПОНАДОБИТСЯ КЛЕЙ, ЧТОБЫ ИСПРАВИТЬ ОШИБКИ.
 2. БУДЬТЕ ГОТОВЫ ИСПАЧКАТЬСЯ. ЛАСЕРЦЕТНЫЙ КАРТОН ОСТАВЛЯЕТ ЧЕРНЫЕ СЛЕДЫ НА ВАШИХ РУКАХ._
(Мы рекомендуем протирать каждую часть бумажной салфеткой.)

---

### Видео-руководство

Здесь вы найдете оригинальное видео-руководство по созданию TJBot. Вы можете им воспользоваться. Единственное существенное отличие заключается в подключении светодиода. TJBotCZ использует традиционный светодиод RGB, который находится на платформе под верхней частью (головой) - см. фотографии ниже. 

**Будьте осторожны:**
 * складывайте картон правильной стороной (на некоторых частях есть инструкции "согнуть вверх" или "согнуть вниз" - лучше проверить несколько раз, чем сожалеть потом :)
 * придерживайтесь инструкций в видео-руководстве, чтобы вам не пришлось повторно собирать эту конструкцию
 * особенно при присоединении ног для стабильности
 * вставляйте сервопривод в правильный момент


<a href="http://www.youtube.com/watch?feature=player_embedded&v=bLt3Cf2Ui3o" target="_blank"><img src="http://img.youtube.com/vi/bLt3Cf2Ui3o/0.jpg" alt="IMAGE ALT TEXT HERE" width="480" border="10" /></a>

### Так что же изменилось в TJBotCZ?

1. Часть, которая держит динамик.
2. Светодиод RGB

Этапы построения TJBot также доступны здесь: 

https://www.instructables.com/id/Build-TJ-Bot-Out-of-Cardboard/

Для большей выдержки мы рекомендуем склеить некоторые части. Особенно ноги и части, которые держат Raspberry Pi внизу. 

### Подключение аппаратных средств

На рисунке ниже показаны все периферийные устройства, которые могут понадобится при соединении TJBota:
* адаптер питания
* HDMI для подключения монитора
* камера
* аудио разъем джек для подключения динамика
* подключение Ethernet к Интернету (если вы не используете WiFi)
* USB-слоты для микрофона, мыши и клавиатуры
* пины на Raspberry Pi для подключения светодиода RGB и сервопривода

![servo](https://raw.githubusercontent.com/tjbotcz/manuals/master/images/rpi-connect.jpg)


**GPIO пины**

Периферийные устройства подсоединяются к Raspberry Pi через отдельные пины. Здесь вы найдете легенду ко всем пинам:


![gpio pins](https://raw.githubusercontent.com/tjbotcz/manuals/master/images/rpi_pins.png)

**Подключение сервопривода к GPIO пинам**

Сервопривод использует 3 пина:

* 5V мощность / + (физический пин 02)
* земля / - (физический пин 14)
* GPIO 7 для команд (физический пин 26) - можно настроить в файле конфигурации TJbotCZ (config.js - см. Оживление)


![servo](https://raw.githubusercontent.com/tjbotcz/manuals/master/images/hw-servo.jpg)

**Подключение светодиода RGB к пинам GPIO**

Светодиод RGB использует 4 пина:
* земля  / - (физический пин 09)
* GPIO 17 / R (физический пин 11) - можно настроить (config.js - см. Оживление)
* GPIO 27 / G (физический пин 13) - можно настроить (config.js - см. Оживление)
* GPIO 22 / B (физический пин 15) - можно настроить (config.js - см. Оживление)

![servo](https://raw.githubusercontent.com/tjbotcz/manuals/master/images/hw-rgbled.jpg)
