---

__system: {"dislikeVariants":["Нет ответа на мой вопрос","Рекомендации не помогли","Содержание не соответствует заголовку","Другое"]}
---
# Типы чартов

В {{ datalens-full-name }} доступны следующие типы чартов:
 * **Диаграммы**:
   - [Линейная диаграмма](#line-chart)
   - [Диаграмма с областями](#area-chart)
   - [Нормированная диаграмма с областями](#normalized-area-chart)
   - [Столбчатая диаграмма](#bar-chart)
   - [Нормированная столбчатая диаграмма](#normalized-bar-chart)
   - [Линейчатая диаграмма](#horizontal-bar-chart)
   - [Нормированная линейчатая диаграмма](#normalized-horizontal-bar-chart)
   - [Точечная диаграмма](#scatter-chart)
   - [Круговая диаграмма](#pie-chart)
   - [Древовидная диаграмма](#tree-chart)
 * **Таблицы**:
   - [Таблица](#flat-table)
   - [Сводная таблица](#pivot-table)
 * **Географическая карта**:
   - [Карта](#map-chart)
     - [Точечная карта](#point-map-chart)
     - [Фоновая карта](#choropleth-map-chart)
     - [Тепловая карта](#heat-map-chart)
 * **Другое**:  
   - [Индикатор](#indicator)

## Диаграммы {#charts}

### Линейная диаграмма {#line-chart}

Отображает изменение показателей по измерениям в виде одной или нескольких горизонтальных линий.

Секция<br/> в визарде| Описание
----- | ----
X | Измерение. Может быть указано только одно поле
Y | Показатель.  Может быть указано несколько показателей.<br/>При добавлении в секцию более одного показателя в секции **Цвета** появится измерение `Measure Names`
Y2 | Показатель.  Позволяет добавить вторую ось Y на диаграмму. Может быть указано несколько показателей.<br/>При добавлении в секцию более одного показателя в секции **Цвета** появится измерение `Measure Names`
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Измерение или поле `Measure Names`. Влияет на цвет линий. `Measure Names` удаляется путем удаления показателей с оси Y
Сортировка | Измерение. Может использовать только одно измерение с оси Х. Влияет на сортировку оси X
Подписи | Показатель. Отображает значения показателя на диаграмме

### Диаграмма с областями {#area-chart}

Отображает изменение показателей по измерениям в виде областей, показывая вклад каждой линии в значение общей суммы.

Секция<br/> в визарде| Описание
----- | ----
X | Измерение. Может быть указано только одно поле
Y | Показатель. Может быть указано несколько показателей. При добавлении в секцию более одного показателя в секции **Цвета** появится измерение `Measure Names`
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Измерение или поле `Measure Names`. Влияет на цвет линий. `Measure Names` удаляется путем удаления показателей с оси Y
Сортировка | Измерение. Может использовать только одно измерение с оси Х. Влияет на сортировку оси X
Подписи | Показатель. Отображает значения показателя на диаграмме

### Нормированная диаграмма с областями {#normalized-area-chart}

Нормированная диаграмма с областями, которая показывает отношение показателей в процентах.

Секция<br/> в визарде| Описание
----- | ----
X | Измерение. Может быть указано только одно поле
Y | Показатель. Может быть указано несколько показателей. При добавлении в секцию более одного показателя в секции **Цвета** появится измерение `Measure Names`
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Измерение или поле `Measure Names`. Влияет на цвет линий. `Measure Names` удаляется путем удаления показателей с оси Y
Сортировка | Измерение. Может использовать только одно измерение с оси Х. Влияет на сортировку оси X
Подписи | Показатель. Отображает значения показателя на диаграмме

### Столбчатая диаграмма {#bar-chart}

Отображает данные в виде плоских вертикальных столбцов.

Секция<br/> в визарде| Описание
----- | ----
X | Измерения. Может быть указано одно или два измерения
Y | Показатель. Может быть указано несколько показателей. При добавлении в секцию более одного показателя в секции **Цвета** появится измерение `Measure Names`. `Measure Names` можно перенести на ось Х
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Измерение или поле `Measure Names`. Влияет на цвет линий. `Measure Names` удаляется путем удаления показателей с оси Y
Сортировка | Измерение или показатель. Влияет на сортировку столбцов
Подписи | Показатель. Отображает значения показателя на диаграмме

### Нормированная столбчатая диаграмма {#normalized-bar-chart}

Нормированная столбчатая диаграмма, которая показывает отношение показателей в процентах.

Секция<br/> в визарде| Описание
----- | ----
X | Измерения. Может быть указано одно или два измерения
Y | Показатель. Может быть указано несколько показателей. При добавлении в секцию более одного показателя в секции **Цвета** появится измерение `Measure Names`. `Measure Names` можно перенести на ось Х
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Измерение или поле `Measure Names`. Влияет на цвет линий. `Measure Names` удаляется путем удаления показателей с оси Y
Сортировка | Измерение или показатель. Влияет на сортировку столбцов
Подписи | Показатель. Отображает значения показателя на диаграмме

### Линейчатая диаграмма {#horizontal-bar-chart}

Отображает данные в виде плоских горизонтальных столбцов.

Секция<br/> в визарде| Описание
----- | ----
Y | Измерения. Может быть указано одно или два измерения
X | Показатель. Может быть указано несколько показателей. При добавлении в секцию более одного показателя в секции **Цвета** появится измерение `Measure Names`. `Measure Names` можно перенести на ось Y
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Измерение или поле `Measure Names`. Влияет на цвет линий. `Measure Names` удаляется путем удаления показателей с оси X
Сортировка | Измерение или показатель. Влияет на сортировку столбцов
Подписи | Показатель. Отображает значения показателя на диаграмме

### Нормированная линейчатая диаграмма {#normalized-horizontal-bar-chart}

Нормированная линейчатая диаграмма, которая показывает отношение показателей.

Секция<br/> в визарде| Описание
----- | ----
Y | Измерения. Может быть указано одно или два измерения
X | Показатель. Может быть указано несколько показателей. При добавлении в секцию более одного показателя в секции **Цвета** появится измерение `Measure Names`. `Measure Names` можно перенести на ось Y
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Измерение или поле `Measure Names`. Влияет на цвет линий. `Measure Names` удаляется путем удаления показателей с оси X
Сортировка | Измерение или показатель. Влияет на сортировку столбцов
Подписи | Показатель. Отображает значения показателя на диаграмме

### Точечная диаграмма {#scatter-chart}

Отображает точки данных для сравнения пар значений.

Секция<br/> в визарде| Описание
----- | ----
X | Измерение или показатель. Задает значение по оси X
Y | Измерение или показатель. Задает значение по оси Y
Точки | Измерение. Определяет количество точек на диаграмме
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Измерение или показатель. Влияет на цвет точек
Сортировка | Показатель. Влияет на сортировку столбцов

### Круговая диаграмма {#pie-chart}

Отображает размер элементов одного ряда данных относительно суммы элементов в виде круга.

Секция<br/> в визарде| Описание
----- | ----
Цвета | Измерение. Может быть указано только одно поле
Показатели | Показатель. Может быть указано только одно поле
Фильтры | Измерение или показатель. Используется в качестве фильтра
Сортировка | Измерение или показатель из секции **Цвета**. Влияет на сортировку
Подписи | Показатель. Отображает значения показателя на диаграмме

### Древовидная диаграмма {#tree-chart}

Отображается в виде набора прямоугольников. Диаграмма позволяет сравнить пропорции в иерархии.

Диаграмма позволяет сравнить пропорции в иерархии.

Секция<br/> в визарде| Описание
----- | ----
Измерения | Измерения. Определяют дерево иерархии вложенности прямоугольников
Размер | Показатель. Один показатель, который определяет площадь прямоугольника
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Измерение или показатель. Влияет на заливку прямоугольников в диаграмме

## Таблицы {#tables}

### Простая таблица {#flat-table}

Отображает данные в табличном виде, где в первой строке определяются наименования полей, в остальных — их значения.

Секция<br/> в визарде| Описание
----- | ----
Столбцы | Измерения и показатели, которые будут использованы в качестве столбцов. Имя поля используется для заголовка столбца
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Показатель. Влияет на заливку всех ячеек в рамках строки. Может содержать не более одного показателя
Сортировка | Измерения и показатели, которые указаны в секции **Столбцы**.<br/>Вы можете использовать несколько измерений и показателей.<br/>Порядок полей в секции влияет на порядок сортировки полей таблицы

### Сводная таблица {#pivot-table}

Отображает данные в табличном виде, где в строках и столбцах могут быть значения измерений, а в ячейках на их пересечении — показатели.

Секция<br/> в визарде| Описание
----- | ----
Столбцы | Измерения
Строки | Измерения
Показатели | Показатели. При добавлении в секцию более одного показателя в секции **Столбцы** появится измерение `Measure Names`, которое определяет расположение заголовков показателей. `Measure Names` можно переносить в **Строки**
Фильтры | Измерение или показатель. Используется в качестве фильтра
Цвета | Показатель. Влияет на заливку всех ячеек с показателями. Может содержать не более одного показателя
Сортировка | Измерения и показатели, которые указаны в секциях **Столбцы** и **Строки**.<br/>Вы можете использовать несколько измерений и показателей.<br/>Порядок полей в секции влияет на порядок сортировки полей таблицы

## Карта {#map-chart}

Карта поддерживает отображение трех типов визуализации:

* [Точечная карта](#point-map-chart)
* [Фоновая карта](#choropleth-map-chart)
* [Тепловая карта](#heat-map-chart)

На одной карте располагаются не более 5 слоев с любыми типами визуализации. Слои в чарте типа **Карта** называются геослоями.

_Геослои_ — визуализация показателей по точкам или полигонам на карте.

С геослоями можно выполнять следующие операции:

* изменять название;
* устанавливать уровень прозрачности;
* менять порядок внутри типа визуализации, при этом порядок типов визуализации остается неизменным (сверху вниз: точечная карта, фоновая карта, тепловая карта).

Вы можете приобрести предрассчитанные геослои от партнеров в {{ marketplace-name }}.

### Точечная карта {#point-map-chart}

Отображает географические точки на карте.

Секция<br/> в визарде| Описание
----- | ----
Геоточки | Измерение с типом `Геоточка`
Размер | Показатель. Влияет на размер точки
Фильтры слоя | Измерение или показатель. Используется в качестве фильтра текущего слоя
Общие фильтры | Измерение или показатель. Используется в качестве фильтра всего чарта
Цвета | Измерение или показатель. Влияет на интенсивность закрашивания точек
Тултипы | Измерение или показатель. Подсказка, которая отобразится при наведении на точку
Подписи | Показатель. Отображается в виде подписи на точке. При использовании подписи блокируется управление размером точки

### Фоновая карта {#choropleth-map-chart}

Отображает закрашенные области на карте.

Секция<br/> в визарде| Описание
----- | ----
Геополигоны | Измерение с типом `Геополигон`
Фильтры слоя | Измерение или показатель. Используется в качестве фильтра текущего слоя
Общие фильтры | Измерение или показатель. Используется в качестве фильтра всего чарта
Цвета | Измерение или показатель. Влияет на цвет точек

### Тепловая карта {#heat-map-chart}

Отображает географические точки на карте с разной интенсивностью закрашивания.

Секция<br/> в визарде| Описание
----- | ----
Геоточки | Измерение с типом `Геоточка`
Фильтры | Измерение или показатель. Используется в качестве фильтра текущего слоя
Общие фильтры | Измерение или показатель. Используется в качестве фильтра всего чарта
Цвета  | Измерение или показатель. Влияет на интенсивность закрашивания точек

## Другие {#other}

### Индикатор {#indicator}

Отображает данные в виде одного числа.

Секция<br/> в визарде| Описание
----- | ----
Показатель  | Показатель. Один показатель, который определяет значение индикатора
Фильтры | Измерение или показатель. Используется в качестве фильтра

#### См. также {#see-also}
- [{#T}](../../operations/chart/create-line-chart.md)
- [{#T}](../../operations/chart/create-pivot-table.md)
- [{#T}](../../operations/chart/create-table.md)
- [{#T}](../../operations/chart/create-area-chart.md)
- [{#T}](../../operations/chart/create-column-chart.md)
- [{#T}](../../operations/chart/create-bar-chart.md)
- [{#T}](../../operations/chart/create-pie-chart.md)
- [{#T}](../../operations/chart/create-map-chart.md)
- [{#T}](../../operations/chart/publish.md)