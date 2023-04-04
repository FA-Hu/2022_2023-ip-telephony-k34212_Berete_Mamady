# Faculty: FICT

# Course: IP telephony technology

# Year: 2023

# Group: K34212

# Author: Berete Mamady

# Lab: 4 Построение сети ip-телефонии между удаленными маршрутизаторами

# Часть 1

Цель работы: Изучить построение сети IP-телефонии между удаленными филиалами с помощью маршрутизаторов Cisco 2811 и коммутаторов Cisco 2950Т.

Результатом лабораторной работы должна стать схема сети, представленная на рисунке ниже:

![image](https://user-images.githubusercontent.com/61075142/229762192-20f41486-28ad-4240-b7c5-5e5ea6f5fafc.png)

Между маршрутизаторами должно быть проложено DCE/DTE соединение. Для этого я добавил роутерам необходимые разъемы:

![image](https://user-images.githubusercontent.com/61075142/229762404-81f8bc4f-1446-4b87-9cb5-3279ee0ae718.png)

Построил топологию:

![image](https://user-images.githubusercontent.com/61075142/229763802-c10a702c-6520-4866-8c15-882736bf6c2e.png)

Назначил портам роутеров, выходящих на коммутатор IP-адреса. Выбрал сети 192.168.1.0 и 172.16.1.0:

![image](https://user-images.githubusercontent.com/61075142/229763951-d5e68b3d-cedb-4fcc-92be-f08f916a9dba.png)

Настроил DCE (Router 0) и DTE (Router 1) порты:

![image](https://user-images.githubusercontent.com/61075142/229764149-c7fe063e-266b-439a-92d1-53fddf67db9d.png)

Настроил DHCP на каждом роутере:

![image](https://user-images.githubusercontent.com/61075142/229765007-4e850e2b-c6fa-4e05-814e-847f325f1efb.png)

Включил VLAN на роутере и коммутаторе, настроил порты на коммутаторе:

![image](https://user-images.githubusercontent.com/61075142/229765167-b098231e-0a11-41d9-ab31-3035859d8873.png)

Настроил телефонию в первой сети. Установил номера 101, 102, 103:

![image](https://user-images.githubusercontent.com/61075142/229765294-09691f9b-05e6-4c86-928c-9bbb237e6649.png)

Портестировал работу сервиса:

![image](https://user-images.githubusercontent.com/61075142/229765479-6394a9a1-a7bc-40f2-94cc-d9843a6e53ea.png)

Повторил настройку коммутатора и сервиса IP-телефонии во второй сети. Установил номера 201, 202, 203.

Настроил на обоих роутерах RIP:

![image](https://user-images.githubusercontent.com/61075142/229765632-2c0bc91b-8bf8-48d9-b628-64b82cbef3e9.png)

Проверил работу протокола, отправив пинг между компьютерами из разных сетей:

![image](https://user-images.githubusercontent.com/61075142/229765773-cf944811-4c8f-443c-b837-2fa25139186f.png)

Настроил соединение между двумя сетями IP-телефонии:

![image](https://user-images.githubusercontent.com/61075142/229765876-c1083cfa-4b57-403b-b8eb-6e41d55859c4.png)

Проверил работу сети, позвонив с номера 102 на номер 202:

![image](https://user-images.githubusercontent.com/61075142/229765994-1dbb36a2-610d-424f-afac-86ae7037c414.png)

Звонок прошел успешно, значит, сеть настроена верно.

Диаграмма сети:

![image](https://user-images.githubusercontent.com/61075142/229766184-f3dce0ea-5e36-43fe-8ebe-f50525aaa67b.png)

# Вывод

В ходе лабораторной работы я научился соединять две сети с IP-телефонией, настроил динамическую маршрутизацию между двумя сетями по протоколу RIP и соединил две сети IP-телефонии с помощью сервиса dial-peer.
