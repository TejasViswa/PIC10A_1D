# Exercises

## Question 1
Write a program to print a square with a function of given size and character
```
Enter the size of square: 5
Enter the character to create the square with: @

@ @ @ @ @
@       @
@       @
@       @
@ @ @ @ @

```
```
Enter the size of square: 3
Enter the character to create the square with: &

& & &
&   &
& & &

```

## Question 2
An Armstrong number of three digits is an integer such that the sum of the cubes of its digits is equal to the number itself. For example, 371 is an Armstrong number since 3**3 + 7**3 + 1**3 = 371. Other examples: 0,1,153,370,371,407,etc
Write a program to check if a given number is an armstrong number.
```
Please enter an integer: 371
It is an armstrong number
```
### Solution
```c++
#include <iostream>
using namespace std;

bool isArmstrong(int num)
{
    int originalNum = num, rem = 0, result = 0;
    
    while (originalNum != 0) {
        // rem contains the last digit
        rem = originalNum % 10;
        
        result += rem * rem * rem;
        
        // removing last digit from the orignal number
        originalNum /= 10;
    }
    
    return (result==num);
}

int main() {
    int num;
    cout << "Enter a three-digit integer: ";
    cin >> num;

    if (isArmstrong(num))
        cout << num << " is an Armstrong number.";
    else
        cout << num << " is not an Armstrong number.";

    return 0;
}
```
An extension of the above problem is to print all 3-digit armstrong numbers.
### Solution
```c++
#include <iostream>
using namespace std;

bool isArmstrong(int num)
{
    int originalNum = num, rem = 0, result = 0;
    
    while (originalNum != 0) {
        // rem contains the last digit
        rem = originalNum % 10;
        
        result += rem * rem * rem;
        
        // removing last digit from the orignal number
        originalNum /= 10;
    }
    
    return (result==num);
}

int main() {
    cout << "The 3 digit armstrong numbers are:"<<endl;
    
    for(int i=0; i<=999; i++)
    {
        if (isArmstrong(i))
            cout << i <<endl;
    }

    return 0;
}
```
