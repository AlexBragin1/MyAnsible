Ansible
Использовал два сервера Debian и OracleLinux(109.207.173.166 и 93.183.75.20)
Роли: 
  - adduser: создает нового пользователя myuser с правами sudo, устанавливет ключ пользователю, правит файл /etc/ssh/ssh_config меняет порт 10022, запрещает по поролю логиниться
  - install_program устанавливает программы -mc;htop,atop,dhcu
  - update_system обновляет систему
  - inst_nginx устанавливает  nginx для дебиан копирует файл myback.conf в папку sites-available и создает симлинк в папке sites-enabled, также создаем нашу страницу index.html в папке /var/www/html. Для Oracle:  копируем наш файл с настройкой сервера в папку /etc/conf.d/nginx1.conf, также скопируем файл nginx.conf c настройками nginx в папку /etc/nginx/, затем нашу страницу в   index.html в папку /var/www/html

  -   ивентори файл - ansible.cfg
  -   групповые переменные в папки groupvars, где указан порт 22(который  меняется при выполненние adduser на порт 10022)




Файл hosts переменная домен kroot.ru:
[start_server_OracleLinux]
93.183.75.20 virt_dom=kroot.ru
[start_server_Debian] 
109.207.173.166 virt_dom=kroot.ru
    файл конфигурации для debian(myback.conf и nginx1.conf)





Если набрать в браузере http://109.207.173.166 и http://93.183.75.20  откроется сайт где будет написано "практичекое задание" 
