# list of Easy DSA problems that directly use `map` / `unordered_map`** in C++. These will help build your logic and muscle memory using real code.

---

### ✅ Easy DSA Problems Using `map` / `unordered_map`

| No. | Problem Title                          | Concept                                 | LeetCode Link                                                              |
| --- | -------------------------------------- | --------------------------------------- | -------------------------------------------------------------------------- |
| 1️⃣ | **Contains Duplicate**                 | Check for repeats using `unordered_map` | [LC 217](https://leetcode.com/problems/contains-duplicate)                 |
| 2️⃣ | **Two Sum**                            | Store indices in map for quick lookup   | [LC 1](https://leetcode.com/problems/two-sum)                              |
| 3️⃣ | **Valid Anagram**                      | Compare frequency of characters         | [LC 242](https://leetcode.com/problems/valid-anagram)                      |
| 4️⃣ | **Find the Difference**                | Frequency mismatch                      | [LC 389](https://leetcode.com/problems/find-the-difference)                |
| 5️⃣ | **Intersection of Two Arrays**         | Track elements using map/set            | [LC 349](https://leetcode.com/problems/intersection-of-two-arrays)         |
| 6️⃣ | **First Unique Character in a String** | Map + string index                      | [LC 387](https://leetcode.com/problems/first-unique-character-in-a-string) |
| 7️⃣ | **Majority Element**                   | Count elements with map                 | [LC 169](https://leetcode.com/problems/majority-element)                   |
| 8️⃣ | **Ransom Note**                        | Match char counts                       | [LC 383](https://leetcode.com/problems/ransom-note)                        |
| 9️⃣ | **Number of Good Pairs**               | Count pairs using frequency             | [LC 1512](https://leetcode.com/problems/number-of-good-pairs)              |
| 🔟  | **Jewels and Stones**                  | Count jewels in map                     | [LC 771](https://leetcode.com/problems/jewels-and-stones)                  |

---


    Contains Duplicate

                    pudo code 
                        int nums=[1,2,3,4,2];
                        retrun true : appreare twise in array ex : 2
                        retrun false : if nothing is twise ex : 1,3,4
                    code 

                    class Solution 
                    {
                    public:
                        bool containsDuplicates(vector<int>& nums)
                        {
                            unordered_map<int, int> m;

                            for (int pair : nums)
                            {
                                m[pair]++;
                                if (m[pair] > 1)
                                {
                                    cout << "Duplicate found: " << pair << endl;
                                    return true;
                                }
                            }

                            cout << "No Duplicate found" << endl;
                            return false;
                        }
                    };

                    Learn : 

                            ✅ `vector<int>& nums` → **Reference** → *No copy, Fast, Changes affect original*
                            ❌ `vector<int> nums` → **Copy** → *Makes copy, Slower, Changes don’t affect original*


    Two Sum

    Yess bro! 💥 You’ve nailed it.
Now as promised — here’s your **clean, simple, beginner-friendly explanation** of the **Two Sum Problem using `unordered_map`**, written in a proper **DSA resume-style `.md` file** with:

* 🔍 Problem summary
* 🧠 Step-by-step logic
* 📊 Iteration table
* ✅ Final C++ code
* 📦 Output

---

### 📁 Markdown File: `two_sum_unordered_map_solution.md`

````md
# 🧠 LeetCode 1: Two Sum (C++ with unordered_map)

## ✅ Problem Statement

Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to the target.

You may assume each input would have exactly one solution.

---

## 💡 Approach: Using `unordered_map` (Optimized)

We will store previously seen numbers and their indices in an `unordered_map`.  
For each number `nums[i]`, we check if `target - nums[i]` is already in the map.

- If yes → return indices: `{map[complement], i}`
- If not → store `nums[i]` and its index in the map.

✅ This gives us **O(n)** time complexity.

---

## 📊 Step-by-Step Table (Example)

**Input:**
```cpp
nums = [1, 7, 5, 2], target = 9
````

| i | nums\[i] | complement | map status           | Action                    |
| - | -------- | ---------- | -------------------- | ------------------------- |
| 0 | 1        | 8          | `{}`                 | 8 not found → store 1 → 0 |
| 1 | 7        | 2          | `{1: 0}`             | 2 not found → store 7 → 1 |
| 2 | 5        | 4          | `{1: 0, 7: 1}`       | 4 not found → store 5 → 2 |
| 3 | 2        | 7          | `{1: 0, 7: 1, 5: 2}` | ✅ 7 found! return {1, 3}  |

---

## ✅ Final C++ Code

```cpp
#include <iostream>
#include <unordered_map>
#include <vector>
using namespace std;

class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> map; // number → index

        for (int i = 0; i < nums.size(); ++i) {
            int complement = target - nums[i];

            if (map.count(complement)) {
                return {map[complement], i};
            }

            map[nums[i]] = i;
        }

        return {}; // shouldn't reach here
    }
};
```

---

## 🟢 Output

```cpp
Input: nums = [1, 7, 5, 2], target = 9
Output: [1, 3]
Explanation: nums[1] + nums[3] = 7 + 2 = 9
```

---

## 🔁 Time & Space Complexity

* Time: O(n)
* Space: O(n) for the map

---

## 🚀 Notes

* `unordered_map` gives O(1) average lookup.
* Map stores only numbers we’ve **seen so far**, not future ones.

```

---

Let me know if you want this as a **downloadable `.md` file** or want me to walk you through another similar hashmap-based problem like Anagram, Ransom Note, etc.

🔥 You’ve mastered this bro — ready for next one anytime.
```

Absolutely bro! 💯
Here’s your complete **WhatsApp-style easy explanation** in a clean **README.md** format — with:

* 🔍 Problem
* 🧠 Approach
* 📊 Iteration Table
* ✅ Final C++ Code
* 🎉 Output & Summary

---

### 📁 File Name: `valid_anagram_solution.md`

````md
# 🔤 LeetCode 242: Valid Anagram (C++ with unordered_map)

## 🔍 Problem Statement

Check if two strings `s` and `t` are anagrams of each other.

✅ Anagram = Same letters, same count, different order is OK.  
❌ If any letter extra/missing → Not anagram.

---

## 🧠 Logic (WhatsApp-style Language)

- Tu `s` string ke sab letters ko **count kar map me store** kar.
- Fir `t` ke letters ko **map me se minus kar**.
- Agar kisi letter ka count **0 se neeche gaya**, toh `t` me extra letter hai ❌
- Agar sab balance ho gaye → ✅ s & t are anagrams.

---

## 🧪 Example Input

```cpp
s = "aabb"
t = "baba"
````

---

## 📊 Iteration Table

### 🔹 Step 1: Count characters from `s`

| Step | Char from `s` | Map after addition |
| ---- | ------------- | ------------------ |
| 1    | a             | `{a:1}`            |
| 2    | a             | `{a:2}`            |
| 3    | b             | `{a:2, b:1}`       |
| 4    | b             | `{a:2, b:2}` ✅     |

---

### 🔹 Step 2: Subtract characters from `t`

| Step | Char from `t` | Map after subtraction | What Happened?            |
| ---- | ------------- | --------------------- | ------------------------- |
| 1    | b             | `{a:2, b:1}`          | b mil gaya, -1 kiya       |
| 2    | a             | `{a:1, b:1}`          | a mil gaya, -1 kiya       |
| 3    | b             | `{a:1, b:0}`          | b again mil gaya, -1 kiya |
| 4    | a             | `{a:0, b:0}` ✅        | a mil gaya, done          |

✔️ Final map values are zero → So it's an **Anagram**

---

## ✅ Final C++ Code

```cpp
#include <iostream>
#include <unordered_map>
#include <string>
using namespace std;

class Solution {
public:
    bool isAnagram(string s, string t) {
        if (s.length() != t.length()) return false;

        unordered_map<char, int> freq;

        // Step 1: Count characters in s
        for (char c : s) {
            freq[c]++;
        }

        // Step 2: Subtract characters in t
        for (char c : t) {
            freq[c]--;
            if (freq[c] < 0) return false;
        }

        return true;
    }
};
```

---

## 🎉 Output

```cpp
Input: s = "aabb", t = "baba"
Output: true ✅

Input: s = "rat", t = "car"
Output: false ❌
```

---

## ⏱ Time & Space Complexity

* Time: O(n)
* Space: O(1) (only 26 characters max in alphabet)

---

## 💬 Summary in 1 Line (Easy Language)

👉 Pehle count karo `s` ke letters
👉 Fir cancel karo `t` ke letters
👉 Sab balance ho gaye? → ✅ It's anagram

---

```

---
Absolutely bro 🔥 You've got the logic perfect — just one **tiny typo** in your code (`vactor` ➝ `vector`), otherwise it's solid!

Here’s your **clean, final `.md` file** with:

* ✅ Full working C++ code
* 🧠 Logic summary
* 📊 Comparison chart between `set`, `unordered_set`, and `unordered_map`

---

### ✅ `349. Intersection of Two Arrays` — LeetCode Solution

```cpp
// ✅ Approach: Use unordered_set to ensure uniqueness and fast lookup

#include <iostream>
#include <unordered_set>
#include <vector>
using namespace std;

class Solution {
public:
    vector<int> intersection(vector<int>& nums1, vector<int>& nums2) {
        unordered_set<int> set1(nums1.begin(), nums1.end());  // Step 1: Store unique nums1 elements
        unordered_set<int> result;                            // Step 2: Store the final result

        for (int num : nums2) {
            if (set1.count(num)) {                            // Step 3: If num exists in set1
                result.insert(num);                           // Add to result (auto handles uniqueness)
            }
        }

        return vector<int>(result.begin(), result.end());     // Step 4: Convert set to vector and return
    }
};
```

---

### 🧠 Logic Recap

| Step | What Happens                                                     |
| ---- | ---------------------------------------------------------------- |
| 1    | Add all elements of `nums1` to a `unordered_set` (unique & fast) |
| 2    | Create an empty set for the result                               |
| 3    | For every number in `nums2`, check if it exists in `set1`        |
| 4    | If yes, insert it into result set (auto-unique)                  |
| 5    | Convert the set to a vector to match return type                 |

---

### 📊 Comparison Table: Set vs Unordered\_Set vs Unordered\_Map

| Feature            | `set`                | `unordered_set`            | `unordered_map`              |
| ------------------ | -------------------- | -------------------------- | ---------------------------- |
| Ordered?           | ✅ Yes (sorted order) | ❌ No (no guaranteed order) | ❌ No                         |
| Stores             | Only keys (unique)   | Only keys (unique)         | Key-Value pairs              |
| Lookup Time        | O(log n)             | ✅ O(1) average             | ✅ O(1) average               |
| Duplicate Handling | ❌ Not allowed        | ❌ Not allowed              | ❌ Key duplicates not allowed |
| Use Case           | When you need order  | ✅ Fast lookup & uniqueness | When you need mapping        |

---

### 🧾 Sample Input & Output

```cpp
Input: nums1 = [1,2,2,1], nums2 = [2,2]
Output: [2]

Input: nums1 = [4,9,5], nums2 = [9,4,9,8,4]
Output: [4,9] or [9,4]
```

---

You're 100% ready to commit this to GitHub bro! 👑
## 387. First Unique Character in a String

### ✅ Problem Summary

Given a string `s`, return the **index** of the **first non-repeating character**. If there is no such character, return `-1`.

### 🔧 Approach: Hash Map + Two Passes

We will:

1. Use an `unordered_map<char, int>` to count character frequencies.
2. Loop through the string again to find the first character with frequency `1`.

This approach ensures **O(n)** time complexity, where `n` is the length of the string.

---

### ✅ C++ Code (with comments)

```cpp
#include <iostream>
#include <unordered_map>
#include <string>
using namespace std;

class Solution {
public:
    int firstUniqChar(string s) {
        unordered_map<char, int> freq; // Step 1: Create frequency map

        // Step 2: Count frequency of each character
        for (char c : s) {
            freq[c]++;
        }

        // Step 3: Find the first character with frequency = 1
        for (int i = 0; i < s.length(); i++) {
            if (freq[s[i]] == 1) {
                return i;
            }
        }

        return -1; // Step 4: No unique character found
    }
};
```

---

### 🧠 Code Explanation (Line-by-Line Table)

| Code Line                              | What It Does                                      |
| -------------------------------------- | ------------------------------------------------- |
| `unordered_map<char, int> freq;`       | Create a map to store frequency of each character |
| `for (char c : s)`                     | Loop through string `s` character by character    |
| `freq[c]++;`                           | Count how many times each character appears       |
| `for (int i = 0; i < s.length(); i++)` | Loop through string again using index             |
| `if (freq[s[i]] == 1)`                 | Check if current character is non-repeating       |
| `return i;`                            | Return index of the first non-repeating character |
| `return -1;`                           | Return -1 if no unique character was found        |

---

### 🔁 Iteration Table: `s = "loveleetcode"`

#### Frequency Map After First Loop:

| Character | Frequency |
| --------- | --------- |
| l         | 1         |
| o         | 2         |
| v         | 1         |
| e         | 3         |
| t         | 1         |
| c         | 1         |
| d         | 1         |

#### Second Loop Execution:

| Index (`i`) | `s[i]` | `freq[s[i]]` | Condition (`== 1`) | Action           |
| ----------- | ------ | ------------ | ------------------ | ---------------- |
| 0           | l      | 1            | ✅ true             | return 0         |
| 1           | o      | 2            | ❌ false            | skip             |
| 2           | v      | 1            | ✅ (not reached)    | already returned |

Result: ✅ Output is `0`

---

### 🏁 Final Notes:

* This method guarantees **correctness and efficiency**.
* You could use `vector<int>` for fixed 26 letters, but `unordered_map` is more flexible.
* Loop once to build the map, once to find the result: **O(n)** overall.
## 389. Find the Difference

### ✅ Problem Summary

You are given two strings `s` and `t`. String `t` is generated by shuffling string `s` and then adding one more letter at a random position.

Your task is to return the letter that was added to `t`.

### 🧪 Examples:

```txt
Input: s = "abcd", t = "abcde"
Output: "e"

Input: s = "", t = "y"
Output: "y"
```

---

### 🔧 Approach: Use `unordered_map<char, int>` to Track Frequencies

We can solve this by:

1. Counting each character in `s`
2. Decreasing the count using characters from `t`
3. The character that ends up with a **negative count** is the extra one

This is efficient with **O(n)** time and **O(1)** space (only 26 lowercase letters).

---

### ✅ C++ Code (with Comments)

```cpp
#include <iostream>
#include <unordered_map>
#include <string>
using namespace std;

class Solution {
public:
    char findTheDifference(string s, string t) {
        unordered_map<char, int> freq;

        // Step 1: Count characters in s
        for (char c : s) {
            freq[c]++;
        }

        // Step 2: Subtract counts using characters in t
        for (char c : t) {
            freq[c]--;

            // Step 3: If count goes below 0, it's the added character
            if (freq[c] < 0) {
                return c;
            }
        }

        return ' '; // should never reach here if input is valid
    }
};
```

---

### 🧠 Code Breakdown (Line-by-Line Table)

| Code Line                        | What It Does                                           |
| -------------------------------- | ------------------------------------------------------ |
| `unordered_map<char, int> freq;` | Create map to count frequency of each character in `s` |
| `for (char c : s)`               | Loop through each character of string `s`              |
| `freq[c]++;`                     | Count how many times each character appears in `s`     |
| `for (char c : t)`               | Loop through each character in `t`                     |
| `freq[c]--;`                     | Subtract 1 for each character seen in `t`              |
| `if (freq[c] < 0)`               | If count becomes negative, it's the extra character    |
| `return c;`                      | Return that extra character immediately                |

---

### 🔁 Dry Run: `s = "abcd"`, `t = "abcde"`

| Step | Character | freq before | freq after | Action         |
| ---- | --------- | ----------- | ---------- | -------------- |
| +    | a         | 0           | 1          | add count      |
| +    | b         | 0           | 1          | add count      |
| +    | c         | 0           | 1          | add count      |
| +    | d         | 0           | 1          | add count      |
| -    | a         | 1           | 0          | subtract       |
| -    | b         | 1           | 0          | subtract       |
| -    | c         | 1           | 0          | subtract       |
| -    | d         | 1           | 0          | subtract       |
| -    | e         | 0           | -1         | **return 'e'** |

---

### 🏁 Final Notes:

* This solution uses `unordered_map` for fast lookup
* It handles any string order
* Time Complexity: **O(n)**
* Space Complexity: **O(1)** (constant characters a-z)
