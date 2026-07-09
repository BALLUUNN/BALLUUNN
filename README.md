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

### StartGrowingUp (Auth Service)
**Стек:** `Go`, `gRPC`, `Protocol Buffers`, `PostgreSQL`, `Redis`, `Kafka`, `Prometheus`, `Grafana`, `Docker`, `GitHub Actions`  
**Период:** март 2026 – настоящее время

Проект по разработке **Auth-сервиса** для микросервисной архитектуры: регистрация и аутентификация пользователей, управление сессиями, refresh-token flow, OTP-коды и интеграция с другими сервисами через Kafka.

**Что сделано:**
- разработал основные auth-сценарии: `Register`, `Login`, `Logout`, `RefreshToken`, `ValidateToken`, `GetUserInfo`;
- спроектировал хранение пользователей и refresh-токенов в **PostgreSQL**, добавил миграции;
- внедрил **Redis** для хранения сессий, OTP-кодов и rate limiting;
- подготовил сервис к production-эксплуатации: структурированные логи, конфигурация через `yaml/env`, контейнеризация через **Docker**;
- заложил observability через **Prometheus** и **Grafana**, а также интеграцию с другими сервисами через **Kafka**;
- настроил базовый **CI/CD** через **GitHub Actions**: сборка, проверки и автоматизация деплоя.
  
 **Репозиторий:** `https://github.com/BALLUUNN/ZenlyAuthService`  
