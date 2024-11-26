# mermaid-practice-12
# Информационная система экспертной оценки неисправностей компьютера

## Описание

Это информационная система, предназначенная для диагностики неисправностей компьютеров с использованием искусственного интеллекта. Система обрабатывает заявки пользователей, анализирует неисправности на основе базы знаний и предоставляет рекомендации. Администратор проверяет рекомендации и обновляет базу знаний для улучшения точности диагностики.

## Диаграмма структуры функциональных возможностей (Mind Map)

**Описание:**  
Эта диаграмма отображает основные функциональные возможности системы и их взаимосвязи. Включены компоненты системы, такие как сервисы регистрации жалоб, диагностики ИИ и администрирования, а также описание задач проектирования, используемых технологий и примеров использования.

```mermaid
mindmap
  root((Информационная система экспертной оценки неисправностей))
    Система диагностики
      Регистрация заявки
      Анализ проблемы
      Предоставление решения
      Обновление базы знаний
    Пользователь
      Запрос на диагностику
      Получение рекомендаций
    Администратор
      Проверка рекомендаций
      Обновление базы знаний
    Архитектура
      Микросервисы
      Взаимодействие с системами
      Базы данных
    Используемые технологии
      TensorFlow
      React.js
      PostgreSQL
      Python
      Spring Boot
    Компоненты
      Сервис интерфейса пользователя
      Сервис регистрации жалоб
      Сервис определения устройства
      Сервис диагностики ИИ
      Сервис базы знаний
      Сервис администрирования
    Примеры использования
      Обработка жалобы пользователя
      Анализ неисправности
      Обновление базы знаний
    Задачи проектирования
      Дизайн системы
      Моделирование данных
      Проектирование API
      Оценка производительности
```

## Диаграмма путешествия пользователя (User Journey)

**Описание:**  
Эта диаграмма иллюстрирует путь пользователя от подачи заявки до получения результатов диагностики.

```mermaid
journey
    title Путешествие пользователя в системе диагностики
    section Регистрация заявки
      Пользователь: 5: Подать заявку на диагностику
    section Анализ проблемы
      Система: 4: Анализирует проблему на основе данных
      ИИ: 5: Генерирует рекомендацию
    section Проверка администратором
      Администратор: 3: Проверяет рекомендации ИИ
    section Выдача результата пользователю
      Система: 5: Отправляет результат пользователю
```

## Квадрант-граф функциональных возможностей

**Описание:**  
Этот квадрант-граф показывает функциональные возможности системы с точки зрения их ценности и легкости использования.

```mermaid
quadrantChart
    title Квадрант-граф функциональных возможностей системы
    x-axis Ease of Use --> Complexity of Use
    y-axis Value --> Low Value
    quadrant-1 High value, easy to use
    quadrant-2 Low value, easy to use
    quadrant-3 High value, complex to use
    quadrant-4 Low value, complex to use
    Complaint Registration: [0.9, 0.8]
    Problem Analysis: [0.7, 0.9]
    Providing Solution: [0.8, 0.7]
    Knowledge Base Update: [0.6, 0.5]
    Submit Complaint: [0.5, 0.6]
    Recommendation Review: [0.8, 0.4]
```

## Диаграмма Git-репозитория

**Описание:**  
Эта диаграмма отображает процесс разработки системы с использованием Git и включает создание и слияние веток для разработки микросервисов.

```mermaid
gitGraph
    commit id: "Initial commit - Setup project structure"
    commit id: "Added complaint registration service"
    branch develop
    checkout develop
    commit id: "Implemented problem analysis functionality"
    commit id: "Added device identification service"
    checkout main
    commit id: "Integrated payment service for diagnostics"
    
    checkout develop
    branch feature/microservice-registration
    checkout feature/microservice-registration
    commit id: "Developed complaint registration microservice"
    checkout develop

    branch feature/microservice-analysis
    checkout feature/microservice-analysis
    commit id: "Developed problem analysis microservice"
    checkout develop

    branch feature/microservice-device
    checkout feature/microservice-device
    commit id: "Developed device identification microservice"
    checkout develop

    branch feature/microservice-ai-diagnostics
    checkout feature/microservice-ai-diagnostics
    commit id: "Developed AI diagnostic microservice"
    checkout develop

    branch feature/microservice-knowledge-base
    checkout feature/microservice-knowledge-base
    commit id: "Developed knowledge base microservice"
    checkout develop

    branch feature/microservice-admin
    checkout feature/microservice-admin
    commit id: "Developed admin microservice"
    checkout develop

    checkout main
    commit id: "Integrated all microservices into main"
    checkout develop
    merge feature/microservice-registration id: "Merged registration service"
    merge feature/microservice-analysis id: "Merged analysis service"
    merge feature/microservice-device id: "Merged device identification service"
    merge feature/microservice-ai-diagnostics id: "Merged AI diagnostics service"
    merge feature/microservice-knowledge-base id: "Merged knowledge base service"
    merge feature/microservice-admin id: "Merged admin service"
    commit id: "Final version with all microservices integrated"
    commit id: "Bug fixes and optimizations"
```
