# Порядок установки

1. Создать файл .env по образу [.env_template](.env_template)
2. В .env и настроить параметры MySQL
   * Настроить название проекта (APP_NAME)
   * Настроить параметры MySQL
   * Настроить порты
3. Из корневой папки запустить команду `sudo docker-compose up -d nginx`
4. Открыть страницу по адресу http://localhost:8000/bitrixsetup.php
   Настроить проект

   Настройка базы данных
   ![img.png](img.png)

5. Из корневой папки запустить команды
   - `sudo chmod -R 777 src` (Меняет права доступа папки /src)
   - `sudo chmod -R 777 dbdata` (Меняет права доступа папки /dbdata)
   
Всё готово

---

Главная страница http://localhost:8000/

phpMyAdmin http://localhost:8001/

[ссылка на хороший урок](https://www.youtube.com/watch?v=5bSA__OWebM&list=PLVbFKmfZNpmS7vzmlwL3j7Mek7EMOGycN&index=9)

[хороший аналог](https://github.com/bitrixdock/bitrixdock/tree/master)

---

# Команды

## Docker-compose

### Запустить

`sudo docker-compose up -d`

`-d` - запуск, чтобы пользоваться консолью


### Запустить только контейнер nginx

`sudo docker-compose up -d nginx`

---

### Остановить

Просто остановить

`sudo docker-compose down`


Остановить и удалить

`sudo docker-compose down -v`

---

### Логи

`sudo docker-compose logs mysql`

---

### Изменять права доступа для проекта на текущего пользователя в текущей папки

`sudo chown -R $USER:$USER .`

---

### Изменить права доступа для папки storage в проекте

`sudo chmod -R 777 src`

---

## MySQL
В локальной системе порт 3316, в контейнерах 3306

Имя хоста такое же, как у контейнера (`mysql`)