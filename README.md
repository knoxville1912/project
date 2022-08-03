## Автоматизированная система анализа данных и передачи данных по жизненным показателям пациентов: (пульс, сатурация, температура, давление и т.д) на основе микросервисной архитектуры ##
Генерирует данные сервис gateway, отправляет их в regular-service с помощью ActiveMQ, откуда данные кладутся в БД и отправляется ежедневный отчет лечащим докторам о состоянии пациентов перед началом рабочего дня  
Если показатели пациентов, лежащих в реанимации требуют немедленного реагирования, то отправляется сообщение по REST в emergency-service, откуда отправляется сообщение в телеграм лечащему доктору  
Подробнее про каждый сервис написано внутри каждого сервиса  
[user-service](https://github.com/knoxville1912/medicine)  
[regular-service](https://github.com/knoxville1912/Regular-service)  
[gateway-service](https://github.com/knoxville1912/gateway-service)  
[emergency-service](https://github.com/knoxville1912/emergency-service)  

## Технологии ##
Библиотека FileWorker, для парсинга файлов, описание библиотеки здесь: [FileWorker](https://github.com/knoxville1912/FileWorker)  
ActiveMQ  
PostgresSQL  
Docker  
Liquibase  
Spring Boot  
Postman
