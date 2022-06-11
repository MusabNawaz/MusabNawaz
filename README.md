#include<iostream>
using namespace std;
class stack
{
	private:
		int top;
		int S[10];
		
	public:
		stack()
		{
			top=-1;
		}
	
	push(int n)
	{
		if(top==9)
		{
			cout<<"Stack Overflow";
		}
		else
		{
			top++;
			S[top]=n;
		}
		
	}
	
	int pop()
	{
		int data;
		if(top==-1)
		{
			cout<<"Stack is empty";
		}
		else
		{
			data = S[top];
			top--;	
		}
		
		return data;
	}
	
	print()
	{
		if(top==-1)
		{
			cout<<"stack is empty\n";
		}
		else
		{
			for(int i=top; i>=0; i--)
			{
				cout<<S[i]<<endl;
			}
		}
	}
};

int main()
{
	stack obj;
	int opt, val;
	while(opt!=3)
	{
		cout<<"1 PUSH\n2 POP\n3 Exit\n";
		cout<<"Enter the choice";
		cin>>opt;
		
		switch(opt)
		{
			case 1:
				system("CLS"); // To clear the screen.
				cout<<"Enter value to insert";
				cin>>val;
				obj.push(val);
				cout<<"Stack after insertion\n";
				obj.print();
				break;
			case 2:
				system("CLS"); // To clear the screen.
				cout<<"Value "<<obj.pop()<<" is popped\n";
				cout<<"Stack after deletion\n";
				obj.print();
				break;
		}
		
	}
}
//Code by HammadMaqbool
