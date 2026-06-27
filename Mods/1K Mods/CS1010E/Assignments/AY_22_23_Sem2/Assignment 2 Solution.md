# Question 1: Make Out Word

>[!example]- Question
> Given a string `s` of exactly 4 characters (e.g. `'<<>>'`) and another string `word` (e.g. `'hi'`), the function `make_out_word(s, word)` returns a **new string** in which `word` is in the middle of `s`, e.g. `'<<hi>>'`.
> 
> More examples:
> - Function call `make_out_word('<<>>', 'Yay')` returns `'<<Yay>>'`
> - Function call `make_out_word('<<>>', 'WooHoo')` returns `'<<WooHoo>>'`
> - Function call `make_out_word('[[]]', 'word')` returns `'[[word]]'`
> 
> Hint: Use string slicing wisely and there is no need to use any loop.

```python
def make_out_word(s, word):
  return s[:2] + word + s[2:]
```

---
# Question 2: Number Concatenation

>[!example]- Question
> Write a function `concat(m, n)` that takes two integers `m` and `n` as parameters, returns an integer in which `m` and `n` are 'concatenated'. You may assume that `m` is not zero and the return value of the function call is not overly large.
> 
> For example, function call `concat(1234, 567)` returns integer `1234567`. Note that the return value of the function call is an integer (i.e. `int` type).
> 
> Hint: The easiest way is to use string concatenation.

```python
def concat(m, n):
  return int(str(m) + str(n))
```

---
# Question 3: Digital Characters

>[!example]- Question
> Write a function `at_most_10(string)` that checks if the given `string` contains at most 10 **digit characters**. The function returns `True` if so, or `False` otherwise.
> 
> Digit characters refer to characters `'0'`, `'1'`, till `'9'`. Note that string `'10'` contains two digit characters.

```python
def at_most_10(string):
  count = 0
  for ch in string:
    if '0' <= ch <= '9':
      count = count + 1
  return count <= 10
```

---
# Question 4: Square Odd Integers

>[!example]- Question
Write a function `square_odd_terms(tpl)` that accepts a tuple of integers as parameter and returns a list in which all the odd integers of `tpl` are squared, even integers remain the same, and the order of all integers remain the same.
> 
> For example, function call `square_odd_terms( (2, 3, 4, 5) )` returns the list `[2, 9, 4, 25]`.

```python
def square_odd_terms(tpl):
  lst = []
  for val in tpl:
    if val%2 == 0:
      lst.append(val)
    else:
      lst.append(val**2)
  return lst
```

---
# Question 5: Is Tuple Sorted?

>[!example]- Question
Write a function `is_sorted(tup)` that takes a tuple of integers `tup` as parameter and returns `True` if all the integers are sorted in **non-decreasing** order, or `False` otherwise. You may assume that `tup` contains at least 2 integers.
>
For example, function call `is_sorted( (1, -2, 8, 6) )` returns `False` and function call `is_sorted( (4, 6, 7, 7, 9) )` returns `True`.

```python
def is_sorted(tup):
  for i in range(len(tup)-1):
    if tup[i] > tup[i+1]:
      return False
  return True
```

---
# Question 6: Max and Min

>[!example]- Question
A function can return at most one value. However, sometimes we may want to return multiple values from a function. Tuples can come in handy in such cases. For example, we can create a tuple containing multiple values and return the tuple when function finishes execution.
>
Write a function `max_and_min(values)` that accepts a tuple of integers as parameter. The function returns a new tuple containing the largest and smallest value in `values`, in that order. You may assume that `values` contains at least one integer.
>
For example, function call `max_and_min( (1, -1, 7, 0) )` returns tuple `(7, -1)`.
>
You are **NOT** allowed to use built-in functions max and min in this question.
>
Hint: Define two variables maximum and minimum. Use a loop to go through the tuple element by element; compare and update maximum and minimum along the way. Also be careful when choosing the initial values of maximum and minimum.

```python
def max_and_min(values):
  maximum = values[0]
  minimum = values[0]
  for val in values:
    if val > maximum:
      maximum = val
    elif val < minimum:
      minimum = val
  return (maximum, minimum)
```

---
# Question 7: Standard Deviation

