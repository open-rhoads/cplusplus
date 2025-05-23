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

### Task 4

### Task 5
