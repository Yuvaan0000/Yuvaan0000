- 👋 Hi, I’m @Yuvaan0000
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Yuvaan0000/Yuvaan0000 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

1.real number imagainary number program
#include <iostream.h>
class complex {
private:

double real;

double imag;

public:

complex(double r = 0, double i = 0): real(r), imag(i) {}

void getval() {

cout << "Enter the real: ";

cin >> real;

cout << "Enter the imaginary: ";

cin >> imag;

}

complex operator+(const complex& obj1) {

return complex(real + obj1.real, imag + obj1.imag); }

complex operator-(const complex& obj1) {

return complex(real - obj1.real, imag - obj1.imag); }

complex operator* (double scalar) {

return complex(real* scalar, imag * scalar); }

void print() {

cout << real << "+" << imag << "i" << endl; }

};

int main() {

complex num1, num2, add, sub, multi_num1,

multi_num2;

double scalar;

num1.getval();

num2.getval();

cout << "Enter the scalar: ";

cin >> scalar;

add=num1 + num2;

cout << "ADDITION: ";

add.print();

sub=num1 - num2;

cout << "SUBTRACTION: ";

sub.print();

cout << "MULTIPLICATION FROM NUM1: ";

multi_num1 = num1 * scalar;

multi_num1.print();

cout << "MULTIPLICATION FROM NUM2: ";

multi_num2 = num2* scalar;

multi_num2.print();

return 0;

}




program  5

#include <iostream.h>
#include <iomanip.h>
class Time
{
private:
long seconds;
int hh, mi, ss;
public:
void setTime (int h, int m, int s)
{
hh = h;
mi = m;
ss = s;
}
void displayTime (void)
{
cout<<"The time is = "<<setw (2) <<setfill ('0') <<hh<<":"
<<setw (2) <<setfill ('0') << mi<<":"
<<setw (2) <<setfill ('0') <<ss<<endl;
}
void converttoSeconds (void)
{
seconds  =hh* 3600 + mi * 60 + ss;
cout<<"Seconds = "<<seconds<<endl;
}
Time calculatetimedifference (Time t1, Time t2)
{
Time temp;
if(t2. ss> t1.ss);
{
--t1.mi;
t1.ss+= 60;
}
temp.ss = t1.ss - t2.ss; 
if(t2 .mi > t1.mi)
{
--t1.hh;
t1.mi += 60;
}
temp.mi = t1.mi-t2.mi;
temp.hh = t1.hh-t2.hh;
return temp;
}
void addduration (int secs)
{
hh = hh + secs / 3600;
mi = mi + (secs % 3600) / 60; 
ss = ss + (secs % 3600) % 60;
}
};
int main ()
{
Time T1, T2, Result;
T1.setTime (15, 15, 35);
T1.displayTime ();
T1.converttoSeconds ();
T2.setTime (10, 10, 20);
T2.displayTime ();
Result = Result. calculatetimedifference (T1, T2); // T1 - T2
Result.displayTime();
int seconds;
cout<<"Enter duration to be added in seconds: ";
cin>>seconds;
T2.addduration (seconds);
T2.displayTime ();
return 0;
}


C++ Program 4

#include<iostream.h>
#include<stdlib.h>
class Shapes
{
int type;
float d1,d2,d3;
float tsa, vol;
public:

void get ()
{
cout<<"1.CUBE 2. CUBOID 3. SPHERE 4. EXIT \n Enter your option:";
cin>>type;
if (type==1)
f1 () ;
else

if (type==2)
f2 () ;
else
if (type==3)
f3 () ;
else
if (type==4)
exit (0) ;
else
cout<<"Give option as 1,2, 3, 4 and try again \n";
}

void f1 ()
{
cout<<"Enter the side of the cone:";
cin>>d1;
tsa=6*d1 *d1;
vol=d1 *d1 *d1;
cout<<"Total Surface Area of the cone="<<tsa<<endl;
cout<<"Volume of the cone="<<vol<<endl;
}

void f2()
{
cout<<"Enter the length, width, and height of the cuboid:";
cin>>d1>>d2>>d3;
tsa=2*(d1*d2+d2*d3+d1*d3);
vol=d1*d2*d3;
cout<<"Total Surface Area of the Cuboid="<<tsa<<endl;
cout<<"Volume of the cuboid="<<vol<<endl;
}

void f3 ()
{
cout<<"Enter the radius of the sphere:";
cin>>d1;
tsa=4*3.14*d1*d1;
vol=4/3*3.14*d1*d1 *d1;
cout<<"Total Surface Area of the cuboid="<<tsa<<endl;
cout<<"Volume of the cuboid="<<vol<<endl;
}
};

