## Simple Console Calculator (C++)

This is a basic command-line calculator written in C++. It allows the user to perform simple arithmetic operations: **addition (+)**, **subtraction (-)**, **multiplication (*)**, and **division (/)**.

### How it works
The program asks the user to enter an expression in the following format:



It then calculates the result and displays it.  
If the user tries to divide by zero, the program shows a warning message.

### Code

```cpp
#include <iostream>
#include <string>
using namespace std;

float calculating() {
    float n1, n2;
    string znak;
    float ans;

    cout << "Input number for example (12 (+,-,/,*) 4)" << endl;
    cin >> n1 >> znak >> n2;

    if (znak == "-") {
        ans = n1 - n2;
    }
    else if (znak == "+") {
        ans = n1 + n2;
    }
    else if (znak == "/") {
        if (n2 == 0 or n1==0) {                  
            cout << "Impossible" << endl;
            return 0;
        }
        ans = n1 / n2;
    }
    else if (znak == "*") {
        ans = n1 * n2;
    }
    else {
        cout << "Unknown operator!" << endl;
        return 0;
    }

    cout << "Answer is: " << ans << endl;
    return 0;
}

int main() {
    calculating();
    return 0;
}
