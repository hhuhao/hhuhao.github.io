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

