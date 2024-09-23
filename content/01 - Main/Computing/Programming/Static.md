In *C++* the keyword `static` can mean many things.

# In Classes

## Functions

If a function is marked static it does not belong to a particular object it just belongs to the class similar to a static variable in a class

````Cpp
#include <iostream>

class MyClass {
public:
    // Regular member function
    void regularFunction() {
        std::cout << "Regular member function called." << std::endl;
    }

    // Static member function
    static void staticFunction() {
        std::cout << "Static member function called." << std::endl;
    }
};

int main() {
    // Call regular member function using an object
    MyClass obj;
    obj.regularFunction();

    // Call static member function without an object
    MyClass::staticFunction();

    return 0;
}

````
