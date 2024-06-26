University: [ITMO University](https://itmo.ru/ru/)

Faculty: [FICT](https://fict.itmo.ru)

Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)  

Year: 2024

Group: K34202

Author: Gololobov Vladimir

Lab: Lab2

Date of create: 24.02.2024

Date of finished: 24.02.2024

---

# Отчет по лабораторной работе №2  
## "Конфигурация voip в среде Сisco packet tracer" 

# Цель работы:
Изучить построение сети IP-телефонии с помощью маршрутизатора Cisco 2811, коммутатора Cisco catalyst 3560 и IP телефонов Cisco 7960. 
## Часть 1  
### Задание 1: Собрать схему соединения  
В среде Cisco Packet Tracer была смоделирована сеть следующей конфигурации (Рис. 1).

![1 1](/lab2/lab_1_1.png)  
Рисунок 1 – Схема сети  

### Задание 2: Настройка адресов
Имя роутера было изменено на CMERouter, был отключен синтаксис ввода слов от DNS серверов, была выполнена настройка интерфейса fa0/0.

![1 2](/lab2/lab_1_2.png)
Рисунок 2 – Настройка роутера

Была выполнена настройка DHCP сервера на маршрутизаторе для передачи данных и голоса.

![1 3(pc1)](/lab2/lab_1_4.png)
Рисунок 3 – Настройка DHCP  

Был создан VLAN на коммутаторе.

![1 4(pc4)](/lab2/lab_1_5.png)
Рисунок 4 – Настройка VLAN  

Была выполнена насторйка телефонов на маршрутизаторе.

![1 4(pc4)](/lab2/lab_1_6.png)
Рисунок 5 – Настройка телефонов  

Результат соединения телефонов представлен на рисунке 6.

![1 4(pc4)](/lab2/lab_1_7.png)
Рисунок 6 – Соединение телефонов  

## Часть 2  
### Задание 1: Создание сети  
Создана новая сеть (Рис. 7).  

![2 1](/lab2/lab_1_8.png)
Рисунок 7 – Схема сети  
  
На коммутаторе были созданы VLAN для даных, голоса и управления, а так же VLAN для не используемых интерфейсов (Рис. 8)

![2 2](/lab2/lab_1_9.png)
Рисунок 8 – Настройка коммутатора  
 
Далее интерфейсы коммутатора были настрооены в соответствии с назначением.
  
![2 3](/lab2/lab_1_10.png)
Рисунок 9 – Настройка интерфейсов  

На следующем рисунке представлена конфигурация интерйесов и VLAN на коммутаторе.

![2 4](/lab2/lab_1_11.png)
Рисунок 10 – Конфигурация  

Была выполнена насторйка маршрутизатора для работы телефонии.

![2 5](/lab2/lab_1_12.png)
Рисунок 11 – Настройка маршрутизатора  

Так же была выполнена настройка DHCP и телефонов.

![2 6](/lab2/lab_1_13.png)
Рисунок 12 – Конфигурация маршрутизатора  

Настройка телефонии завершена. Выполним тестовый прозвон.

![2 7](/lab2/lab_1_14.png)
Рисунок 11 – Прозвон	  
 
![2 9](/lab2/lab_1_15.png)
Рисунок 12 – Успешное соединение  

## Вывод:
В результате выполнения лаб.работы было изучено построение сети IP-телефонии с помощью маршрутизатора Cisco 2811, коммутатора Cisco catalyst 3560 и IP телефонов Cisco 7960.
