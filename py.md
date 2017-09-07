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
# The line above it'a actually doing something like:
# Husky.__init__(remy, 'Remy')
print('Remy sit.')
print('Speak!')
remy.speak()
print('Good boy!')
```

```python
# inheritance, polymorphism
class Dog:
    def __init__(self, name):
        self.name = name
    def run(self):
        print(self.name, "run")

class Husky(Dog):
    def bark(self):
        print(self.name, "barks:", "Fuck!")

class Schnauzer(Dog):
    def bark(self):
        print(self.name, "barks:", "Bark!")
```

```python
# namespace
>>> dir()
['__builtins__', '__doc__', '__name__', '__package__']
```

```python
>>> def test():
...     foo = "bar"
...     baz = {'qux': 'qux'}
...
>>> test()
{'baz': {'qux': 'qux'}, 'foo': 'bar'}
```

```python
>>> isinstance('fuck you', str)
True
```

```python
>>> truth = ['ben', 'loves', 'to', 'eat', 'shit']
>>> for i, e in enumerate(truth):
...    print(i, e)
...
0 ben
1 loves
2 to
3 eat
4 shit
```

```python
# re to check whether a string contains Chinese character or not
import re
re.search(u'[\u4e00-\u9fff]', 'hen想下班')
```
