

Program 1:

#include<iostream.h>
class Complex
{
int real, imaginary;
public:
void set (int rl, int img)
{
real = rl;
imaginary = img;
}
void show ()
{
cout<<real<<" + i"<<imaginary<<endl;
}
Complex add(Complex x, Complex y)
{
Complex temp;
temp.real = x.real + y.real;
temp.imaginary = x.imaginary + y.imaginary;
return temp;
}
Complex sub (Complex x, Complex y)
{
Complex temp;
temp. real = x.real - y.real;
temp. imaginary = x.imaginary - y.imaginary;
return temp;
}
Complex mul(Complex x, Complex y)
{
Complex temp;
/* Formula for multiplying complex numbers is (a + ib) (c + id) = (ac - bd) + i(ad+ bc).*/
temp.real = (x.real*y.real) - (x.imaginary*y.imaginary);
temp.imaginary = (x.real*y.imaginary) + (x.imaginary*y.real);
return temp;
}
Complex scalarmul(Complex x, int z)
{
	Complex temp;
	/* To multiply a complex number by a scalar, multiply the real part by the scalar and multiply the
	imaginary part by the scalar: c(a + bi) = ca t cbi, */
	temp.real = x.real*z;
	temp.imaginary = x.imaginary*z;
	return temp;
	}
};

int main ()
{
Complex c1,c2,c3;
c1.set(8,12) ;
c2.set(4,5) ;
cout<<endl<<"Result of complex addition:"<<endl;
c3 = c3.add (c1,c2) ;
c3.show() ;
cout<<endl<<"Result of complex subtraction:"<<endl;
c3 = c3.sub (c1,c2) ;
c3.show() ;
cout<<endl<<"Result of complex multiplication:"<<endl;
c3 = c3.mul (c1,c2) ;
c3.show () ;
cout<<endl<<"Result of complex multiplication with a scalar:"<<endl;
c3 = c3.scalarmul (c1,2) ;
c3.show ();
return 0;
}











Program 2:

#include<iostream.h> 
#include<math.h>
#include<conio.h>
class point
{
int x1,y1,x2,y2;
public:
void getvalue()
{
cout<<"\n Enter the value of (X1,X2) and (Y1,Y2):"; 
cin>>x1>>y1>>x2>>y2;
}
void display()
{
cout<<"\n First Coordinates:"<< x1<<"\t" << y1;
cout<<"\n Second Coordinates:"<< x2<<"\t" << y2;
}
void calculate()
{	
int a; float b;
a=(pow(x2-x1,2)+pow(y2-y1,2)); 
b=pow(a,0.5);
cout<<"\n Distance between point(X1,Y1) and (X2,Y2) is: "<<b << "\n\n";
}
void equal()
{
if((x1==x2)&&(y1==y2)) 
cout<<"\nBoth Points are Equal"; 
else
cout<<"\nBoth points are not Equal";
}
};
void main()
{
clrscr(); 
point p; 
p.getvalue(); 
p.calculate(); 
p.display();
p.equal();
getch();
}








Program 3:

#include <iostream.h> 
#include<conio.h> 
class HP
{
float i; 
int n;
long d,a1; 
float an; 
public:
void sum( )
{ 
S=0;
cout<<"Enter the value of n:"; 
cin>>n;
cout<<"1";
for(i = 1; i <= n; i++)
cout << " + 1/" << (int)i + 1; 
s = s + 1 / i;
cout<<"Sum is:"<<s;
}
void Nterm()
{
cout<<"\nEnter first term "; cin>>a1;
cout<<"\nEnter difference "; cin>>d;
cout<<"\nEnter nth term "; cin>>n;
cout<<n<<"th term of H.P. : "; an=a1+(n-1)*d; cout<<"1/"<<an<<" ";
}
};
int main()
{
HP h1;
h1.sum();
h1.Nterm();
getch();
return 0; 
}














Program 4:

#include<iostream.h>
#include<conio.h>
class Shapes
{
int type;
clrscr();
float d1, d2, d3;
float tsa, vol;
public:
void get()
{
cout<<"l. CUBE 2. CUBOID 3. SPHERE 4. EXIT \n Enter your option:";
cin>>type;
if (type==1)
f1();
else
if (type==2)
f2();
else
if (type==3)
f3();
else
cout<<"Give option as 1, 2, 3, 4 and try again \n";
}
void f1()
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
cout<<"Enter the length, width and height of the cuboid:";
cin>>d1>>d2>>d3;
tsa=2*(d1*d2+d2*d3+d1*d3);
vol=d1*d2*d3;
cout<<"Total Surface Area of the Cuboid="<<tsa<<endl;
cout<<"Volume of the cuboid="<<vol<<endl;
}
void f3()
{
cout<<"Enter the radius of the sphere:";
cin>>d1;
tsa=4*3.14*d1 *d1;
vol=4/3*3.14*d1 *d1 *d1;
cout<<"Total Surface Area of the cuboid="<<tsa<<endl;
cout<<"Volume of the cuboid="<<vol<<endl;
}
};

int main()
{
Shapes s;
s.get();
getch();
return 0;
}










