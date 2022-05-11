# stack-operations
#include<iostream.h>
#include<conio.h>
class arr
{
	int a[10],n;
	public:
	void get();
	void sort();
	void display();
	
};
void arr::get()
{
	cout<<"enter size of array"<<endl;
	cin>>n;
	cout<<"enter array elements "<<endl;
	for(int i=0;i<=n;i++)
	{
		cin>>a[i];
	}
	cout<<"Elements are"<<endl;
	for(int j=0;j<=n;j++)
	{
		cout<<a[j]<<"  "<<endl;
	}
	cout<<endl;
}
void arr::sort()
{
	for(int j=1;j<=n;j++)
	{
		int temp=a[j];
		int k=j-1;
		while(k>=0 && a[k]>temp)
		{
			a[k+1]=a[k];
			k--;
		}
		a[k+1]=temp;
	}
}
void arr::display()
{
	cout <<"Sorted Element List ...\n";
for(int i = 0; i<=n; i++) 
{
   cout <<a[i]<<endl;
}

}


void main()
{
	clrscr();
	arr a;
	a.get();
	a.sort();
	a.display();
	getch();
}
Algorithm:
Puse. 
Procedure: PUSH (STACK,TOP,MAX,ITEM)
 //This procedure pushes an ITEM onto stack.
1.	[Stack already full]
 If TOP=MAX, then Print: UNDERFLOW, and Return.
2.	Set TOP: =TOP+1 [Increase TOP by 1]
3.	SetSTACK [TOP]:=ITEM. [Insert ITEM in new TOP position]
4.	Return.

5)pop
Procedure: POP (STACK,TOP,ITEM)
 //This procedure Deletes the top element of STACK and assigns it to the variable ITEM.
1.	[Stack Empty or Not]
 If TOP=0, then Print: OVERFLOW, and Return.
2.	Set ITEM: =STACK [TOP]. [Assigns Top element to ITEM] 
3.	Set TOP: =TOP-1 [Decrease TOP by 1]
4.	Return.
