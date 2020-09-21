# Tribonacci Sequence

## ��������

> n��° ���� n-3, n-2, n-1��° ���� ���̴�.  ���� ������ �־�����.

## ���� Ǯ�� ���

 ```python
import unittest


def tribonacci(signature, n):
    list_tribonacci = signature
    if n < 4:
        return signature[:n]
    else:
        for i in range(3, n):
            list_tribonacci.append(sum(list_tribonacci[-3:]))
        return list_tribonacci


class TestTribonacci(unittest.TestCase):
    def test_signature_is_111(self):
        self.assertEqual(tribonacci([1, 1, 1], 10), [1, 1, 1, 3, 5, 9, 17, 31, 57, 105])

    def test_signature_is_000(self):
        self.assertEqual(tribonacci([0, 0, 0], 10), [0, 0, 0, 0, 0, 0, 0, 0, 0, 0])

    def test_when_n_is_1(self):
        self.assertEqual(tribonacci([1, 1, 1], 1), [1])

    def test_when_n_is_0(self):
        self.assertEqual(tribonacci([300, 200, 100], 0), [])

 ```

> �ñ״��� 2 ������ ���� �׽�Ʈ �ϰ�
>
> n �� 1 �϶��� 2�϶� �ΰ��� ��쿡 ���� �׽�Ʈ �غ��Ҵ�.




## �ٸ� ����� Ǯ�� ���

```python
# Best Practices 1
def tribonacci(signature, n):
  res = signature[:n]
  for i in range(n - 3): res.append(sum(res[-3:]))
  return res
```

> n�� ũ�⿡ ���� �˻��� �ʿ䰡 ���ٴ� �� �����.
>
> �� �� n�� 3 �̻��̸� `n-3`�� ��ŭ�� �ڿ� �߰����־���.



## ��� ��

>  index�� �� Ȱ���ϸ� ���ʿ��� �˻縦 ���� �� �ִ�.



## �ݼ��� ��

> �����丵 ������ �����ߴ�.



## Action Item

> indexȰ��