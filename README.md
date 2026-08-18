<div align="center">
  <h1>Привет, я Вова</h1>
  <p>
    <b>Backend-разработчик на Go</b> · Студент 3 курса СПбГУ<br>
    Специализация: <b>«Большие данные и распределённые цифровые платформы»</b>
  </p>
  <p>
    <a href="https://t.me/vovoqwe"><img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"></a>
    <a href="https://spb.hh.ru/profile/me?hhtmFrom=ProfileActivator"><img src="https://img.shields.io/badge/hh.ru-FF6600?style=for-the-badge&logoColor=white" alt="hh.ru"></a>
    <a href="mailto:boldakovvova06@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  </p>
</div>


## Ключевой стек

![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?style=for-the-badge&logo=clickhouse&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![REST API](https://img.shields.io/badge/REST_API-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-4285F4?style=for-the-badge&logo=google&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apache-kafka&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)

## Проекты

### Авито "Коробыш"
**Стек:** `Go`, `PostgreSQL`, `WebSocket`, `REST API`, `Docker`, `CI`  
**Период:** август 2026

Разрабатывал в команде геймификацию для Авито. Реализовал компоненты, отвечающее за валюту, прогресс питомца, награды, магазин и задания.

**Основные направления работы:**
- Построил экономическую модель: начисление и списание игровой валюты, автоматическое повышение уровней питомца по заданной шкале, ведение журнала транзакций.
- Реализовал систему наград за уровни с ограничением по времени получения, а также механику сундуков со случайными призами за фиксированную плату — все операции выполняются атомарно в транзакциях БД.
- Создал магазин аренды предметов с разными бонусами и сроками действия, с возможностью продления и замены активного предмета.
- Разработал ежедневные персональные задания, прогресс которых обновляется через подтверждённые действия пользователя, и добавил возможность получать награду за каждое выполненное задание.
- Настроил WebSocket-каналы для мгновенной рассылки клиентам обновлений баланса, уровня и состояния заданий, обеспечив интерактивность.
- Написал REST API для параллельной разработки с фронтендом. Заложил защиту от повторных начислений и состояние гонки на уровне БД и транзакций.
- Организовал Docker-сборку и базовый CI для автоматической проверки кода.

**Репозиторий:** `https://github.com/BALLUUNN/avito-hackathon`

### FilmBuddy
**Стек:** `Go`, `Chi`, `PostgreSQL`, `Docker`, `Nginx`, `HTML/CSS`  
**Период:** сентябрь 2025 – декабрь 2025

Учебный командный проект, в котором я занимался backend-разработкой и выполнял роль **тимлида**.

**Что сделано:**
- разработал два микросервиса: сервис авторизации/регистрации/профиля и сервис оценок/логики друзей;
- настроил API Gateway на Nginx для маршрутизации, балансировки и базовой защиты;
- координировал команду, распределял задачи и проводил код-ревью;
- помог организовать развёртывание и связал фронтенд с бэкендом.

**Репозиторий:** `https://github.com/BALLUUNN/zavozwww/tree/main/zavozwww`

### StartGrowingUp (Auth Contracts)
**Стек:** `Protocol Buffers (proto3)`, `gRPC`, `Buf`, `Makefile`, `GitHub Actions`, `BSR`  
**Период:** декабрь 2025 – настоящее время

Проект по созданию **единого репозитория контрактов** (contract-first подход) для микросервисной архитектуры StartGrowingUp. На данный момент реализованы контракты для **Auth-сервиса**, в планах – добавление других сервисов (Users, Notifications, Analytics).

**Что сделано:**
- разработал **6 gRPC-методов** для Auth-сервиса: `Register`, `Login`, `Logout`, `RefreshToken`, `ValidateToken`, `GetUserInfo`;
- описал **10+ proto-сообщений** для запросов/ответов и общих типов (Timestamp, Pagination, ErrorDetails);
- настроил **Buf** для линтинга и управления зависимостями – обеспечил совместимость версий и автоматическую генерацию кода;
- настроил публикацию контрактов в **BSR (Buf Schema Registry)** – теперь клиенты могут подтягивать актуальные определения через `go get`;
- написал **Makefile** с командами: `gen` (генерация кода), `lint` (проверка стиля), `breaking` (проверка обратной совместимости), `publish` (публикация в BSR);
- настроил **CI/CD через GitHub Actions**: автоматическая проверка при каждом push и pull request (линтинг, проверка на breaking changes, генерация документации);
- добавил **CHANGELOG.md** и **CONTRIBUTING.md** – поддерживаю документацию для команды;

 **Репозиторий:** `https://github.com/BALLUUNN/startgrowingup-contracts`  
 **BSR-публикация:** `https://buf.build/balluunns/repositories`  

