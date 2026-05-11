# Top 50 Placement Coding Questions in Python (with Explanation)

---

# 1. Reverse a String

### Problem

Reverse a given string.

### Code

```python
s = "python"

reversed_string = s[::-1]

print(reversed_string)
```

### Explanation

* `[::-1]` means traverse the string from end to start.
* Time Complexity: O(n)

---

# 2. Check Palindrome String

### Code

```python
s = "madam"

if s == s[::-1]:
    print("Palindrome")
else:
    print("Not Palindrome")
```

### Explanation

* A palindrome reads same forward and backward.

---

# 3. Swap Two Numbers

### Code

```python
a = 10
b = 20

a, b = b, a

print(a, b)
```

### Explanation

* Python supports tuple unpacking.

---

# 4. Find Largest Element in Array

### Code

```python
arr = [10, 20, 4, 45, 99]

largest = max(arr)

print(largest)
```

### Explanation

* `max()` returns largest element.

---

# 5. Find Second Largest Element

### Code

```python
arr = [10, 20, 4, 45, 99]

arr.sort()

print(arr[-2])
```

### Explanation

* Sort array and access second last element.

---

# 6. Count Vowels in String

### Code

```python
s = "programming"

count = 0

for ch in s:
    if ch.lower() in "aeiou":
        count += 1

print(count)
```

### Explanation

* Check every character against vowels.

---

# 7. Fibonacci Series

### Code

```python
n = 10

a, b = 0, 1

for i in range(n):
    print(a, end=" ")
    a, b = b, a + b
```

### Explanation

* Each number is sum of previous two numbers.

---

# 8. Factorial of Number

### Code

```python
n = 5
fact = 1

for i in range(1, n + 1):
    fact *= i

print(fact)
```

### Explanation

* Multiply all numbers from 1 to n.

---

# 9. Prime Number Check

### Code

```python
n = 13

flag = True

for i in range(2, int(n**0.5) + 1):
    if n % i == 0:
        flag = False
        break

if flag and n > 1:
    print("Prime")
else:
    print("Not Prime")
```

### Explanation

* Check divisibility up to square root of n.

---

# 10. Armstrong Number

### Code

```python
n = 153

temp = n
sum = 0

while n > 0:
    digit = n % 10
    sum += digit ** 3
    n //= 10

print(temp == sum)
```

### Explanation

* Sum of cube of digits equals original number.

---

# 11. Reverse Number

### Code

```python
n = 1234

rev = 0

while n > 0:
    digit = n % 10
    rev = rev * 10 + digit
    n //= 10

print(rev)
```

### Explanation

* Extract digits one by one using modulo.

---

# 12. Sum of Digits

### Code

```python
n = 1234

total = 0

while n > 0:
    total += n % 10
    n //= 10

print(total)
```

### Explanation

* Add last digit repeatedly.

---

# 13. Count Digits

### Code

```python
n = 12345

count = 0

while n > 0:
    count += 1
    n //= 10

print(count)
```

---

# 14. Find GCD

### Code

```python
a = 12
b = 18

while b:
    a, b = b, a % b

print(a)
```

### Explanation

* Euclidean Algorithm.

---

# 15. Find LCM

### Code

```python
a = 12
b = 18

gcd = a

temp_b = b

while temp_b:
    gcd, temp_b = temp_b, gcd % temp_b

lcm = (a * b) // gcd

print(lcm)
```

---

# 16. Remove Duplicates from List

### Code

```python
arr = [1,2,2,3,4,4]

result = list(set(arr))

print(result)
```

### Explanation

* Set removes duplicates.

---

# 17. Find Missing Number

### Code

```python
arr = [1,2,3,5]

n = 5

missing = n*(n+1)//2 - sum(arr)

print(missing)
```

---

# 18. Check Anagram

### Code

```python
s1 = "listen"
s2 = "silent"

print(sorted(s1) == sorted(s2))
```

### Explanation

* Anagrams have same sorted characters.

---

# 19. Frequency of Characters

### Code

```python
s = "apple"

freq = {}

for ch in s:
    freq[ch] = freq.get(ch, 0) + 1

print(freq)
```

---

# 20. Linear Search

### Code

```python
arr = [10,20,30,40]

target = 30

for i in arr:
    if i == target:
        print("Found")
```

---

# 21. Binary Search

### Code

```python
arr = [1,2,3,4,5]

target = 4

low = 0
high = len(arr)-1

while low <= high:
    mid = (low + high)//2

    if arr[mid] == target:
        print("Found")
        break
    elif arr[mid] < target:
        low = mid + 1
    else:
        high = mid - 1
```

### Explanation

* Divide search space into half each time.

---

# 22. Bubble Sort

### Code

```python
arr = [5,1,4,2]

for i in range(len(arr)):
    for j in range(len(arr)-i-1):
        if arr[j] > arr[j+1]:
            arr[j], arr[j+1] = arr[j+1], arr[j]

print(arr)
```

---

# 23. Selection Sort

### Code

```python
arr = [64,25,12,22,11]

for i in range(len(arr)):
    min_idx = i

    for j in range(i+1, len(arr)):
        if arr[j] < arr[min_idx]:
            min_idx = j

    arr[i], arr[min_idx] = arr[min_idx], arr[i]

print(arr)
```

---

# 24. Insertion Sort

### Code

