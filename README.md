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

#include <iostream>
using namespace std;

class Complex {
    int real, imaginary;
public:
    void set(int rl, int img) {
        real = rl;
        imaginary = img;
    }
    void show() {
        cout << real << " + " << imaginary << "i" << endl;
    }
    Complex add(Complex x, Complex y) {
        Complex temp;
        temp.real = x.real + y.real;
        temp.imaginary = x.imaginary + y.imaginary;
        return temp;
    }
    Complex sub(Complex x, Complex y) {
        Complex temp;
        temp.real = x.real - y.real;
        temp.imaginary = x.imaginary - y.imaginary;
        return temp;
    }
    Complex mul(Complex x, Complex y) {
        Complex temp;
        temp.real = (x.real * y.real) - (x.imaginary * y.imaginary);
        temp.imaginary = (x.real * y.imaginary) + (x.imaginary * y.real);
        return temp;
    }
    Complex scalarmul(Complex x, int z) {
        Complex temp;
        temp.real = x.real * z;
        temp.imaginary = x.imaginary * z;
        return temp;
    }
};

int main() {
    Complex c1, c2, c3;
    c1.set(8, 12);
    c2.set(4, 5);

    cout << "Result of complex addition:" << endl;
    c3 = c3.add(c1, c2);
    c3.show();

    cout << "\nResult of complex subtraction:" << endl;
    c3 = c3.sub(c1, c2);
    c3.show();

    cout << "\nResult of complex multiplication:" << endl;
    c3 = c3.mul(c1, c2);
    c3.show();

    cout << "\nResult of complex multiplication with a scalar:" << endl;
    c3 = c3.scalarmul(c1, 2);
    c3.show();

    return 0;
}






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
