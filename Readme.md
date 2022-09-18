## 1.1. Введение в DevOps - Ляшенко Андрей

[netology.tf](https://github.com/and1V/Netology.DevOps-HomeWork/blob/main/netology.tf.png)

[netology.sh](https://github.com/and1V/Netology.DevOps-HomeWork/blob/main/netology.sh.png)

[netology.md](https://github.com/and1V/Netology.DevOps-HomeWork/blob/main/netology.md.png)

[netology.yaml](https://github.com/and1V/Netology.DevOps-HomeWork/blob/main/netology.yaml.png)

[netology.jsonnet](https://github.com/and1V/Netology.DevOps-HomeWork/blob/main/netology.jsonnet.png)
____________________

## 2. Описание жизненного цикла задачи 

+ **Идея**

 Набор вопросов, входящих в сформулированное предложение для решения конкретной задачи
 
+ **Определение требований**

Как правило, требования определяет руководитель проекта совместно с бизнес аналитиками. Это ряд обязательных направлений (технических характеристик), которые должны быть соблюдены в поекте

+ **Дизайн (архитектура) системы**

Архитекторы ПО прорабатывают и выбирают каркас системы, определяют набор используемых технологий, инстурментов, которые способствуют взаимойдвствию между участниками цикла

+ **Разработка**

Разработчики создают, изменяют, обновляют ПО согласно техническим требованиях от бизнес аналитиков 

+ **Тестирование**

Тестировщики проверяют код разработки на наличие багов, стабильности. Если есть отклонения от требований, то тестировщики офорпляют отчет на испрвления со стороны отдела разработки, до тех пор, пока не будет исправлено в соответствии с определенными требованиями 

+ **Развертывание**

После успешного этапа тестирования следует развертывание продукта и передача заказчику в пользование

+ **Поддержка**

По сути это повторение таких этапов жизненного цикла как: ***Опредление требований (новых), разработка, тестирование, развертывание***. 

_______________

## Системы контроля версий!

### В файле .gitignore будут проигнорированы следующие файлы 

 Во всех вложенных *Директориях* - **/.terraform/*

+ .tfstate - файлы с расширением, отвечающие за текущее состояние инфраструктуры в терраформ
+ crash.log - журнал событий информирующий о внезапном\экстренном завершении работы программы
+ .tfvars - игнориует файлы, хранящие конфеденциальную информацию: пароли, секретные ключи
+ override.tf,
override.tf.json - расширениния позволяющие переопределить метод базового класса из А в В, например
+ .terraformrc,
terraform.rc - расширение скрытое и не скрытое конфигурационных файлов интерфейса командной строки (CLI)

______________

## Основы гит 

+ [repo github](https://github.com/and1V/Netology.DevOps-HomeWork/tree/main)

+ [repo bitbucket](https://bitbucket.org/and1v/netology-devops/src/main/)

+ [repo gitlab](https://gitlab.com/and1V/netology-devops/-/tree/main)

+ [График веток Фикс,Мейн](https://github.com/and1V/Netology.DevOps-HomeWork/network)

____________________________________________

## Ветвления гит

[Github](https://github.com/and1V/Netology.DevOps-HomeWork)
[Gitlab](https://gitlab.com/and1V/netology-devops)
[Bitbucket](https://bitbucket.org/and1v/netology-devops/src/main/)

## Инструменты Гит

1. ***git show aefea***

commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545

Author: Alisdair McDiarmid <alisdair@users.noreply.github.com>

Date:   Thu Jun 18 10:29:58 2020 -0400

    Update CHANGELOG.md

2. ***git show 85024d3***

commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)

3. ***git show --pretty=format:' %P' b8d720***

56cd7859e05c36c06b56d013b55a252d0bb7e158 - родительский хэш

56cd7859e05c36c06b56d013b55a252d0bb7e158 - родительский хэш

4. ***git log  v0.12.23..v0.12.24  --oneline***

33ff1c03b (tag: v0.12.24) v0.12.24

b14b74c49 [Website] vmc provider links

3f235065b Update CHANGELOG.md

6ae64e247 registry: Fix panic when server is unreachable

5c619ca1b website: Remove links to the getting started guide's old location

06275647e Update CHANGELOG.md

d5f9411f5 command: Fix bug when using terraform login on Windows

4b6d06cc5 Update CHANGELOG.md

dd01a3507 Update CHANGELOG.md

225466bc3 Cleanup after v0.12.23 release

5. ***git log -S'func providerSource' --oneline***

5af1e6234 main: Honor explicit provider_installation CLI config when present

8c928e835 main: Consult local directories as potential mirrors of providers

6.  ***git log -L :'func globalPluginDirs':plugins.go --oneline***

   78b122055 Remove config.go and update things using its aliases

   52dbf9483 keep .terraform.d/plugins for discovery

   41ab0aef7 Add missing OS_ARCH dir to global plugin paths

   66ebff90c move some more plugin search path logic to command

   8364383c3 Push plugin discovery down into command package

7. ***git log -S'func synchronizedWriters'***

   commit 5ac311e2a91e381e2f52234668b49ba670aa0fe5
Author: ***Martin Atkins*** <mart@degeneration.co.uk>
Date:   Wed May 3 16:25:41 2017 -0700

## Работа в терминале №1

1. ***Установите средство виртуализации Oracle VirtualBox***

sudo apt install virtualbox


2. ***Установите средство автоматизации Hashicorp Vagrant.***

sudo apt-get install vagrant


3. ***С помощью базового файла конфигурации запустите Ubuntu 20.04 в VirtualBox посредством Vagrant:***

vagrant up


4. ***Ознакомьтесь с графическим интерфейсом VirtualBox, посмотрите как выглядит виртуальная машина, которую создал для вас Vagrant, какие аппаратные ресурсы ей выделены. Какие ресурсы выделены по-умолчанию?***

RAM:1024mb

CPU:2

HDD:64gb

video:4mb


5. ***Ознакомьтесь с возможностями конфигурации VirtualBox через Vagrantfile: документация. Как добавить оперативной памяти или ресурсов процессора виртуальной машине?***

С помощью добавления командного синтаксиса в VagrantFile:

config.vm.provider "virtualbox" do |v|

     v.memory = 1024
     v.cpu = 2

или командами ВМ

   config.vm.provider "virtualbox" do |vb|

     vb.memory = "1024"
     vb.cpu = "2"
   end
  

6. ***Команда vagrant ssh из директории, в которой содержится Vagrantfile, позволит вам оказаться внутри виртуальной машины без каких-либо дополнительных настроек. Попрактикуйтесь в выполнении обсуждаемых команд в терминале Ubuntu.***
  
Ознакомиться с разделами man bash, почитать о настройках самого bash:


7. ***какой переменной можно задать длину журнала history, и на какой строчке manual это описывается?***

HISTFILESIZE - максимальное число строк в файле истории для сохранения, 
строка 1155

HISTSIZE - число команд для сохранения  , 
строка 1180


8. ***что делает директива ignoreboth в bash?***

ignoreboth это сокращение для 2х директив ignorespace and ignoredups, 

    ignorespace - не сохранять команды начинающиеся с пробела, 
    ignoredups - не сохранять команду, если такая уже имеется в истории

Строка в man bash 1142


9. ***В каких сценариях использования применимы скобки {} и на какой строчке man bash это описано?***

{} - зарезервированные слова, список, в т.ч. список команд в отличии от "(...)" исполнятся в текущем инстансе, 
используется в различных условных циклах, условных операторах, или ограничивает тело функции, 
В командах выполняет подстановку элементов из списка , если упрощенно то  цикличное выполнение команд с подстановкой 
например mkdir ./DIR_{A..Z} - создаст каталоги сименами DIR_A, DIR_B и т.д. до DIR_Z
строка 343


10. ***Основываясь на предыдущем вопросе, как создать однократным вызовом touch 100000 файлов? А получилось ли создать 300000?***

touch {000001..100000}.txt - создаст в текущей директории соответсвющее число фалов

300000 - создать не выйдет, в связи с слишком большой длинной списока аргументов,
Узнаем максимальную длину списка аргументов:

vagrant@vagrant:~/testouch/test2$ getconf ARG_MAX
2097152


11. ****В man bash поищите по /\[\[. Что делает конструкция [[ -d /tmp ]]***

Возвращает статус 0 или 1 в зависимости от оценки условного выражения. Разделение слов и раскрытие имени пути не выполняется для слов между [[и]]; расширение тильды, параметри расширение переменных, арифметическое расширение, подстановка команд, подстановка процессов и повторные кавычки. В данной конструкции мы проверяем наличие файла и являеться ли он папкой.


12. ***Основываясь на знаниях о просмотре текущих (например, PATH) и установке новых переменных; командах, которые мы рассматривали, добейтесь в выводе type -a bash в виртуальной машине наличия первым пунктом в списке:***


vagrant@vagrant:~$ mkdir /tmp/new_path_bash

vagrant@vagrant:~$ cp /bin/bash /tmp/new_path_bash

vagrant@vagrant:~$ export PATH=/tmp/new_path_bash:$PATH

vagrant@vagrant:~$ type -a bash

bash is /tmp/new_path_bash/bash

bash is /usr/bin/bash

bash is /bin/bash


13. ***Чем отличается планирование команд с помощью batch и at?***

Команда at используется для назначения одноразового задания на заданное время Команда batch — для назначения одноразовых задач, которые должны выполняться, когда загрузка системы становится меньше 0,8.

Чтобы использовать at или batch, необходимо, чтобы был установлен RPM-пакет at и запущена служба atd. Чтобы узнать, установлен ли этот пакет, выполните команду rpm -q at. Чтобы определить, работает ли служба, воспользуйтесь командой /sbin/service atd status.


14. ***Завершите работу виртуальной машины чтобы не расходовать ресурсы компьютера и/или батарею ноутбука.***

vagrant suspend - остановка виртуальной машины, при следующем запуске все процессы восстановятся

 или 

vagrant halt - штатное выключение виртуальной машины, полное завершение процессов, не остановка.



    

## Работа в терминале №2
1.	Какого типа команда cd? Попробуйте объяснить, почему она именно такого типа; опишите ход своих мыслей, если считаете что она могла бы быть другого типа.
Ответ:

Это команда встроеннная.
Встроенная, потому что, работать внутри сессии терминала логичнее менять указатель на текущую директорию внутренней функцией, 
Если использовать внешний вызов, то он будет работать со своим окружением, и менять  текущий каталог внутри своего окружения, а на вызвавший shell влиять не будет.  

Теоретически можно сделать CD внешней программой, но после смены директории необходимо вызвать bash из этого (нового каталога), но тогда мы получим новый shell.
И покидая сессию придется выходить, опять же, из всех сессий, которые создали при каждом вызове внешней CD.


2.	Какая альтернатива без pipe команде grep <some_string> <some_file> | wc -l? man grep поможет в ответе на этот вопрос. Ознакомьтесь с документом о других подобных некорректных вариантах использования pipe.


Ответ:

vagrant@vagrant:~$cat tst_bash


if [[ -d /tmp ]];
sdgsdfgfd
sdgsdfgfghdgfd
123

vagrant@vagrant:~$grep 123 tst_bash -c

1

vagrant@vagrant:~$grep 123 tst_bash |wc -l

1

3.	Какой процесс с PID 1 является родителем для всех процессов в вашей виртуальной машине Ubuntu 20.04?


Ответ:


На хостовой машине  - systemd:

0:25:28 andiv@upc(0):~$ pstree -p

systemd(1)─┬─ModemManager(1366)─┬─{ModemManager}(1392)
           │                    └─{ModemManager}(1419)


На виртуальной машине  - systemd:

vagrant@vagrant:~$ pstree -p

systemd(1)─┬─VBoxService(754)─┬─{VBoxService}(755)
           │                  ├─{VBoxService}(756)
           │                  ├─{VBoxService}(757)
           

4.	Как будет выглядеть команда, которая перенаправит вывод stderr ls на другую сессию терминала?


Ответ:

Вызов из pts/0:

vagrant@vagrant:~$ ls -l \root 2>/dev/pts/1

vagrant@vagrant:~$ 
    

Вывод в другой сессии pts/1:    

vagrant@vagrant:~$ who

vagrant  pts/0        2020-11-01 12:58 (10.0.2.2)

vagrant  pts/1        2020-11-01 12:59 (10.0.2.2)

vagrant@vagrant:~$ ls: cannot access 'root': No such file or directory


5.	Получится ли одновременно передать команде файл на stdin и вывести ее stdout в другой файл? Приведите работающий пример.


ответ:

vagrant@vagrant:~$ cat tst_bash

if [[ -d /tmp ]];

sdgsdfgfd

sdgsdfgfghdgfd

123

new line

11111111


vagrant@vagrant:~$ cat tst_bash_out


cat: tst_bash_out: No such file or directory 

vagrant@vagrant:~$ cat <tst_bash >tst_bash_out

vagrant@vagrant:~$ cat tst_bash_out

if [[ -d /tmp ]];

sdgsdfgfd

sdgsdfgfghdgfd

123

new line

11111111


vagrant@vagrant:~$ 


6.	Получится ли вывести находясь в графическом режиме данные из PTY в какой-либо из эмуляторов TTY? Сможете ли вы наблюдать выводимые данные?


Ответ:


Вывести полуится при использовании перенаправлении вывода:

    15:04:58 andiv@upc(0):~/vagrant$ tty
    
    /dev/pts/3
    
    15:05:45 andiv@upc(0):~/vagrant$ echo Hello from pts3 to tty3 >/dev/tty3
    
    15:06:19 andiv@upc(0):~/vagrant$ 
    

но наблюдать в графическом режиме не получится, следует переключиться в контекст TTY (Ctrl-Alt-F3)

Так же можно перенаправить контекст из tty в pty, этот вывод можно наблюдать уже будет, но после возврата в графический режим:

    15:05:03 andiv@upc(1):~/vagrant$ tty
    
    /dev/pts/1
    
    15:05:43 andiv@upc(1):~/vagrant$ hello from tty3 to pts1

Или перенаправление вывода из tty3 при работе на гостевой ОС:


    vagrant@vagrant:~$ 
    
    vagrant@vagrant:~$ tty
    
    /dev/pts/0
    
    vagrant@vagrant:~$ hello from tty3 to pts0


7.	Выполните команду bash 5>&1. К чему она приведет? Что будет, если вы выполните echo netology > /proc/$$/fd/5? Почему так происходит?


Ответ:

bash 5>&1 - Создаст дескриптор с 5 и перенаправит его в stdout

echo netology > /proc/$$/fd/5 - выведет в дескриптор "5", который был перенаправлен в stdout

если запустить echo netology > /proc/$$/fd/5 в новой сесии, получим ошибку, так как такого дескриптора нет на данный момент в текущей(новой) сессии


    
vagrant@vagrant:~$ echo netology > /proc/$$/fd/5

-bash: /proc/1096/fd/5: No such file or directory


vagrant@vagrant:~$ bash 5>&1

vagrant@vagrant:~$ echo netology > /proc.$$/fd/5

bash: /proc.1114/fd/5: No such file or directory

vagrant@vagrant:~$ echo netology > /proc/$$/fd/5

netology

vagrant@vagrant:~$ 
    
    
8.	Получится ли в качестве входного потока для pipe использовать только stderr команды, не потеряв при этом отображение stdout на pty? Напоминаем: по умолчанию через pipe передается только stdout команды слева от | на stdin команды справа. Это можно сделать, поменяв стандартные потоки местами через промежуточный новый дескриптор, который вы научились создавать в предыдущем вопросе.


Ответ:

vagrant@vagrant:~$ ls -l /root 9>&2 2>&1 1>&9 |grep denied -c 
1

9>&2 - новый дескриптор перенаправили в stderr

2>&1 - stderr перенаправили в stdout 

1>&9 - stdout - перенаправили в в новый дескриптор


9.	Что выведет команда cat /proc/$$/environ? Как еще можно получить аналогичный по содержанию вывод?


Ответ:

Будут выведены переменные окружения:

можно получить тоже самое (только с разделением по переменным по строкам):

printenv

env


10.	Используя man, опишите что доступно по адресам /proc/<PID>/cmdline, /proc/<PID>/exe.
Ответ:

/proc/<PID>/cmdline - полный путь до исполняемого файла процесса [PID]  (строка 231)
 
/proc/<PID>/exe - содержит ссылку до файла запущенного для процесса [PID], 
 
                        cat выведет содержимое запущенного файла, 
 
                        запуск этого файла,  запустит еще одну копию самого файла  (строка 285)
 
 
11.	Узнайте, какую наиболее старшую версию набора инструкций SSE поддерживает ваш процессор с помощью /proc/cpuinfo.
 
Ответ:
 
 
SSE 4.2
 
vagrant@vagrant:~$ grep sse /proc/cpuinfo
 
 
12.	При открытии нового окна терминала и vagrant ssh создается новая сессия и выделяется pty. Это можно подтвердить командой tty, которая упоминалась в лекции 3.2. Однако:
 
	vagrant@netology1:~$ ssh localhost 'tty'
 
not a tty
 
Почитайте, почему так происходит, и как изменить поведение.
Ответ:

Единственное что с мог найти: то, что при подключении ожидается пользователь, а не другой процесс, и нет локального tty в данный момент. 
для запуска можно добавить -t - , и команда исполняется c принудительным созданием псевдотерминала

vagrant@vagrant:~$ ssh -t localhost 'tty'
 
vagrant@localhost's password: 
/dev/pts/2
 
Connection to localhost closed.
 
vagrant@vagrant:~$ 

 
 
13.	Бывает, что есть необходимость переместить запущенный процесс из одной сессии в другую. Попробуйте сделать это, воспользовавшись reptyr. Например, так можно перенести в screen процесс, который вы запустили по ошибке в обычной SSH-сессии.
 
 
Ответ:

 
При первых запусках ругался на права, 10-patrace.conf
 
после установки знаачения  kernel.yama.ptrace_scope = 0
 
после чего процесс был перехвачен в screen, и продолжил работу после закрытия терминала. 
 
единственное в pstree процесс не отображался, точнее оботражался в виде процесса reptyr. не сразу сообразил что это то, что нужно 
 
14.	sudo echo string > /root/new_file не даст выполнить перенаправление под обычным пользователем, 
 
так как перенаправлением занимается процесс shell'а, который запущен
без sudo под вашим пользователем. 
 
 Для решения данной проблемы можно использовать конструкцию echo string | sudo tee /root/new_file. Узнайте что делает команда tee и почему в отличие от sudo echo команда с sudo tee будет работать.
 
 
Ответ:

команда tee делает вывод одновременно и в файл, указаный в качестве параметра, и в stdout, 
 
в данном примере команда получает вывод из stdin, перенаправленный через pipe от stdout команды echo
 
и так как команда запущена от sudo , соответственно, имееет права на запись в файл




## Операционные системы №1


1.	Какой системный вызов делает команда cd? В прошлом ДЗ мы выяснили, что cd не является самостоятельной программой, это shell builtin, поэтому запустить strace непосредственно на cd не получится. Тем не менее, вы можете запустить strace на /bin/bash -c 'cd /tmp'. В этом случае вы увидите полный список системных вызовов, которые делает сам bash при старте. Вам нужно найти тот единственный, который относится именно к cd. Обратите внимание, что strace выдаёт результат своей работы в поток stderr, а не в stdout.

Ответ:

	системный вызов команды CD -> chdir("/tmp") в нашем случае. 


2.  Попробуйте использовать команду file на объекты разных типов на файловой системе. Например:

	vagrant@netology1:~$ file /dev/tty

	/dev/tty: character special (5/0)

	vagrant@netology1:~$ file /dev/sda

	/dev/sda: block special (8/0)

	vagrant@netology1:~$ file /bin/bash

    /bin/bash: ELF 64-bit LSB shared object, x86-64


Используя strace выясните, где находится база данных file на основании которой она делает свои догадки.

Ответ:

Файл базы типов - /usr/share/misc/magic.mgc

в тексте это:

openat(AT_FDCWD, "/usr/share/misc/magic.mgc", O_RDONLY) = 3

так же ищет пользовательские файлы, по всей видимости

stat("/home/alex/.magic.mgc", 0x7ffedefbea50) = -1 ENOENT (Нет такого файла или каталога)

stat("/home/alex/.magic", 0x7ffedefbea50) = -1 ENOENT (Нет такого файла или каталога)

openat(AT_FDCWD, "/etc/magic.mgc", O_RDONLY) = -1 ENOENT (Нет такого файла или каталога)

stat("/etc/magic", {st_mode=S_IFREG|0644, st_size=111, ...}) = 0

openat(AT_FDCWD, "/etc/magic", O_RDONLY) = 3

поведение аналогичное и на хоствой машине и на виртуалке.


3.	Предположим, приложение пишет лог в текстовый файл. Этот файл оказался удален (deleted в lsof), однако возможности сигналом сказать приложению переоткрыть файлы или просто перезапустить приложение – нет. Так как приложение продолжает писать в удаленный файл, место на диске постепенно заканчивается. Основываясь на знаниях о перенаправлении потоков предложите способ обнуления открытого удаленного файла (чтобы освободить место на файловой системе).

Ответ:

	Попробовал с текстовым редактором vi
	
	vagrant@vagrant:~$ lsof -p 1126

	...

	vi      1126 vagrant    4u   REG  253,0    12288  526898 /home/vagrant/.tst_bash.swp (deleted)
	
	vagrant@vagrant:~$ echo '' >/proc/1126/fd/4
	
	
	где 1126 - PID процесса vi

	4 - дескриптор файла , который предварительно удалил. 
	
4.	Занимают ли зомби-процессы какие-то ресурсы в ОС (CPU, RAM, IO)?

Ответ:

	"Зомби" процессы, в отличии от "сирот" освобождают свои ресурсы, но не освобождают запись в таблице процессов. 

	запись освободиться при вызове wait() родительским процессом. 
	
5.	В iovisor BCC есть утилита opensnoop:

	root@vagrant:~# dpkg -L bpfcc-tools | grep sbin/opensnoop

    /usr/sbin/opensnoop-bpfcc


На какие файлы вы увидели вызовы группы open за первую секунду работы утилиты? Воспользуйтесь пакетом bpfcc-tools для Ubuntu 20.04. Дополнительные сведения по установке.

Ответ:

Без SUDO не запустилось, пришлось переходить в Root

Если правильно понял то нужен именно этот список файлов, которые отображаеются первыми?

(судя по слаку это именно то, что требовалось)

vagrant@vagrant:~sudo -i

root@vagrant:~# dpkg -L bpfcc-tools | grep sbin/opensnoop

/usr/sbin/opensnoop-bpfcc

root@vagrant:~# /usr/sbin/opensnoop-bpfcc


PID    COMM               FD ERR PATH

766    vminfo              6   0 /var/run/utmp

562    dbus-daemon        -1   2 /usr/local/share/dbus-1/system-services

562    dbus-daemon        18   0 /usr/share/dbus-1/system-services

562    dbus-daemon        -1   2 /lib/dbus-1/system-services

562    dbus-daemon        18   0 /var/lib/snapd/dbus-1/system-services/

6.	Какой системный вызов использует uname -a? Приведите цитату из man по этому системному вызову, где описывается альтернативное местоположение в /proc, где можно узнать версию ядра и релиз ОС.

Ответ:

	системный вызов uname()
	
	Цитата :

	     Part of the utsname information is also accessible  via  /proc/sys/ker‐

	       nel/{ostype, hostname, osrelease, version, domainname}.
	

7.	Чем отличается последовательность команд через ; и через && в bash? Например:

	root@netology1:~# test -d /tmp/some_dir; echo Hi

	Hi

	root@netology1:~# test -d /tmp/some_dir && echo Hi

root@netology1:~#

Есть ли смысл использовать в bash &&, если применить set -e?
Ответ:

&& -  условный оператор 

;  - разделитель последовательных команд

test -d /tmp/some_dir && echo Hi - в данном случае echo  отработает только при успешном завершении команды test

set -e - прерывает сессию при любом ненулевом значении исполняемых команд в конвеере кроме последней.

в случае &&  вместе с set -e- вероятно не имеет смысла, так как при ошибке , выполнение команд прекратиться. 

8.	Из каких опций состоит режим bash set -euxo pipefail и почему его хорошо было бы использовать в сценариях?

Ответ:

	-e прерывает выполнение исполнения при ошибке любой команды кроме последней в последовательности 

	-x вывод трейса простых команд 

	-u неустановленные/не заданные параметры и переменные считаются как ошибки, с выводом в stderr текста ошибки и выполнит завершение неинтерактивного вызова

	-o pipefail возвращает код возврата набора/последовательности команд, ненулевой при последней команды или 0 для успешного выполнения команд.
	
	По сути, для сценария, повышает деталезацию вывода ошибок (логирования), 

	и завершит сценарий при наличии ошибок, на любом этапе выполнения сценария, кроме последней завершающей команды

9.	Используя -o stat для ps, определите, какой наиболее часто встречающийся статус у процессов в системе. В man ps ознакомьтесь (/PROCESS STATE CODES) что значат дополнительные к основной 

заглавной буквы статуса процессов. Его можно не учитывать при расчете (считать S, Ss или Ssl равнозначными).

Ответ:

	Самые частые (прямо говоря):

	S*(S,S+,Ss,Ssl,Ss+) - Процессы ожидающие завершения (спящие с прерыванием "сна")

	I*(I,I<) - фоновые(бездействующие) процессы ядра
	
	доп символы это доп характеристики, например приоритет.



## Операционные системы №2

1.	На лекции мы познакомились с node_exporter. В демонстрации его исполняемый файл запускался в background. Этого достаточно для демо, но не для настоящей production-системы, где процессы должны находиться под внешним управлением. Используя знания из лекции по systemd, создайте самостоятельно простой unit-файл для node_exporter:
o	поместите его в автозагрузку,
o	предусмотрите возможность добавления опций к запускаемому процессу через внешний файл (посмотрите, например, на systemctl cat cron),
o	удостоверьтесь, что с помощью systemctl процесс корректно стартует, завершается, а после перезагрузки автоматически поднимается.

Ответ:

Установлено, порт  9100 проброшен на хостовую машину:
 

Сервис стартует и перезапускается корректно

1. Проверка после перезапуска работы процесса
2. Остановка
3. Проверка работы процесса
4. Запуск процесса 
5. Проверка работы процесса
 
vagrant@vagrant:~$ ps -e |grep node_exporter   

   1375 ?        00:00:00 node_exporter

vagrant@vagrant:~$ systemctl stop node_exporter

==== AUTHENTICATING FOR org.freedesktop.systemd1.manage-units ===

Authentication is required to stop 'node_exporter.service'.

Authenticating as: vagrant,,, (vagrant)

Password: 

==== AUTHENTICATION COMPLETE ===


vagrant@vagrant:~$ ps -e |grep node_exporter

vagrant@vagrant:~$ systemctl start node_exporter

==== AUTHENTICATING FOR org.freedesktop.systemd1.manage-units ===

Authentication is required to start 'node_exporter.service'.

Authenticating as: vagrant,,, (vagrant)

Password: 

==== AUTHENTICATION COMPLETE ===

vagrant@vagrant:~$ ps -e |grep node_exporter

   1420 ?        00:00:00 node_exporter

vagrant@vagrant:~$ 

Прописан конфигруационный файл:
vagrant@vagrant:/etc/systemd/system$ cat /etc/systemd/system/node_exporter.service
[Unit]
Description=Node Exporter
 
[Service]
ExecStart=/opt/node_exporter/node_exporter
EnvironmentFile=/etc/default/node_exporter
 
[Install]
WantedBy=default.target


при перезапуске переменная окружения выставляется :


vagrant@vagrant:/etc/systemd/system$ sudo cat /proc/1809/environ

LANG=en_US.UTF-8LANGUAGE=en_US:PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin

INVOCATION_ID=0fcb24d52895405c875cbb9cbc28d3ffJOURNAL_STREAM=9:35758MYVAR=some_value

2.	Ознакомьтесь с опциями node_exporter и выводом /metrics по-умолчанию. Приведите несколько опций, которые вы бы выбрали для базового мониторинга хоста по CPU, памяти, диску и сети.

Ответ:

CPU:

    node_cpu_seconds_total{cpu="0",mode="idle"} 2238.49
    node_cpu_seconds_total{cpu="0",mode="system"} 16.72
    node_cpu_seconds_total{cpu="0",mode="user"} 6.86
    process_cpu_seconds_total
    
Memory:

    node_memory_MemAvailable_bytes 
    node_memory_MemFree_bytes
    
Disk(если несколько дисков то для каждого):

    node_disk_io_time_seconds_total{device="sda"} 
    node_disk_read_bytes_total{device="sda"} 
    node_disk_read_time_seconds_total{device="sda"} 
    node_disk_write_time_seconds_total{device="sda"}
    
Network(так же для каждого активного адаптера):

    node_network_receive_errs_total{device="eth0"} 
    node_network_receive_bytes_total{device="eth0"} 
    node_network_transmit_bytes_total{device="eth0"}
    node_network_transmit_errs_total{device="eth0"}
    
3.	Установите в свою виртуальную машину Netdata. Воспользуйтесь готовыми пакетами для установки (sudo apt install -y netdata). После успешной установки:

o	в конфигурационном файле /etc/netdata/netdata.conf в секции [web] замените значение с localhost на bind to = 0.0.0.0,
o	добавьте в Vagrantfile проброс порта Netdata на свой локальный компьютер и сделайте vagrant reload:
config.vm.network "forwarded_port", guest: 19999, host: 19999
После успешной перезагрузки в браузере на своем ПК (не в виртуальной машине) вы должны суметь зайти на localhost:19999. Ознакомьтесь с метриками, которые по умолчанию собираются Netdata и с комментариями, которые даны к этим метрикам.

Ответ:

Netdata установлена, но проброшен порт 9999, так как 19999 - занять на хостовой машине под локальный netdata 

информация с хостовой машины:

21:56:36 andiv@upc(0):~/vagrant$ sudo lsof -i :19999

COMMAND   PID    USER   FD   TYPE  DEVICE SIZE/OFF NODE NAME

netdata 50358 netdata    4u  IPv4 1003958      0t0  TCP localhost:19999 (LISTEN)


21:56:39 andiv@upc(0):~/vagrant$ sudo lsof -i :9999

COMMAND     PID USER   FD   TYPE  DEVICE SIZE/OFF NODE NAME

chrome     4089 andiv   80u  IPv4 1112886      0t0  TCP localhost:38598->localhost:9999 (ESTABLISHED)

VBoxHeadl 52075 andiv   21u  IPv4 1053297      0t0  TCP *:9999 (LISTEN)

VBoxHeadl 52075 andiv   30u  IPv4 1113792      0t0  TCP localhost:9999->localhost:38598 (ESTABLISHED)

информация с vm машины:
vagrant@vagrant:~$ sudo lsof -i :19999

COMMAND  PID    USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
netdata 1895 netdata    4u  IPv4  30971      0t0  TCP *:19999 (LISTEN)
netdata 1895 netdata   55u  IPv4  31861      0t0  TCP vagrant:19999->_gateway:38598 (ESTABLISHED)


 
4.	Можно ли по выводу dmesg понять, осознает ли ОС, что загружена не на настоящем оборудовании, а на системе виртуализации?

Ответ:

Судя по выводу dmesg да, причем даже тип ВМ, так как есть соответсвующая строка: 

    vagrant@vagrant:~$ dmesg | grep virtualiz

[    0.002836] CPU MTRRs all blank - virtualized system.

[    0.074550] Booting paravirtualized kernel on KVM

[    4.908209] systemd[1]: Detected virtualization oracle.



Если сравнить с хостовой машиной то это становится очевидным (ps:хорошо когда такая есть под рукой для обучения :) ):

21:56:42 andiv@upc(0):~/vagrant$ dmesg | grep virtualiz

[    0.048461] Booting paravirtualized kernel on bare hardware

... on bare hardware - что означает на чистом железе.

5.	Как настроен sysctl fs.nr_open на системе по-умолчанию? Узнайте, что означает этот параметр. Какой другой существующий лимит не позволит достичь такого числа (ulimit --help)?

Ответ:

vagrant@vagrant:~$ /sbin/sysctl -n fs.nr_open

1048576

Это максимальное число открытых дескрипторов для ядра (системы), для пользователя задать больше этого числа нельзя (если не менять). 

Число задается кратное 1024, в данном случае =1024*1024. 

Но макс.предел ОС можно посмотреть так :

vagrant@vagrant:~$ cat /proc/sys/fs/file-max

9223372036854775807

 

vagrant@vagrant:~$ ulimit -Sn
1024

мягкий лимит (так же ulimit -n)на пользователя (может быть увеличен процессов в процессе работы)
 

vagrant@vagrant:~$ ulimit -Hn

1048576

жесткий лимит на пользователя (не может быть увеличен, только уменьшен)

Оба ulimit -n НЕ могут превысить системный fs.nr_open

6.	Запустите любой долгоживущий процесс (не ls, который отработает мгновенно, а, например, sleep 1h) в отдельном неймспейсе процессов; покажите, что ваш процесс работает под PID 1 через nsenter. Для простоты работайте в данном задании под root (sudo -i). Под обычным пользователем требуются дополнительные опции (--map-root-user) и т.д.

Ответ:

root@vagrant:~# ps -e | grep sleep

   2020 pts/2    00:00:00 sleep

root@vagrant:~# nsenter --target 2020 --pid --mount

root@vagrant:/# ps

    PID TTY          TIME CMD
      2 pts/0    00:00:00 bash
     11 pts/0    00:00:00 ps

7.	Найдите информацию о том, что такое :(){ :|:& };:. Запустите эту команду в своей виртуальной машине Vagrant с Ubuntu 20.04 (это важно, поведение в других ОС не проверялось). Н екоторое время все будет "плохо", после чего (минуты) – ОС должна стабилизироваться. Вызов dmesg расскажет, какой механизм помог автоматической стабилизации. Как настроен этот механизм по-умолчанию, и как изменить число процессов, которое можно создать в сессии?

Ответ:

Из предыдущих лекций ясно что это функция внутри "{}", судя по всему с именем ":" , которая после опредения в строке запускает саму себя.
внутринности через поиск нагуглил, пораждает два фоновых процесса самой себя,
получается этакое бинарное дерево плодящее процессы 

А функционал судя по всему этот:

[ 3099.973235] cgroup: fork rejected by pids controller in /user.slice/user-1000.slice/session-4.scope

[ 3103.171819] cgroup: fork rejected by pids controller in /user.slice/user-1000.slice/session-11.scope

Судя по всему, система на основании этих файлов в пользовательской зоне ресурсов имеет определенное ограничение на создаваемые ресурси 
и соответсвенно при превышении начинает блокировать создание числа 

Если установить ulimit -u 50 - число процессов будет ограниченно 50 для пользоователя. 


## Файловые системы 

1.	Узнайте о sparse (разряженных) файлах.

Ответ:

    Изучил. разреженные файлы изначально занимают меньший объем носителя, чем их реальный объем. Хорошее решение для использования в Торрентах.

2.	Могут ли файлы, являющиеся жесткой ссылкой на один объект, иметь разные права доступа и владельца? Почему?

Ответ:

Так как hardlink это ссылка на тот же самый файл и имеет тот же inode то права будут одни и теже.
в качестве эксперемента проверил:

vagrant@vagrant:~$ touch test_hl

vagrant@vagrant:~$ ln test_hl test_link

vagrant@vagrant:~$ ls -ilh

total 4.0K

526889 -rw-rw-r-- 2 vagrant vagrant  0 Nov 14 11:06 test_hl  

526889 -rw-rw-r-- 2 vagrant vagrant  0 Nov 14 11:06 test_link


vagrant@vagrant:~$ chmod 0755 test_hl 


vagrant@vagrant:~$ ls -ilh

total 4.0K

526889 -rwxr-xr-x 2 vagrant vagrant  0 Nov 14 11:06 test_hl

526889 -rwxr-xr-x 2 vagrant vagrant  0 Nov 14 11:06 test_link


vagrant@vagrant:~$ 

3.	Сделайте vagrant destroy на имеющийся инстанс Ubuntu. Замените содержимое Vagrantfile следующим:  

	Vagrant.configure("2") do |config|
	  config.vm.box = "bento/ubuntu-20.04"
	  config.vm.provider :virtualbox do |vb|
	    lvm_experiments_disk0_path = "/tmp/lvm_experiments_disk0.vmdk"
	    lvm_experiments_disk1_path = "/tmp/lvm_experiments_disk1.vmdk"
	    vb.customize ['createmedium', '--filename', lvm_experiments_disk0_path, '--size', 2560]
	    vb.customize ['createmedium', '--filename', lvm_experiments_disk1_path, '--size', 2560]
	    vb.customize ['storageattach', :id, '--storagectl', 'SATA Controller', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', lvm_experiments_disk0_path]
	    vb.customize ['storageattach', :id, '--storagectl', 'SATA Controller', '--port', 2, '--device', 0, '--type', 'hdd', '--medium', lvm_experiments_disk1_path]
	  end
end
Данная конфигурация создаст новую виртуальную машину с двумя дополнительными неразмеченными дисками по 2.5 Гб.

Ответ:

    Настроено:
root@vagrant:~# lsblk
NAME                 MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sda                    8:0    0   64G  0 disk 
├─sda1                 8:1    0  512M  0 part /boot/efi
├─sda2                 8:2    0    1K  0 part 
└─sda5                 8:5    0 63.5G  0 part 
  ├─vgvagrant-root   253:0    0 62.6G  0 lvm  /
  └─vgvagrant-swap_1 253:1    0  980M  0 lvm  [SWAP]
sdb                    8:16   0  2.5G  0 disk 
sdc                    8:32   0  2.5G  0 disk 

4.	Используя fdisk, разбейте первый диск на 2 раздела: 2 Гб, оставшееся пространство.

Ответ:

Выполнено:
    
Device     Boot   Start     End Sectors  Size Id Type

/dev/sdb1          2048 4196351 4194304    2G 83 Linux

/dev/sdb2       4196352 5242879 1046528  511M 83 Linux

5.	Используя sfdisk, перенесите данную таблицу разделов на второй диск.

Ответ:

root@vagrant:~# sfdisk -d /dev/sdb|sfdisk --force /dev/sdc

Checking that no-one is using this disk right now ... OK

Disk /dev/sdc: 2.51 GiB, 2684354560 bytes, 5242880 sectors

Disk model: VBOX HARDDISK  

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes

>>> Script header accepted.

>>> Script header accepted.

>>> Script header accepted.

>>> Script header accepted.

>>> Created a new DOS disklabel with disk identifier 0xb289fd48.

/dev/sdc1: Created a new partition 1 of type 'Linux' and of size 2 GiB.

/dev/sdc2: Created a new partition 2 of type 'Linux' and of size 511 MiB.

/dev/sdc3: Done.

New situation:

Disklabel type: dos

Disk identifier: 0xb289fd48


Device     Boot   Start     End Sectors  Size Id Type

/dev/sdc1          2048 4196351 4194304    2G 83 Linux

/dev/sdc2       4196352 5242879 1046528  511M 83 Linux


The partition table has been altered.

Calling ioctl() to re-read partition table.

Syncing disks.

root@vagrant:~# 
 

результат:

Disk /dev/sdb: 2.51 GiB, 2684354560 bytes, 5242880 sectors

Disk model: VBOX HARDDISK   

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes

Disklabel type: dos

Disk identifier: 0xb289fd48


Device     Boot   Start     End Sectors  Size Id Type

/dev/sdb1          2048 4196351 4194304    2G 83 Linux

/dev/sdb2       4196352 5242879 1046528  511M 83 Linux



Disk /dev/sdc: 2.51 GiB, 2684354560 bytes, 5242880 sectors

Disk model: VBOX HARDDISK   

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes

Disklabel type: dos

Disk identifier: 0xb289fd48


Device     Boot   Start     End Sectors  Size Id Type

/dev/sdc1          2048 4196351 4194304    2G 83 Linux

/dev/sdc2       4196352 5242879 1046528  511M 83 Linux


6.	Соберите mdadm RAID1 на паре разделов 2 Гб.

Ответ:

Выполнено:

root@vagrant:~# mdadm --create --verbose /dev/md1 -l 1 -n 2 /dev/sd{b1,c1}

mdadm: Note: this array has metadata at the start and

    may not be suitable as a boot device.  If you plan to
    
    store '/boot' on this device please ensure that

    your boot-loader understands md/v1.x metadata, or use

    --metadata=0.90

mdadm: size set to 2094080K

Continue creating array? y

mdadm: Defaulting to version 1.2 metadata

mdadm: array /dev/md1 started.

root@vagrant:~# 

7.	Соберите mdadm RAID0 на второй паре маленьких разделов.

Ответ:

Выполнено:

root@vagrant:~# mdadm --create --verbose /dev/md0 -l 1 -n 2 /dev/sd{b2,c2}

mdadm: Note: this array has metadata at the start and

    may not be suitable as a boot device.  If you plan to

    store '/boot' on this device please ensure that

    your boot-loader understands md/v1.x metadata, or use

    --metadata=0.90

mdadm: size set to 522240K

Continue creating array? y
Continue creating array? (y/n) y

mdadm: Defaulting to version 1.2 metadata

mdadm: array /dev/md0 started.

root@vagrant:~# 


8.	Создайте 2 независимых PV на получившихся md-устройствах.

Ответ:

Выполнено:

root@vagrant:~# pvcreate /dev/md1 /dev/md0

  Physical volume "/dev/md1" successfully created.

  Physical volume "/dev/md0" successfully created.


9.	Создайте общую volume-group на этих двух PV.

Ответ:

Выполнено:

root@vagrant:~# vgcreate vg1 /dev/md1 /dev/md0

  Volume group "vg1" successfully created


root@vagrant:~# vgdisplay

  --- Volume group ---
  VG Name               vgvagrant
  System ID             
  Format                lvm2
  Metadata Areas        1
  Metadata Sequence No  3
  VG Access             read/write
  VG Status             resizable
  MAX LV                0
  Cur LV                2
  Open LV               2
  Max PV                0
  Cur PV                1
  Act PV                1
  VG Size               <63.50 GiB
  PE Size               4.00 MiB
  Total PE              16255
  Alloc PE / Size       16255 / <63.50 GiB
  Free  PE / Size       0 / 0   
  VG UUID               5zL1A7-9ldG-J06F-1Pnu-m7we-mAzr-wBnOoF
   
  --- Volume group ---
  VG Name               vg1
  System ID             
  Format                lvm2
  Metadata Areas        2
  Metadata Sequence No  1
  VG Access             read/write
  VG Status             resizable
  MAX LV                0
  Cur LV                0
  Open LV               0
  Max PV                0
  Cur PV                2
  Act PV                2
  VG Size               2.49 GiB
  PE Size               4.00 MiB
  Total PE              638
  Alloc PE / Size       0 / 0   
  Free  PE / Size       638 / 2.49 GiB
  VG UUID               tojQnc-yOx3-L2uF-35cS-agip-bkwo-5Sz4ol

10.	Создайте LV размером 100 Мб, указав его расположение на PV с RAID0.

Ответ:

Выполнено:

root@vagrant:~# lvcreate -L 100M vg1 /dev/md0

  Logical volume "lvol0" created.

root@vagrant:~# vgs

  VG        #PV #LV #SN Attr   VSize   VFree
  vg1         2   1   0 wz--n-   2.49g 2.39g
  vgvagrant   1   2   0 wz--n- <63.50g    0 

root@vagrant:~# lvs

  LV     VG        Attr       LSize   Pool Origin Data%  Meta%  Move Log Cpy%Sync Convert
  lvol0  vg1       -wi-a----- 100.00m                                                    
  root   vgvagrant -wi-ao---- <62.54g                                                    
  swap_1 vgvagrant -wi-ao---- 980.00m  

11.	Создайте mkfs.ext4 ФС на получившемся LV.

Ответ:

Выполнено:

root@vagrant:~# mkfs.ext4 /dev/vg1/lvol0

mke2fs 1.45.5 (07-Jan-2020)

Creating filesystem with 25600 4k blocks and 25600 inodes

Allocating group tables: done     

Writing inode tables: done       

Creating journal (1024 blocks): done

Writing superblocks and filesystem accounting information: done



12.	Смонтируйте этот раздел в любую директорию, например, /tmp/new.

Ответ:

Выполнено:

root@vagrant:~# mkdir /tmp/new

root@vagrant:~# mount /dev/vg1/lvol0 /tmp/new


13.	Поместите туда тестовый файл, например wget https://mirror.yandex.ru/ubuntu/ls-lR.gz -O /tmp/new/test.gz.

Ответ:

Выполнено:

root@vagrant:~# wget https://mirror.yandex.ru/ubuntu/ls-lR.gz -O /tmp/new/test.gz

--2020-11-14 14:53:09--  https://mirror.yandex.ru/ubuntu/ls-lR.gz

Resolving mirror.yandex.ru (mirror.yandex.ru)... 213.180.204.183, 2a02:6b8::183

Connecting to mirror.yandex.ru (mirror.yandex.ru)|213.180.204.183|:443... connected.

HTTP request sent, awaiting response... 200 OK

Length: 20488555 (20M) [application/octet-stream]

Saving to: ‘/tmp/new/test.gz’

/tmp/new/test.gz     100%[=====================>]  19.54M  6.65MB/s    in 2.9s    

2020-11-14 14:53:12 (6.65 MB/s) - ‘/tmp/new/test.gz’ saved [20488555/20488555]

root@vagrant:~# ls -l /tmp/new

total 20012

-rw-r--r-- 1 root root 20488555 Nov 14 14:17 test.gz

root@vagrant:~# 

14.	Прикрепите вывод lsblk.

Ответ:

Выполнено:

root@vagrant:~# lsblk

NAME                 MAJ:MIN RM  SIZE RO TYPE  MOUNTPOINT
sda                    8:0    0   64G  0 disk  
├─sda1                 8:1    0  512M  0 part  /boot/efi
├─sda2                 8:2    0    1K  0 part  
└─sda5                 8:5    0 63.5G  0 part  
  ├─vgvagrant-root   253:0    0 62.6G  0 lvm   /
  └─vgvagrant-swap_1 253:1    0  980M  0 lvm   [SWAP]
sdb                    8:16   0  2.5G  0 disk  
├─sdb1                 8:17   0    2G  0 part  
│ └─md1                9:1    0    2G  0 raid1 
└─sdb2                 8:18   0  511M  0 part  
  └─md0                9:0    0  510M  0 raid1 
    └─vg1-lvol0      253:2    0  100M  0 lvm   /tmp/new
sdc                    8:32   0  2.5G  0 disk  
├─sdc1                 8:33   0    2G  0 part  
│ └─md1                9:1    0    2G  0 raid1 
└─sdc2                 8:34   0  511M  0 part  
  └─md0                9:0    0  510M  0 raid1 
    └─vg1-lvol0      253:2    0  100M  0 lvm   /tmp/new


15.	Протестируйте целостность файла:

	root@vagrant:~# gzip -t /tmp/new/test.gz

	root@vagrant:~# echo $?

    0

Ответ:

Выполнено:
root@vagrant:~# gzip -t /tmp/new/test.gz && echo $?

0

16.	Используя pvmove, переместите содержимое PV с RAID0 на RAID1.

Ответ:

Выполнено:

root@vagrant:~# pvmove /dev/md0

  /dev/md0: Moved: 12.00%

  /dev/md0: Moved: 100.00%

root@vagrant:~# lsblk

NAME                 MAJ:MIN RM  SIZE RO TYPE  MOUNTPOINT
sda                    8:0    0   64G  0 disk  
├─sda1                 8:1    0  512M  0 part  /boot/efi
├─sda2                 8:2    0    1K  0 part  
└─sda5                 8:5    0 63.5G  0 part  
  ├─vgvagrant-root   253:0    0 62.6G  0 lvm   /
  └─vgvagrant-swap_1 253:1    0  980M  0 lvm   [SWAP]
sdb                    8:16   0  2.5G  0 disk  
├─sdb1                 8:17   0    2G  0 part  
│ └─md1                9:1    0    2G  0 raid1 
│   └─vg1-lvol0      253:2    0  100M  0 lvm   /tmp/new
└─sdb2                 8:18   0  511M  0 part  
  └─md0                9:0    0  510M  0 raid1 
sdc                    8:32   0  2.5G  0 disk  
├─sdc1                 8:33   0    2G  0 part  
│ └─md1                9:1    0    2G  0 raid1 
│   └─vg1-lvol0      253:2    0  100M  0 lvm   /tmp/new
└─sdc2                 8:34   0  511M  0 part  
  └─md0                9:0    0  510M  0 raid1 
root@vagrant:~# 

17.	Сделайте --fail на устройство в вашем RAID1 md.

Ответ:

Выполнено:

root@vagrant:~# mdadm /dev/md1 --fail /dev/sdb1

mdadm: set /dev/sdb1 faulty in /dev/md1

root@vagrant:~# mdadm -D /dev/md1
/dev/md1:
           Version : 1.2
*******
Consistency Policy : resync

              Name : vagrant:1  (local to host vagrant)
              UUID : 1aac0a29:
root@vagrant:~# mdadm -D /dev/md1
/dev/md1:
           Version : 1.2
0fa0dc73:082e1042:fe00b376
            Events : 19

    Number   Major   Minor   RaidDevice State
       -       0        0        0      removed
       1       8       33        1      active sync   /dev/sdc1

       0       8       17        -      faulty   /dev/sdb1

18.	Подтвердите выводом dmesg, что RAID1 работает в деградированном состоянии.

Ответ:

Выполнено:

root@vagrant:~# dmesg |grep md1

[  480.422928] md/raid1:md1: not clean -- starting background reconstruction
[  480.422930] md/raid1:md1: active with 2 out of 2 mirrors
[  480.422945] md1: detected capacity change from 0 to 2144337920
[  480.425781] md: resync of RAID array md1
[  490.758344] md: md1: resync done.
[ 2325.890719] md/raid1:md1: Disk failure on sdb1, disabling device.
               md/raid1:md1: Operation continuing on 1 devices.

19.	Протестируйте целостность файла, несмотря на "сбойный" диск он должен продолжать быть доступен:

	root@vagrant:~# gzip -t /tmp/new/test.gz

	root@vagrant:~# echo $?

    0

Ответ:

Выполнено:

root@vagrant:~# gzip -t /tmp/new/test.gz && echo $?

0

20.	Погасите тестовый хост, vagrant destroy.

Ответ:

Выполнено:

22:12:43 andiv@upc(0):~/vagrant$ vagrant destroy

    default: Are you sure you want to destroy the 'default' VM? [y/N] y

==> default: Forcing shutdown of VM...

==> default: Destroying VM and associated drives...


## Компьютерные сети №1

1. Работа c HTTP через телнет. Подключитесь утилитой телнет к сайту stackoverflow.com telnet stackoverflow.com 80 отправьте HTTP запрос GET /questions HTTP/1.0 HOST: stackoverflow.com [press enter] [press enter] В ответе укажите полученный HTTP код, что он означает?

Ответ:

andiv@vm netology % telnet stackoverflow.com 80
Trying 151.101.193.69...
Connected to stackoverflow.com.
Escape character is '^]'.
GET /questions HTTP/1.0
Host: stackoverflow.com

HTTP/1.1 301 Moved Permanently
Server: Varnish
Retry-After: 0
Location: https://stackoverflow.com/questions
Content-Length: 0
Accept-Ranges: bytes
Date: Sat, 17 Sep 2022 09:44:27 GMT
Via: 1.1 varnish
Connection: close
X-Served-By: cache-hhn4042-HHN
X-Cache: HIT
X-Cache-Hits: 0
X-Timer: S1663407867.398777,VS0,VE0
Strict-Transport-Security: max-age=300
X-DNS-Prefetch-Control: off

Connection closed by foreign host.

Код HTTP ответа: 301 

Перенаправление на другой ресурс, или проще говоря - "Редирект", классический код ответа HTTP, который мы получаем в ответ от нашего запроса, в ситуации, когда ресурс имеет другое месторасположения.

2. Повторите задание 1 в браузере, используя консоль разработчика F12. откройте вкладку Network отправьте запрос http://stackoverflow.com найдите первый ответ HTTP сервера, откройте вкладку Headers укажите в ответе полученный HTTP код. проверьте время загрузки страницы, какой запрос обрабатывался дольше всего? приложите скриншот консоли браузера в ответ.

Ответ: код 200 дольше всех обрабатывался stackoverflow 303,67 ms

![ms](https://github.com/and1V/netology.devops/blob/main/pictures/stack_ms.png?raw=true)

![http_200](https://github.com/and1V/netology.devops/blob/main/pictures/stack_200_http.png?raw=true)


3. Какой IP адрес у вас в интернете?

Ответ: 185.20.45.14

4. Какому провайдеру принадлежит ваш IP адрес? Какой автономной системе AS? Воспользуйтесь утилитой whois

Ответ:

 netname: NECSTEL-NET descr: OOO "Necstel" origin: AS - AS61068


5. Через какие сети проходит пакет, отправленный с вашего компьютера на адрес 8.8.8.8? Через какие AS? Воспользуйтесь утилитой traceroute

Ответ:
Трассировка маршрута к dns.google [8.8.8.8]

andiv@vm netology.devops % traceroute 8.8.8.8

traceroute to 8.8.8.8 (8.8.8.8), 64 hops max, 52 byte packets

 1  router.lan (192.168.10.1)  9.127 ms  1.764 ms  2.460 ms

 2  dns.google (8.8.8.8)  3.743 ms  2.276 ms  1.787 ms

 3  185.20.45.1 (185.20.45.1)  2.795 ms  4.606 ms  2.751 ms

 4  vrrp8.naukanet.ru (77.94.164.129)  16.229 ms  5.204 ms  2.944 ms

 5  77.94.160.77 (77.94.160.77)  8.724 ms  5.182 ms  2.696 ms

 6  209.85.148.20 (209.85.148.20)  4.056 ms  4.687 ms  3.355 ms

 7  108.170.250.66 (108.170.250.66)  4.558 ms

    108.170.250.113 (108.170.250.113)  29.452 ms

    108.170.250.83 (108.170.250.83)  4.710 ms

 8  142.251.238.82 (142.251.238.82)  22.338 ms

    142.251.49.78 (142.251.49.78)  19.110 ms

    142.251.237.154 (142.251.237.154)  20.903 ms

 9  72.14.232.76 (72.14.232.76)  18.888 ms

    142.250.235.62 (142.250.235.62)  20.865 ms

    216.239.43.20 (216.239.43.20)  21.829 ms

10  209.85.246.111 (209.85.246.111)  25.456 ms

    216.239.49.115 (216.239.49.115)  24.871 ms

    216.239.58.65 (216.239.58.65)  24.840 ms

11  * * *

12  * * *

13  * * *

14  * * *

15  * * *

16  * * *

17  * * *

18  * * *

19  * * *

20  * dns.google (8.8.8.8)  21.444 ms  18.233 ms

Проходит через сети:

router.lan (192.168.10.1) - мой роутер

dns.google (8.8.8.8) - NetName: LVLT-ORG-8-8

185.20.45.1 - netname: NECSTEL-NET origin: AS61068

vrrp8.naukanet.ru (77.94.164.129) - Technical Center of Internet

77.94.160.77 - netname: RU-NAUKANET-20070605

209.85.148.20 - NetName: GOOGLE NetHandle: NET-209-85-128-0-1

108.170.250.66 - NetName: GOOGLE NetHandle: NET-108-170-192-0-1

108.170.250.113 - NetName: GOOGLE NetHandle: NET-108-170-192-0-1

108.170.250.83 - NetName: GOOGLE NetHandle: NET-108-170-192-0-1 OriginAS: AS15169

142.251.238.82 - NetName: GOOGLE NetHandle: NET-142-250-0-0-1 OriginAS: AS15169

72.14.232.76 - NetName: GOOGLE NetHandle: NET-72-0-0-0-0

209.85.246.111 - NetName: GOOGLE NetHandle: NET-209-0-0-0-0

6. Повторите задание 5 в утилите mtr. На каком участке наибольшая задержка - delay?   

Ответ: наибольшая задержка между 77.94.164.129 (средняя 5.204 ms) и 77.94.160.77 (средняя 5.182 ms)

7. Какие DNS сервера отвечают за доменное имя dns.google? Какие A записи? воспользуйтесь утилитой dig

Ответ:

8.8.8.8

8.8.4.4

;; ANSWER SECTION:

dns.google. 176 IN A 8.8.8.8

dns.google. 176 IN A 8.8.4.4

andiv@vm netology.devops % dig dns.google +nssearch

SOA ns1.zdns.google. cloud-dns-hostmaster.google.com. 1 21600 3600 259200 300 from server 216.239.38.114 in 16 ms.

SOA ns1.zdns.google. cloud-dns-hostmaster.google.com. 1 21600 3600 259200 300 from server 216.239.36.114 in 19 ms.

SOA ns1.zdns.google. cloud-dns-hostmaster.google.com. 1 21600 3600 259200 300 from server 216.239.34.114 in 46 ms.

SOA ns1.zdns.google. cloud-dns-hostmaster.google.com. 1 21600 3600 259200 300 from server 216.239.32.114 in 48 ms.

8. Проверьте PTR записи для IP адресов из задания 7. Какое доменное имя привязано к IP? воспользуйтесь утилитой dig
Ответ:

ANSWER SECTION:

8.8.8.8.in-addr.arpa. 75016 IN PTR dns.google.

ptr адресс - 8.8.8.8.in-addr.arpa.

а доменное имя привязанное dns.google.


## Копьютерные сети №2

1. Проверьте список доступных сетевых интерфейсов на вашем компьютере. Какие команды есть для этого в Linux и в Windows? 

Ответ: 

Windows: 

Для ipv4 GetAdaptersInfo Для Ipv6 GetAdaptersAddresses Можно получить список сетевых адаптеров GetIfTable или GetIfEntry или GetIfTabl, ipconfig /all

Linux: 

nmcli con show

ifocnfig

ip a |awk '/state UP/{print $2}' eth0:

или ip -o a show | cut -d ' ' -f 2,7

или

ip a |grep -i inet | awk '{print $7, $2}'


2. Какой протокол используется для распознавания соседа по сетевому интерфейсу? Какой пакет и команды есть в Linux для этого?

Ответ: 

Neighbor Discovery Protocol (NDP) , пакет iproute2

3. Какая технология используется для разделения L2 коммутатора на несколько виртуальных сетей? Какой пакет и команды есть в Linux для этого? Приведите пример конфига.

Ответ: 

vlan и пакет iproute2 

Пример конфига: ip link add link eth0 name eth0.111 type vlan id 111 ip link set dev eth0.111 up ip a add 192.168.111.2/24 dev eth0.111

или

TYPE-Ethernet

VLAN=yes

ONBOOT=yes

BOOTPROTO=static

DEVICE=eth0.111

IPADDR=192.168.111.2

GATEWAY=192.168.111.1

DNS1=8.8.8.8

DNS2=8.8.4.4

4. Какие типы агрегации интерфейсов есть в Linux? Какие опции есть для балансировки нагрузки? Приведите пример конфига.

Ответ:
 Mode-0(balance-rr Mode-1(active-backup) Mode-2(balance-xor) Mode-3(broadcast) Mode-4(802.3ad) Mode-5(balance-tlb) Mode-6(balance-alb) Б) [root@andiv]# modprobe bonding [root@andiv]# ip addr add 192.168.100.33/24 brd + dev bond0 [root@andiv]# ip link set dev bond0 up [root@andiv]# ifenslave bond0 eth2 eth3 master has no hw address assigned; getting one from slave! The interface eth2 is up, shutting it down it to enslave it. The interface eth3 is up, shutting it down it to enslave it. [root@andiv]# ifenslave bond0 eth2 eth3 [root@andiv]# cat /proc/net/bond0/info Bonding Mode: load balancing (round-robin) MII Status: up MII Polling Interval (ms): 0 Up Delay (ms): 0 Down Delay (ms): 0

Slave Interface: eth2 MII Status: up Link Failure Count: 0

Slave Interface: eth3 MII Status: up Link Failure Count: 0

5. Сколько IP адресов в сети с маской /29 ? Сколько /29 подсетей можно получить из сети с маской /24. Приведите несколько примеров /29 подсетей внутри сети 10.10.10.0/24

Ответ:
 8 адресов с маской подсети /29, минус броадкаст и адрес сети - в этой сети может быть 6 хостов 32 шт 29 посетей помещается в 24 подсети примеры: 10.10.10.0/29 10.10.10.8/29 10.10.10.16/29 10.10.10.24/29 10.10.10.32/29

6. Задача: вас попросили организовать стык между 2-мя организациями. Диапазоны 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 уже заняты. Из какой подсети допустимо взять частные IP адреса? Маску выберите из расчета максимум 40-50 хостов внутри подсети. 

Ответ: 
192.0.0.0/26 на 62 хоста

Можно взять из 100.64.0.0/10

In 2012, the IETF defined a Shared Address Space[4] for use in ISP CGN deployments and NAT devices that can handle the same addresses occurring both on inbound and outbound interfaces. ARIN returned space to the IANA as needed for this allocation and[5] "The allocated address block is 100.64.0.0/10".[4][6]

7. Как проверить ARP таблицу в Linux, Windows? Как очистить ARP кеш полностью? Как из ARP таблицы удалить только один нужный IP? 

Ответ: 

Для windows:
Посмотреть все ip: arp –a Удалить все ip: netsh interface ip delete arpcache удалить один ip: arp -d 192.168.3.171

 для Linux: 
 посмотреть все - ip n удалить все ip n flush all удалить один ip n del 192.168.0.1 dev eth0


## Командная оболочка Bash: Практические навыки"

Обязательная задача 1

Есть скрипт:

a=1
b=2
c=a+b
d=$a+$b
e=$(($a+$b))
Какие значения переменным c,d,e будут присвоены? Почему?

Знак $ отличает,что хочешь взять строку или переменную. Если $ есть,то это переменная.

Переменная	Значение	Обоснование
c	a+b	указали текст а не переменные
d	1+3	команда преобразовала вывела значения переменных, но не выполнила арифметические операции так как по умолчанию это строки
e	3	так как теперь за счет скобок мы дали команду на выполнение арифметической операции со значениями переменных

Обязательная задача 2

На нашем локальном сервере упал сервис и мы написали скрипт, который постоянно проверяет его доступность, записывая дату проверок до тех пор, пока сервис не станет доступным (после чего скрипт должен завершиться). В скрипте допущена ошибка, из-за которой выполнение не может завершиться, при этом место на Жёстком Диске постоянно уменьшается. Что необходимо сделать, чтобы его исправить:

while ((1==1)
do
	      curl https://localhost:4757
	      if (($? != 0))
	      then
		            date >> curl.log
	      fi
done

Ваш скрипт:

2а В условии не хватает закрывающей скобки ) 
2б Слишком частые проверки забивают файл, нужно добавить sleep $timeout - для задания интервала проверки 
2в Нужно добавить проверку успешности чтобы выйти из цикла например: else exit В итоге так: 
    while (( 1 == 1 ))
 do
        curl https://localhost:4757
        if (($? != 0))
        then
            date >> curl.log
        else exit
        fi
        sleep 5
    done

Обязательная задача 3

Необходимо написать скрипт, который проверяет доступность трёх IP: 192.168.0.1, 173.194.222.113, 87.250.250.242 по 80 порту и записывает результат в файл log. Проверять доступность необходимо пять раз для каждого узла.

Ваш скрипт:

andiv@andiv:~/bash$ cat check_hosts
hosts=(192.168.0.1 173.194.222.113 87.250.250.24)
timeout=5
for i in {1..5}
do
date >>hosts.log
    for h in ${hosts[@]}
    do
	      curl -Is --connect-timeout $timeout $h:80 >/dev/null
        echo "    check" $h status=$? >>hosts.log
    done
done

Обязательная задача 4

Необходимо дописать скрипт из предыдущего задания так, чтобы он выполнялся до тех пор, пока один из узлов не окажется недоступным. Если любой из узлов недоступен - IP этого узла пишется в файл error, скрипт прерывается.

Ваш скрипт:
Надо добавить в начало скрипта указание списка хостов через переменную, а так же таймаут на ожидания коннекта для курла в цикле укажем выполнять пока переменная res = 0 (в которую занишем результат curl)
andiv@andiv(0):~/bash$ cat check2_hosts
hosts=(192.168.0.1 173.194.222.113 87.250.250.24)
timeout=5
res=0

while (($res == 0))
do
    for h in ${hosts[@]}
    do
	      curl -Is --connect-timeout $timeout $h:80 >/dev/null
	      res=$?
	      if (($res != 0))
	      then
	          echo "    ERROR on " $h status=$res >>hosts2.log
	      fi
    done
done
