# Stop gninnipS My sdroW!

## ��������

> ���� ���ڿ��� ���̰� 5�̻��� �ܾ�� �Ųٷ� ����� ����Ѵ�.

## ���� Ǯ�� ���

 ```python
def spin_words(sentence):
    words = sentence.split()
    return " ".join(
        [
            element if len(element) < 5 else "".join(list(reversed(element)))
            for element in words
        ]
    )


class Test_spin_words(unittest.TestCase):
    def test_length_of_word_is_less_than_five_when_given_only_one_word(self):
        self.assertEqual(spin_words("1234"), "1234")

    def test_length_of_word_is_five_or_above_when_given_only_one_word(self):
        self.assertEqual(spin_words("12345"), "54321")

    def test_length_of_word_is_less_than_five_when_given_more_than_one_word(self):
        self.assertEqual(spin_words("123 456 7890"), "123 456 7890")

    def test_length_of_word_is_five_or_above_when_given_more_than_one_word(self):
        self.assertEqual(spin_words("123 456 78910"), "123 456 01987")

 ```

> 1.  ���ڿ��� �ܾ� �ϳ��� ��
>    - ���̰� 5 ������ ��
>    - ���̰� 5 �̻��� ��
> 2.  ���ڿ��� �ܾ� �� �̻��� ��
>    - ��� �ܾ��� ���̰� 5 ������ ��
>    - �ܾ��� ���̰� 5�̻��� �ܾ ���� ��

>���� ���� �׽�Ʈ�� �����ߴ�.




## �ٸ� ����� Ǯ�� ���

```python
# Best Practices 1
def spin_words(sentence):
    return " ".join([x[::-1] if len(x) >= 5 else x for x in sentence.split(" ")])
```

> `x[::-1]`�� ����ߴ�. ���� `reversed()`�� ����� �ٽ� `list`�� ��ȯ�� �ʿ䰡 ������.



## ��� ��

>  index �̿��ϱ�.



## �ݼ��� ��

> �̹��� ������ �� ���� �� ����.



## Action Item

> 