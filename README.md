# copy-constructor
#include<iostream>
using namespace std;
class code{
    int a,b;
    public:
    code()
    {
        a=30;
        b=60;
       
    }
    code(code &i);
    void display(void)
    {
    cout<<"a="<<a<<"b="<<b; 
    }
};
 code::code(code &i)
 {
     a=i.a;
     b=i.b;
 }
 
    int  main()
 {
     code c1,c2(c1);
     cout<<"First object"<<endl;
     c1.display();
     cout<<"Second object"<<endl;
     c2.display();
     cout<<"Third object"<<endl;
     code c3=c2;
     c3.display();
     return 0;
 }
