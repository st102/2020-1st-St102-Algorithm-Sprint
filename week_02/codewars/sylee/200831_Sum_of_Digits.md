# Create Phone Number

## ��������

> 10���� ������ �޾� (xxx) xxx-xxxx�� ���·� ����ϱ�

## ���� Ǯ�� ���

 ```python
def create_phone_number(n):
    return "({}{}{}) {}{}{}-{}{}{}{}".format(*n[:10])
 ```

> ���� ����� *args�� �̿��� Ǯ����.




## �ٸ� ����� Ǯ�� ���

```python
# Best Practices 1
def create_phone_number(n):
    return "({}{}{}) {}{}{}-{}{}{}{}".format(*n)
```

> �� Ǯ�̿� ���� ����ϴ�.



```python
def create_phone_number(n):
    n = "".join([str(x) for x in n] )
    return("(" + str(n[0:3]) + ")" + " " + str(n[3:6]) + "-" + str(n[6:]))
```

> �б� ���� �ڵ��� �� ����. ���ڿ��� ������ �� �ǵ��� `+` ����� ���� �ؾ߰ڴ�.



## ��� ��

>  *args�� ���Ҿ� **kwargs�� �� �˾ƺ���



## �ݼ��� ��

> Ư���� ���ٰ� �����Ѵ�.

## Action Item

> ���ڵ��� ������ �������� ì�ܰ��� ���� �� ����.