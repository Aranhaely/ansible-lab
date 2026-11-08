# Ansible Infrastructure Provisioning

Декларативный провижининг веб-серверов и Docker-хостов на Ubuntu 26.04 LTS.
Реализованно через утилиту multipass и wsl2 на одной машине.
Wsl2: control node.
Multipass: node1 and node2.

## Возможности

- Идемпотентность: повторный запуск даёт `changed=0`
- Бинарные GPG-ключи и DEB822-репозитории (требование Ubuntu 24.04+)
- Разделение данных и логики через `group_vars`
- Проходит `ansible-lint` без предупреждений

## Быстрый старт

multipass.exe ls - взять IP и перенести вручную в inventory.ini

# Запуск
ansible-playbook site.yml