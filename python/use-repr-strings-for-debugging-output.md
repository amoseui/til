# Use repr strings for debugging output

repr returns strings of object info

```python
b = eval(repr(a))
asser a == b
```
---
Declare \_\_repr\_\_ method to represent object.

```python
class ReprClass(object):
    def __init__(self, x, y):
      self.x = x
      self.y = y

    def __repr__(self):
      return 'ReprClass(%d, %d)' % (self.x, self.y)
```
```python
obj = ReprClass(1, 2):
print(obj)

>>>
ReprClass(1, 2)
```
---
If you can't control declaration of the class,

```python
obj = ReprClass(3, 4):
print(obj.__dict__)

>>>
{'y': 4, 'x': 3}
```
---

##### Reference

- [Effective Python #56](https://www.amazon.com/Effective-Python-Specific-Software-Development/dp/0134034287)
  - [한글 번역: 파이썬 코딩의 기술](http://www.yes24.com/24/goods/25138160?scode=032&OzSrank=6)
