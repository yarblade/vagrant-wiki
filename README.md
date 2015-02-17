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
- Создать пустую папку для работы с box-ом и открыть ее 
- В папке создать ярлык для консоли "C:\Program Files (x86)\Git\bin\sh.exe" --login -i
- Запустить консоль
``` 
vagrant add box base \\ofc-cls\fs\Common\vagrant\base.box
vagrant init base
```

# Работа с VM
Для начала нужно запустить консоль

запуск VM
- `vagrant up`

остановить VM
- `vagrant suspend`

ssh
 - `vagrant ssh`


