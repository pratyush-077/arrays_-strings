# Experiment-7
# Name- Pratyush Saha
# Prn-24070123078
Arrays and strings are fundamental data structures in C++. Here's a clear overview of both, with syntax and examples.

🔢 Arrays in C++

An array is a collection of elements of the same type stored in contiguous memory locations.

Syntax:
type arrayName[size];

Example:
#include <iostream>
using namespace std;

int main() {
    int numbers[5] = {10, 20, 30, 40, 50};

    for (int i = 0; i < 5; i++) {
        cout << "Element at index " << i << ": " << numbers[i] << endl;
    }

    return 0;
}

Key Points:

Indexing starts at 0.

If you don't initialize all elements, the rest are set to 0 (for global/static arrays).

You can also declare and initialize like this:

int arr[] = {1, 2, 3}; // Size is inferred to be 3

🧵 Strings in C++
1. C-style Strings (Character Arrays)
char str[6] = {'H', 'e', 'l', 'l', 'o', '\0'};


Or using string literals:

char str[] = "Hello";


The \0 null character marks the end of the string.

Example:
#include <iostream>
using namespace std;

int main() {
    char greeting[] = "Hello";

    cout << "Greeting: " << greeting << endl;
    return 0;
}


📌 Use <cstring> for functions like strlen(), strcpy(), strcmp(), etc.

2. C++ string Class (Preferred)
#include <iostream>
#include <string>
using namespace std;

int main() {
    string name = "Alice";

    cout << "Name: " << name << endl;
    cout << "Length: " << name.length() << endl;

    name += " Smith"; // Concatenation
    cout << "Full name: " << name << endl;

    return 0;
}


📌 std::string is part of the Standard Template Library (STL), more powerful and safer than C-style strings.

✅ Quick Comparison
Feature	C-style String	std::string
Header	<cstring>	<string>
Null Terminator	Required (\0)	Handled internally
Safer	❌ Manual handling needed	✅ Yes
Functions	strlen(), etc.	.length(), .substr(), .find(), etc.