Program 5:

#include <iostream.h>
class Time {
private:
int hours, minutes, seconds;
public: // function to set time
void setTime(int h, int m, int s) {
hours = h;
minutes = m;
seconds = s;
}
void showTime() {
cout << hours << ":" << minutes << ":" << seconds <<
endl;
} // function to find difference between two time objects
Time difference(Time t) {
int diffSecs = 0, diffMins = 0, diffHrs = 0;
// calculate difference in seconds
if(seconds < t.seconds) {
diffSecs = t.seconds - seconds; --minutes;
} else { diffSecs = seconds - t.seconds;
} // calculate difference in minutes
if(minutes < t.minutes) {
diffMins = t.minutes - minutes; --hours;
} else { diffMins = minutes - t.minutes;
} // calculate difference in hours diffHrs = hours -
t.hours;
// return the difference time object
Time diffTime;
diffTime.setTime(diffHrs, diffMins, diffSecs);
return diffTime;
} // function to convert time object to seconds
int toSeconds() {
return hours * 3600 + minutes * 60 + seconds;
}
};
int main() {
Time t1, t2, diff;
t1.setTime(13, 34, 55);
t1.showTime();
// outputs: 13:34:55
t2.setTime(8, 12, 15);
t2.showTime();
// outputs: 8:12:15
diff = t1.difference(t2);
diff.showTime();
// outputs the difference time
cout << "Difference in seconds: " << diff.toSeconds() <<
endl;
return 0;
}










Program 6:

#include<iostream.h> 
#include<conio.h> 
class mat 
 { 
       private: 
                     int s[10][10]; 
                     int u,v; 
       public: 
                     void show(); 
                     mat operator +(mat); 
                     mat operator *(mat); 
                     void read(); 
 }; 
            mat mat::operator+(mat uu2) 
       { 
                mat t; 
                t.u=u; 
                t.v=v; 
                cout<<t.u; 
                cout<<t.v; 
                for(int i=0;i<t.u;i++) 
                     for(int j=0;j<t.v;j++) 
                          t.s[i][i]=s[i][i]+uu2.s[i][i]; 
                          return t; 
       } 
           mat mat::operator*(mat uu2) 
      { 
                mat t; 
                t.u=u; 
                t.v=uu2.v; 
                for(int i=0;i<t.u;i++) 
                     for(int j=0;j<t.v;j++) 
                         { 
                            t.s[i][i]=0; 
                            for(int k=0;k<v;k++) 
                                   t.s[i][j]+=s[i][k]*uu2.s[k][j]; 
                         } 
                                   return t; 
        } 
            void mat::read() 
        { 
               cout<<"Enter Size of Matrix like 3 x 3:\n"; 
               cin>>u>>v; 
               cout<<"Enter the Elements of Matrix :\n"; 
               for(int i=0;i<u;i++) 
                    for(int j=0;j<v;j++) 
                        cin>>s[i][j]; 
      } 
              void mat::show() 
      { 
              for(int i=0;i<u;i++) 
                   { 
                   for(int j=0;j<v;j++) 
                        { 
                              cout<<s[i][j]<<"\t"; 
                              
                         } 
                              cout<<"\n"; 
                   } 
      } 
              void main() 
      { 
                 mat obj1 ,obj2,obj3; 
                 clrscr(); 
                 cout<<"Enter First Matrix\n"; 
                 obj1.read(); 
                 cout<<"Enter Second Matrix\n"; 
                 obj2.read(); 
                 obj3=obj1 +obj2; 
                 cout<<"Result After Addition of two Matrix\n"; 
                 obj3.show(); 
                 obj3=obj1 *obj2; 
                 cout<<"Result After Multiplication of two Matrix\n"; 
                 obj3.show(); 
                 getch(); 
      }













OUTPUT:





  


Program 7:

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








OUTPUT:
























Program 9:

#include<iostream>
using namespace std;

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
st-calculate_area();
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




PROGRAM 11:

#include <iostream.h> 
#include<conio.h> 
#include <vector.h> 
void main()
{
clrscr(); 
vector<int> a; 
int num,n,len; 
a.push_back(10); 
a.push_back(20); 
a.push_back(30); 
a.push_back(40); 
a.push_back(50);
cout << "The elements of Vector are "; 
for (int i = 0; i < a.size(); i++)
 cout<<a[i]<<endl;
cout<<"Size of Vector:";
 cout<<a.size();
cout<<"\n The First Element is " <<a.front(); 
cout << "\nThe Last Element is " << a.back(); 
a.pop_back();
cout<<"\n After deleting Last Element"; 
cout << "\n The vector contains \n";
for (int i = 0; i < a.size(); i++) 
cout << a[i] <<endl;
cout<<"\n After Insering Element"; 
a.insert(a.begin(), 3);
for (int i = 0; i < a.size(); i++) 
cout << a[i] << " ";
cout<<"\n After Deleting First Element \n"; 
a.erase(a.begin());
for (int i = 0; i < a.size(); i++) 
cout << a[i] <<endl;
getch();
}












OUTPUT:





