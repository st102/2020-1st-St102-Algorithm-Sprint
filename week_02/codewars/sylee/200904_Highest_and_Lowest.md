# Highest and Lowest

## ��������

> ���� ���ڿ� �� ũ�Ⱑ ���� ū ������ ���� ���� ������ ���ʷ� ����Ѵ�.

## ���� Ǯ�� ���

 ```python
def high_and_low(numbers):
    list_of_number = [x for x in numbers.split()]
    return "{} {}".format(max(list_of_number), min(list_of_number))
 ```

> ó�� Ǯ���̴�. �� ����� ���� ���� �ϴ� �� �;��µ�, �׽�Ʈ���̽��� ����� ���ߴ�.
>
> "4 5 29 54 4 0 -214 542 -64 1 -3 6 -6" ���� ����� '6 -214'�� ���Դ�.
>
> ����Ʈ�� ������ �� string type���� ������ �ż� 542 ���� 6�� �� �Ǵ� ���̴�.



```python
def high_and_low(numbers):
    list_of_number = [x for x in map(int, numbers.split())]
    return "{} {}".format(max(list_of_number), min(list_of_number))
```

> map�� �̿��Ͽ� �����ߴ�.




## �ٸ� ����� Ǯ�� ���

```python
# Best Practices 1
def high_and_low(numbers):
    nn = [int(s) for s in numbers.split(" ")]
    return "%i %i" % (max(nn),min(nn))
```

> ���� ����� Ǯ���̴�.



```python
# Best Practices 2
def high_and_low(numbers):
  return " ".join(x(numbers.split(), key=int) for x in (max, min))
```

> for���� �̿��� �Լ��� ���� ���� �� �ִٴ� ���� �˰� �ƴ�.

> `return " ".join(x(numbers.split(), key=int) for x in (max, min))` ���ٴ�
>
> `return " ".join(function(numbers.split(), key=int) for function in (max, min))`�� �� ����.
>
> �׳� x �θ� �Ἥ ó���� ���ذ� �� �ȵƴ�.

> (����)       sort(), sorted() �� �ƴ� max,min���� key����� �����Ѱ���?



## ��� ��

>  for���� ���� �Լ����� �ޱ�, sorted() �� ���� ���� �˰� �ƴ�.
>
>  key�� ����.



## �ݼ��� ��

> ��ȯ��(type) �� �����ϸ� Ǯ��� �Ѵ�. (Ʋ�� ������ ã�µ� �� �ɷȴ�.)



## Action Item

> �پ��� ��� �����غ���, type �����ؼ� Ǯ��

