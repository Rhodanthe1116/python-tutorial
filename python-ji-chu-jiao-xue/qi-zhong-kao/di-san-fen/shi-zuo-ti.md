# 實作題

## 流程控制 作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=a006" %}

基本的流程控制

```cpp
#include<iostream>
#include<math.h>
using namespace std;
int main()
{
	int a,b,c;
	float x1,x2,temp;
	
	while(cin>>a>>b>>c)
	{
		if(b*b-4*a*c>0)
		{
			temp=sqrt(b*b-4*a*c);
			x1=(-b+temp)/(2*a);
			x2=(-b-temp)/(2*a);
			cout<<"Two different roots x1="<<x1<<" , x2="<<x2<<endl;
		}
		else if(b*b-4*a*c==0)
		{
			temp=sqrt(b*b-4*a*c);
			x1=(-b)/(2*a);
			cout<<"Two same roots x="<<x1<<endl;
		}
		else
		{
			cout<<"No real root"<<endl;
		}
	}
}
```



## list 作業

{% embed url="https://zerojudge.tw/ShowProblem?problemid=d573" %}

考list對資料處理的基本操作，和面對不同數量級測資。

```python
import sys
for inputString in sys.stdin:
    n = int(inputString)
    groupOfKnight = [0] * (100000 + 1)
    for _ in range(n):
        newLine = list(map(int, input().split()))
        groupNumber = newLine[0]
        p = newLine[1]
        knights = newLine[2:]

        for knight in knights:
            groupOfKnight[knight] = groupNumber
            
    y = int(input())
    print(groupOfKnight[y])
```

