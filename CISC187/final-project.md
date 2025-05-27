## CISC 187 Final Project
### Task 1
```c++
#include <iostream>
#include <vector>
#include <unordered_set>
#include <string>

using namespace std;

// define a custom Player stucture with 3 members to store first/last name & team
struct Player {
    string f_name;
    string l_name;
    string team;
};

// function to find common players accepts two vectors of Players by reference (one for football, one for basketball)
vector<string> find_common_players(
    const vector<Player>& bball_players,
    const vector<Player>& fball_players
) {
    // create an unordered set to store the names of the basketball players
    // a set can be used to save memory because we only need to check for values in this task, we don't need a key
    unordered_set<string> bball_names;
    vector<string> common_players; // create a new vector of strings to store any common names

    // Add basketball player full names to the set by looping through the basketball Players vector and inserting the first/last name into the basketball names set.
    for (const auto& player : bball_players) {
    bball_names.insert(player.f_name + " " + player.l_name);
}

    // Check football players against the set by looping through the football players vector
    for (const auto& player : fball_players) {
        string full_name = player.f_name + " " + player.l_name; // store football player full name
        if (bball_names.find(full_name) != bball_names.end()) { // search the set for the full name - find will either return an iterator to the found element or the end of the vector, therefore, not equal to end means it was found
            common_players.push_back(full_name); // push back if not equal to end / name was found
        }
    }

    return common_players;
    }


int main() {
    vector<Player> basketball_players = {
        {"Jill", "Huang", "Gators"},
        {"Janko", "Barton", "Sharks"},
        {"Wanda", "Vakulskas", "Sharks"},
        {"Jill", "Moloney", "Gators"},
        {"Luuk", "Watkins", "Gators"}
    };

    vector<Player> football_players = {
        {"Hanzla", "Radosti", "32ers"},
        {"Tina", "Watkins", "Barleycorns"},
        {"Alex", "Patel", "32ers"},
        {"Jill", "Huang", "Barleycorns"},
        {"Wanda", "Vakulskas", "Barleycorns"}
    };

    auto result = find_common_players(basketball_players, football_players);

    for (const auto& name : result) {
        cout << name << endl;
    }
}
```
### Task 2
```c++
#include <iostream>
#include <vector>
#include <unordered_set>

using namespace std;

int find_missing_number(const vector<int>& nums) { // accepts a vector of integers by reference
    unordered_set<int> numSet(nums.begin(), nums.end()); // use of range constructor to initialize the set with all the elements from the nums vector
    for (int i = 0; i <= nums.size(); ++i) { // loop through the nums vector, start at 0 and include last number to get ALL (i.e. 0-6)
        if (numSet.find(i) == numSet.end()) { // search for each value in the numSet unordered set... if it's equal to the end, it means it was not found and therefore, i is the missing number.
            return i;
        }
    }
    return -1; // Should never happen if there is always a missing number
}

int main() {
    vector<int> nums1 = {2, 3, 0, 6, 1, 5};
    vector<int> nums2 = {8, 2, 3, 9, 4, 7, 5, 0, 6};
    cout << "Find the Missing Number\n";
    cout << "Missing number in nums1: " << find_missing_number(nums1) << endl;
    cout << "Missing number in nums2: " << find_missing_number(nums2) << endl;
}
```
### Task 3
```c++
#include <iostream>
#include <vector>
#include <stack>
#include <algorithm>

using namespace std;

int get_max_profit(const vector<int>& prices) { // function accepts a vector of stock prices by reference
    if (prices.empty()) return 0; // return if the vector is empty

    stack<int> buy_stack; // create a stack of integers to track the lowest price
    int max_profit = 0; // set the max profit equal to 0

    for (int price : prices) { // loop through the vector of stock prices
        if (buy_stack.empty() || price < buy_stack.top()) { // if there is nothing in the stack OR if the current price is lower than the top of the stack, push the price to the top of the stack
            buy_stack.push(price); // therefore, the stack will have the lowest price on top
        } else { // if the current price is not the lowest so far, calculate potential profit with the current lowest price
            int profit = price - buy_stack.top(); // subtract the current lowest price from the current price to calc profit
            max_profit = max(max_profit, profit); // set max profit to the profit value, IF higher than the current max
        }
    }
    return max_profit; // return the max
}

int main() {
    vector<int> prices = {10, 7, 5, 8, 11, 2, 6};
    cout << "Maximum Profit: $" << get_max_profit(prices) << endl;
}
```
### Task 4
```c++
#include <iostream>
#include <vector>
#include <queue>
#include <algorithm>

using namespace std;

// Function to compute the maximum product of any two numbers using heaps
int max_product_two_ints(const vector<int>& nums) { // function accepts a vector of integers by reference
    if (nums.size() < 2) { // throw an error if there are not at least two ints
        throw invalid_argument("Array must contain at least two numbers.");
    }

    // Min-heap to track the two largest numbers - create one by telling it to prioritize smaller values with greater
    priority_queue<int, vector<int>, greater<int>> two_largest;

    // Track two smallest using a max-heap (default behavior)
    std::priority_queue<int> two_smallest;



    for (int num : nums) { // loop through the nums
        // Track the two largest numbers
        two_largest.push(num); // push the num to the min-heap
        if (two_largest.size() > 2) { // if it has more than two nums now
            two_largest.pop();  // pop the smallest off the top to keep only the top 2 largest
        }

        // Track two smallest numbers using max-heap behavior by storing negative values
        two_smallest.push(num);
        if (two_smallest.size() > 2) {
            two_smallest.pop(); // remove the largest numbers if more than 3
        }
    }

    // Extract the two largest numbers from min heap
    int largest1 = two_largest.top(); two_largest.pop();
    int largest2 = two_largest.top();

    // Extract the two smallest numbers from max heap (negate back to get original smallest values)
    int smallest1 = -two_smallest.top(); two_smallest.pop();
    int smallest2 = -two_smallest.top();

    // Return the maximum product between the two largest and two smallest numbers
    return max(largest1 * largest2, smallest1 * smallest2);
}

int main() {
    vector<int> nums = {5, -10, -6, 9, 4};

    try {
        int result = max_product_two_ints(nums);
        cout << "Maximum product of two numbers: " << result << endl;
    } catch (const exception& e) {
        cerr << "Error: " << e.what() << endl;
    }
}
```
### Task 5
```c++
#include <iostream>
#include <vector>
#include <iomanip>

using namespace std;

void sort_temps(vector<float>& temps) { // function accepts a vector of temps by reference
    const int range = 21; // We have a known range from 97.0 to 99.0 inclusive (in 0.1 increments) - this makes count sort approach more efficient
    const float base = 97.0; // define the starting value
    vector<int> count(range, 0); // create a vector of ints of the range size and initialize values to 0

    // Count occurrences
    for (float temp : temps) { // loop through the temps
        int index = static_cast<int>((temp - base) * 10 + 0.5); // map the temp to an index by subtracting from lowest possible, multiplying by 10, and then adding 0.5 and static casting to get nearest int and avoid floating point error
        count[index]++; // increment the value in count vector at the corresponding index (will add one every time this temp is found)
    }

    // Reconstruct the sorted array
    int pos = 0;
    for (int i = 0; i < range; ++i) { // loop through each possible index value in range
        float value = base + i * 0.1f; // convery temp back into its floating point full value
        for (int j = 0; j < count[i]; ++j) { // loop the number of times for the value found at each count value at each i
            temps[pos++] = value; // write the value to the temps array (will be in sorted order) and then increment pos variable. pos tracks temps vector whereas i is always the range of indices
        }
    }
}

int main() {
    // create vector of temps and pass to function
    vector<float> temps = {98.6, 98.0, 97.1, 99.0, 98.9, 97.8, 98.5, 98.2, 98.0, 97.1};
    sort_temps(temps);
    
    // output the temps
    cout << "Sorted temperatures:\n";
    for (float temp : temps) {
        cout << fixed << setprecision(1) << temp << " ";
    }
    cout << endl;
}
```
### Task 6
```c++
#include <iostream>
#include <vector>
#include <unordered_set>

using namespace std;

int longest_sequence(const vector<int>& nums) { // function accepts a vector of ints by reference
    unordered_set<int> num_set(nums.begin(), nums.end()); // create an unordered set of ints that contains each number in the vector
    int longest = 0; // define longest and initialize to 0

    for (int num : num_set) { // loop through the nums in set
        // if the number before the current one is not in the set, this might be a new sequence, so start counting
        if (num_set.find(num - 1) == num_set.end()) {
            int current_num = num; // store the curret num
            int current_streak = 1; // set streak to 1

            while (num_set.find(current_num + 1) != num_set.end()) { // as long as the next number after num in sequence is not the end (i.e. it exists in the set)
                current_num++; // increment the current num
                current_streak++; // and increment the current streak
            }
            longest = max(longest, current_streak); // set the longest streak using max function
        }
    }
    return longest;
}

int main() {
    vector<int> arr1 = {10, 5, 12, 3, 55, 30, 4, 11, 2};
    vector<int> arr2 = {19, 13, 15, 12, 18, 14, 17, 11};

    cout << "Longest sequence length (arr1): " << longest_sequence(arr1) << endl;
    cout << "Longest sequence length (arr2): " << longest_sequence(arr2) << endl;
}
```
