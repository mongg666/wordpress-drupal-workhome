# Ansible Playbook для установки WordPress на Debian 12

## Требования
- Ansible 2.9+
- Хост с Debian 12 (IP: `192.168.1.100` в примере)
- Доступ по SSH: пользователь `vboxuser`, пароль `king_clown666`, права sudo

## Шаги развертывания

1. **Подготовка инвентаря**
   - Откройте файл `inventories/production/hosts`
   - Замените `192.168.1.100` на IP вашего сервера

2. **Настройка переменных**
   - Откройте `inventories/production/group_vars/all.yml`
   - Измените пароли (особенно `mysql_root_password` и `mysql_password`)

3. **Запуск Playbook**
   ```bash
   ansible-playbook -i inventories/production/hosts site.yml -K
