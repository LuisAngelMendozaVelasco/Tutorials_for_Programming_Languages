# Files

## Create, write and read a text file

Code:

```cpp
#include <iostream>
#include <fstream>
#include <string>
using namespace std;

int main() {
    // Create a text file
    ofstream MyWriteFile("filename.txt");

    // Write to the file
    MyWriteFile << "Files can be tricky, but it is fun enough!";

    // Close the file
    MyWriteFile.close();

    // Create a text string, which is used to output the text file
    string myText;

    // Read from the text file
    ifstream MyReadFile("filename.txt");

    // Use a while loop together with the getline() function to read the file line by line
    while(getline(MyReadFile, myText)) {
        // Output the text from the file
        cout << myText << endl;
    }

    // Close the file
    MyReadFile.close();

    // Deletes the file
    remove("filename.txt");

    return 0;
}
```

Output:

```text
Files can be tricky, but it is fun enough!
```