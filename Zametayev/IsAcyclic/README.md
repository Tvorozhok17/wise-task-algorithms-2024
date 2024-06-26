# Ациклический граф

## Определение

**Ациклический граф** – граф, не содержащий циклов.

**Цикл** – последовательность вершин, начинающаяся и завершающаяся в той же самой вершине, и в этой последовательности для любых двух последовательных вершин существует дуга из более ранней в более позднюю.

## Алгоритм

### Основная идея

Для проверки ацикличности графа можно использовать алгоритм поиска в глубину (_DFS_). Идея заключается в том, чтобы отслеживать вершины, которые находятся в текущем стеке вызовов (рекурсивных вызовов). Если мы встречаем вершину, которая уже находится в текущем стеке вызовов, это означает наличие цикла.

### Шаги алгоритма

**1. Инициализация:**
- Создаём массив _visited_, чтобы отслеживать посещенные вершины;
- Создаем массив _recStack_, чтобы отслеживать вершины в текущем стеке вызовов.

**2. Запуск _DFS_:**
- Для каждой вершины, если она еще не была посещена, запускаем _DFS_;
- В процессе _DFS_, помечаем вершину как посещенную и добавляем ее в _recStack_.

**3. Проверка на цикл:**
- Для каждой соседней вершины, если она еще не была посещена, рекурсивно запускаем _DFS_;
- Если соседняя вершина уже находится в _recStack_, значит, найден цикл.

**4. Завершение _DFS_:**
- Убираем вершину из _recStack_ перед возвратом из функции.
