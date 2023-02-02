# Problems

## Question 1:
Write a program to emulate a simple calculator using switch statements.
```
Enter an operator (+, -, *, /): +
Enter two numbers: 
2.3
4.5
2.3 + 4.5 = 6.8
```
```
Enter an operator (+, -, *, /): -
Enter two numbers: 
2.3
4.5
2.3 - 4.5 = -2.2
```
### Solution
```c++
// Program to build a simple calculator using switch Statement
#include <iostream>
using namespace std;

int main() {
    char oper;
    float num1, num2;
    cout << "Enter an operator (+, -, *, /): ";
    cin >> oper;
    cout << "Enter two numbers: " << endl;
    cin >> num1 >> num2;

    switch (oper) {
        case '+':
            cout << num1 << " + " << num2 << " = " << num1 + num2;
            break;
        case '-':
            cout << num1 << " - " << num2 << " = " << num1 - num2;
            break;
        case '*':
            cout << num1 << " * " << num2 << " = " << num1 * num2;
            break;
        case '/':
            cout << num1 << " / " << num2 << " = " << num1 / num2;
            break;
        default:
            // operator is doesn't match any case constant (+, -, *, /)
            cout << "Error! The operator is not correct";
            break;
    }

    return 0;
}
```
## Question 2:
Write a program to enter a sequence of integers and find their sum.
```
Input(Enter -1 to quit): 1 2 1 8 8 9 K 
Output: 29
```
```
Input(Enter -1 to quit): 1 K 
Output: 1
```
### Solution
You can use a while loop to keep checking if K was entered
```c++
#include <iostream>
using namespace std;
int main()
{
  int x = 0, sum = 0;
  cout<<"Input(Enter -1 to quit): ";
  while(x!=-1)
  {
    cin>>x>>endl;
    sum+=x;
  }
  cout<<"Output: "<<sum;
  return 0;
}
```

## Question 2:
Print the following pattern:
```
1
2
3
4
```
### Solution
To print the above pattern, a simple for loop with n=4 is sufficient:
```c++
#include <iostream>
using namespace std;
int main()
{
  int n = 4;
  for(int i = 1; i <= n; i++)
  {
    cout<<i<<endl;
  }
  
  return 0;
}
```
