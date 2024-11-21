### Лабораторная работа №3. Работа с базой данных
## Выполнила: Лепехина А.Д. ИСП-211о

## Описание
Это приложение позволяет работать с базой данных SQLite в Android. Оно реализует функции добавления, обновления и просмотра записей в базе данных об одноклассниках.

## Структура проекта
1. MainActivity - главная активность приложения, содержащая кнопки для работы с базой данных.
2. GroupmatesActivity - активность для отображения всех записей из базы данных.
3. DatabaseHelper - класс для взаимодействия с базой данных SQLite, включающий методы для добавления, обновления и извлечения данных.

## Первоначальная версия приложения
Первое приложение работает с базой данных SQLite, где хранятся записи об одноклассниках. Основные функции включают:
1. Создание и заполнение таблицы `Groupmates` с начальными данными.
2. Добавление новой записи об однокласснике.
3. Обновление данных о последнем добавленном однокласснике.

## Обновленная версия приложения
Второе приложение представляет собой улучшенную версию первой. Оно включает поддержку миграций базы данных, разделяя поле `ФИО` на отдельные поля — фамилию, имя и отчество.

## Структура базы данных
База данных содержит таблицу `Groupmates` с полями:
- **ID** — уникальный идентификатор записи.
- **ФИО** — полное имя одноклассника.
- **Время добавления записи** — автоматически устанавливается при добавлении записи.

## Описание активности
- **Главное активити**: Включает три кнопки:
    - **1** — открывает активити для отображения списка одноклассников.
    - **2** — добавляет новую запись в таблицу.
    - **3** — заменяет ФИО последней добавленной записи на "Иванов Иван Иванович".

## Начальные данные
При первом запуске приложение создаёт базу данных и добавляет пять записей об одноклассниках.

## Миграция базы данных
Во второй версии приложения структура таблицы `Groupmates` была изменена. Теперь она включает отдельные поля для фамилии, имени и отчества:
- **ID** — уникальный идентификатор записи.
- **Фамилия**, **Имя**, **Отчество** — раздельные строки для каждого элемента ФИО.
- **Время добавления записи** — дата и время создания записи.
  

## Обновленный DatabaseHelper
- Класс `DatabaseHelper` обновлён для обработки изменений в структуре базы данных.
- При изменении версии базы данных (переменная `DATABASE_VERSION` обновлена до 2) происходит удаление старой таблицы и создание новой с обновленной структурой.

## Описание активности
Функционал активити во второй версии приложения остался аналогичным первой:
- **Просмотр** — отображает одноклассников в новом формате (с разделением на фамилию, имя и отчество).
  <p align="center">
    <img src="https://github.com/user-attachments/assets/d46a2aba-1273-425e-a8d3-9f70932cd02f" width="250">
    <img src="https://github.com/user-attachments/assets/885fc66a-61f0-4706-a40d-15eb548ef1ca" width="250">
</p> 

- **Добавить** — добавляет новую запись.
<p align="center">
    <img src="https://github.com/user-attachments/assets/e8a7cca4-e750-4bc8-ab50-23238512fa55" width="250">
    <img src="https://github.com/user-attachments/assets/7e20833f-2a2b-4951-b2e3-6fb58419617f" width="250">
    <img src="https://github.com/user-attachments/assets/d8df91be-fad6-48d7-975e-0657967c1a96" width="250">
</p> 

- **Обновить** — изменяет данные последней добавленной записи на "Иванов Иван Иванович".
<p align="center">
     <img src="https://github.com/user-attachments/assets/f2c585a3-246c-41dd-abc9-aa5478069c5d" width="250">
</p> 

## Установка и запуск
1. Скачать ZIP проекта.
2. Распаковать загруженный архив.
3. Склонируйте или загрузите проект в вашу интегрированную среду. В нашем случае это Android Studio.
4. Откройте проект:
 - Нажимаем на "Open" на начальном экране в верхней панели.
 - Выбрать распакованный архив.
 - Дождаться завершения всех процессов внутри проекта.
6. Подключите физическое устройство с помощью кабеля/Wi-Fi подключения или эмулятор для запуска приложения.
7. Нажмите Run, чтобы запустить приложение.

## Что было использовано:
- Язык программирования: Java
- Среда разработки: Android Studio
- Операционная система: Android
- База данных: SQLite

   
