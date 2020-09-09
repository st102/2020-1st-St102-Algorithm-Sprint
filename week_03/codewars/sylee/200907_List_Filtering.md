# List Filtering

## ��������

>  ������ ���ڰ� ���� ����Ʈ�� �־�����, �������� ������ ����Ʈ�� ����Ѵ�.

## ���� Ǯ�� ���

 ```python
# ���� 1
import unittest


def filter_list(l):
    return l


class TestFilter(unittest.TestCase):
    def test_should_fail_when_given_only_int(self):
        self.assertEqual(filter_list([1, 2, 3]), [1, 2, 3])
 ```

> ù ��°�� ����(integer)�� ������ ��츦 �׽�Ʈ�Ѵ�. (`self.fail`�� �����ߴ�.)

- RED

  - ```python
    def filter_list(l):
        return
    ```

  - ���� ����� ���з� ���Դ�.

- GREEN

  - ```python
    def filter_list(l):
        return l
    ```

  - ���� ��� ������ ���Դ�.

- REFATOR

  - Ư���� �����丵 ������ ����.



```python
# ���� 2 (����)
import unittest


def filter_list(l):
    return [element for element in l if type(element) == type(1)]


class TestFilter(unittest.TestCase):
    def test_should_fail_when_given_only_int(self):
        self.assertEqual(filter_list([1, 2, 3]), [1, 2, 3])

    def test_should_fail_when_given_int_with_string(self):
        self.assertEqual(filter_list([1, "2", 3]), [1, 3])
```

>�� ��°�� ������ ���ڰ� ���� ����Ʈ�� �־� ������ ��� ����Ʈ�� ��µž� �Ѵ�.

- RED

  - ```python
    def filter_list(l):
        return l
    ```

  - ���� ����� ���з� ���Դ�.

- GREEN

  - ```python
    def filter_list(l):
        return return [element for element in l if type(element) == type(1)]
    ```

  - ���� ��� ������ ���Դ�.

- REFATOR

  - Ư���� �����丵 ������ ���ٰ� �����ߴ�.






## �ٸ� ����� Ǯ�� ���

```python
# Best Practices 1
def filter_list(l):
    return [i for i in l if not isinstance(i, str)]
```

> `isinstance()`�޼ҵ带 �˰� �Ǿ���.
>
> �ٵ� `return [i for i in l if isinstance(i, int)]` �� �ϸ� �� �������̰� �����Ѱ� �ƴѰ�?
>
> > `str�� �ƴϸ� �ִ´�` ���ٴ� ` int�̸� �ִ´� `�� �� �������ΰ� ����.



```python
# Best Practices 2
def filter_list(l):
  return [x for x in l if type(x) is not str]
```

> `A is B`������ �ذ� �־���. ��� �� �ڵ忡�� `if type(element) == type(1)`�� �˻��ϴ� �� ����
>
> `if type(x) is not str`�� �ϴ� ���� �� ����.
>
> ������ �� ���õ� `if type(x) is int`�� �� ����.



## ��� ��

>  `A is B` => `True or False`

> `isinstance()`



## �ݼ��� ��

> �⺻ ���������� �ذ� �־���.



## Action Item

> TDD������� ��� �غ��� 