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



    




