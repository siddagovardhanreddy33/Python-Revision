# Pattern Printing in Python — Complete Explanation

Pattern printing is one of the best ways to improve:

* Loop understanding
* Nested loop logic
* Thinking ability
* Problem-solving skills

In placement rounds, interviewers use patterns to test:

* Logic building
* Loop control
* Mathematical thinking

---

# Basic Concept of Pattern Printing

Most patterns use:

## 1. Outer Loop

Controls **rows**

```python
for i in range(rows):
```

---

## 2. Inner Loop

Controls **columns / printing**

```python
for j in range(columns):
```

---

# Example 1: Square Pattern

## Pattern

```python id="bgjlwm"
* * * *
* * * *
* * * *
* * * *
```

## Code

```python id="zef10g"
rows = 4

for i in range(rows):
    for j in range(rows):
        print("*", end=" ")
    print()
```

## Explanation

* Outer loop → rows
* Inner loop → stars in each row
* `end=" "` keeps printing in same line
* `print()` moves to next line

---

# Example 2: Right Triangle

## Pattern

```python id="fw2o5q"
*
* *
* * *
* * * *
```

## Code

```python id="9rdbsg"
rows = 4

for i in range(1, rows + 1):
    for j in range(i):
        print("*", end=" ")
    print()
```

## Explanation

* Row 1 → 1 star
* Row 2 → 2 stars
* Row 3 → 3 stars

Stars increase with row number.

---

# Types of Pattern Printing

| Type              | Example          |
| ----------------- | ---------------- |
| Star Patterns     | `* * *`          |
| Number Patterns   | `1 2 3`          |
| Alphabet Patterns | `A B C`          |
| Pyramid Patterns  | Triangle         |
| Inverted Patterns | Reverse triangle |
| Diamond Patterns  | Diamond shape    |
| Pascal Triangle   | Binomial pattern |

---

# TOP 50 Pattern Printing Questions

---

# 1. Square Star Pattern

```python id="w4jlwm"
n = 5

for i in range(n):
    for j in range(n):
        print("*", end=" ")
    print()
```

---

# 2. Right Triangle

```python id="yqjx7v"
n = 5

for i in range(1, n+1):
    print("* " * i)
```

---

# 3. Inverted Right Triangle

```python id="o6p7qj"
n = 5

for i in range(n, 0, -1):
    print("* " * i)
```

---

# 4. Left Triangle

```python id="rttwwd"
n = 5

for i in range(1, n+1):
    print("  " * (n-i) + "* " * i)
```

---

# 5. Inverted Left Triangle

```python id="j9hy8r"
n = 5

for i in range(n, 0, -1):
    print("  " * (n-i) + "* " * i)
```

---

# 6. Full Pyramid

```python id="nyewbf"
n = 5

for i in range(n):
    print(" " * (n-i-1) + "* " * (i+1))
```

---

# 7. Inverted Pyramid

```python id="fyfd9s"
n = 5

for i in range(n, 0, -1):
    print(" " * (n-i) + "* " * i)
```

---

# 8. Diamond Pattern

```python id="mqq2e1"
n = 5

for i in range(n):
    print(" "*(n-i-1) + "* "*(i+1))

for i in range(n-1, 0, -1):
    print(" "*(n-i) + "* "*i)
```

---

# 9. Hollow Square

```python id="m10nt4"
n = 5

for i in range(n):
    for j in range(n):
        if i == 0 or i == n-1 or j == 0 or j == n-1:
            print("*", end=" ")
        else:
            print(" ", end=" ")
    print()
```

## Logic

Print stars only on borders.

---

# 10. Hollow Triangle

```python id="ek3mtg"
n = 5

for i in range(1, n+1):
    for j in range(1, i+1):
        if j == 1 or j == i or i == n:
            print("*", end=" ")
        else:
            print(" ", end=" ")
    print()
```

---

# 11. Number Triangle

```python id="3f4r9u"
n = 5

for i in range(1, n+1):
    for j in range(1, i+1):
        print(j, end=" ")
    print()
```

---

# 12. Floyd’s Triangle

```python id="9a2rbv"
n = 5
num = 1

for i in range(1, n+1):
    for j in range(i):
        print(num, end=" ")
        num += 1
    print()
```

---

# 13. Binary Triangle

```python id="wt7a7f"
n = 5

for i in range(1, n+1):
    for j in range(1, i+1):
        print((i+j)%2, end=" ")
    print()
```

---

# 14. Pascal Triangle

```python id="j6tkho"
n = 5

for i in range(n):
    num = 1
    for j in range(i+1):
        print(num, end=" ")
        num = num * (i-j) // (j+1)
    print()
```

---

# 15. Butterfly Pattern

```python id="7bdrr8"
n = 5

for i in range(1, n+1):
    print("*"*i + " "*(2*(n-i)) + "*"*i)

for i in range(n,0,-1):
    print("*"*i + " "*(2*(n-i)) + "*"*i)
```

---

# 16. Hourglass Pattern

```python id="0kivpi"
n = 5

for i in range(n,0,-1):
    print(" "*(n-i) + "* "*i)

for i in range(2,n+1):
    print(" "*(n-i) + "* "*i)
```

---

# 17. Rhombus Pattern

