# Exercises

## Question 1

Write a program that prints all solutions to the quadratic equation $ax^2+bx+c=0$. Remember that the solutions are: $$\frac{-b+\sqrt{b^2-4ac}}{2a}$$ and $$\frac{-b-\sqrt{b^2-4ac}}{2a}$$ Read in $a$, $b$, $c$ and use the quadratic formula. If the discriminant $b^2−4ac$ is negative, display a message stating that there are no solutions.
#### Note: The solution here is more than what the question asks
### Solution
```c++
#include <iostream>
#include <cmath>
using namespace std;

int main() {

    float a, b, c, x1, x2, discriminant, realPart, imaginaryPart;
    cout << "Enter coefficients a, b and c: ";
    cin >> a >> b >> c;
    discriminant = b*b - 4*a*c;
    
    if (discriminant > 0) {
        x1 = (-b + sqrt(discriminant)) / (2*a);
        x2 = (-b - sqrt(discriminant)) / (2*a);
        cout << "Roots are real and different." << endl;
        cout << "x1 = " << x1 << endl;
        cout << "x2 = " << x2 << endl;
    }
    
    else if (discriminant == 0) {
        cout << "Roots are real and same." << endl;
        x1 = -b/(2*a);
        cout << "x1 = x2 =" << x1 << endl;
    }

    else {
        realPart = -b/(2*a);
        imaginaryPart =sqrt(-discriminant)/(2*a);
        cout << "Roots are complex and different."  << endl;
        cout << "x1 = " << realPart << "+" << imaginaryPart << "i" << endl;
        cout << "x2 = " << realPart << "-" << imaginaryPart << "i" << endl;
    }

    return 0;
}
```
Output
```
Enter coefficients a, b and c: 4
5
1
Roots are real and different.
x1 = -0.25
x2 = -1
```

## Question 2

Write a program that asks the user to enter a month (1 for January, 2 for February, and so on) and then prints the number of days in the month. For February, print “28 or 29 days”.
```
Enter a month: 5
30 days
```

## Question 3

Write a program that takes user input describing a playing card in the following shorthand notation:
```
A         - Ace
2 ... 10  - Card Values
J         - Jack
Q         - Queen
K         - King
D         - Diamond
H         - Hearts
S         - Spades
C         - Clubs
```
Your program should print the full description of the card. For example,
```
Enter the card notation: QS
Queen of spades
```
