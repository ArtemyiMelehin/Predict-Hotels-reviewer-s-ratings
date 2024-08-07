# Predict-Hotels-reviewer-s-ratings
Full ML project to predict reviewer's ratings

# <center> Очистка данных на Python </center>
## Оглавление
1. [Описание проекта](#Описание-проекта)
2. [Описание данных](#Описание-данных)
3. [Зависимости](#Зависимости)
4. [Установка проекта](#Установка-проекта)
5. [Использование проекта](#Использование-проекта)
6. [Авторы](#Авторы)
7. [Выводы](Использование-проекта)

## Описание проекта
![image](https://i.pinimg.com/originals/d0/b4/98/d0b4983d1d8472cbbc5701ac39e5c5cd.jpg)

Представьте, что вы работаете датасаентистом в компании Booking. Одна из проблем компании — это нечестные отели, которые накручивают себе рейтинг. Одним из способов нахождения таких отелей является построение модели, которая предсказывает рейтинг отеля. Если предсказания модели сильно отличаются от фактического результата, то, возможно, отель играет нечестно, и его стоит проверить. Вам поставлена задача создать такую модель.

## <center> Основные этапы проекта:
1) Постановка задачи и импорт библиотек: 
    * описание всех признаков
    * импорт необходимых библиотек и данных
    * Разбиение данных на train и test части в отношении 3 к 1.

2) Подготовка нужных функций:
   * функция для построения гипотез.
   * функция для построения графиков.
   * функция для уменьшения кол-ва категорий в признаке.
   * функция очистки признака tags.
   * функция для OHE-кодировки.

3) Импорт данных с Kaggle: 
    * Добавление столбцов sample для train/test data

4) Работа с пропусками + EDA-анализ:
    * Заполнение lat/lng с помощью Google Maps.
    * Выделение страны из признака hotel_address.
    * Выделение дня недели и месяца из признака review_date.
    * Выделение национальности интервьюера.
    * Разбор тегов.
    * Анализ эмоционального окраса текста (negative/positive_review).
    * Нормализация числовых признаков.
    * Перекодировка категориальных признаков OHE-методом.
    * Проверка на мультиколлениарность с помощью визуализации.
    * Удаление менее важных признаков.

5) Моделирование
    * Убираем признак sample.
    * Ограничиваем тренировочную выборку для валидации.
    * Импорт необходимых библиотек ([RandomForestRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html))
    * Осуществление предсказания и получение MAPE.
    * submission в Kaggle.
    
**Данный проект** направлен на демонстрацию применения различных методов в Разведывательном-анализе для подготовки данных и построения базовой модели.

**О структуре проекта:**
* [data](./data) - папка с исходными табличными данными
* [images](./images) - папка с изображениями, необходимыми для проекта
* [Проект предсказания оценок на отели](<Проект предсказания оценок на отели .ipynb>) - jupyter-ноутбук, содержащий основной код проекта, в котором демонстрируются методы и подходы решения поставленной задачи.


## Описание данных
### <center> Dataset Description
### Файлы для соревнования
* hotels_train.csv - набор данных для обучения
* hotels_test.csv - набор данных для оценки качества
* submission.csv - файл сабмишна в нужном формате

## Признаки
* hotel_address - адрес отеля
* review_date - дата, когда рецензент разместил соответствующий отзыв.
* average_score - средний балл отеля, рассчитанный на основе последнего комментария за последний год
* hotel_name - название отеля
* reviewer_nationality - национальность рецензента
* negative_review - отрицательный отзыв, который рецензент дал отелю.
* review_total_negative_word_counts - общее количество слов в отрицательном отзыв
* positive_review - положительный отзыв, который рецензент дал отелю
* review_total_positive_word_counts - общее количество слов в положительном отзыве
* reviewer_score - оценка, которую рецензент поставил отелю на основе своего опыта
* total_number_of_reviews_reviewer_has_given - количество отзывов, которые рецензенты дали в прошлом
* total_number_of_reviews - общее количество действительных отзывов об отеле
* tags - теги, которые рецензент дал отелю.
* days_since_review - продолжительность между датой проверки и датой очистки
* additional_number_of_scoring - есть также некоторые гости, которые просто поставили оценку сервису, а не оставили отзыв. Это число указывает, сколько там действительных оценок без проверки.
* lat - широта отеля
* lng - долгота отеля

## Используемые библиотеки: 
```    
    requirements.txt
```
## Установка проекта

```
git clone https://github.com/ArtemyiMelehin/Predict-Hotels-reviewer-s-ratings
```

## Использование
Вся информация о работе представлена в jupyter-ноутбуке.

## Авторы

* [Мелехин Артемий](https://vk.com/rationality1379)

## Выводы

В данном проекте была проделанна большая работа по Разведывательному анализу данных, были испоьзованны различные библиотеки для представления данных в науилучшем свете для модели. Благодараря проделанной работе мы выяснили определенную последовательность действий, необходимых для успешного результата предсказывающей модели машинного обучения.
