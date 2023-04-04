# University: ITMO University

# Faculty: FICT

# Course: IP telephony technology

# Year: 2023

# Group: K34212

# Author: Berete Mamady

# Lab: 2

## Часть 1 

В первой части лабораторной работы необходимо было собрать сеть из 3 IP-телефонов. Целевая схема изображена на рисунке ниже:

![image](https://user-images.githubusercontent.com/61075142/229523431-b590cc85-86c9-43e0-9fa1-0d3c4ade2c06.png)

Перед началом работы подключил телефоны к сети через интерфейс:

![image](https://user-images.githubusercontent.com/61075142/229751441-85e157f7-683a-4295-bd71-261827e73a2f.png)

Собрал в Cisco Packet Tracer модель, соответствующую схеме:

![image](https://user-images.githubusercontent.com/61075142/229752370-39140fbd-6810-4182-8811-b96072014a59.png)

Через CLI роутера включил порт, к которому подключен коммутатор:

![image](https://user-images.githubusercontent.com/61075142/229753059-35abb34a-c706-41bd-a444-ae9303b52ec9.png)

Изменил имя маршрутизатора:

![image](https://user-images.githubusercontent.com/61075142/229753382-178d3edc-eb9b-4849-a311-a55c733f1520.png)

Отключил синтаксис ввода слов от DNS серверов:

![image](https://user-images.githubusercontent.com/61075142/229753608-f6e62090-59ef-411a-94d1-1aa28dace609.png)

Задал пароли для защиты маршрутизатора в удаленном режиме и режиме консоли. Команда line vty 0 1 настраивает подключение только для двух одновременных клиентов:

![image](https://user-images.githubusercontent.com/61075142/229753733-5cec9c5b-ac41-4f9d-95e4-68944eda6f4a.png)

Назначил интерфейсу маршрутизатора IP-адрес:

![image](https://user-images.githubusercontent.com/61075142/229753898-0e3aa327-53b6-4c13-ac13-99054986f853.png)

Настроил DHCP-сервер:

![image](https://user-images.githubusercontent.com/61075142/229754057-4b36b9df-ce11-4be5-96de-4ffec08f7624.png)

Включил VLAN-порты на маршрутизаторе и коммутаторе:

![image](https://user-images.githubusercontent.com/61075142/229754356-ef55daa2-a6c4-4aa3-92c6-ff0672e82ab6.png)

Назначил диапазон VLAN портов на коммутаторе:

![image](https://user-images.githubusercontent.com/61075142/229754568-92e9c876-b61d-4486-936f-631a0b71b295.png)

Настроил сервис телефонии на роутере. Установил количество линий и телефонов равное 3, назначил линиям номера:

![image](https://user-images.githubusercontent.com/61075142/229754811-c3235f65-73e7-4788-8375-8674c6cf6f0d.png)

Проверил работу сети, позвонив с номера 11111 на номер 22222:

![image](https://user-images.githubusercontent.com/61075142/229755040-14cc19e9-c39f-4772-ab4b-a49422897bb5.png)

Диаграмма топологии:

![image](https://user-images.githubusercontent.com/61075142/229756750-a1f83478-2b95-498a-af0e-a964bf198446.png)

## Часть 2

Во второй части лабораторной работы необходимо было собрать сеть по данной схеме с несколькими VLAN'ами:

![image](https://user-images.githubusercontent.com/61075142/229757088-3434dc77-b5b8-40b2-87de-e5a6ab617cfc.png)

Создал три VLAN'а: Data, Voice и Managment:

![image](https://user-images.githubusercontent.com/61075142/229757233-87d4ce69-b23f-4a05-ae98-291f51647a3c.png)

Настроил VLAN 30:

![image](https://user-images.githubusercontent.com/61075142/229757370-6add2560-18aa-41e1-b132-9fe28eaee6fd.png)

Установил маршрут по умолчанию:

![image](https://user-images.githubusercontent.com/61075142/229757506-ea4b0312-666c-4efe-bc4b-4830cbe34876.png)

Назначил режимам доступа access и voice свои VLAN'ы:

![image](https://user-images.githubusercontent.com/61075142/229757767-9499f8bb-317a-4916-abc9-61c24797a04d.png)

Создал логические подыинтерфейсы для VLAN'ов:

![image](https://user-images.githubusercontent.com/61075142/229758017-9bf8e926-f3e7-4e05-b8f5-d499bebaf128.png)

Создал логические подыинтерфейсы для VLAN'ов:

![image](https://user-images.githubusercontent.com/61075142/229758127-f7d34b26-5b9a-4d28-beb8-ac7b8ff9a40e.png)

Исключил из DHCP-пула адреса маршрутизатора и DNS-сервера:

![image](https://user-images.githubusercontent.com/61075142/229758237-4777161b-c457-44c7-bc12-026134dc18f1.png)

Настроил DHCP для VLAN 10 и VLAN 20:

![image](https://user-images.githubusercontent.com/61075142/229758360-72dff456-8b33-455a-9acd-433e18c9190d.png)

Настроил сервис IP-телефонии:

![image](https://user-images.githubusercontent.com/61075142/229758657-9c38b8fa-11ed-455b-8eda-3030b5a4d8f9.png)

Назначил номера телефонов:

![image](https://user-images.githubusercontent.com/61075142/229759133-1f5fdc00-2ecc-4c7f-bebc-bc723f337824.png)

Подключил телефоны к сервису:

![image](https://user-images.githubusercontent.com/61075142/229759236-f26490b4-47be-413a-970b-58263f5fe462.png)

Назначил компьютерам IP-адреса через DHCP:

![image](https://user-images.githubusercontent.com/61075142/229759423-fc85c8f9-3395-44a8-a2ea-06032c044e12.png)

Теперь можно проверить работоспособность системы. Протестируем звонок по сети VLAN 20:

![image](https://user-images.githubusercontent.com/61075142/229759626-3b7f6e6f-a757-4c8d-8f9d-4bc5dc45c475.png)

Протестируем передачу данных между компьютерами в сети VLAN 10:

![image](https://user-images.githubusercontent.com/61075142/229759775-8c7b57a9-3647-4e8e-b660-8ae26b722801.png)

Схема топологии:

![image](https://user-images.githubusercontent.com/61075142/229760002-a20b648f-2f2f-470d-9006-52d8b32edb9a.png)

## Вывод

В ходе лабораторной работы я получил базовые навыки работы с IP-телефонией на базе Cisco Callmanager Express, научился устанавливать аутентификацию на маршрутизатор, настраивать сеть из IP-телефонов и PC, выделяя на передачу данных между компьютерами и телефонами разные VLAN'ы.



