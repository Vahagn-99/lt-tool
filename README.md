# 🛠️ LT - Laravel Tool CLI

**LT** — это лёгкий CLI-инструмент, альтернативный Laravel Sail, для удобного взаимодействия с Docker Compose без привязки к Laravel-проекту.

📦 Упрощённая работа с контейнерами  
⚙️ Не требует модификации проекта  
🧠 Использует переменные из `.env`

---

## 📥 Установка

Скачай `.deb` файл с [Releases](https://github.com/Vahagn-99/lt-tool/releases), затем:

```bash
sudo dpkg -i lt_1.0.0_all.deb
```

После установки будет доступна команда `lt` в любом Laravel-проекте.

---

## 🚀 Быстрый старт

```bash
lt up                         # Запустить контейнеры
lt artisan migrate            # Artisan команда
lt composer install           # Composer команда
lt shell                      # Bash/SH внутри контейнера
lt logs mysql                 # Логи сервиса
lt down                       # Остановить контейнеры
```

---

## ⚙️ Настройка через `.env`

LT ищет `.env` в корне проекта. Поддерживаются следующие переменные:

```env
LT_CONTAINER_NAME=app         # имя контейнера по умолчанию
LT_CONTAINER_SHELL=bash       # шелл внутри контейнера
```

---

## 📚 Полный список команд

```bash
lt up                         # docker compose up -d
lt down                       # docker compose down
lt restart                    # docker compose restart
lt build                      # docker compose build
lt ps                         # docker compose ps
lt logs [service]             # docker compose logs
lt exec [cmd]                 # docker compose exec app [cmd]
lt artisan [cmd]              # php artisan ...
lt composer [cmd]             # composer ...
lt shell                      # bash/sh внутри контейнера
lt help                       # Справка
```

---

## 🛠 Сборка .deb вручную

```bash
git clone https://github.com/USERNAME/lt-tool.git
cd lt-tool
cp bin/lt debian/usr/local/bin/lt
dpkg-deb --build debian lt_1.0.0_all.deb
```

---

## 📄 Лицензия

MIT © 2025. Сделано с ❤️ для Laravel разработчиков.
