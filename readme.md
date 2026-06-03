# Деплой Nginx с помощью Ansible

Автоматизация развертывания веб-сервера Nginx на удаленном хосте.

## Требования
* Целевой хост (`VM-2`) доступен по SSH для пользователя `runner` с беспарольным `sudo`.
* IP-адрес целевого хоста прописан в inventory.ini.

## Запуск плейбука
```bash
# Тестовый прогон
ansible-playbook playbook.yml -i inventory.ini --check --diff

# Установка Nginx и деплой index.html
ansible-playbook playbook.yml -i inventory.ini
```

## Структура проекта
* inventory.ini — конфигурационный файл инвентаря с целевыми хостами.
* playbook.yml — сценарий установки и копирования страницы.
* index.html — развертываемая веб-страница.

## Результат работы
![Результат работы](result.png)
