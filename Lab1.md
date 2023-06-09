# University: ITMO University

# Faculty: FICT

# Course: IP telephony technology

# Year: 2023

# Group: K34212

# Author: Berete Mamady

# Lab: 1

Тема работы: Базовая настройка ip-телефонов в среде Сisco packet tracer 

Цель работы: Изучить рабочую среду Cisco Packet Tracer, ознакомиться с интерфейсами основных устройств, типами кабелей, научиться собирать топологию. Изучить построение сети IP-телефонии с помощью маршрутизатора, коммутатора и IP телефонов Cisco 7960 в среде Packet tracer

# Часть 1 Задание 1: Собрать схему соединения В среде Cisco Packet Tracer была смоделирована сеть следующей конфигурации 

![image](https://user-images.githubusercontent.com/61075142/229492298-c497f096-c9c2-46f2-a144-c66520393d46.png)


Далее я назначил каждому компьютеру локальный IPv4-адрес с помощью графического интерфейса (для той же цели можно воспользоваться командой ipconfig) в диапазоне 192.168.1.2-8:

![image](https://user-images.githubusercontent.com/61075142/229501835-e4348445-d63f-489d-81a2-e7b17ec3ce32.png)

Теперь можно проверить работоспособность сети с помощью пингов:

![image](https://user-images.githubusercontent.com/61075142/229507437-647cf793-41b6-4909-b8e6-724144a61167.png)

Все пакеты достигли своих адресатов, значит, сеть настроена корректно.


 # Часть 2
-------------------------------------------------------------------------------------------------------------------------------------------------------
Во второй части лабораторной работы необходимо было настроить IP-телефонию в простой топологии из двух IP-телефонов, коммутатора и роутера с поддержкой Cisco CallManager Express (CME). Схема сети представлена на рисунке ниже:

![image](https://user-images.githubusercontent.com/61075142/229511199-2dba3a58-7422-42ba-8948-25f183d313ac.png)

Перед началом работы подключим телефоны к сети через интерфейс:

![image](https://user-images.githubusercontent.com/61075142/229511467-5f681928-067a-4e0e-8cac-b87f02e91ae0.png)

Чтобы изменять конфигурации устройст через терминал, необходимо зайти в привелигерованный режим:

                                                    Router>enable
                                                    Router#config terminal
                                                   
Теперь изменим имя роутера на CMERouter:

![image](https://user-images.githubusercontent.com/61075142/229512989-31b4a9a6-7c78-445a-941f-d40fe103d7cf.png)

Назначим интерфейсу, к которому подсоединен коммутатор, IP-адрес 192.168.1.1:

![image](https://user-images.githubusercontent.com/61075142/229513139-9791f903-a282-4ccc-8455-6bd497f8dbc4.png)

Настроим DHCP-сервер для автоматической настройки телефонов. Для этого создаем пул с TELEPHONY, назначаем ему сеть 192.168.1.0 и дефолтный роутер, который мы настроили в предыдущем пункте. При передаче голоса необходимо включить на DHCP опцию 150, чтобы телефоны импортировали настройки с TFTP (Trivial File Transfer Protocol):

![image](https://user-images.githubusercontent.com/61075142/229513372-8d3a1652-62d6-4102-afa4-1267ca615da3.png)

Устанавливаем максимальное количество номеров и телефонов, указываем адрес голосового шлюза и настраиваем автоматическое назначение линий:

![image](https://user-images.githubusercontent.com/61075142/229513602-42d1f030-d10c-472a-838e-3b4792099d06.png)

Назначаем портам коммутатора VLAN:

![image](https://user-images.githubusercontent.com/61075142/229513764-9cdb11b9-3cd8-4754-85d9-0c174ba4881b.png)

Включаем все VLAN интерфейсы на коммутаторе и маршрутизаторе:


                                                   interface vlan1
                                                    no shutdown


Проверим настройки отправив пинг с роутера на оба телефона:


![image](https://user-images.githubusercontent.com/61075142/229514124-34eb9398-463e-4f6a-b2db-4a54ac0e2a4d.png)


Пинги проходят, значит, сеть настроена корректно. Попробуем совершить "звонок":


![image](https://user-images.githubusercontent.com/61075142/229514718-67da3f8f-1d89-4433-8a69-44a807edaab7.png)


Звонок проходит успешно, можно послать короткое звуковое сообщение с одного телефона на другой. Протестировать работу перевода звонков, перехвата не предоставляется возможным, так как роутер не поддерживает эти функции.

Диаграмма получившейся сети представлена на рисунке ниже:


![image](https://user-images.githubusercontent.com/61075142/229518099-11a37e19-2c1b-41d9-8c4c-49a674a5c39b.png)

# Вывод

В ходе лабораторной работы я получил базовые навыки работы с IP-телефонией на базе Cisco Callmanager Express, смоделировал PC-сеть и сеть IP-телефонов. Для сети c телефонией настроил VLAN и DHCP-сервер, автоматически выдал телефонам линии и смог провести "звонок" между двумя устройствами.
