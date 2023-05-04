# otus-ansible
Работа с Ansible

Описание:

После запуска vagrant up разворачивается стенд при помощи libvirt (сменить провайдер можно в вагрантфайле):

1. Для установки сервисов используется модуль yum
2. Конфигурационные файлы взяты из шаблона jinja2 (playbooks/templates/nginx.conf.j2)
3. После установки статус сервиса nginx в systemd - enabled
4. Для рестарта сервиса использован notify
5. Сайт слушает на нестандартном порту - 8080, для этого использовалась переменная "nginx_listen_port: 8080"

Для проверки выполнить:

vagrant up

Проверить доступность сайта:
http://192.168.122.150:8080
