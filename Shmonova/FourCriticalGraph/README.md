Шмонова Наталья 2383, Лустенкова Диана 2383

Критический граф — граф, в котором удаление любой вершины или ребра приводит к уменьшению хроматического числа графа (неориентированный граф, все подграфы которого имеют меньшее хроматическое число).
4-критический граф — это критический граф с хроматическим числом 4, а хроматическим числом графа называют минимальное число цветов,
которыми можно раскрасить вершины графа, чтобы смежные вершины быи разных цветов.

Алгоритм по определению такого графа:
1. Находим изначальное хроматическое число графа.
2. Циклом проходимся по каждой вершине графа и удаляем рёбра выходящие из каждой вершины графа.
3. Проверяем хроматическое число.

Если хроматическое число уменьшается по сравнению с 4 при каждой итерации, то граф является 4-критическим.