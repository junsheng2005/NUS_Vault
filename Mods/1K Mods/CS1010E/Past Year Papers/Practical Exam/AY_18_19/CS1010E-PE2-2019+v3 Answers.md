# Part 1
## Task 1
```python
def superFibonacciSeqR(t2,n):
	if n == 2:
		return [1,t2] 
	elif n > 0:
		return superFibonacciSeqR(t2,n-1) + [(1 + t2)*2**(n-3)]
```
## Task 2
```python
def superFibonacciSeqI(t2,upperbound):
	t1 = 1
	t3 = t2 + 1
	n = 1
	lst = [1,t2,t3]
	while True:
		tn = t3*2**n
		n += 1
		if tn > upperbound:
			break
		else:
			lst.append(tn)
	return lst
```
## Task 3
```python
def smallestSecondTermSFScontains(n):
	while n%2 == 0:
		n = n/2
	return int(n-1)
```

# Part 2
## Task 4
```python
from math import sqrt

class PizzaShop:
	def __init__(self,pos,name,radius,starthour,endhour):
		self.pos = pos
		self.name = name
		self.radius = radius
		self.starthour = starthour
		self.endhour = endhour
		
	def distanceSquareTo(self,i,j):
		distance = sqrt((self.pos[0] - i)**2 + (self.pos[1] - j)**2)
		return distance
```
## Task 5
```python
def PDMap(r,c,allPS,currentHour):
	matrix = [['.' for i in range(c)] for i in range(r)]
	coord_y = 0
	for row in matrix:
		coord_x = 0

		for colum in row:
			shop_distance = {}

			for shop in allPS:
				pos = shop.pos
				Letter = shop.name[0]
				distance = shop.distanceSquareTo(coord_x,coord_y)

				if distance<=shop.radius and shop.starthour<=currentHour<shop.endhour:
					shop_distance[Letter] = distance

			
			if shop_distance:
				min_dist = min(shop_distance.values())
				shop_list = [k for k,v in shop_distance.items() if v == min_dist]
				if len(shop_list) == 1:
					matrix[coord_y][coord_x] = shop_list[0]
				
				elif len(shop_list) > 1:
					matrix[coord_y][coord_x] = 'X'
			
			coord_x += 1
		
		coord_y += 1

	return matrix
```
# Part 3

## Task 6
```python
def sumTo(leftdigits: str, ops: str, n: int) -> list:
    if not leftdigits:
        return []
    
    solutions = []
    
    def backtrack(index: int, current_expr: str):
        # Base case: if we have processed all digits, evaluate the expression
        if index == len(leftdigits):
            try:
                # eval handles standard mathematical precedence for +, -, *, and %
                if eval(current_expr) == n:
                    solutions.append(f"{current_expr}={n}")
            except ZeroDivisionError:
                # Catch potential modulo by zero errors if % is used
                pass
            return
        
        # Option 1: Place no operator (concatenate the next digit)
        backtrack(index + 1, current_expr + leftdigits[index])
        
        # Option 2: Place one of the allowed operators before the next digit
        for op in ops:
            backtrack(index + 1, current_expr + op + leftdigits[index])

    # Start the recursion with the first digit already in the expression
    backtrack(1, leftdigits[0])
    
    # Return the results sorted in ascending lexicographic order
    return sorted(solutions)
```