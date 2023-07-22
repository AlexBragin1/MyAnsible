Ansible
Использовал два сервера Debian и OracleLInux
Роли: 
  - adduser: создает нового пользователя myuser с правами sudo, устанавливет ключпользователю, правит файл /etc/ssh/ssh_config меняет порт 10022, запрещает по поролю логиниться
  - install_program устанавливает программы -mc;htop,atop,dhcu
  - update_system обновляет систему
  - inst_nginx устанавливает  nginx

