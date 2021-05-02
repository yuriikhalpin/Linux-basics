# Общие навыки

## Filesystem Hierarchy Standard, «стандарт иерархии файловой системы»
Литература:
* https://ru.wikipedia.org/wiki/FHS
* https://zen.yandex.ru/media/merion_networks/obiasnenie-struktury-katalogov-linux-6044b12d9e9a5735c16be613

#### Примеры использования

N/A

#### Самостоятельная работа

Задача 1. Изучить FHS

## Типы файлов в Linux
Литература:
* https://ravesli.com/tipy-fajlov-v-linux/

#### Примеры использования

N/A

#### Самостоятельная работа

Задача 1. Изучить типы файлов в Linux

## Права доступ в Linux
Литература:
* https://losst.ru/prava-dostupa-k-fajlam-v-linux
* https://community.vscale.io/hc/ru/community/posts/211809385-%D0%A3%D0%BF%D1%80%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BF%D1%80%D0%B0%D0%B2%D0%B0%D0%BC%D0%B8-%D0%B4%D0%BE%D1%81%D1%82%D1%83%D0%BF%D0%B0-%D0%B2-Linux
* https://ravesli.com/tipy-polzovatelej-i-prava-dostupa-k-fajlam-katalogam-v-linux/

#### Примеры использования

N/A

#### Самостоятельная работа

Задача 1. Изучить права доступа в Linux

## Подключение к серверу
Литература:
* https://losst.ru/kak-polzovatsya-putty
* https://zvondozvon.ru/tehnologii/protokoli/dns#_DNS

#### Примеры использования

Подключение по IPv4
```
ssh user@192.168.0.1 -p 22
```

Подключение по доменному имени
```
ssh user@server.example.com -p 22
```

#### Самостоятельная работа

Задача 1. Подключиться к удаленному серверу с помощью PuTTY(по паролю)

Задача 2. Настроить подключение по ключу к пользователю root

Задача 3. Подключиться к удаленному серверу с помощью PuTTY(по ключу)

Задача 4. Изучить работу основы работы протокола DNS
* Подключится к серверу под пользователем root по доменному имени(по паролю)
* Подключится к серверу под пользователем root по доменному имени(по ключу)

---

## Пакетный менеджер APT
Литература:
* https://losst.ru/kak-polzovatsya-apt
* https://pingvinus.ru/note/apt

#### Примеры использования

Обновить список пакетов
```
apt-get update
```

Установить в систему последние версии следующих пакетов
* man
* vim
* tree
* openssh-client
* nmap
* nano

```
apt-get install man vim tree openssh-client nmap nano
```

Удалить из системы следующие пакеты
* nmap

```
apt-get remove nmap
```

#### Самостоятельная работа

Задача 1.  Установить Midnight Commander

Задача 2.  Удалить Midnight Commander

---

## Работа со справочной системой
Литература:
* https://losst.ru/chto-takoe-man

!!! Для выхода нажми q !!!

## MAN / APROPOS / WHATIS / INFO

#### Примеры использования

Построить индекс справочных страниц
```
mandb
```

Получить справку о команде
```
man passwd
```

Получение справки о конфигурационном файле
```
man 5 passwd
```

Поиск справки по ключевому слову
```
man -k xfs
apropos xfs
```

Вывод короткой справки
```
man -f pwd
whatis pwd
```

Вывод справки в формате "документа"
```
info pwd
```

#### Самостоятельная работа

Задача 1. Изучить системную справку следующих утилит
* pwd
* uptime

---