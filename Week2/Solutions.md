# Solutions

## Question 1

```c++
#include <iostream>
using namespace std;

int main(){
  int num,a,b,c,d;
  
  cout << "Please enter the input sequence: " << endl;
  cin >> num;
  
  d = num % 10;
  c = (num / 10) % 10;
  b = (num / 100) % 10;
  a = (num / 1000) % 10;
  
  cout << a << " " << b << " " << c << " " << d << endl;
  
  return 0;
}
```

## Question 2

```c++
// Swap with temporary variable
#include <iostream>
using namespace std;

int main(){
  
  int a = 5, b = 10, temp;

  cout << "Before swapping." << endl;
  cout << "a = " << a << ", b = " << b << endl;

  temp = a;
  a = b;
  b = temp;

  cout << "\nAfter swapping." << endl;
  cout << "a = " << a << ", b = " << b << endl;

  return 0;
}
```
```c++
// Swap without temporary variable
#include <iostream>
using namespace std;

int main()
{
    
  int a = 5, b = 10;

  cout << "Before swapping." << endl;
  cout << "a = " << a << ", b = " << b << endl;

  a = a + b;
  b = a - b;
  a = a - b;
  
  // or alternatively using multiplication and division for swapping
  // a = a * b;    
  // b = a / b;  
  // a = a / b;    

  cout << "\nAfter swapping." << endl;
  cout << "a = " << a << ", b = " << b << endl;

  return 0;
}
```

## Question 3

```c++
#include <iostream>
using namespace std;

int main(){
  
  int t1, t2, t1h, t2h, t1m, t2m, t1tm, t2tm, tdtm, hours, minutes;
  
	cout << "Please enter the first time:";
	cin >> t1;
	cout << "Please enter the second time:";
	cin >> t2;
  
	t1h = t1 / 100; // time1 hours
	t2h = t2 / 100; // time2 hours
  
  t1m = t1 % 100; // time1 minutes
  t2m = t2 % 100; // time2 minutes
  
  t1tm = (t1h * 60) + t1m; // time1 total time in minutes
  t2tm = (t2h * 60) + t2m; // time2 total time in minutes
  
  tdtm = t2tm - t1tm; // total difference time in minutes
  
  hours = tdtm / 60;
  minutes = tdtm % 60;
  
	cout << hours << " hours " << minutes << " minutes";

  return 0;
}
```
