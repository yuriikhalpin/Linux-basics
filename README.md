# Linux-basics
Linux basics

---

# Рабочее окружение

## Windows
Задача 1: Установить последнюю версию PuTTY 

Задача 2: Создать пары ключей открытый/закрытый
* RSA, 2048 бит
* Ed25519

Задача 3: Установить VirtualBox
Литература:
* https://poznyaev.ru/blog/linux/debian-v-virualbox
* https://lumpics.ru/how-install-debian-on-virtualbox/
* https://pikabu.ru/story/ustanovka_debian_10_busterna_realnuyu_mashinu_desktop_iili_virtualbox_v_kartinkakh__dlya_chaynikov_8016771

Задача 3.1: Создать виртуальный сервер

* CPU CORES: 1
* RAM: 512MB
* DISK TYPE: VHD
* DISK SIZE: 10GB

Задача 4. Установить Debian на виртуальный сервер
* ISO: https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-10.8.0-amd64-netinst.iso
* Разделы диска: 
``` 
  /boot 
  / 
  SWAP
```

---

## Linux

TBD

---

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

---

### Пакетный менеджер APT
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

---

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

### CAT
Литература:
``` man cat ```

Задача 1. Выводим содержимое файлов 
``` 
cat /etc/passwd

cat /etc/shadow

cat /etc/hosts

cat /etc/shells
 
```

Задача 2. Сохранение вывода в файл
``` 
cat /etc/passwd > /srv/1

cat /etc/shadow > /srv/2

cat /etc/hosts > /srv/3

cat /etc/shells > /srv/4
 
```

Задача 3. Сохранение вывода нескольких файлов в один файл
``` 

cat /etc/hosts >> /srv/merge

cat /etc/shells >> /srv/merge
 
```

Задача 4. Самостоятельная работа

Задача 4.1. Вывессти содержимое файла с нумерацией строк
* /etc/shells
* /etc/shadow
* /etc/hosts
* /etc/services

### CP
Литература:
``` man cp ```

Задача 1. Копируем файл 
``` 
cp /etc/hosts /srv/
cp /etc/hosts /srv/hosts_copy

cp /etc/shells /srv/
cp /etc/shells /srv/shells_copy

``` 

Задача 2. Самостоятельная работа

Задача 2.1. Скопировать следующие файлы в /srv c новым именем
* /etc/services
* /etc/shadow

### Touch
Литература:
``` man touch ```

Задача 1. Создаем пустой файл
``` 
touch file
touch /srv/file
touch /srv/{f1,f2,f3}

``` 

Задача 2. Самостоятельная работа

Задача 2.1. Создать файл new_file в следующих каталогах
* ~/
* ./
* /srv


### MV
Литература:
``` man mv ```

Задача 1. Переименовываем файл 
``` 
mv file file_moved
mv /srv/file /srv/file_moved

``` 

Задача 2. Перемещаем файл
``` 
mv /srv/f1 /tmp
mv /srv/f2 /tmp

``` 

Задача 2. Самостоятельная работа

Задача 2.1. Создать каталог new_dir и переименовать его в old_dir

Задача 2.2. Создать каталог new_dir и переместить его в /srv


### RM
Литература:
``` man rm ```

Задача 1. Удаляем файл
``` 
touch test_file1
rm test_file1
touch test_file1
rm -v test_file1

``` 

Задача 2. Удаляем не пустой каталог
``` 
mkdir dir1
touch dir1/file1
rmdir dir1
rm -R dir1

``` 

Задача 2. Самостоятельная работа

Задача 2.1. Создать каталог new_dir c двумя пустыми файлами и и удалить его 

Задача 2.2. Создать пустой файл new_file и удалить его

### ECHO
Литература:
``` man echo ```

Задача 1. Выводим строку на экран
``` 
echo "Hello World!"
echo 'Hello World!'
echo Hello
echo
echo  World
echo !
``` 

