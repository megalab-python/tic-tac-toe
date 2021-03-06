# Проект "Крестики нолики"

Пользуяюсь парадигмами ООП, вашей задачей будет написать игру крестики-нолики в двух режимах:
- против второго игрока
- против компьютера

Обязательные требования для Python разработчиков:
- Ваш код должен соблюдать PEP 8 конвенцию
- Используйте [black](https://pypi.org/project/black/) для форматирования кода
- Выбирайте хорошие названия для ваших переменных и функций, которые будут описывать их суть в полной мере. Никаких i, j, k, x, y, z, test, tmp и так далее.

### Поле

Поле выглядит следующим образом:

```
  X | O | X
----+---+----
  X | O | X
----+---+----
  X | O | X
```

### Против игрока

Ход действий против игрока 

1. Второму игроку дается право выбора знака: крестик или нолик.
2. Первым ходит игрок, который выбрал крестик.
3. Далее по очереди игроки занимают ячейки на поле.
4. В ходе игры ваш алгоритм должен проверять наличие победителя.

### Против компьютера

1. Вам дается на выбор знак: крестик или нолик.
2. Первым ходит Х
3. Далее по очереди игрок и компьютер занимают ячейки на поле.
   1. Когда ходит компьютер, он должен выбирать ячейку случайным образом.
4. В ходе игры алгоритм должен определить победителя или объявить ничью

### Определение победителя

1. В случае если игрок занял любую диагональ, он считается победителем. К примеру:

```
  X | O | O
----+---+----
  O | X | 
----+---+----
  O | O | X   <-- Победил X!
```

2. В случае если игрок занял любую горизонталь, он считается победителем. К примеру:

```
  O | O | O   <-- Победил O!
----+---+----
  X | X | O
----+---+----
  O | O | X
```

3. В случае если игрок занял любую вертикаль, он считается победителем. К примеру:

```
  O | X | O   
----+---+----
  O | X | O
----+---+----
  O | O | X
  
  ^
  Победил O!
```

4. Если все ячейки заняты, но ни одно из условий указанных выше не выполнено, значит результатом является - ничья!

Полный пример работы кода [здесь](example.md)
