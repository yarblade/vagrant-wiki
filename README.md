# Установка
- (если в BIOS есть галка hardware virtualization technology (VT-x) то ее нужно включить)
- [VirtualBox] (https://www.virtualbox.org/wiki/Downloads)
- [Git] (http://git-scm.com/downloads)
- [Vagrant] (https://www.vagrantup.com/)

# Настройка новой VM
- Скопируйте папку \ofc-cls\fs\Common\vagrant\VM\ к себе.
- В файлике reinstall.sh поправьте CONF_PATH(путь до конфига sphinx в формате linix т.е. меняем \ на /).
- Запустите ярлычок bash 
- Выполните в консоли (чтобы вставить в консоль из буфера обмена используем Shift+Insert)
``` 
vagrant box add base //ofc-cls/fs/Common/vagrant/base.box -f
sh update.sh
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
- кликнуть по файлику update.sh в проводнике или sh update.sh в консоли
 


