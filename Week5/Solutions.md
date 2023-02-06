# Exercise

## Question 1
Write a program that prints the multiplication table for 1 to 10 using nested for loops
### Solution
```c++
#include <iostream>
using namespace std;
int main()
{
  for (int i = 1; i <= 10; i++) {
    for (int j = 1; j <= 10; j++) {
      cout << i * j << '\t';
    }
    cout << endl;
  }
  return 0;
}
```

## Question 2
Write a program that asks the user to enter a number and then prints the factorial of
that number using a do-while loop. A factorial of a number is the product of all
positive integers less than or equal to that number.
### Solution
```c++
#include <iostream>
using namespace std;
int main() 
{
  int number, factorial = 1;
  cout << "Enter a positive integer: ";
  cin >> number;
  int i = 1;
  do {
    factorial *= i;
    i++;
  } while (i <= number);
  cout << "The factorial of " << number << " is " << factorial << endl;
  return 0;
}
```

## Question 3
Write a program that prints all even numbers between 1 and 100 but stops after it has
printed the number 20. The program should use the "break" statement to stop after
printing the 20th even number. The program should also skip printing the number 4.
### Solution
```c++
#include <iostream>
using namespace std;
int main() {
  int i = 2;
  while (i <= 100) {
    if (i == 4) {
      i += 2;
      continue;
    }
    if (i > 20) {
      break;
    }
    cout << i << endl;
    i += 2;
  }
  return 0;
}
```
