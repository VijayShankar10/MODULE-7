# Ex.No:3  
# Ex.Name: Function Overriding using Virtual Functions  

## Date:  

## Aim:  
To write a C++ program to override the `print()` function in the base class with the `print()` function in the derived class using the concept of virtual functions.  

## Algorithm:  
1. Start the program.  
2. Create a base class `Base` with a virtual function `print()`.  
3. Create a derived class `Derived` that overrides the `print()` function.  
4. Use a base class pointer to point to the derived class object.  
5. Call the `print()` function to demonstrate runtime polymorphism (base pointer calls derived function).  
6. Stop the program.  

## Program:
```cpp
#include <iostream>
using namespace std;

class Base {
public:
    virtual void print(string msg) {
        cout << msg << endl;
    }
};

class Derived : public Base {
public:
    void print(string msg) override {
        cout << msg << endl;
    }
};

int main() {
    Base* basePtr;
    Derived d;

    string input;
    cin >> input;

    basePtr = &d;
    basePtr->print(input);

    return 0;
}
```

## Output:
```
Input:
VirtualOne

Output:
VirtualOne



Input:
VirtualTwo

Output:
VirtualTwo


Input:
VirtualThree

Output:
VirtualThree
```
## Result:
<img width="866" height="365" alt="image" src="https://github.com/user-attachments/assets/bb1f3dbd-dad3-4631-b8fb-fd9856d90f7d" />

