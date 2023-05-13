
An **operator** is a symbol used to perform certain operations on given data and provide a result.

-   An expression is a collection of variables connected with an operator.
-   Python has 7 operators, including arithmetic, assignment, relational, logical, bitwise, membership, and identity operators.
-   Python does not support unary or ternary operators like other programming languages.
-   Python has shorthand operators and its own ternary operator called the if...else operator.

## **Arithmetic Operators**

<aside> 😎 Arithmetic operators are used to perform mathematical operations on numbers. The arithmetic operators in Python include addition (+), subtraction (-), multiplication (*), division (/), modulus (%), exponentiation (**), and floor division (//).

</aside>

```python
# Addition operator
x = 2 + 3
print(x) # Output: 5

# Subtraction operator
y = 5 - 2
print(y) # Output: 3

# Multiplication operator
z = 4 * 2
print(z) # Output: 8

# Division operator
a = 10 / 2
print(a) # Output: 5.0

# Modulus operator
b = 7 % 3
print(b) # Output: 1

# Exponentiation operator
c = 2 ** 3
print(c) # Output: 8

# Floor division operator
d = 7 // 3
print(d) # Output: 2
```


## **Assignment Operator**

<aside> 😎 Assignment operator is used to assign a value to a variable. The assignment operator in Python is **`=`**

</aside>

```python
# Assignment operator
x = 5
print(x) # Output: 5
```

## **Relational Operators**

>[!Intro] 😎 Relational operators are used to compare two values. The relational operators in Python include greater than (>), less than (<), equal to `==`), not equal to (!=), greater than or equal to (>=), and less than or equal to

```python
# Greater than operator
x = 5 > 3
print(x) # Output: True

# Less than operator
y = 5 < 3
print(y) # Output: False

# Equal to operator
z = 5 == 5
print(z) # Output: True

# Not equal to operator
a = 5 != 3
print(a) # Output: True

# Greater than or equal to operator
b = 5 >= 5
print(b) # Output: True

# Less than or equal to operator
c = 3 <= 5
print(c) # Output: True
```

## **Logical Operators**

<aside> 😎 Logical operators are used to combine multiple conditions and return a boolean value. The logical operators in Python include and, or, and not.

</aside>

1.  **AND (`and`) Operator:**

The AND operator returns **`True`** if both operands are **`True`**, otherwise it returns **`False`**. In Python, any non-zero value is considered **`True`** and any zero value is considered **`False`**.

1.  **OR (`or`) Operator:**

The OR operator returns **`True`** if either of the operands is **`True`**, otherwise it returns **`False`**. In Python, any non-zero value is considered **`True`** and any zero value is considered **`False`**.

1.  **NOT (`not`) Operator:**

The NOT operator returns **`True`** if the operand is **`False`**, otherwise it returns **`False`**.

```python
# And operator
x = 5 > 3 and 3 > 1
print(x) # Output: True

# Or operator
y = 5 < 3 or 3 > 1
print(y) # Output: True

# Not operator
z = not(5 > 3)
print(z) # Output: False
```

### **Bitwise Operators**

<aside> 😎 Bitwise operators are used to perform bitwise operations on numbers. The bitwise operators in Python include AND (&), OR (|), XOR (^), NOT (~), left shift (<<), and right shift (>>).

</aside>

1.  **AND (&) Operator:** The AND operator returns a 1 in each bit position where both operands have a 1, and a 0 otherwise.
2.  **OR (|) Operator:** The OR operator returns a 1 in each bit position where either of the operands have a 1, and a 0 otherwise.
3.  **XOR (^) Operator:** The XOR operator returns a 1 in each bit position where the corresponding bits of either but not both operands are 1s.
4.  **NOT (~) Operator:** The NOT operator returns the one's complement of the operand i.e. it changes each 1 to 0 and each 0 to 1.
5.  **Left shift (<<) Operator:** The left shift operator shifts the bits of the left operand to the left by the number of positions specified in the right operand. The leftmost bits are lost and zeroes are added to the right end. The left shift operator is often used in computer programming to perform multiplication by powers of two.
6.  **Right shift (>>) Operator:** The right shift operator shifts the bits of the left operand to the right by the number of positions specified in the right operand. The rightmost bits are lost and zeroes are added to the left end. The right shift operator is mainly used for integer division by powers of two.

```python
# AND operator
x = 5 & 3
print(x) # Output: 1

# OR operator
y = 5 | 3
print(y) # Output: 7

# XOR operator
z = 5 ^ 3
print(z) # Output: 6

# NOT operator
a = ~5
print(a) # Output: -6

# Left shift operator
b = 5 << 1
print(b) # Output: 10 => which is (5 * 2^1)

# Right shift operator
c = 5 >> 1
print(c) # Output: 2 => which is( 5 / 2^1) (2.5) but c is integer
```

## **Membership Operators**

<aside> 😎 Membership operators are used to test whether a value is a member of a sequence or not. The membership operators in Python include in and not in.

</aside>

```python
# In operator
x = 'e' in 'hello'
print(x) # Output: True

# Not in operator
y = 'z' not in 'hello'
print(y) # Output: True
```

## **Identity Operators**

<aside> 😎 Identity operators are used to compare the memory addresses of two objects. The identity operators in Python include is and is not.

</aside>

```python
# Is operator
x = 5
y = 5
z = x is y
print(z) # Output: True

# Is not operator
a = 5
b = 6
c = a is not b
print(c) # Output: True
```

