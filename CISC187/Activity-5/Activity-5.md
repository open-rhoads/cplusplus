# Hash Table
This project demonstrates a simple has table with an unordered map. It also computes the hash value of a string key with the default hash function.
## Number 1
```c++
    // the following array would take O(N) or O(logN) steps to search using linear or binary search, respectively
    // int numbers[5] = {200, 400, 100, 50, 350};
    // let's use an unordered map, which can potentially cut the efficiency down to O(1).
    // We'll use a string key to store each number
    unordered_map<string, int> ints_map =
    {{"number1", 200},{"number2", 400},{"number3", 100},{"number4", 50},{"number5", 350}};
    // now we can search for and access an element immediately using its key.
    // Assuming the element was able to be placed in the correct computed index (no collision occurred), then this will result in an efficiency of O(1).
    // all you have to do is change the key below and it will return the value
    const auto desired_number = ints_map.find("number2");
    if (desired_number != ints_map.end()) {
        cout << desired_number->first << " is " << desired_number->second << endl;
    } else {
        cout << "The key was not found.\n";
    }
```
## Number 2
```c++
    // Now let's use the default hash function to compute the hash value of my name as a key
    // store my name as a string, to be used as the key pass to the hash function object
    string key = "Mikaela";
    // create a hash function object that is optimized for string data type
    hash<string> hash_object;
    // create an unsigned integer type to store the hash value in bytes; passing the key to the hash function object
    size_t hash_value = hash_object(key);
    // output the hash value
    cout << "The hash value of my name - " << key << " - is: " << hash_value << endl;
```
## Number 3
Below is my diagram of how tombstones create inefficiencies:
[Lab 5.pdf](https://github.com/user-attachments/files/19153593/Lab.5.pdf)
