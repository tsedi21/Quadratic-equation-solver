#include <iostream>
#include <cmath>
using namespace std;

int main() {
    double a, b, c;
    double discriminant, root1, root2;

    cout << "Enter the coefficient a: ";
    
    cin >> a;
    if (a == 0) {
        cout << "This is not a quadratic equation because a = 0." << endl;
        return 1; // Exit the program
    }

    cout << "Enter the coefficient b: ";
    cin >> b;

    cout << "Enter the constant term c: ";
    cin >> c;

    discriminant = b * b - 4 * a * c;

    if (discriminant < 0) {
        cout << "The quadratic equation with leading coefficient of " << a
             << ", coefficient of x " << b << " and constant term " << c
             << " has no real solution." << endl;
    }
    else if (discriminant == 0) {
        root1 = -b / (2 * a);
        cout << "The quadratic equation with leading coefficient of \033[1;31m" << a
             << "\033[0m, coefficient of x \033[1;31m" << b
             << "\033[0m and constant term \033[1;31m" << c
             << "\033[0m is: \033[1;31m" << root1 << "\033[0m" << endl;
    }
    else {
        root1 = (-b + sqrt(discriminant)) / (2 * a);
        root2 = (-b - sqrt(discriminant)) / (2 * a);
        cout << "The quadratic equation with leading coefficient of \033[1;31m" << a
             << "\033[0m, coefficient of x \033[1;31m" << b
             << "\033[0m and constant term \033[1;31m" << c
             << "\033[0m has two solutions: \033[1;31m" << root1
             << "\033[0m and \033[1;31m" << root2 << "\033[0m" << endl;
    }

    // Step 6: End
    return 0;
}
