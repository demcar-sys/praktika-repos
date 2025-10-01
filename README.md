# АИС "Учет текущей успеваемости студентов"

Автоматизированная информационная система для учета успеваемости студентов образовательного учреждения.

## Функциональность

### Для студентов:
- Просмотр оценок и рейтинга
- Мониторинг академического прогресса
- Получение выписок об успеваемости

### Для преподавателей:
- Выставление и редактирование оценок
- Ведение электронного журнала
- Формирование ведомостей
- Анализ успеваемости групп

### Для администраторов:
- Управление пользователями
- Настройка учебного процесса
- Генерация отчетности
- Системное администрирование

## 🛠 Технологический стек

### Backend:
- Python 3.11
- Django 4.2
- Django REST Framework
- PostgreSQL
- Redis

### Frontend:
- Vue.js 3
- Bootstrap 5
- Chart.js
- Vite

### Инфраструктура:
- Docker
- GitHub Actions
- Nginx
- Celery

## Установка и запуск

### Предварительные требования:
- Python 3.11+
- Node.js 18+
- PostgreSQL 13+
- Redis

### Backend установка:
```bash
cd backend
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