Задача 2. выводим значние переменных
``` 
echo $PWD
echo $SHELL
echo $USER
echo %HOME
echo $PATH
VAR="Hello!"
echo $VAR
``` 
Задача 3. Создание файла
``` 
echo $PWD > test_file123
echo $SHELL > test_file123
echo $USER > test_file123
echo %HOME > test_file123
echo $PATH > test_file123
VAR="Hello!" 
echo $VAR > test_file123
``` 
Задача 4. Самостоятельная работа

Задача 2.1. Создать файл /tmp/HW содержищий строку "dfksfjkvzbvmsjkthryhl"

---

## Продвинутые утилиты

### FIND
Литература:
``` find echo ```

Примеры использования 

Поиск файлов
```bash
# Все файлы в текущем каталоге
find . -type f 
# Файлы в каталоге /etc/ssh
find /etc/ssh -type f
find /etc/ssh -type f -ls
find /etc/ssh -type f -print
# Файлы в каталоге /var/log по шаблону *.log
find /var/log -type f -name "*.log"
```

Поиск каталогов
```bash
# Все каталоги в текущем каталоге
find . -type d
# Все каталоги в каталоге /etc
find /etc -type d
find /etc -type d -ls
find /etc -type d -print
# Все каталоги в каталоге /etc по шаблону *ssh*
find /etc -type d -name "*ssh*"
```

Самостоятельная работа
Задача 1. Все каталоги в /etc без подкаталогов(глубина 1)
Задача 2. Все файлы в /etc только из подкаталогов(глубина 2)

### LN / UNLINK
Литература:
* https://losst.ru/simvolicheskie-i-zhestkie-ssylki-linux
``` find ln ```
``` find unlink ```

Примеры использования

Создание символьной ссылки файлов
```bash
# Создаем ссылку на файл в текущем каталоге
mkdir test
touch test/sfile
ln -s ./test/sfile .

# Проверяем
ls -l
file sfile

# Записываем строку в исходный файл
cat sfile
echo "Hello" > test/sfile
cat sfile

# Создаем ссылку на файл в каталоге /tmp
touch sfile1
ln -s $(pwd)/sfile1 /tmp

# Проверяем
ls -l /tmp
file /tmp/sfile1

# Записываем строку в исходный файл
cat /tmp/sfile1
echo "Hello" > sfile1
cat /tmp/sfile1

unlink sfile
unlink /tmp/sfile1
```

Создание жесткой ссылки файлов
```bash
# Создаем ссылку на файл в текущем каталоге
mkdir test
touch test/sfile2
ln ./test/sfile2 .

# Проверяем
ls -l
file sfile2

# Записываем строку в исходный файл
cat sfile2
echo "Hello" > test/sfile2
cat sfile2

# Создаем ссылку на файл в каталоге /tmp
touch sfile3
ln $(pwd)/sfile3 /tmp

# Проверяем
ls -l /tmp
file /tmp/sfile3

# Записываем строку в исходный файл
cat /tmp/sfile3
echo "Hello" > sfile3
cat /tmp/sfile3

unlink sfile2
unlink /tmp/sfile3
```

Самостоятельная работа
Задача 1. Создать символьную ссылку на следующие файлы в текущем каталоге
* /etc/passwd
* /etc/hosts

Задача 2. Создать символьную ссылку на следующие каталоги в текущем каталоге
* /etc/ssh 
* /var/log

Задача 3. Выяснить разницу между символьной и жесткой ссылкой

### CHOWN

### CHMOD

### TAR

### MORE / LESS

### HEAD / TAIL

### GREP

### SORT

### WC

### DIFF

### MOUNT / UMOUNT

## "Диагностические" утилиты

### DATE

### TIME

### DU

### DF

### UPTIME

### UNAME

### FREE

### TOP

### PS

### IP

### PING

### TRACEROUTE

### SS

## Другие

## SU / SUDO

### KILL

### SLEEP

### TIMEOUT

## Управления пользователем

# Первоначальная настройка

TBD