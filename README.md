# Подключение к серверу НИРФИ

## 1.  Установка OpenVPN Connect

Загрузка установочного файла по этой [ссылке] (https://openvpn.net/downloads/openvpn-connect-v3-windows.msi) напрямую, или на официальном [сайте] (https://openvpn.net/client/client-connect-vpn-for-windows/) (также доступна х32 версия).
Установка - как обычно.

## 2. Добавление ключевого файла
- Получите сам ключевой файл
- Запускаем OpenVPN Connect
- Переключаемся на вкладку ```upload file```
- Перетаскиваем ключевой файл в окно
- Нажимаем оранжевую кнопку ```connect```
- В случае удачного подключения - появится надпись ```connected``` и статистика переданных данных

В дальнейшем подключение и отключение VPN регулируется переключателем рядом с именем профиля

![Успешное подключение](img/OVPNC.png)

## 3. Подключение к серверу Windows

_В дальнейшем в Windows попадать нужно будет через Linux - она будет ведущей системой. Пока что загрузка по умолчанию в Windows, это временно_

- Подключаемся к VPN
- Запускаем диспетчер подключений к удаленному рабочему столу одним из способов:
    - В поле поиска на панели задач введите Подключение к удаленному рабочему столу и выберите Подключение к удаленному рабочему столу (нажатием на ПКМ можно закрепить это окно в панели Пуск)
    - Нажмите сочетание клавиш Win+R, введите ```mstsc.exe``` и далее - выполнить

Появится окно:

  ![RDP1](img/RDP1.png)

- Раскрываем дополнительное меню "Показать параметры"
- В поле "Компьютер" вводим ```10.0.0.133```
- В поле "Пользователь" вводим имя вашего пользователя, одно из:
    - ```Sergey```
    - ```Dmitry```
- Для облечения дальнейшего подключения можно выставить галочку на пункт с сохранением данных авторизаций, а также создать ярлык на Рабочем столе или в любом другом удобном вам месте для быстрого соединения

![RDP2](img/RDP2.png)

- Нажать "Подключить"
- При первом подключении подтвердить сертификат:

![RDP3](img/RDP3.png)

**Вы подключились!**

## 4. Правильное отключение от Windows

Чтобы не создавать помех другим пользователям, если у вас не запущено активных расчетов, правильным отключением будет не закрыть окно соединения на локальной машине, а выйти из пользователя на удаленном сервере через меню Пуск:

![RDP4](img/RDP4.png)