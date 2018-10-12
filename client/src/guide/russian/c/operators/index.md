---
title: Operators
localeTitle: операторы
---
# Операторы в C

## 1\. Арифметические операторы

*   `+` Добавляет в операнды (значения) `C int a = 6; int c = a + 1; // c = 7`
*   `-` вычитает второй операнд с первого `C int a = 8; int b = 9; int c = a - b; // c = -1`
*   `*` Умножает два операнда `C int a = 8; int b = 9; int c = a * b; // c = 72`
*   `/` Делит первый операнд на второй `C int a = 8; int b = 4; int c = a / b; // c = 2`
*   `%` Дает остаток после целочисленного деления `C int a = 8; int b = 9; int c = b % a; // c = 1 because b = 1*a + 1 = 8 + 1`
*   `++` Увеличивает значение int на единицу `C int a = 8; a++; // a = 9 int b = a++; // postfix operator; a = 10, b = 9 int c = ++a; // prefix operator; a = 11, c = 11`
*   `--` Уменьшает значение int на единицу `C int a = 8; a--; // a = 7 int b = a--; // postfix operator; a = 6, b = 7 int c = --a; // prefix operator; a = 5, c = 5` // C Программа для демонстрации работы арифметических операторов

# включают

int main () { int a = 9, b = 4, c;
```
c = a+b; 
 printf("a+b = %d \n",c); 
 
 c = ab; 
 printf("ab = %d \n",c); 
 
 c = a*b; 
 printf("a*b = %d \n",c); 
 
 c=a/b; 
 printf("a/b = %d \n",c); 
 
 c=a%b; 
 printf("Remainder when a divided by b = %d \n",c); 
 
 return 0; 
```

}

## 2\. Реляционные операторы

*   `==` Equal - true, когда оба операнда равны `C int a = 5, b = 5; bool c = (a == b); // c = true`
*   `!=` Не равно - true, когда оба операнда НЕ равны `C int a = 5, b = 6; bool c = (a != b); // c = true`
*   `>` Больше - True, когда первый операнд больше второго. `C int a = 8, b = 5; bool c = (a > b); // c = true`
*   `<` Меньше чем - Истина, когда первый операнд меньше, чем второй. `C int a = 5, b = 8; bool c = (a < b); // c = true`
*   `>=` Больше или равно - Истина, когда первый операнд больше или равен второму. `C int a = 8, b = 5; bool c = (a >= b); // c = true bool d = (a >= 8); // d = true`
*   `<=` Меньше или равно - Истина, когда первый операнд меньше или равен второму. `C int a = 5, b = 8; bool c = (a <= b); // c = true`

## 3\. Логические операторы

*   `&&` AND - Истина, когда **оба** операнда верны. `C bool c = (5 < 6) && (8!=7); // both operands true, therefore c = true`
*   `||` OR - True, когда либо первый, либо второй операнды верны (или оба) `C bool c = (5 < 6) || (8 == 7) // first operand is true, therefore c = true`
*   `!` NOT operator - True, если операнд ложный. `C bool c = !(8 == 7) // translate: NOT (false), therefore c = true`

## 4\. Побитовые операторы

*   `&` AND - если в месте есть бит в обоих операндах, то он копируется в результат `C A = 11001 B = 01000 RESULT = 01000`
*   `|` OR - если в месте есть бит в обоих операндах, то он копируется в результат `C A = 11001 B = 01000 RESULT = 11001`
*   `^` Оператор XOR (исключающий ИЛИ) - если в месте есть бит в одном из операндов (не оба), то он копируется в результат `C A = 11001 B = 01000 RESULT = 10001`
*   `~` Отрицательный оператор - Реверсирует бит. 1 -> 0, 0 -> 1 `C C = 01000 RESULT = 10111`
*   `<<` Оператор левого сдвига. Левый операнд перемещается влево на столько битов, как правый операнд `C A = 11001 A << 2 RESULT = 00100`
*   `>>` Оператор правого сдвига. Левый операнд перемещается вправо на столько битов, как правый операнд `C A = 11001 A >> 2 RESULT = 00110`

## 5\. Операторы присваивания

*   `=` `C int a = 7; // 'a' is going to be equal to 7`
*   `+=` `C int a = 7; a += 5; // equivalent to a = a + 5 = 7 + 5 = 12`
*   `-=` `C int a = 7; a -= 2; // equivalent to a = a - 2 = 7 - 2 = 5`
*   `*=` `C int a = 7; a *= 3; // equivalent to a = a * 3 = 7 * 3 = 21`
*   `/=` `C int a = 21; a /= 3; // equivalent to a = a / 3 = 21 / 3 = 7`
*   `%=`  
    `C int a = 21; a %= 5; // equivalent to a = a % 5 = 21 % 5 = 1`

Разное Операторы ↦ размер и тройка Помимо операторов, о которых говорилось выше, есть еще несколько важных операторов, включая sizeof и? : поддерживается языком C.

Пример описания оператора sizeof () Возвращает размер переменной. sizeof (a), где a целое число, вернет 4. & Возвращает адрес переменной. & А; возвращает фактический адрес переменной.

*   Указатель на переменную. \* А; ? : Условное выражение. Если условие верно? то значение X: иначе значение Y

## 6\. Приоритет оператора в C

Операторы с наивысшим приоритетом отображаются в верхней части списка. В выражении оператор с более высоким приоритетом будет оцениваться в первую очередь.

*   Postfix `() [] -> . ++ --`
*   Унары `+ - ! ~ ++ -- (type)* & sizeof`
*   Мультипликативный `* / %`
*   Добавка `+ -`
*   Shift `<< >>`
*   Реляционная `< <= > >=`
*   Равенство `== !=`
*   Побитовое И `&`
*   Побитовое XOR `^`
*   Побитовое ИЛИ `|`
*   Логические AND `&&`
*   Логический ИЛИ `||`
*   Условный `?:`
*   Назначение `= += -= *= /= %= >>= <<= &= ^= |=`
*   Comma `,`