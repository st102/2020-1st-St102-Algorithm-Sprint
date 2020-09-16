# Take a Ten Minute Walk

## ��������

> �� ������ ��Ÿ���� ���ĺ� n,s,w,e �� �־����� �� ���ĺ����� ���� 10�̸鼭 �̵� �� �������� ���ԵǸ� True �ƴϸ� False�� �����ϴ� �Լ��� �����

## ���� Ǯ�� ���

 ```python
import unittest


def is_valid_walk(walk):
    return (
        True
        if len(walk) == 10
        and walk.count("s") == walk.count("n")
        and walk.count("e") == walk.count("w")
        else False
    )


class MyTestCase(unittest.TestCase):
    def test_length_is_not_ten(self):
        self.assertEqual(
            is_valid_walk(["w", "e", "w", "e", "w", "e", "w", "e", "w", "e", "w", "e"]),
            False,
        )

    def test_length_is_ten(self):
        self.assertEqual(
            is_valid_walk(["n", "s", "n", "s", "n", "s", "n", "s", "n", "s"]), True
        )
        self.assertEqual(
            is_valid_walk(["w", "e", "w", "e", "w", "e", "w", "e", "w", "e"]), True
        )
        self.assertEqual(
            is_valid_walk(["w", "e", "s", "s", "s", "e", "e", "e", "w", "e"]), False
        )

 ```

> 1. ������ ������ 10�� �ƴҶ�	-	False
> 2. ������ ������ 10�϶�
>    - �̵� �� ������ ��	-	True
>    - �̵� �� ������ �ƴ� �� 	-	False

> ���� ���� ��Ŀ�������� �׽�Ʈ ������ ���ߴ�. 




## �ٸ� ����� Ǯ�� ���

```python
# Best Practices 1
def isValidWalk(walk):
    return len(walk) == 10 and walk.count('n') == walk.count('s') and walk.count('e') == walk.count('w')
```

> ���� ���� ��������� ��������  `And`���� ��ü�� `True`, `False`�� ��ȯ�ߴ�.



## ��� ��

>  ������ ����, ���� ��ü�� True, False�� ��ȯ�ϱ�.



## �ݼ��� ��

> Ư���� �ݼ� �� ���� ���� �� ����.



## Action Item

> TDD, �׽�Ʈ�ڵ