>[!example]- Question
Write a function `deviation(tpl)` that accepts a tuple of integers as parameter and returns the standard deviation of all the integers.
>
The standard deviation $s$ is computed according to the following formula:
>
$$s = \sqrt{\frac{(x_1 - \bar{x})^2 + (x_2 - \bar{x})^2 + \cdots + (x_n - \bar{x})^2}{n}}$$
>
The variable $\bar{x}$ is the average of all the integers in tpl.
>
You are allowed to use (1) Python built-in function `sum()`, and (2) `sqrt()` function from the `math` module.

```python
def deviation(tpl):
  n = len(tpl)
  avg = sum(tpl) / n # average
  total = 0
  for val in tpl:
    total = total + (val-avg)**2
  return (total/n)**0.5
```

---
# Question 8: Anagram

An anagram is a word formed by rearranging letters of a different word and using all the original letters exactly once. For instance, Listen and Silent are anagram because of the mapping shown in Figure 1.

![[Assignment 2 Solution-1782562418923.webp]]

Figure 1: Mapping between listen and silent.

Write a function `is_anagram(s1, s2)` that returns `True` if two strings `s1` and `s2` are anagram of each other, or `False` otherwise. You may assume that `s1` and `s2` consists of only lowercase or uppercase letters from the English alphabets.

For example,

- function call `is_anagram('ABC', 'BCA')` returns `True`
- function call `is_anagram('ABC', 'bca')` returns `False`

You are **NOT allowed** to use any sorting functions provided by Python. Instead, you are supposed to use **dictionary** to solve this question.

Hint: Use dictionary to note down the occurrence of each letter.

```python
def is_anagram(s1, s2):
  d = {}
  for ch in s1:
    if ch in d: # already in dictionary
      d[ch] = d[ch] + 1
    else:
      d[ch] = 1

  for ch in s2:
    if not ch in d: # s1 doesn't have this character!
      return False
    else:
      d[ch] = d[ch] -1

  for val in d.values():
    if val != 0:
      return False
  return True
```

---
# Question 9: Merged Sorted Tuples

**Merge Sort** is an advanced sorting technique that will be introduced in second programming module. Here, we are not going to explain how merge sort works, but focus on one idea engaged in merge sort: merging two sorted tuples into a bigger sorted tuple.

For instance, given two sorted tuples (-1, 1, 3, 5) and (-2, 4, 6, 7), the merged tuple would be (-2, -1, 1, 3, 4, 5, 6, 7).

Write a function `merge(tup1, tup2)` that accepts two sorted tuples as parameters, and returns the merged tuple in which all integers appears in ascending order.

You may assume that

1. `tup1` and `tup2` each contains distinct integers sorted in ascending order.
2. integers in `tup1` are different from those in `tup2`.

You are **NOT allowed** to do sorting or use any sorting functions provided by Python.

Hint: A smart algorithm just needs a single loop to solve this problem. However, using single loop or nested loop doesn't affect your attempt mark.

```python
def merge(tup1, tup2):
  idx1, idx2 = 0, 0
  res = ()
  
  while idx1<len(tup1) and idx2<len(tup2):
    if tup1[idx1] < tup2[idx2]:
      res = res + (tup1[idx1],)
      idx1 = idx1 + 1
    else:
      res = res + (tup2[idx2],)
      idx2 = idx2 + 1

  # at most one of the following two loops will run
  while idx1 < len(tup1):
    res = res + (tup1[idx1],)
    idx1 = idx1 + 1

  while idx2 < len(tup2):
    res = res + (tup2[idx2],)
    idx2 = idx2 + 1
  
  return res
```

---
# Question 10: Resistors

In electrical circuits, a resistor is used to reduce the flow of current. Its capability to reduce the flow of current depends on its resistance value, measured on ohm ($\Omega$).

![[Assignment 2 Solution-1782562543300.webp]]

Figure 2: IEC resistor symbol (www.wikipedia.org).

When connected in series, the total resistance is the sum of each individual resistance values.

![[Assignment 2 Solution-1782562553643.webp]]

Figure 3: Resistor connected in series, the equivalent resistance value is $R_{eq} = R_1 + R_2 + \cdots + R_n$.

As an engineer, you are given a sequence of resistors which are already sorted in ascending order of resistance values.

Write a function `resistors(seq, R)` that takes in a tuple of resistors `seq` and a value `R` as parameter. The function checks if any two resistors in `seq` that add up to `R`. It returns `True` if so, or `False` otherwise.

For example, function call `resistors((1, 3, 4), 4)` returns `True` because $1 + 3 = 4$ and function call `resistors((1, 3, 5, 7), 5)` returns `False`.

