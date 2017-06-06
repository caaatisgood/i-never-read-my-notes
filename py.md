## py

```python
try:
    # do whatever ya wanna do
except:
    # who cares?
    pass
```

```python
>>> lst = [True, True, False]
>>> all(lst)
False
>>> any(lst)
True
```

```python
>>> lst = [1, 2, 3]
>>> tup = (1, 2, 3)
>>> dic = {1: 1, 2: 2, 3: 3}
>>> max(lst)
3
>>> max(tup)
3
>>> min(lst)
1
>>> min(tup)
1
>>> sum(lst)
6
>>> sum(tup)
6
>>> len(lst)
3
>>> len(tup)
3
>>> len(dic)
3
```

```python
>>> for n in range(4, 8):
...     print(n)
...
4
5
6
7
```

```python
>>> def add(*tup):
...     print(tup)
...     return sum(tup)
...
>>> add(1, 2, 3)
(1, 2, 3)
6
```

```python
>>> def power(base, exp):
...     return base ** exp
...
>>> dic = {'base': 2, 'exp': 3}
>>> power(**dic)  # same as power(base=2, exp=3)
8
```

```python
>>> def test(*args, **kwargs):
...     print(args)
...     print(kwargs)
...
>>> test(1, 2, 3, ['a', 'b'], {'d': 'dic'}, -2, fuck='you')
(1, 2, 3, ['a', 'b'], {'d': 'dic'}, -2)
{'fuck': 'you'}
```

```python
class Husky:
    def __init__(self, name):
        self.name = name
    def speak(self):
        print('{}:'.format(self.name), 'Fuck!')

remy = Husky('Remy')
print('Remy sit.')
print('Speak!')
remy.speak()
print('Good boy!')
```
