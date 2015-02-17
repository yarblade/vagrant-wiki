# vagrant-wiki

[что умеет vagrant] (https://drive.draw.io/?#G0B2HYM9B-AFTrWVdaYTMzRjNyNjA)

[как изменять конфигурацию] (https://drive.draw.io/#G0B2HYM9B-AFTrbkhyWjdLdW95ZVU)

А как у других? [Rails] (https://github.com/rails/rails-dev-box)


# Установка
- (если в BIOS есть галка hardware virtualization technology (VT-x) то ее нужно включить)
- [VirtualBox] (https://www.virtualbox.org/wiki/Downloads)
- [Git] (http://git-scm.com/downloads)
- [Vagrant] (https://www.vagrantup.com/)

# Настройка новой VM
- Создать пустую папку для работы с box-ом(папка VM)
- Скопируйте в папку VM каталог sql\sphinx из проекта
- Создайте файлик update.sh содержаший следующий скрипт
```
cp {Путь до проекта}/sql/sphinx/sphinx.conf ./sphinx
cd sphinx 
SphinxConfigGenerator.exe sphinx.conf sphinx_config.ini sprint
cp sphinx_sp.conf ../sphinx.conf
vagrant destroy
vagrant up
```
  впишите туда путь до проекта
- Откройте файл /sphinx/sphinx_config.ini в блоке [sprint] пропишите новые значения
```
 dbServer = 4.4.4.1
 dbPort = порт бд (например 3306)
 dbName = название базы (например job)
 pid_file = /var/run/sphinxsearch/searchjob.pid
```

- В папке VM создать ярлык для консоли "C:\Program Files (x86)\Git\bin\sh.exe" --login -i
- Выполните в консоли (чтобы вставить в консоль из буфера обмена используем Shift+Insert)
``` 
vagrant box add base //ofc-cls/fs/Common/vagrant/base.box -f
vagrant init base -m
```

# Работа с VM
Для начала нужно запустить консоль

запуск VM
- `vagrant up`

остановить VM
- `vagrant suspend`

ssh
 - `vagrant ssh`
 
перестройка VM
- sh update.sh (либо кликнуть по файлику в проводнике)
 


