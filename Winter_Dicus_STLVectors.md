# data-structure-proj

## Intro to Vectors

<p>STL Vectors are one of the most used functions in C++; you're more likely familiarized with how to introduce it into your code, with a simple #include. Vectors are used in cases where the developer expects to need a data structure that can expand and shrink as data is added or removed from the structure. Standard arrays aren't flexible enough to pull this off, so developers use vectors instead.</p>

## How to use vectors?
Vectors are fairly easy to introduce into your project. Simply use
```
#include <vector>

vector<(datatype)> (variablename)
```
to add vectors into your code. The #include line is necessary. Vectors can dynamically change their size according to data inputted, but require more memory than arrays. 

One can check the size of an array using the `v.size()` function, and to print the contents of an array, one can simply write a `print()` function in the following manner:
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
The `v.at(X)` function displays the element in the array that is in the Xth position. `v.front()` and `v.back()` are self-explanatory, displayng the element in the front and back of the vector, respectively. `v.insert(X)` and `v.erase(X)` are capable of adding or deleting an element at the Xth position.

One can use the `v.push_back()` function to add an element to the end of an array, and use `v.pop_back()` to remove the last element in an array, with `v.clear()` emptying the entire vector.

`v.resize(#)` changes the size of the vector to only allow for # amount of elements with subsequent elements being deleted, but the user can still add or remove elements after the fact. Using `v.capacity()` displays how many elements the vector can currently hold. `v.empty()` displays whether a vector contains any elements or not.

Vectors are flexible and easily modified, making them appealing to use for data storage. 

## How is it useful?
<p>Vectors are useful because they automatically resize in order to fit new data into themselves by allocating more storage to accomodate new elements added to the end of a vector. Even then, developers can declare a vector's size when needed. Furthermore, similarly to arrays, elements within a vector can be easily accessed, added and removed, but attempting to insert or remove elements in the middle of a vector is more inefficient than using a list to perform the same action as vectors rely heavily on the element in the back.

Vectors are recommended for when the user expects to have to process an influx of data that can change, or when the user has no idea how much data they can expect to have to process, as a vector's ability to dynamically allocate memory for storage makes them more suited for this task than arrays. Vectors are also easier to copy.</p>

## Further reading

https://cplusplus.com/reference/vector/vector/ - For a more in-depth explanation about vectors

https://www.mygreatlearning.com/blog/vectors-in-c/ - For further explanation on a majority of vector functions with examples.

https://www.geeksforgeeks.org/vector-in-cpp-stl/ - For examples on how to utilize vectors.
