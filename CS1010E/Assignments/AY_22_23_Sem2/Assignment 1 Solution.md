# Question 1

```run-python
def compute_bmi():
    height = float(input("Enter height: "))
    weight = float(input("Enter weight: "))
    BMI = weight/(height**2)
    if BMI < 18.5:
        return "Under"
    elif BMI < 25 and BMI >= 18.5:
          return "Normal"
    elif BMI < 35 and BMI >+ 25:
          return "Over"
    else:
          return "Obese"
    
print(compute_bmi())
```

---
# Question 2

```run-python
def triangle(a, b, c):
    lst = [a, b, c]
    x = max(lst)
    lst.remove(x)
    if sum(lst) > x:
        if a == b and a == c:
            return "Equilateral"
        elif a == b or a == c or b == c:
            return "Isosceles"
        else:
            return "Scalene"
    else:
        return "Not a triangle"
    
print(triangle(1,1,2))
```

---
# Question 3

```run-python
def factorial(n):
    if n <= 1:
        return 1
    else:
        return n*factorial(n-1)
    
print(factorial(5))
```

---
# Question 4

```run-python
def is_sum_odd(number):
    lst = []
    while number != 0:
        lst.append(number%10)
        number = number // 10

    if sum(lst) % 2 == 0:
        return False
    else:
        return True

print(is_sum_odd(110))
```

---
# Question 5

 ```run-python
def perfect_number(n):
    lst = [1]
    n1 = 2
    n2 = n
    if n == 1:
        return True
    else:
        while n2 > 1:
            for i in range(n1,n2):
                if n%i == 0:
                    lst.append(i)
                    n1 = i
                    n2 = int(n2/i)
    
    total = sum(lst)
    if n == total:
        return True
    else:
        return False
    
print(perfect_number(6))
 ```

---
# Question 6

```run-python
def contain_digit(number, digit):
    lst = []
    while number != 0:
        lst.append(number%10)
        number = number // 10
    
    if digit in lst:
        return True
    else:
        return False
    
def find_winners(factor, must_have, n):
    must_have_lst = []
    for i in range(n+1):
        if contain_digit(i,must_have):
            must_have_lst.append(i)
    
    winner_lst = [x for x in must_have_lst if x % factor == 0]
    return len(winner_lst)

print(find_winners(7,7,200))
```

---
# Question 7

```run-python
def double_char(word):
    new_word = ""
    for i in word:
        new_word = new_word + i*2

    return new_word

print(double_char("hello"))
```

---
# Question 8

```run-python
import turtle

def draw_reg_poly(d,n):
    angle = poly_angle(n)
    polygon = turtle.Turtle()
    for i in range(n):
        polygon.forward(d)
        polygon.right(180-angle)
    
    turtle.done


def poly_angle(n):
    angle = ((n-2)*180)/n
    return angle

draw_reg_poly(100,5)
```

---
# Question 9

```run-python
import turtle

def draw_flower(d,n,p):
    petal = int(360//p)
    angle = poly_angle(n)
    polygon = turtle.Turtle()
    for j in range(p):
        for i in range(n):
            polygon.forward(d)
            polygon.right(180-angle)
        polygon.right(petal)
        
def poly_angle(n):
    angle = ((n-2)*180)/n
    return angle

draw_flower(100,8,10)
```

---
# Question 10

```run-python
def invert_number(n):
    lst = []
    while n != 0:
        lst.append(n%10)
        n = n // 10


    inv_n = 0
    multiplier = len(lst) - 1
    for i in lst:
        inv_n = inv_n + i*(10**multiplier)
        multiplier -= 1

    return inv_n

print(invert_number(123000))
```

---
# Question 11

```run-python
def invert_number(n):
    lst = []
    while n != 0:
        lst.append(n%10)
        n = n // 10


    inv_n = 0
    multiplier = len(lst) - 1
    for i in lst:
        inv_n = inv_n + i*(10**multiplier)
        multiplier -= 1

    return inv_n

def reversed_number(low,high):
    number = 0
    for i in range(low,high+1):
        if i == invert_number(i):
            number += 1

    return number

print(reversed_number(150,202))
```

