# Построение модели для рекомендации подходящих тарифов мобильной связи

## Статус проекта: 
завершен

## Ключевые слова проекта: 
- классификация
- fbeta-мера 
- подбор гиперпараметров
- классические методы ML

## Вводные данные проекта:

**Заказчик:** оператор мобильной связи «Мегалайн».

Они хотят построить систему, способную проанализировать поведение клиентов и предложить пользователям новый тариф: «Смарт» или «Ультра».

**Целью проекта** является построение качественной модели для получения максимального дохода для компании с значением accuracy не ниже 0.75.

**Данные для анализа и построения модели:** данные о поведении клиентов, которые уже перешли на эти тарифы (из проекта курса «Статистический анализ данных»).

**Дополнительные условия заказчика:** предварительная предобработка не требуется, она уже выполнена.

**Этапы проекта:**
- Изучить общую информацию об имеющихся данных
- Разделить данные на три выборки: обучающую, валидационную и тестовую
- Исследовать различные модели посредством изменения гиперпараметров, выбрать наиболее качественную модель
- Проверить качество полученной модели на тестовой выборке
- Проверить модель на адекватность


## Используемые библиотеки:
- pandas
- numpy
- seaborn
- matplotlib
- sklearn

## Выводы по проекту

Полученная модель дерева решений достигла целевой метрики Accuracy более 0.75:
- accuracy модели "дерево решений" на тестовой выборке: 0.77
- fbeta модели "дерево решений" на тестовой выборке: 0.62

Accuracy модели dummy_model на тестовой выборке составляет 0.68 (ниже 0.75), кроме того модель она не выявила ни одного объекта с классом 1.
Таким образом, можно считать, что полученная модель дерева решений прошла проверку на адекватность.
