# Linux-basics
Linux basics

# Рабочее окружение
## Windows
Задача 1: Установить последнюю версию PuTTY 

Задача 2: Создать пары ключей открытый/закрытый
* RSA, 2048 бит
* Ed25519

Задача 3: Установить VirtualBox

Задача 3.1: Создать виртуальный сервер
* CPU CORES: 1
* RAM: 512MB
* DISK TYPE: VHD
* DISK SIZE: 10GB

Задача 4. Установить Debian на виртуальный сервер
* ISO: https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-10.8.0-amd64-netinst.iso
* Разделы диска: 
``` /boot 
  / 
  SWAP
```

## Linux

TBD

# Общие навыки 

## Подключение к серверу
Литература:
* https://losst.ru/kak-polzovatsya-putty
* https://zvondozvon.ru/tehnologii/protokoli/dns#_DNS

Задача 1. Подключиться к удаленному серверу с помощью PuTTY(по паролю)

Задача 2. Настроить подключение по ключу к пользователю root

Задача 3. Подключиться к удаленному серверу с помощью PuTTY(по ключу)

Задача 4. Изучить работу основы работы протокола DNS
* Подключится к серверу под пользователем root по доменному имени(по паролю)
* Подключится к серверу под пользователем root по доменному имени(по ключу)

## Пакетный менеджер APT
Литература:
* https://losst.ru/kak-polzovatsya-apt
* https://pingvinus.ru/note/apt

Задача 1. Изучить использование команды APT

Задача 1.1. Обновить список пакетов

``` apt-get update ``` 

Задача 1.2. Установить в систему последние версии следующих пакетов
* man
* vim
* tree
* mc
* openssh-client
* nmap
* nano
* htop

``` apt-get install ... ```

Задача 1.3. Удалить из системы следующие пакеты
* nmap

``` apt-get remove ... ```

## Man

Задача 1. Системная справка
Статьи:
* https://losst.ru/chto-takoe-man

Задача 2. Самостоятельная работа
Задача 2.1. Изучить системную справку следующих утилит
* pwd


## Стандартные утилиты

### PWD
Литература:
``` man pwd ```

Задача 1. Определить путь к текущему каталогу

``` pwd```

Задача 2. Самостоятельная работа
Задача 2.1. Изучить разницу между опциями -P и -L

### LS
Литература:
``` man ls ```

Задача 2. Выести содержимое текущего каталога - всё

``` ls -a ```

Задача 3. Выести содержимое текущего каталога - только каталоги

``` ls -d ```

Задача 4. Выести содержимое текущего каталога - "длинный" формат(списком)

``` ls -l ```

Задача 5. Самостоятельная работа
Задача 5.1. Выести содержимое текущего каталога - вывести все содержимое кроме . и ..
Задача 5.2. Выести содержимое текущего каталога - вывести список с данными об inode
Задача 5.3. Выести содержимое текущего каталога - вывести список в человекоудобном формате

### CD
Литература:
``` man cd ```

Задача 1. Переход в каталог с логами

``` cd /var/log ```

Задача 2. Самостоятельная работа
Задача 2.1. Переместится в домашний каталог
Задача 2.2. Переместится в каталог /usr/local/share/man
Задача 2.2.1 Переместится на один уровень выше из текущего каталог

### MKDIR
Литература:
``` man mkdir ```

Задача 1. Создаем временные каталог

``` mkdir /tmp/test1 ```

``` mkdir /tmp/test2 /tmp/test3 ```

``` mkdir /tmp/{test4,test5} ```

Задача 2. Самостоятельная работа
Задача 2.1. Создать каталоги
* /srv
* /srv/site1
* /srv/site2

Задача 2.2. Создать каталог /srv/site3/log
Задача 2.3. Создать каталог /srv/site1/log c правами 111
Задача 2.3. Создать каталог /srv/site2/log c правами 333(одной командой)

### RMDIR
Литература:
``` man rmdir ```

Задача 1. Удаляем временные каталог

``` rmdir /tmp/test1 ```

``` rmdir /tmp/test2 /tmp/test3 ```

``` rmdir /tmp/{test4,test5} ```

Задача 2. Самостоятельная работа
Задача 2.1. Удалить каталог каталог /srv/site3 


# Первоначальная настройка

TBD