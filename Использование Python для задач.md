## Использование Python для решения типовых DevOps задач

***Обязательная задача 1***
______________
***Есть скрипт:***
```
#!/usr/bin/env python3
a = 1
b = '2'
c = a + b
```
Вопросы:

| Вопрос        | Ответ      
| ------------- |:-------------:| 
| Какое значение будет присвоено переменной c?      | Возникнет ошибка, (не соответствие типы переменных, нельзя сложить строку и число, питон так не умеет)| 
| Как получить для переменной c значение 12?      | надо добавить кавычки‘1’     |   
| Как получить для переменной c значение 3? | надо убрать из переменной b (‘2’), кавычки и оставить просто число     |    
		
	
***Обязательная задача 2***
___________________________
Мы устроились на работу в компанию, где раньше уже был DevOps Engineer. Он написал скрипт, позволяющий узнать, какие файлы модифицированы в репозитории, относительно локальных изменений. Этим скриптом недовольно начальство, потому что в его выводе есть не все изменённые файлы, а также непонятен полный путь к директории, где они находятся. Как можно доработать скрипт ниже, чтобы он исполнял требования вашего руководителя?
```
#!/usr/bin/env python3

import os

bash_command = ["cd ~/netology/netology.devops", "git status"]
result_os = os.popen(' && '.join(bash_command)).read()
is_change = False
for result in result_os.split('\n'):
    if result.find('modified') != -1:
        prepare_result = result.replace('\tmodified:   ', '')
        print(prepare_result)
        break
```
***Ваш скрипт:***
```
import os

DIR = '~/netology/netology.devops'

bash_command = [f"cd {DIR} 2>&1", "pwd", "git status --porcelain 2>&1"]

result_os = os.popen(' && '.join(bash_command)).read().split('\n')

#first string is our basepath
project_dir = result_os.pop(0)

#if cd command rerutns something like "/bin/sh: line 0: cd: " assuming no such dir
if project_dir.find('/bin/sh: line 0: cd:') != -1: 
  print('No such dir')
  exit(2)

#if git command rerutns something like "fatal: Not a git repository ..." assuming not a repository
if result_os[0].find('fatal:') != -1: 
  print('Not a repo')
  exit(2)

#remove tailing empty string
if result_os[-1] == '':
    result_os.pop()

def resolve_status(status):
    status_mapping = {
      'M': 'modified',
      'A': 'added',
      'D': 'deleted',
      'R': 'renamed',
      'C': 'copied',
      'U': 'updated',
      '??': 'untracked'
  }
    try:
        return status_mapping[status]
    except KeyError:
        return status


for f in result_os:
    status = resolve_status(f[0:2].strip())
    path = os.path.join(project_dir, f[3:len(f)])

    print(f'{status}: {path}')
```
***Вывод скрипта при запуске при тестировании:***
```
Он не должен принимать никакие параметры и просто искать в папке
Например, 
Если удалить папку или файлы то он найдет их тоже 
[root@localhost andiv]# python3 test.py /home/andiv/netology.devops/
deleted: /home/andiv/netology.devops/README.md
 клонировал репозиторий и изменил только один файл и он вывел его. 
[root@localhost andiv]# python3 test.py /home/andiv/netology.devops/
untracked: /home/andiv/netology.devops/Readme.md
```                                                                                                          
***Обязательная задача 3***
________________________

