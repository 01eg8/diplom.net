
1. При падении основного канала связи не произойдёт автоматического переключения на резерв. Этого можно добиться добавив маршрут по умолчанию на основном бордере в сторону резервного с большой AD.
- Добавил маршрут по умолчанию на основном бордере.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-10-05%2020-26-15.png)

2. NAT
Стоит добавить проброс порта и на второй бордер, чтобы к серверу можно было обращаться при выходе из строя основного канала связи по второму Ip-адресу.
- Добавил проброс порта
![image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-10-05%2020-28-28.png)

3. ASA +
Здесь уже можно навесить ACL permit ip any any на все интерфейсы, чтобы не ловить баг CPT

4. ACL +-
1) ACL на коммутаторах ядра не пропускает траффик с ПК в интернет, нужно исправить. Аналогичная проблема с ноутбуками ЦО и филиала.
2) ACL на коммутаторах ядра не пропускает служебный HSRP траффик, поэтому коммутаторы не могут согласовать роли:
- Исправил правила для пользователей на коммутаторах ядра.
![image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-10-05%2020-31-01.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-10-05%2020-31-30.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-10-05%2020-33-13.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-10-05%2020-37-32.png)
- В задании указано: 
Устройства филиала имеют доступ только к внутренним сетям компании, не имеют выхода в интернет.
- Добавил правила для служебного HSRP трафика
![image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-10-05%2020-34-35.png)
![image](https://github.com/01eg8/diplom.net/blob/main/pic/Screenshot%20from%202026-10-05%2020-34-58.png)