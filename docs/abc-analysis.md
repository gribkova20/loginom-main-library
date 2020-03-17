# ABC-анализ

[Назад к списку компонентов](../README.md)

## Назначение

В компоненте реализован метод, который позволяет классифицировать ресурсы по степени их важности на основе принципа Парето. 
Происходит разделение объектов на три группы (A, B, C) согласно границам групп. Границы групп задаются в переменных.

## Входные порты

| Название             | Тип        |
|:---------------------|:-----------|
| Входной набор данных | Таблица    |
| Груницы групп        | Переменные |

### Структура таблицы "Входной набор данных"

| Метка      | Тип                                    | Описание                                                                                         |
|:-----------|:---------------------------------------|:-------------------------------------------------------------------------------------------------|
| Объект     | ![](./img/string.svg) Строковый        | Идентификатор или наименование объекта, по которому проводится анализ. Например, артикул товара  |
| Показатель | ![](./img/realnumber.svg) Вещественный | Значение показателя по объекту. Например, сумма продаж                                           |

### Переменные в порте "Границы групп"

| № | Метка               | Тип                                    | Значение  |
|:--|:--------------------|:---------------------------------------|:----------|
| 1 | Граница группы A, % | ![](./img/realnumber.svg) Вещественный |        80 |
| 2 | Граница группы B, % | ![](./img/realnumber.svg) Вещественный |        95 |

Границы групп устанавливаются пользователем. По умолчанию указаны границы, которые используются чаще всего.

## Выходные порты

| Название                     | Тип     |
|:-----------------------------|:--------|
| ABC-группы и вклады объектов | Таблица |

### Структура таблицы "ABC-группы и вклады объектов"

| Метка                    | Тип                                    | Описание                                 |
|:-------------------------|:---------------------------------------|:-----------------------------------------|
| Объект                   | ![](./img/string.svg) Строковый        | Идентификатор или наименование объекта   |
| Показатель               | ![](./img/realnumber.svg) Вещественный | Значение показателя по объекту           |
| Вклад нарастающим итогом | ![](./img/realnumber.svg) Вещественный | Накопительный вклад объектов             |
| Группа                   | ![](./img/string.svg) Строковый        | Идентификатор группы объекта             |

## Алгоритмы

* [ABC-анализ](https://wiki.loginom.ru/articles/abc-analysis.html)