Доработать скрипт выше так, чтобы он мог проверять не только локальный репозитори й в текущей директории, а также умел воспринимать путь к репозиторию, который мы передаём как входной параметр. Мы точно знаем, что начальство коварное и будет проверять работу этого скрипта в директориях, которые не являются локальными репозиториями.
***Ваш скрипт:***
```
import os, sys

DIR = '~/netology/netology.devops'

try:
    DIR = sys.argv[1]
except IndexError:
    pass

bash_command = [f"cd {DIR} 2>&1", "pwd", "git status --porcelain 2>&1"]

result_os = os.popen(' && '.join(bash_command)).read().split('\n')

#first string is our basepath
project_dir = result_os.pop(0)

#if cd command rerutns something like "/bin/sh: line 0: cd: " assuming no such dir
if project_dir.find('/bin/sh: line 0: cd:') != -1: 
  print('No such dir')
  exit(2)

#if git command rerutns something like "fatal: Not a git repository ..." assuming not a repository
if result_os[0].find('fatal:') != -1: 
  print('Not a repo')
  exit(2)

#remove tailing empty string
if result_os[-1] == '':
    result_os.pop()

def resolve_status(status):
    status_mapping = {
      'M': 'modified',
      'A': 'added',
      'D': 'deleted',
      'R': 'renamed',
      'C': 'copied',
      'U': 'updated',
      '??': 'untracked'
  }
    try:
        return status_mapping[status]
    except KeyError:
        return status


for f in result_os:
    status = resolve_status(f[0:2].strip())
    path = os.path.join(project_dir, f[3:len(f)])

    print(f'{status}: {path}') 
```
***Вывод скрипта при запуске при тестировании:***
```
Вывод похож на вторую задачу только принимает путь в параметр. 
Например, клонировал репозиторий и изменил только один файл и он вывел его. 
[root@localhost andiv]# python3 test.py /home/andiv/netology.devops/
untracked: /home/andiv/netology.devops/Readme.md

Если удалить папку или файлы то он найдет их тоже 
[root@localhost andiv]# python3 test.py /home/andiv/netology.devops/
deleted: /home/andiv/netology.devops/README.md
deleted: /home/andiv/netology.devops/bash.png
deleted: /home/andiv/netology.devops/jsonnet.png
deleted: /home/andiv/netology.devops/markdown.png
deleted: /home/andiv/netology.devops/terraform.png
deleted: /home/andiv/netology.devops/yaml.png
deleted: /home/andiv/netology.devops/netology.jsonnet
deleted: /home/andiv/netology.devops/netology.md
deleted: /home/andiv/netology.devops/netology.sh
deleted: /home/andiv/netology.devops/netology.tf
deleted: /home/andiv/netology.devops/netology.yaml
untracked: /home/andiv/netology.devops/Readme.md
```
***Обязательная задача 4***
_____________
Наша команда разрабатывает несколько веб-сервисов, доступных по http. Мы точно знаем, что на их стенде нет никакой балансировки, кластеризации, за DNS прячется конкретный IP сервера, где установлен сервис. Проблема в том, что отдел, занимающийся нашей инфраструктурой очень часто меняет нам сервера, поэтому IP меняются примерно раз в неделю, при этом сервисы сохраняют за собой DNS имена. Это бы совсем никого не беспокоило, если бы несколько раз сервера не уезжали в такой сегмент сети нашей компании, который недоступен для разработчиков. Мы хотим написать скрипт, который опрашивает веб-сервисы, получает их IP, выводит информацию в стандартный вывод в виде: <URL сервиса> - <его IP>. Также, должна быть реализована возможность проверки текущего IP сервиса c его IP из предыдущей проверки. Если проверка будет провалена - оповестить об этом в стандартный вывод сообщением: [ERROR] <URL сервиса> IP mismatch: <старый IP> <Новый IP>. Будем считать, что наша разработка реализовала сервисы: drive.google.com, mail.google.com, google.com.
***Ваш скрипт:***
```
import socket, sys, json

HISTORY_FILE = 'history.json'


def main():

  if len(sys.argv) < 2:
    print("No hostname specified")
    exit()

  history = load_history(HISTORY_FILE)

  for hostname in sys.argv[1:]:
    process_host(hostname, history)

  save_history(HISTORY_FILE, history)


def load_history(filename):
  
  try:
    with open(filename) as f:
      return json.load(f)

  except FileNotFoundError:
    print('History bot found, creating new history')
    return {}


def save_history(file, history):

  with open(file, 'w') as f:
    json.dump(history, f)


def process_host(hostname, known_names):

  last_ip = False

  try:
    last_ip = known_names[hostname]

  except KeyError:
    pass

  try:
      ip = socket.gethostbyname(hostname)

  except socket.gaierror:
      print('Host resolve failed')
      exit()
      
  if last_ip and last_ip != ip:
    print(f'[ERROR] {hostname} IP mismatch: {last_ip} {ip}')
    
  else:
    print(f'{hostname} - {ip}')

  known_names[hostname] = ip


if __name__ == "__main__":
  main()
```
***Вывод скрипта при запуске при тестировании:***
```
py .\test2.py drive.google.ru google.com  mail.google.com
drive.google.ru - 87.250.250.242
google.com - 74.125.131.138
[ERROR] mail.google.ru IP mismatch: 217.69.139.202 94.100.180.201
mail.google.com - 209.85.233.18
```