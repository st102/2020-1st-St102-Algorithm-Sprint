# Find the next perfect square!

## ��������

> ������ �ϳ� �޾� �������� ��ȯ���� ��, 1�� ������ ��ȯ

 ```python
import math


def find_next_square(sq):
    root = math.sqrt(sq)
    return -1 if root % 1 else (root + 1) ** 2


class TestFindNextSquare(unittest.TestCase):
    def test_not_perfect_square(self):
        self.assertEqual(find_next_square(111), -1)

    def test_perfect_sqaure(self):
        self.assertEqual(find_next_square(121), 144)
 ```

> ������ ���ϴ� �޼ҵ� `sqrt()`�� ����ߴ�.




## �ٸ� ����� Ǯ�� ���

```python
# Best Practices 1
def find_next_square(sq):
    root = sq ** 0.5
    if root.is_integer():
        return (root + 1)**2
    return -1.
```



```python
# Best Practices 2
def find_next_square(sq):
    x = sq**0.5    
    return -1 if x % 1 else (x+1)**2
```

> �� �ΰ����� ���ļ�
>
> ```python
> def find_next_square(sq):
>     x = sq**0.5    
>     return (x+1)**2 if x.is_integer() else -1
> ```
>
> �̷��� ����� ���� �� ����.





## ��� ��

>  `is_integer()`�޼ҵ带 �˰� �Ǿ���.



## �ݼ��� ��

> Ư���� �����ٰ� �����Ѵ�.



## Action Item

> .

