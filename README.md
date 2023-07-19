# AnsibleTask
Выпускная квалификационная работа

## Поддерживаемые роли

На данный момент доступны следующие функции:

1. Обновление всех программ (роль upgrade_programs)
2. Добавление нового пользователя (роль add_users)
3. Добавление прав sudo (роль add_sudo)
4. Добавление новому пользователю ключа SSH (роль add_ssh)
5. Установку пакетов mc, htop, atop, ncdu (роль install_smth)
6. Смену порта SSH и закрытие доступа по паролю (роль ssh_work)
7. Установка и настройка конфигурации nginx (роль nginx)

Для ролей определены теги, описанные в файле `playbook.yml`. Запуск осуществляется с помощью команды:
```
ansible-playbook -i inventory/inventory.yml playbook.yml --tags=<имена_выполняемых_тегов>
```

## Переменные

Перед выполнением команд необходимо заполнить переменные, используемые в выполняемых действиях: имя пользователя, пароль, публичный SSH ключ и т.д.
Смотрите папки `roles/*/vars/`.
