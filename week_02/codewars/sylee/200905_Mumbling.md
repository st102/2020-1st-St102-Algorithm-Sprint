# Mumbling

## ��������

> ���� ���ڿ����� ù��° ���ڴ� 1��, �ι�° ���ڴ� 2��, ... , n��° ���ڴ� n���� ����Ѵ�.
>
> ��, n���� ù��°�� �빮�ڷ� ����Ѵ�.



## ���� Ǯ�� ���

 ```python
def accum(string):
    return "-".join(string[i].upper()+string[i].lower()*i for i in range(len(string)))
 ```

> ó�� Ǯ���̴�.  �̹� ������ ���ڿ��� ��ҿ� �ε��� ���� ���� �޴´ٸ� �� ����ϰ� © �� ���� �� ���Ҵ�.



```python
def accum(string):
    return "-".join(
        element.upper() + element * index
        for index, element in enumerate(string.lower())
    )
```

> ��ҿ� �ε����� ���� ��ȯ���ִ� `enumerate()`�� ����Ͽ� Ǯ����.




## �ٸ� ����� Ǯ�� ���

```python
# Best Practices
def accum(s):
    return '-'.join(c.upper() + c.lower() * i for i, c in enumerate(s))
```

> �� Ǯ�̿� ����ϴ�. �ƽ��� ���� `i, c`�� ������ �̸��� �ܹ��� �����ϱ� ��ƴ�.



```python
# Clever
def accum(s):
    return '-'.join((a * i).title() for i, a in enumerate(s, 1))
```

> ù ���ڸ� �빮�ڷ� ������ִ� `title()`�� �̿��Ͽ� Ǯ����.  ���п� �� ����� ���δ�.
>
> `enumerate(s,1)`�� ����Ͽ� �ε��� ������ `0`�� �ƴ� `1`�� �����ϴ� ���� ���Ҵ�.



## ��� ��

>  �ٸ� Ǯ�̵��� ���ٰ� `capitalize()` ��� �޼ҵ带 ���Ҵ�. `title()`���� ��������� �ٸ���.



>  `title()` : **��** �ܾ��� ù���ڸ� �빮�ڷ� �ٲ��ش�.
>
>  - Ex)	`python` => `Python` ,	`hello python` => `Hello Python`



>  `capitalize()` : ù ���ڸ� �빮�ڷ� �ٲپ��ش�. ( => ù ����**��** �빮�ڷ� ����Ѵ�.)
>
>  - Ex)	`python` => `Python` ,	`hello Python` => `Hello python`, 



## �ݼ��� ��

> Ư���� ������ �� ����.



## Action Item

> ���̽��� �پ��� method�� �ִ� �� ����. ����� ����̾ ���̰� �ִ�.
>
> �� �����ؼ� ����.

