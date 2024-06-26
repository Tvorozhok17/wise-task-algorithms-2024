Шмонова Наталья 2383, Лустенкова Диана 2383
# Задача: Определить равно ли хроматическое число графа 6

Определение:
Хроматическое число графа G - наименьшее натуральное число, для которого существует
правильная раскраска вершин графа G в такое количество цветов.
Правильная раскраска графа — это процесс присвоения цветов вершинам
графа таким образом, что любые две смежные вершины имеют разные цвета.

Реализация алгоритма:
Для реализации используется алгоритм последовательной раскраски:
1. Сортировка вершин графа в порядке невозрастания степеней.
2. Окрашиваем первую вершину списка в цвет 1 и удаляем её из списка.
3. Пока все вершины не окрашены:
- Окрашиваем в цвет p все вершины списка (в порядке невозрастания степеней доступных элементов), которые не смежны с вершинами, уже окрашенными в данный цвет
- Удаляем данные вершины из списка
- Увеличиваем p
- Если p < 6, причем все вершины окрашены, возвращаем false; Если p > 6 и не все вершины окрашены, заканчиваем цикл и возвращаем false
- Иначе возвращаем true