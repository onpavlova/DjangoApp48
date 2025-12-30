📚 Магазин разных товаров - Django Web Application
Веб-приложение Store
Реализуется функционал ДЗ 44, 45, 48, 49.
CRUD через CBV
Тесты
Celery и Redis
Настроен GitHubAction
Настроен pipline GitLab

🚀 Быстрый старт
Предварительные требования
Python 3.13+
SQLite (по умолчанию SQLite)
pip (менеджер пакетов Python)
Установка

Клонирование репозитория
git clone https://github.com/onpavlova/DjangoApp48.git
cd DjangoApp48

Создание виртуального окружения
python -m venv venv
# Для Windows:
venv\Scripts\activate
# Для Linux/Mac:
source venv/bin/activate

Установка зависимостей
pip install -r requirements.txt

Настройка базы данных
python manage.py migrate

Создание суперпользователя
python manage.py createsuperuser

Загрузка тестовых данных (опционально)
python manage.py load_store_data

Запуск сервера разработки
python manage.py runserver

Приложение будет доступно по адресу: http://127.0.0.1:8000

Требуется установленный локально или поднятый контейнер docker с redis

Запуск celery
celery -A config  worker --loglevel=info --pool=solo -E


📝 Админ-панель
Админ-панель доступна по адресу: http://127.0.0.1:8000/admin
Функции админки:
Управление товарами, категориями
Управление пользователями
Bulk actions (массовые операции)

🎨 Фронтенд
Используемые технологии
Шаблоны: Django Templates
Стили: Bootstrap 5 + Custom CSS

Основные страницы
Главная (/store/) - иинформация о продукте
Все товары (/store/products) - список товаров
Добавить товар (/store/products/add/) - добавление товара
Редактировать товар (/store/products/{id}/edit/) - редактирование товара
Детали товаров (/store/products/{id}/) - полная информация о товаре