int main ()
{
Shapes s;
s.get () ;
return 0;
}


7th Program

#include<iostream.h>
class Cstring
{
char str[100];
public:
Cstring (Cstring&s) // copy constructor
{
int i;
for (i=0; s.str[i] != '\0'; i++){
str[i] = s.str[i];
}
str[i] ='\0';
}
Cstring(){};
void readstring()
{
cin>>str;
}
void display()
{
cout<<endl<<str<<endl;
}
int getlen()
{
int len;
for (len=0;str[len]!='\0'; len++);
return len;
}
void reverse()
{
int len;
for (len=0;str[len]!='\0';len++);
cout<<endl<<"The reverse of the string "<<str<<" is ";
for (int i=len;i>=0;i--)
cout<<str[i];
cout<<endl;
}
friend void concat (Cstring&s1, Cstring&s2)
{
int p;
for(p=0;s1.str[p] != '\0'; p++);// pointing to the index of the last // character of firststring
for(int q=0; s2.str[q] != '\0'; q++,p++)
{
s1.str[p]=s2.str[q];
}
s1.str[p]='\0';
}

void compare (Cstring&s)
{
int i=0, flag=0, difference;
while(str[i]!='\0' || s.str[i]!='\0')
{
if (str[i] !=s.str[i])
{
flag = 1;
break;
}
i++;
}
if (flag==0)
cout<< endl<<"String"<<str<<" and String "<<s.str<<" are Equal"<<endl;
else
cout<<endl<<"String "<<str<<" and String "<<s.str<<" are not Equal"<<endl;
}
};

int main()
{
Cstring mystring1;
int len;
cout<<"Enter a String:"<<endl;
mystring1.readstring();
cout<<"First string:"<<endl;
mystring1.display();
Cstring mystring2(mystring1); // copy constructor
Cstring mystring3(mystring2); // copy constructor
cout<<endl<<"Second string:"<<endl;
mystring2.display();
len = mystring1.getlen();
cout<<endl<<"Length of the string: "<<len<<endl;
mystring1.reverse();
cout<<endl<<"Concatenation of 2 strings is "<<endl;
concat (mystring1,mystring2);
mystring1.display();
mystring1.compare(mystring2);
mystring2.compare(mystring3);
return 0;
}


Program 9


#include<iostream.h>
class Shape
{

public: double a,b;
void get_data()
{
cin>>a>>b;
}
virtual void calculate_area () = 0;
};

class Triangle:public Shape
{
public: void calculate_area ()
{
cout<<"Area of triangle "<<0.5*a*b<<endl;
}
};
class Rectangle:public Shape
{
public: void calculate_area()
{
cout<<"Area of rectangle "<<a*b<<endl;
}
};
class Circle:public Shape
{
int radius;
public: void calculate_area()
{
cout<<endl<<"Enter radius:"<<endl;
cin>>radius;
cout<<"Area of Circle "<<3.14159 * radius * radius<<endl;
}
};
int main()
{
Triangle t;
Shape *st = &t;
cout<<"Enter base and altitude: ";
st->get_data();
st->calculate_area();
Rectangle r;
Shape *sr = &r;
cout<<"Enter length and breadth: ";
sr->get_data();

sr->calculate_area();
Circle c;
Shape *sc = &c;
sc->calculate_area();
return 0;
}





