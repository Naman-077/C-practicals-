// Q11-Write a program to read two numbers p and q. If q is 0 then throw an exception else display the result of p/q.

#include <iostream>
#include <stdexcept> // For standard exceptions
using namespace std;

int main() {
    int p, q;

    try {
        cout << "Enter the value of p: ";
        cin >> p;

        cout << "Enter the value of q: ";
        cin >> q;

        if (q == 0) {
            throw runtime_error("Division by zero is not allowed!");
        }

        // If no exception, calculate and display the result
        float result = static_cast<float>(p) / q;
        cout << "Result of p / q: " << result << endl;

    } catch (const runtime_error& e) {
        // Catch and display the exception message
        cout << "Exception occurred: " << e.what() << endl;
    }

    return 0;
}
