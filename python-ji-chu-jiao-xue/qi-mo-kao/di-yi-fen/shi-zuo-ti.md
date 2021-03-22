# 實作題

## class, sort

{% embed url="https://zerojudge.tw/ShowProblem?problemid=a362" %}

```python
class S:
    id = 0
    h = 0
    w = 0
    
n = int(input())
l = []
for i in range(n):
    h, w = map(int, input().split())
    s = S()
    s.id = i
    s.h = h
    s.w = w
    l.append(s)
sl = sorted(l, key=lambda s: (s.h, s.w))

sum = 0
for i in range(n):
    sum += abs(i - sl[i].id)
print(sum)
```

## 簡單dict

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e839" %}

```python
import sys
for input_string in sys.stdin:
    n = int(input_string)
    food = {}
    for _ in range(n):
        food_name, food_type = input().split()
        if food_type in food:
            food[food_type].append(food_name) 
        else:
            food[food_type] = [food_name]
    search_type = input()
    if search_type in food:
        for output_food in sorted(food[search_type]):
            print(output_food)
    else:
        print('No')
```



## 字串處理 非作業

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

## 二維list 非作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=e798" %}

```cpp
#include<stdio.h>

int main()
{	
	int n = 0;
	scanf("%d", &n);

	int Image[25][25]={};
	for( int i=0; i<n; i+=1 )
	{
		for( int j=0; j<n; j+=1 )
		{
			scanf("%d",&Image[i][j]);
		}
	}

	int Max_Pooling[25][25]={};
	for( int i=0; i<n; i+=2 )
	{
		for( int j=0; j<n; j+=2 )
		{
			int Max = 0;
			
			if( Image[i][j] > Max )
				Max = Image[i][j];
			if( Image[i][j+1] > Max )
				Max = Image[i][j+1];
			if( Image[i+1][j] > Max )
				Max = Image[i+1][j];
			if( Image[i+1][j+1] > Max )
				Max = Image[i+1][j+1];

			Max_Pooling[i/2][j/2] = Max;
		}	
	}

	for( int i=0; i<n/2; i+=1 )
	{
		for( int j=0; j<n/2; j+=1 )
		{
			printf("%d ", Max_Pooling[i][j]);
		}
		printf("\n");
	}

	return 0;
}


```

