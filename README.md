# Test Task

## __Описание__:
У некой компании reactive logistics, которая занимается автоматизацией доставок, имеется задача - разбить набор локаций на кластеры. Кластеры должны иметь примерно равный размер, так же количество кластеров не должно превышать __K__.

## __Входные данные__:
__N__ - количестко локаций (__N <= 5000__)

__locations__ - массив локаций.

__matrix__ - матрица дистанций, размером __NxN__. __matrix[i][j]__ - минимальная дистанция от __locations[i]__ до __locations[j]__ по дорогам. Дистанция дана в метрах.

__K__ - макс. количества кластеров (__K <= 100__).

## __Советы и пожелания__:
- Использовать сумму попарных дистанций для оценки "размера" кластера."размеры" будут оценивать равномерность кластеризаций
- Использовать silhouette score
- Приветствуется использование других метрик
- Время работы решения меньше 5 минут
- Объяснение выбора метрик и алгоритмов решения
- Сделать отображение локаций на карте, для python можно использовать folium

## __Тесты__:
Тесты находятся в директории ___/test___

Каждый тест это json обект собержаший аргкменты matrix, points и K.

Пример теста:
~~~
{
    "points": [
        {
            "lat": 43.236054,
            "lng": 76.958991
        },
        {
            "lat": 43.238116,
            "lng": 76.924232
        },
        {
            "lat": 43.219580,
            "lng": 76.854531
        }
    ],
    "matrix": [
        [0, 10, 12], 
        [13, 0, 33],
        [12, 11, 0]
    ],
    "K": 2
}
~~~
_Тесты являются обезличенными данными из продакшена_