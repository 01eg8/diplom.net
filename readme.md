Дипломная работа по курсу «Сетевой инженер» Макина Олега.

Задание

Нужно настроить отказоустойчивую, безопасную, масштабируемую сеть и запустить на ней пользовательские сервисы.

1. Собрать топологию сети.
[схема](https://github.com/01eg8/diplom.net/blob/main/diplom.38.aaa.pkt)
2. Заполнить таблицу распределения подсетей и адресов.
[таблица](https://github.com/01eg8/diplom.net/blob/main/ip-address-table.add.xlsx)
3. Настройть на коммутаторах доступа порты.
[sw0](https://github.com/01eg8/diplom.net/blob/main/config_device/sw0.txt)
[sw1](https://github.com/01eg8/diplom.net/blob/main/config_device/sw1.txt)
[sw2](https://github.com/01eg8/diplom.net/blob/main/config_device/sw2.txt)
[sw3](https://github.com/01eg8/diplom.net/blob/main/config_device/sw3.txt)
4. Настроить коммутаторы ядра.
[core1](https://github.com/01eg8/diplom.net/blob/main/config_device/msw0.txt)
[core2](https://github.com/01eg8/diplom.net/blob/main/config_device/msw1.txt)
5. Настроить сервисы для распределения сетевых настроек.
[image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-09-26%2000-16-13.png)
6. Настроить сервис БЛВС.
[image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-09-26%2000-13-12.png)
[image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-09-26%2000-13-33.png)
7. На коммутаторах ядра запустить протокол маршрутизации ospf
8. На каждом межсетевом экране настроить адресацию и три зоны: inside, outside, DMZ.
[asa0](https://github.com/01eg8/diplom.net/blob/main/config_device/asa0.txt)
[asa1](https://github.com/01eg8/diplom.net/blob/main/config_device/asa1.txt)
9. На Cisco ASA настроить протокол ospf.
10. Настройте пограничные маршрутизаторы.
[R1](https://github.com/01eg8/diplom.net/blob/main/config_device/R1.txt)
[R2](https://github.com/01eg8/diplom.net/blob/main/config_device/R2.txt)
11. Настройте маршрутизацию ospf
12. Настройте ebgp-сессии с оборудованием провайдера.
13. Настройте правила NAT,PAT на пограничных маршрутизаторах.
14. Настройте маршрутизатор филиала.
[RR](https://github.com/01eg8/diplom.net/blob/main/config_device/remote.router.txt)
15. На маршрутизаторе филиала настройте Tunnel-интерфейсы gre до бордеров ЦО. 
16. Настройте коммутатор доступа филиала для подключения к сети ip-телефона, ПК и точки доступа.
[R0](https://github.com/01eg8/diplom.net/blob/main/config_device/R0.txt)
17. Настройте БЛВС ТД филиала, подключить к ней ноутбук.
18. Настройте на АСО интерфейсы для управления. 
19. Настройте ip-телефоны, проверьте дозвон.
[image](https://github.com/01eg8/diplom.net/blob/main/pic/6.2.png)


Чем чреват чистый GRE:
- Нет шифрования. Главный минус: трафик внутри туннеля передаётся в открытом виде.
- Дополнительная нагрузка. GRE добавляет служебный заголовок (минимум 24 байта: 20 байт внешнего IP + 4 байта GRE). Если не скорректировать MTU, пакеты могут фрагментироваться — это снизит производительность и увеличит задержки. 
- Нет встроенных механизмов безопасности. В GRE по умолчанию нет аутентификации и контроля целостности данных. 
