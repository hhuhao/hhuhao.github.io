### Important

Bit is a good alogrithm.

### Problem

#### Description

Give you some operate.

$0\ l\ r\ w\ \ \  $:$f_{l..r}+=w$

$1\ x\ \ \ \ \ \ \ \ $:Ask $f_x$

#### Sample:

```
Input:
10 10
0 2 8 5
1 7
1 2
0 3 9 8
1 7
1 3
1 5
1 5
0 1 5 6
1 2
Output:
5
5
13
13
13
13
11
```

#### Constraints

|  Data   |   n    |   m    |
| :-----: | :----: | :----: |
| $1..3$  | $10^3$ | $10^3$ |
| $4..10$ | $10^5$ | $10^5$ |

#### Solution

$0$:

```c++
add(l,w);
add(r+1,-w);
```

$1$:

```c++
query(x);
```

#### Code

```c++
int bit[100010],n,t,l,r,h;
void add(int x,int y)
{
	while(x<=n)
	{
		bit[x]+=y;
		x+=x&(-x);
	}
}
int query(int x)
{
	int r=0;
	while(x)
	{
		r+=bit[x];
		x-=x&(-x);
	}
	rt r;
}
int main(){
	n=read();
	t=read();
	while(t--)
		if(!read())
		{
			l=read(),r=read(),h=read();
			add(l,h);
			add(r+1,-h);
		}
		else
			printf("%d\n",query(read()));
	rt 0;
}
```

