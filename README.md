# Привет, я Александр 👋

QA-инженер, расту в автоматизацию тестирования на Python. Учусь быстро, довожу дело до конца, пишу тесты так, чтобы их можно было читать как документацию.

## Что умею

- **Python**: функции, ООП, работа со строками и структурами данных
- **Автотесты**: pytest, parametrize, TestClient (FastAPI), Allure, техники тест-дизайна (классы эквивалентности, граничные значения)
- **API-тестирование**: FastAPI, REST, Pydantic-валидация, HTTP-статусы
- **БД**: SQLite, FOREIGN KEY, CHECK-ограничения, JOIN/агрегация, db-level тесты
- **Ручное тестирование**: тест-кейсы, чек-листы, баг-репорты
- **CI/CD**: GitHub Actions, workflow, артефакты
- **Инструменты**: Git, Linux (базово), Postman, PyCharm

## Что осваиваю сейчас

- JWT-авторизация в FastAPI
- Playwright для E2E-тестов
- Telegram-боты (aiogram / python-telegram-bot)
- n8n и интеграции по API
- Whisper / LLM в QA-задачах

## Проекты

- [**family_budget**](https://github.com/AlexanderFrl/family_budget) — REST API семейного бюджета. FastAPI + SQLite + 20 зелёных тестов (unit/API/DB) + CI на GitHub Actions + Allure-отчёты. Архитектура: database.py (схема + FK/CHECK), models.py (бизнес-логика баланса), server.py (роуты), tests/ (пирамида тестов).
- [**qa-portfolio**](https://github.com/AlexanderFrl/qa-portfolio) — учебные кейсы и чек-листы.
- [**forest_traveler**](https://github.com/AlexanderFrl/forest_traveler) — unit-тесты игровой логики (parametrize, mock, fixtures).

## family_budget — подробнее

![CI Status](https://github.com/AlexanderFrl/family_budget/actions/workflows/ci.yaml/badge.svg)

### Стек
- Python 3.13, FastAPI, SQLite, Pydantic v2
- Pytest + TestClient + Allure
- GitHub Actions (pytest на push/PR)

### API Endpoints
| Метод | Путь | Описание |
|-------|------|----------|
| POST | `/transactions` | Добавить трату |
| GET | `/balance` | Баланс между пользователями |
| GET | `/budget/{month}` | Остаток по лимиту |
| GET | `/report/{month}` | Отчёт по категориям (JOIN + GROUP BY) |
| POST/GET/DELETE | `/categories` | Управление категориями |

### Как запустить
```bash
git clone https://github.com/AlexanderFrl/family_budget.git
cd family_budget
python3 -m venv family && source family/bin/activate
pip install -r requirements.txt
python server.py
# Swagger UI: http://localhost:8000/docs
