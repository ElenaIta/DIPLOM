# Дипломный проект профессии «Тестировщик»
## Описание проекта

Дипломный проект представляет собой автоматизацию тестирования комплексного сервиса, взаимодействующего с СУБД и API Банка.
<img width="705" alt="service" src="https://user-images.githubusercontent.com/95982934/177042992-b3da8104-ff5d-40b5-aad9-d26e4da97964.png">

Приложение представляет собой веб-сервис, который предоставляет возможность купить тур по определённой цене с помощью двух способов:
- оплата по дебетовой карте
- выдача кредита по данным банковской карты


## ДОКУМЕНТАЦИЯ
[1. План автоматизации](https://github.com/ElenaIta/DIPLOM/blob/master/Plan.md)



## Запуск

### Предварительная подготовка к тестированию:

**1. Установить IntelliJ Idea.** 

Скачать и ознакомиться с документацией можно на официальном сайте https://www.jetbrains.com/ru-ru/idea/.


**2. Установить Docker Desktop.** 

Скачать и ознакомиться с документацией можно на официальном сайте https://www.docker.com/get-started.


**3. Запустить контейнеры docker:**
Для работы с базой данных mysql выполнить команду:
docker-compose -f docker-compose-mysql.yml up -d После прогона тестов остановить контейнеры:
docker-compose -f docker-compose-mysql.yml down


**4. Для работы с базой данных postgres выполнить команду:**

docker-compose -f docker-compose-postgres.yml up -d После прогона тестов остановить контейнеры:
docker-compose -f docker-compose-postgres.yml down


**5. Запустить приложение:**

Для запуска приложения с базой данных mysql выполнить команду:
java -Dspring.datasource.url=jdbc:mysql://localhost:3306/app -jar aqa-shop.jar

Для запуска приложения с базой данных postgres выполнить команду:
java -Dspring.datasource.url=jdbc:postgresql://localhost:5432/app -jar aqa-shop.jar



**6. Запустить тесты:**

Для запуска тестов с базой данных mysql выполнить команду:
gradlew test -Ddb.url=jdbc:mysql://localhost:3306/app

Для запуска тестов с базой данных postgres выполнить команду:
gradlew test -Ddb.url=jdbc:postgresql://localhost:5432/app


**7. Сформировать отчеты командой:**

gradlew allureReport


**8. Открыть отчеты в браузере командой:**

gradlew allureServe