You may assume that `seq` contains distinct integers sorted in ascending order.

Note: This question can be done using a nested loop. However, such a design is not the best as the program is complex and execution takes longer time. For strong students, you may challenge yourself to use one single loop to solve this question.

**Restrictions

- You are not allowed to modify the input sequence.
**Assumptions

- `len(seq) >= 2`
- `seq[i]` contains only positive integers sorted in ascending order

```python
def resistors(seq, R):
  left, right = 0, len(seq)-1
  while left < right:
    if seq[left] + seq[right] == R:
      return True
    elif seq[left] + seq[right] > R:
      right = right - 1
    else:
      left = left + 1
  return False
```

---
# Question 11: Ancestry Tree

All of us may come from different families, but we may share common ancestors! In this question, we will explore the use of a dictionary to model ancestry trees.

Given some ancestry information such as shown in Figure 4, we may list the following information:

![[Assignment 2 Solution-1782562671672.webp]]


We may easily construct the _graphical representation_ of the ancestry tree 
(_right_) and we can also construct a dictionary to represent our ancestry tree:

``` python
tree = {
    'Amy': 'Ben', 'Tom': 'Ben', 'Frank': 'Amy',
    'May': 'Tom', 'Ben': 'Howard', 'Howard': 'George'
}
```

In the dictionary above, the _keys_ of the dictionary represent the _child_ while the _values_ of the dictionary represent the _parent_. You can check that indeed Ben is Amy's parent since given the key `'Amy'` it gives us the value `'Ben'` (i.e., `tree['Amy'] == 'Ben'`).

**Assumptions

- Every name in the dictionary is unique.
- Every person has at most one parent.
- Your code should work any ancestry tree.
- There will be no cycle (_i.e., I am my own grandparent scenario_).

**Restrictions

- The dictionary `tree` should not be modified.

**Find your Ancestor

Write a function `find_ancestor(name, tree)` that returns the ancestor of `name`. You may assume that `name` belongs to the ancestry `tree`.

For example, function call `find_ancestor('Amy', tree)` will return `'George'`.

**Are They Related?

Two people are related if they share a common ancestor in the ancestry tree. In the example ancestry tree given above, any two _distinct_ people are related to one another. For instance, Amy and Tom are related since they share a common ancestor George. Additionally, Ben and Howard are related since they share a common ancestor George.

On the other hand, if we introduce a new person Luna with no ties to anyone in the given tree above, then Luna is not related to anyone else. By convention, a person must be related to himself/herself.

Write the function `is_related(name1, name2, tree)` to check if the person `name1` is related to the person `name2` in the ancestry tree `tree`. The function returns `True` if so, or `False` otherwise.

You may assume that `name1` is different from `name2`.

Consider the following modified ancestry tree:

``` python
tree2 = {
    'Amy' : 'Ben'   , 'Tom'  : 'Ben'  , 'Frank' : 'Amy',
    'May' : 'Tom'   , 'Ben'  : 'Howard', 'Howard': 'George',
    'Joe' : 'Bill'  , 'Bill' : 'Mary' , 'Zoe'   : 'Mary',
    'Mary': 'Philip', 'Simon': 'Bill'
}
```

```python
def find_ancestor(name, tree):
  while name in tree:
    name = tree[name] # update name to his/her parent
  return name

def is_related(name1, name2, tree):
  anc1 = find_ancestor(name1, tree)
  anc2 = find_ancestor(name2, tree)
  return anc1 == anc2
```

---
# Question 12: Counting Substring \[Hard]

Write a function `count_substring(string)` that accepts a `string` as parameter, and returns the number of substrings that begin with character `'A'` and ends with character `'X'`.

For example, suppose `string = 'CAXAAYXZA'`, there are four substrings that begin with `'A'` and ends with `'X'`, namely: `'AX'`, `'AXAAYX'`, `'AAYX'`, and `'AYX'`. Therefore, function call `count_substring('CAXAAYXZA')` returns `4`.

You can assume that `string` is composed of upper case letters only.

Note: This question can be done using a nested loop. However, such a design is not the best as the program is complex and execution takes longer time. For strong students, you **may challenge** yourself to use one single loop to solve this question.

```python
def count_substring(string):
  count_A = 0   # count the number of 'A'
  count_sub = 0 # count the number of substring 'A..X'
  for ch in string:
    if ch == 'A':
      count_A = count_A + 1
    elif ch == 'X':
      count_sub = count_sub + count_A
  return count_sub
```
