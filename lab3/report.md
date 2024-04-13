University: [ITMO University](https://itmo.ru/ru/)

Faculty: [FICT](https://fict.itmo.ru)

Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)  

Year: 2024

Group: K34202

Author: Gololobov Vladimir

Lab: Lab3

Date of create: 24.02.2024

Date of finished: 24.02.2024

---

# Отчёт по лабораторной работе №3 
## "Использование Asterisk в качестве SIP proxy

## Цель работы: 
Изучить программный комплекс Asterisk. Настроить Asterisk для локальных звонков.

## Ход работы:
Работа выполнена на витруальной машине на Ubuntu.

### Установика Asterisk.
На ВМ был установлен Asterisk командой 
```
sudo apt-get install asterisk
```

![1](/lab3/lab_3_1.png)  


### Настрйка SIP каналов.
Далее в директории /etc/asterisk был отредактирован файл sip.conf, куда была добавлена информация о телефонах 1000 и 1001:
```
[1000]
type=friend
host=dynamic
secret=123
context=ext_1000

[1001]
type=friend
host=dynamic
secret=123
context=ext_1001
```

В файл extensions.conf был определен тип канала – SIP:
```
[ext_1000]
exten => _XXXX,1,Dial(SIP/${EXTEN})

[ext_1001]
exten => _XXXX,1,Dial(SIP/${EXTEN})
```
После измененя файлов Asterisk был перезапущен:
```
sudo service asterisk restart
```

Проверим его статус:
```
sudo systemctl status asterisk
```

![1](/lab3/lab_3_2.png)  


### Установика soft телефонов на рабочую станцию и подключение к SIP каналам soft телефона.
Далее были установлены софтфоны Zoiper5 и MicroSIP. Так как работа выполнялась на Ubuntu нужно было также установить wine, настроить и с помощью него уже установить MicroSIP.  
Далее софтфоны были подключены: введены указанные ранее номера и пароли, а также адрес сервера – адрес текущего хоста 127.0.0.1.  
Настройка Zoiper5:  
![1](/lab3/lab_3_3.png)  
Настройка MicroSIP:  
![1](/lab3/lab_3_4.png)  
Для проверки успешной настройки связи был совершен звонок на телефон 1000 с телефона 1001. Как видно, соединение было установлено, на экране виден номер звонящего телефона:  
![1](/lab3/lab_3_5.png)  

### Вывод  
В результате выполнения работы были изучены програмный комплекс Asterisk и настройка Asterisk для локальных звонков.