```python id="bl89bn"
n = 5

for i in range(n):
    print(" "*(n-i-1) + "* "*n)
```

---

# 18. Hollow Diamond

```python id="e6bkhq"
n = 5

for i in range(n):
    print(" "*(n-i-1) + "* " + "  "*i + "*")

for i in range(n-1,-1,-1):
    print(" "*(n-i-1) + "* " + "  "*i + "*")
```

---

# 19. Alphabet Triangle

```python id="r8ym4u"
n = 5

for i in range(n):
    ch = 65
    for j in range(i+1):
        print(chr(ch), end=" ")
        ch += 1
    print()
```

---

# 20. Reverse Alphabet Triangle

```python id="x2n2wm"
n = 5

for i in range(n,0,-1):
    ch = 65
    for j in range(i):
        print(chr(ch), end=" ")
        ch += 1
    print()
```

---

# 21. Continuous Numbers

```python id="yw0ym0"
n = 5
num = 1

for i in range(n):
    for j in range(i+1):
        print(num, end=" ")
        num += 1
    print()
```

---

# 22. Reverse Number Triangle

```python id="dz2d6y"
n = 5

for i in range(n,0,-1):
    for j in range(1,i+1):
        print(j, end=" ")
    print()
```

---

# 23. Centered Number Pyramid

```python id="5z8a7s"
n = 5

for i in range(1,n+1):
    print(" "*(n-i), end="")
    for j in range(1,i+1):
        print(j, end=" ")
    print()
```

---

# 24. Palindrome Pyramid

```python id="9n4d6t"
n = 5

for i in range(1,n+1):
    for j in range(i,0,-1):
        print(j,end="")
    for j in range(2,i+1):
        print(j,end="")
    print()
```

---

# 25. Hollow Pyramid

```python id="l6sn0m"
n = 5

for i in range(n):
    for j in range(2*n):
        if j == n-i-1 or j == n+i-1 or i == n-1:
            print("*", end="")
        else:
            print(" ", end="")
    print()
```

---

# 26. Zig-Zag Pattern

```python id="qhnpdd"
n = 9

for i in range(3):
    for j in range(n):
        if ((i+j)%4 == 0) or (i == 1 and j%4 == 0):
            print("*", end="")
        else:
            print(" ", end="")
    print()
```

---

# 27. Cross Pattern

```python id="o6ykm6"
n = 5

for i in range(n):
    for j in range(n):
        if i == j or i+j == n-1:
            print("*", end=" ")
        else:
            print(" ", end=" ")
    print()
```

---

# 28. X Pattern

```python id="jovr7u"
n = 5

for i in range(n):
    for j in range(n):
        if i == j or j == n-i-1:
            print("*", end="")
        else:
            print(" ", end="")
    print()
```

---

# 29. Plus Pattern

```python id="8v0l4s"
n = 5

for i in range(n):
    for j in range(n):
        if i == n//2 or j == n//2:
            print("*", end=" ")
        else:
            print(" ", end=" ")
    print()
```

---

# 30. Checkerboard Pattern

```python id="kef96o"
n = 5

for i in range(n):
    for j in range(n):
        print("*" if (i+j)%2 == 0 else "#", end=" ")
    print()
```

---

# 31–50 Important Practice Patterns

## 31. Hollow Rectangle

## 32. Number Pyramid

## 33. Reverse Pyramid

## 34. Sandglass Pattern

## 35. Hollow Butterfly

## 36. Character Pyramid

## 37. Triangle of Alphabets

## 38. Mirrored Triangle

## 39. Double Pyramid

## 40. Hollow Rhombus

## 41. Spiral Matrix

## 42. Snake Pattern

## 43. Diamond with Numbers

## 44. Binary Pyramid

## 45. Heart Pattern

## 46. Christmas Tree Pattern

## 47. Star Wave Pattern

## 48. Numeric Diamond

## 49. Reverse Hollow Pyramid

## 50. Pascal Triangle Advanced

---

# Important Pattern Logic Tricks

---

# 1. Space Logic

```python
" " * (n-i)
```

Used for alignment.

---

# 2. Star Logic

```python
"* " * i
```

Used to print stars.

---

# 3. Border Logic

```python
if i == 0 or i == n-1:
```

Used in hollow patterns.

---

# 4. Diagonal Logic

```python
if i == j
```

Main diagonal.

```python
if i + j == n - 1
```

Secondary diagonal.

---

# Most Asked Interview Patterns

| Easy              | Medium          | Hard           |
| ----------------- | --------------- | -------------- |
| Square            | Pyramid         | Butterfly      |
| Triangle          | Hollow Square   | Diamond        |
| Number Triangle   | Pascal Triangle | Hollow Diamond |
| Alphabet Triangle | Zig-Zag         | Spiral         |

---

# Best Way to Master Patterns

## Step-by-Step Roadmap

### Step 1

Learn:

* loops
* nested loops

### Step 2

Practice:

* square
* triangle
* inverted triangle

### Step 3

Learn:

* spaces
* alignment

### Step 4

Practice:

* pyramids
* diamonds
* hollow patterns

### Step 5

Solve:

* mixed logic patterns

---

# Golden Rule for Pattern Printing

Always ask:

1. How many rows?
2. How many columns?
3. Where to print star/number?
4. Where to print spaces?
