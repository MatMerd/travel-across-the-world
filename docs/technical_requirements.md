# 1. Цель проекта

Цель проекта - разработать систему планирования (далее Система) путешествий для любого человека. Человек должен иметь возможность создавать свои маршруты для путешествий, просматривать маршруты от других пользователей и подписываться на интересных путешественников.

# 2. Описание системы

Система состоит из следующих функциональных блоков:

1. Регистрация, авторизация и аутентификация пользователей в системе
2. Функционал для пользователя
3. Оповещение о новых маршрутах от подписок (В телеграм)
4. Оповещение о новых маршрутах от подписок (На почту)


## 2.1 Типы пользователей

Любой человек может войти в систему и стать её анонимным пользователем. Для него будет доступен просмотр контента, котрый создают другие пользователи. Другие функции сервиса анонимным пользователем не доступны. Авторизованный пользователь может создавать контент,
редактировать его, просматривать контент других пользователей и взаимодействовать с ним.

## 2.2 Регистрация

Система задумана как SaaS, поэтому у любого пользователя должна быть возможность зарегестрироваться в системе и пользоваться её возможностями. Регистрация будет происходить с помощью:
- email (обязательное поле)
- password (обязательное поле)

Так же нужно продумать возможность зарегестрироваться через сторонние сервисы, типа Google, Yandex и т.д

После регистрации, пользователю нужно дать возможность настроить свой личный кабинет, а именно:
- предпочтения по виду отдыха (активный/умеренный/лежачий)
- предпочтения по странам для отдыха
- его нынешнее местоположение
- другое..

На основе этих предпочтений пользователю будут рекомендоваться маршруты и путешественники. (Рекомендации это не мвп, можно перенести в другой файл)

## 2.3 Авторизация и Аутентификация пользователей

Аутентификация пользователей будет осуществляться с помощью access и refresh jwt, если они существуют у пользователя в локальном хранилище. Если их нет, 
пользователь вводит пароль. Так же нужно добавить возможность двухфакторной аутентификации через почту.

## 2.4 Функционал для пользователя

После авторизации пользователь получает доступ ко всем возможностям Системы. Этот функционал состоит из следующих блоков:

1. Редактирование данных профиля
2. Создание и редактирование новых туристических маршрутов
3. Планирование путешествий на каждый день поездки
4. Подписка на людей, маршруты которых понравились
5. Возможность добавлять медиа и описания к точкам маршрута

## 2.5 Оповещение пользователя о новом маршруте от подписок

Так как человек может подписываться на других пользователей, то он может получать оповещения о новых маршрутах. Удобнее всего разработать телеграм бота, чтобы не спамить почту человека. Поэтому при создании нового маршрута, если это совпадает с интересами человека, ему приходит оповещение от бота.

# 3. Архитектура и моделирование системы
...

