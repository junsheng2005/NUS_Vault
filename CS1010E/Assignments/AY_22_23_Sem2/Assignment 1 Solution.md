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
