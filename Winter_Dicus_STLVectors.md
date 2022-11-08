# data-structure-proj

## Intro to Vectors

<p>STL Vectors are one of the most used functions in C++; you're more likely familiarized with how to introduce it into your code, with a simple #include. Vectors are used in cases where the developer expects to need a data structure that can expand and shrink as data is added or removed from the structure. Standard arrays aren't flexible enough to pull this off, so developers use vectors instead.</p>

## How does it work?
Vectors are fairly easy to introduce into your project. Simply use
```
#include <vector>

vector<(datatype)> (variablename)
```
to add vectors into your code. Vectors can dynamically change their size according to data inputted, but require more memory than arrays. 

One can check the size of an array using the `size()` function, and to print the contents of an array, one can simply use the `print()` function in the following manner:
```
void print(std::vector<(datatype)> const &(variablename) {
  std::cout << "Vector elements: " << endl;
  
  for(int i = 0; i < (variablename).size(); i++)
    std::cout << (variablename).at(i); << " ";
}

int main() {
  std::vector<(datatype)> (variablename) = { (data) };
  print((variablename));
}
```
The `at(X)` function displays the element in the array that is in the Xth index.

One can use the `push_back()` function to add an element to the end of an array, and use `pop_back()` to remove the last element in an array, with `clear()` emptying the entire vector.

## How is it useful?
<p>Vectors are useful because they automatically resize in order to fit new data into themselves. Even then, developers can declare a vector's size when needed. Furthermore, similarly to arrays, elements within a vector can be easily accessed, added and removed, but attempting to insert or remove elements in the middle of a vector is more inefficient than using a list to perform the same action.</p>

## Further reading

https://cplusplus.com/reference/vector/vector/ - For a more in-depth explanation about vectors

https://www.geeksforgeeks.org/vector-in-cpp-stl/ - For examples on how to utilize vectors
