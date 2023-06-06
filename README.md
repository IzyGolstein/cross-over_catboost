## Алгоритм "Перекрестный CatBoost"

### Описание идеи
Алгоритм "Перекрестный CatBoost" основан на использовании двух признаковых пространств, которые отображают значения одной и той же переменной. Предположим, что эти показатели являются кумулятивными, и для каждой строки данных мы суммируем показатели в каждом признаковом пространстве, получая значения "target".

Основная идея заключается в том, чтобы обучить классификаторы для предсказания "target" в одном признаковом пространстве, используя данные из другого признакового пространства, и затем поменять местами признаковые пространства и повторить процесс обучения.

### Шаги по реализации:
1. Создание двух признаковых пространств, которые отображают значения одной переменной.
2. Для каждой строки данных, суммируем показатели в каждом признаковом пространстве, получая значения "target".
3. Разделение данных на обучающую и тестовую выборки.
4. Обучение классификатора, используя одно признаковое пространство и предсказывая "target" из другого признакового пространства.
5. Повторение шага 4, меняя местами признаковые пространства.
6. Оценка производительности классификатора на тестовой выборке для каждой комбинации признаковых пространств.
7. Анализ результатов и выбор оптимальной комбинации признаковых пространств.

"Перекрестный CatBoost" может быть полезной для исследования взаимосвязи между различными признаковыми пространствами и определения наиболее значимых показателей. Это также может помочь в построении более точных моделей предсказания на основе доступных данных.
