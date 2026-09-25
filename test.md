### Тестирование

1) Проверка STP, HSRP. Роль Root bridge и HSRP-active на одном устройстве. Команды: show spanning-tree, show standby на этом устройстве.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/1.1.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/1.2.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/1.3.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/1.4.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/1.5.png)
2) Проверка маршрутизации на коммутаторах ядра. Show ip route. Должен присутствовать маршрут по-умолчанию и маршруты до интерфейсов ASA и бордеров.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/2.1.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/2.2.png)
3) Проверка LAG на коммутаторах ядра show etherchannel summary.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/3.1.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/3.2.png)
4) Маршрутизация на бордерах sh ip route. В таблице маршрутизации должны присутствовать bgp-маршруты от провайдера, ospf-маршруты до внутренних подсетей ЦО и филиала.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/4.1.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/4.2.png)
5) Туннель CAPWAP на БЛВС ТД в статусе Connected, с ноутбуков есть связь с 8.8.8.8.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/5.1.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/5.2.png)
6) Телефонные аппараты зарегестрированы на VoIP сервере, прозвон с одного на другой работает.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/6.1.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/6.2.png)
7) На все сетевые устройства можно попасть по учётной записи tacacs+ сервера.
8) Время на устройствах синхронизировано. Show ntp status.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/8.1.png)
9) С 8.8.8.8 есть доступ к web-серверу в DMZ. Обратный доступ тоже есть. Проверять доступ необходимо браузером.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/9.1.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/9.2.png)
10) Отключение одного из каналов связи не приводит к потере доступа в интернет с пользовательских ПК(ping до сервера 8.8.8.8). 
![image](https://github.com/01eg8/diplom.net/blob/main/pic/10.1.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/10.2.png)
11) Выход из строя одного из коммутаторов ядра, межсетевого экрана или бордер роутера не приводит к потере доступа в интернет с пользовательских ПК(ping до сервера 8.8.8.8). Потеря доступа к web-серверу извне доспускается.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/11.1.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/11.2.png)
12) Ноутбуки не имеют доступа к внутренним сетям компании(ping svi users, mgmt, printer).
![image](https://github.com/01eg8/diplom.net/blob/main/pic/12.png)
13) Устройства филиала имеют доступ только к внутренним сетям компании, не имеют выхода в интернет.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/13.png)
