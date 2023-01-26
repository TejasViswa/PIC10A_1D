# Exercises

## Question 1
Find out if a given number is even or odd
```
Enter an integer: 23
23 is odd.
```
### Solution
```c++
#include <iostream>
using namespace std;

int main() {
  int n;

  cout << "Enter an integer: ";
  cin >> n;

  if ( n % 2 == 0)
    cout << n << " is even.";
  else
    cout << n << " is odd.";

  return 0;
}
```

## Question 2
Find out the middle number of 3 given numbers
### Solution
```c++
#include <iostream>
using namespace std;

int main() {
  int a,b,c;

  cout << "Enter 3 numbers: ";
  cin >> a >> b >> c;

   if (a > b)
    {
        if (b > c)
            cout << b << " is the middle number "<<endl;
        else if (a > c)
            cout << c << " is the middle number "<<endl;
        else
            cout << a << " is the middle number "<<endl;
    }
    else
    {
        // Decided a is not greater than b.
        if (a > c)
            cout << a << " is the middle number "<<endl;
        else if (b > c)
            cout << c << " is the middle number "<<endl;
        else
            cout << b << " is the middle number "<<endl;
    }
  return 0;
}
```
## Question 3
Write a program that prompts the user to enter a word in English. If the word ends with "ing", the program should translate it to "in' in alien language. If the word ends with "ly", the program should translate it to "li" in alien language. If the word ends with "ed", the program should translate it to "oda" in alien language. If the word does not end with "ing", "ly" or "ed", the program should translate it to "beep" in alien language.
### Solution
```c++
#include <iostream>
#include <string>
using namespace std;
int main() {
  string input;
  cout <<"Enter a word in English:";
  cin >> input;
  int len = input.length();
  string lastTwo = input.substr(len - 2);
  string lastThree = input.substr(len - 3);
  if (lastThree == "ing") {
  cout << "The alien translation is: " << input.substr(0, len - 3) << "in'" << endl;
  } else if (lastTwo == "ly") {
  cout << "The alien translation is: " << input.substr(0, len - 2) << "li" << endl;
  } else if (lastTwo == "ed") {
  cout << "The alien translation is: " << input.substr(0, len - 2) << "oda" <<
  endl;
  } else {
  cout << "The alien translation is: beep" << endl;
  }
  return 0;
}
```