```python
arr = [12,11,13,5,6]

for i in range(1, len(arr)):
    key = arr[i]
    j = i - 1

    while j >= 0 and key < arr[j]:
        arr[j+1] = arr[j]
        j -= 1

    arr[j+1] = key

print(arr)
```

---

# 25. Merge Two Sorted Arrays

### Code

```python
a = [1,3,5]
b = [2,4,6]

result = sorted(a+b)

print(result)
```

---

# 26. Find Common Elements

### Code

```python
a = [1,2,3]
b = [2,3,4]

print(list(set(a) & set(b)))
```

---

# 27. Two Sum Problem

### Code

```python
arr = [2,7,11,15]

target = 9

seen = {}

for i, num in enumerate(arr):
    diff = target - num

    if diff in seen:
        print(seen[diff], i)

    seen[num] = i
```

### Explanation

* Store visited elements in dictionary.

---

# 28. Move Zeros to End

### Code

```python
arr = [0,1,0,3,12]

result = [x for x in arr if x != 0]

zeros = [0] * (len(arr)-len(result))

print(result + zeros)
```

---

# 29. Rotate Array

### Code

```python
arr = [1,2,3,4,5]

k = 2

print(arr[-k:] + arr[:-k])
```

---

# 30. Maximum Element in Array

### Code

```python
arr = [1,7,3,9,5]

print(max(arr))
```

---

# 31. Minimum Element in Array

### Code

```python
arr = [1,7,3,9,5]

print(min(arr))
```

---

# 32. Kadane’s Algorithm

### Problem

Maximum subarray sum.

### Code

```python
arr = [-2,1,-3,4,-1,2,1,-5,4]

max_sum = current = arr[0]

for i in arr[1:]:
    current = max(i, current + i)
    max_sum = max(max_sum, current)

print(max_sum)
```

### Explanation

* Track current maximum sum dynamically.

---

# 33. Find Duplicate Elements

### Code

```python
arr = [1,2,3,2,4,5,1]

duplicates = set()

seen = set()

for num in arr:
    if num in seen:
        duplicates.add(num)
    else:
        seen.add(num)

print(duplicates)
```

---

# 34. Count Words in Sentence

### Code

```python
s = "Python is easy"

print(len(s.split()))
```

---

# 35. Reverse Words in Sentence

### Code

```python
s = "Python is easy"

print(" ".join(s.split()[::-1]))
```

---

# 36. Find Largest Word

### Code

```python
s = "Python programming language"

words = s.split()

print(max(words, key=len))
```

---

# 37. Check Balanced Parentheses

### Code

```python
s = "{[()]}"

stack = []

pairs = {')':'(', '}':'{', ']':'['}

balanced = True

for ch in s:
    if ch in "({[":
        stack.append(ch)
    else:
        if not stack or stack[-1] != pairs[ch]:
            balanced = False
            break
        stack.pop()

print(balanced and not stack)
```

---

# 38. Find Frequency of Elements

### Code

```python
arr = [1,2,2,3,3,3]

freq = {}

for num in arr:
    freq[num] = freq.get(num, 0) + 1

print(freq)
```

---

# 39. Matrix Addition

### Code

```python
a = [[1,2],[3,4]]
b = [[5,6],[7,8]]

result = []

for i in range(len(a)):
    row = []

    for j in range(len(a[0])):
        row.append(a[i][j] + b[i][j])

    result.append(row)

print(result)
```

---

# 40. Transpose Matrix

### Code

```python
matrix = [[1,2,3],[4,5,6]]

transpose = list(zip(*matrix))

print(transpose)
```

---

# 41. Check Leap Year

### Code

```python
year = 2024

if (year % 400 == 0) or (year % 4 == 0 and year % 100 != 0):
    print("Leap Year")
else:
    print("Not Leap Year")
```

---

# 42. Generate Random Password

### Code

```python
import random
import string

length = 8

chars = string.ascii_letters + string.digits

password = ''.join(random.choice(chars) for _ in range(length))

print(password)
```

---

# 43. Find ASCII Value

### Code

```python
ch = 'A'

print(ord(ch))
```

---

# 44. Convert Decimal to Binary

### Code

```python
n = 10

print(bin(n)[2:])
```

---

# 45. Find Power Without pow()

### Code

```python
a = 2
b = 5

result = 1

for i in range(b):
    result *= a

print(result)
```

---

# 46. Count Even and Odd Numbers

### Code

```python
arr = [1,2,3,4,5,6]

even = odd = 0

for i in arr:
    if i % 2 == 0:
        even += 1
    else:
        odd += 1

print(even, odd)
```

---

# 47. Find Intersection of Arrays

### Code

```python
a = [1,2,3]
b = [2,3,4]

print(list(set(a).intersection(set(b))))
```

---

# 48. Check Substring

### Code

```python
s = "programming"

sub = "gram"

print(sub in s)
```

---

# 49. Longest Substring Without Repeating Characters

### Code

```python
s = "abcabcbb"

seen = set()

left = 0
max_len = 0

for right in range(len(s)):
    while s[right] in seen:
        seen.remove(s[left])
        left += 1

    seen.add(s[right])

    max_len = max(max_len, right-left+1)

print(max_len)
```

---

# 50. Valid Palindrome (Ignoring Special Characters)

### Code

```python
s = "A man, a plan, a canal: Panama"

filtered = ""

for ch in s:
    if ch.isalnum():
        filtered += ch.lower()

print(filtered == filtered[::-1])
```

