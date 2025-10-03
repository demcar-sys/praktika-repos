# 🎓 АИС "Учет успеваемости студентов"

Автоматизированная информационная система для учета успеваемости студентов, разработанная в рамках учебной практики.

## 📋 О проекте

Система предназначена для автоматизации процессов учета и контроля успеваемости студентов в образовательных учреждениях. Реализована на Django с использованием SQLite базы данных.

### 🎯 Основной функционал

- **👥 Ролевая модель доступа** (Студент/Преподаватель/Администратор)
- **📊 Учет оценок** и посещаемости
- **📈 Статистика успеваемости**
- **👨‍🏫 Электронный журнал** для преподавателей
- **📱 Адаптивный интерфейс** на Bootstrap 5

## 🚀 Быстрый старт

### Предварительные требования

- Python 3.8+
- Django 4.2+
- SQLite3

### Установка и запуск

1. **Клонируйте репозиторий**
```bash
git clone https://github.com/your-username/student-performance-system.git
cd student-performance-system
```

2. **Установите зависимости**
```bash
pip install -r requirements.txt
```

3. **Настройте базу данных**
```bash
python manage.py makemigrations
python manage.py migrate
```

4. **Создайте суперпользователя**
```bash
python manage.py createsuperuser
```

5. **Запустите сервер**
```bash
python manage.py runserver
```

6. **Откройте в браузере**
```
http://localhost:8000
```

## 👤 Роли пользователей

### 🎓 Студент
- Просмотр своих оценок
- Мониторинг среднего балла
- Просмотр расписания

### 👨‍🏫 Преподаватель  
- Ведение электронного журнала
- Выставление оценок
- Просмотр статистики по группам

### 🔧 Администратор
- Управление пользователями
- Настройка учебного процесса
- Генерация отчетов

## 🏗️ Архитектура проекта

```
student_performance/
├── core/                 # Настройки Django
├── journal/              # Основное приложение
│   ├── models.py        # Модели данных
│   ├── views.py         # Представления
│   ├── admin.py         # Админ-панель
│   └── services.py      # Бизнес-логика
├── templates/           # HTML шаблоны
└── static/             # Статические файлы
```

## 🛠️ Технологический стек

- **Backend**: Django 4.2.7
- **Database**: SQLite3
- **Frontend**: HTML5, CSS3, Bootstrap 5
- **Authentication**: Django Auth System
- **Configuration**: python-decouple

## 📊 Модели данных

### Основные сущности:
- **User** - Пользователи системы
- **Student** - Студенты
- **Teacher** - Преподаватели  
- **Grade** - Оценки
- **Discipline** - Учебные дисциплины

## 🔧 Разработка

### Создание миграций
```bash
python manage.py makemigrations journal
```

### Применение миграций
```bash
python manage.py migrate
```

### Запуск тестов
```bash
python manage.py test
```

### Создание фикстур
```bash
python manage.py dumpdata journal --indent=2 > fixtures/journal_data.json
```

## 📝 API endpoints

- `GET /` - Главная страница
- `GET /admin/` - Админ-панель
- `GET /login/` - Страница входа
- `GET /journal/grades/` - Журнал оценок

## 🐛 Отладка

Для отладки используйте:
```python
# В settings.py
DEBUG = True

# В коде
import logging
logger = logging.getLogger(__name__)
logger.debug('Отладочная информация')
```

## 📈 Производительность

- Время отклика: < 200мс
- Поддержка 50+ одновременных пользователей
- Оптимизированные SQL-запросы

## 🤝 Вклад в проект

1. Форкните репозиторий
2. Создайте ветку для функции (`git checkout -b feature/AmazingFeature`)
3. Закоммитьте изменения (`git commit -m 'Add AmazingFeature'`)
4. Запушьте ветку (`git push origin feature/AmazingFeature`)
5. Откройте Pull Request

---

⭐ Не забудьте поставить звезду, если проект был полезен!
