# Operators

## Arithmetic / operator precedence

1. What is the value of each of these expressions?

```java
13 + 6;
20 - 7;
5 * 7;
10 / 3;
45 % 6;
```

2. What is the result of each of these expressions?

```java
1 + 2 * 3;
1 * 2 + 3;
(1 + 2) * 3 - 4 * 5 % 6 + 7;
```

3. What are the values of the variables at each point marked by a comment?

```java
int a = 3;
int b = a++; // What are the values of `a` and `b`?

int c = 7;
int d = --c; // What are the values of `c` and `d`?

int e = 2;
int f = e++ + --e; // What are the values of `e` and `f`?

int g = 5;
int h = g++ - 2 * --g + ++g;; // What are the values of `g` and `h`?
```

## Logical / relational operators

4. Which of the following conditions are true?

```java
boolean a = true, b = true;
boolean c = false, d = false;

boolean cond1 = (a || c) && (b || d);
boolean cond2 = (a || b) && (c || d);
boolean cond3 = (a && b) || (c && d);
boolean cond4 = (a && c) || (b && d);
```

5. What values are held by each variable at each of the marked points?

```java
int a = 4;
boolean b = (a > 5) && (a < 10); // What are the values of `a` and `b`?

int c = 4;
boolean d = (c > 5) || (c < 10); // What are the values of `c` and `d`?

int e = 4;
boolean f = (e > 5) && (++e < 10); // What are the values of `e` and `f`?

int g = 4;
boolean h = (g > 5) || (++g < 10); // What are the values of `g` and `h`?

int i = 4;
boolean j = (i > 5) & (++i < 10); // What are the values of `i` and `j`?

int k = 4;
boolean l = (k > 5) | (++k < 10); // What are the values of `k` and `l`?
```

## Equality operators

6. Which of the following conditions are true? Assume that the `Blob` class exists and is correct.

```java
int a = 3;
int b = 3;
int c = 1 + 2;

Blob d = new Blob(3);
Blob e = new Blob(3);
Blob f = new Blob(1 + 2);

boolean cond1 = a == b;
boolean cond2 = a == c;
boolean cond2 = b == c;

boolean cond4 = d == e;
boolean cond5 = d == f;
boolean cond6 = e == f;

boolean cond7 = a == d.getValue();
boolean cond8 = a == e.getValue();
boolean cond9 = a == f.getValue();
```

## Assignment operators

7. What is the value of each variable at the marked points?

```java
boolean a = false, b;
if (a == true) { b = true; } else { b = false; } // What are `a` and `b`?

boolean c = false, d;
if (c = true) { d = true; } else { d = false; } // What are `c` and `d`?

boolean e = true, f;
if (e == true || e = false) { f = true; } else { f = false; } // What are `e` and `f`?

boolean g = true, h;
if (g = false || g == true) { h = true; } else { h = false; } // What are `g` and `h`?
```

8. What is the value of each variable at the marked points?

```java
int a = 3;
a += 2; // What is the value of `a`?

int b = 15;
b %= 6; // What is the value of `b`?

int c = 6, d;
d = c -= 3; // What are the values of `c` and `d`?

int e = 11, f;
f = (f = e *= 2) - 13; // What are the values of `e` and `f`?
```

## Numeric promotion

9. Which of these expressions compile?

```java
byte b = 1; short s = 1; int i = 1; long l = 1; float f = 1.0f; double d = 1.0;

byte expr1 = b + b;
short expr2 = s + s;
int expr3 = i + i;
long expr4 = l + l;

int expr5 = b + b;
int expr6 = s + s;
int expr7 = i + i;
int expr8 = l + l;

float expr9 = b + f;
float expr10 = l + f;
double expr11 = b + f;
double expr12 = l + f;

float expr13 = b + d;
float expr14 = l + d;
double expr15 = b + d;
double expr16 = l + d;

double expr17 = b + s * i / l;
```