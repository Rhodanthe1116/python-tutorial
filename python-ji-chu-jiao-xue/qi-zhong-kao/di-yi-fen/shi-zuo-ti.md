# 實作題

## 流程控制 作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d584" %}

照著題目好好做就可以拿到分數，但題目較複雜，可能會花比較多的時間看題目。

```python
import sys
for ss in sys.stdin:
    role, level = map(int, ss.split())
    point = 0

    # level up
    if level > 10 and role is not 0:
        point += 3 * (level - 10)
    if role is 2 and level > 8:
        point += 3 * (min(level, 10) - 8)

    # upgrade role
    if role is not 0:
        if level >= 8 and role is 2:
            point += 1
        if level >= 10 and role is not 2:
            point += 1
        if level >= 30:
            point += 1
        if level >= 70:
            point += 1
        if level >= 120:
            point += 3

    print(point)
```

## list 作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d562" %}

考怎麼運用list的操作，可以用內建函數，也可以自己用for跑，如果寫過的話不會花太多時間。

```python
import sys
for ss in sys.stdin:
    n = int(ss)
    l = list(map(int, input().split()))

    print(*l)
    
    for _ in range(n-1):
        l.reverse()
        l.pop()
        print(*l)
```

## 字串處理

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e975" %}

字串處理，需要熟悉內建函數如len\(\), find\(\), ord\(\), chr\(\), isalpha\(\), 字串拼接等，和判斷邊界條件，需要注意Python不像C++一樣可以用=來指定字串中的字元，也不能直接對字元做加減。

```python
import sys
for encoded_letter in sys.stdin:

    k = 0
    while True:
        is_love_found = encoded_letter.find('love') != -1 or \
            encoded_letter.find('Love') != -1
        if is_love_found:
            break
        else:
            decoded_letter = ''
            for char in encoded_letter:
                if char.isalpha():
                    decoded_char = chr(ord(char) + 1)
                    if decoded_char == chr(ord('z') + 1):
                        decoded_char = 'a'
                    elif decoded_char == chr(ord('Z') + 1):
                        decoded_char = 'A'
                    decoded_letter += decoded_char
                else:
                    decoded_letter += char
            encoded_letter = decoded_letter
            k += 1
    print(k)
```

## list 二進位

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e799" %}

需要有二進位的觀念，其他照著做即可，主要要花時間處理進位轉換。

```python
import sys
for input_string in sys.stdin:
    n, m = map(int, input_string.split())
    symbol = input()

    for _ in range(n):
        num = int(input())

        binary_num = [0] * m
        for i in range(m):
            if (num % 2 == 1):
                binary_num[-i-1] = 1
            num = int(num / 2)

        for digit in binary_num:
            if digit == 0:
                print('.', end=' ')
            elif digit == 1:
                print(symbol, end=' ')
        print()

```

