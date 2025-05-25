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
#include <queue>
#include <algorithm>

using namespace std;

int maxProductWithHeaps(const std::vector<int>& nums) {
    if (nums.size() < 2) {
        throw std::invalid_argument("Array must contain at least two numbers.");
    }

    std::priority_queue<int, std::vector<int>, std::greater<int>> maxHeap; // min-heap for largest
    std::priority_queue<int> minHeap; // max-heap for smallest

    for (int num : nums) {
        // Track two largest
        maxHeap.push(num);
        if (maxHeap.size() > 2) maxHeap.pop();

        // Track two smallest
        minHeap.push(-num);
        if (minHeap.size() > 2) minHeap.pop();
    }

    int max1 = maxHeap.top(); maxHeap.pop();
    int max2 = maxHeap.top();

    int min1 = -minHeap.top(); minHeap.pop();
    int min2 = -minHeap.top();

    return std::max(max1 * max2, min1 * min2);
}

int main() {
    vector<int> nums = {5, -10, -6, 9, 4};

    try {
        int result = maxProductWithHeaps(nums);
        cout << "Maximum product of two numbers: " << result << std::endl;
    } catch (const std::exception& e) {
        cerr << "Error: " << e.what() << std::endl;
    }
}
```
### Task 6
```c++
#include <iostream>
#include <vector>
#include <unordered_set>

using namespace std;

int longestConsecutiveSequence(const vector<int>& nums) {
    unordered_set<int> numSet(nums.begin(), nums.end());
    int longest = 0;

    for (int num : numSet) {
        // Only start counting if it's the beginning of a sequence
        if (numSet.find(num - 1) == numSet.end()) {
            int currentNum = num;
            int currentStreak = 1;

            while (numSet.find(currentNum + 1) != numSet.end()) {
                currentNum++;
                currentStreak++;
            }

            longest = max(longest, currentStreak);
        }
    }

    return longest;
}

int main() {
    vector<int> arr1 = {10, 5, 12, 3, 55, 30, 4, 11, 2};
    vector<int> arr2 = {19, 13, 15, 12, 18, 14, 17, 11};

    cout << "Longest sequence length (arr1): " << longestConsecutiveSequence(arr1) << endl;
    cout << "Longest sequence length (arr2): " << longestConsecutiveSequence(arr2) << endl;

    return 0;
}
```
