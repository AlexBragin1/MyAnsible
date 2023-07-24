Ansible
Использовал два сервера Debian и OracleLinux(109.207.173.166 и 93.183.75.20)
Роли: 
  - adduser: создает нового пользователя myuser с правами sudo, устанавливет ключ пользователю, правит файл /etc/ssh/ssh_config меняет порт 10022, запрещает по поролю логиниться
  - install_program устанавливает программы -mc;htop,atop,dhcu
  - update_system обновляет систему
  - inst_nginx устанавливает  nginx
  ивентори файл - ansible.cfg
  групповые переменные в папки groupvars, где указан порт 10022
файл hosts переменная домен kroot.ru:
[start_server_OracleLinux]
93.183.75.20 virt_dom=kroot.ru
[start_server_Debian] 
109.207.173.166 virt_dom=kroot.ru
