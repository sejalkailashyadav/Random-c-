
---

### 🔰 **Basic Set Questions (Step 1)**

#### 1. Insert and Print (Warm-up)

> Insert these numbers into a set: `4, 2, 7, 2, 5`. Print the set.

🧠 Expect: No duplicates, sorted output.

---

#### 2. Insert from Array

> Given an array `arr = {3, 1, 4, 1, 5, 9, 2, 6, 5}`, insert all elements into a set and print them.

🎯 Goal: Practice using loop + `set.insert()`.

---

#### 3. Insert Random Order

> Insert: `10, 1, 7, 6, 2, 2, 10, 4` into a set.
> Then print the elements in sorted order.

---

#### 4. Count Unique Numbers

> Given a vector of numbers, use a set to count **how many unique elements** are in it.

Example:

```cpp
vector<int> nums = {5, 5, 7, 8, 8, 9};
```

Expected: 3 unique numbers → Output: `3`

---

#### 5. Is the Set Empty?

> Create an empty set and check:

* Is it empty?
* Then insert 3 values and print the size.

---


#include <iostream>
#include <set>
#include <vector>
using namespace std;

int main() {
    vector<int> arr = {3, 1, 4, 1, 5, 9, 2, 6, 5};
    set<int> s;

    for (int val : arr) {
        s.insert(val);
    }

    for (int val : s) {
        cout << val << " ";
    }

    return 0;
}

//Insert Random Order
//Insert: 10, 1, 7, 6, 2, 2, 10, 4 into a set.
//Then print the elements in sorted order.
#include <iostream>
#include <set>
#include <vector>
using namespace std;

int main() {
    vector<int> v = {10, 1, 7, 6, 2, 2, 10, 4};
    set<int> s;

    for (int val : v) {
        s.insert(val);
    }

    cout << "Sorted set: ";
    for (int val : s) {
        cout << val << " ";
    }

    return 0;
}


//Count Unique Numbers Given a vector of numbers,
// // use a set to count how many unique elements are in it.

#include <iostream>
#include <set>
#include <vector>
using namespace std;

int main() {
    vector<int> v = {10, 1, 7, 6, 2, 2, 10, 4};
    set<int> s;

    for (int val : v) {
        s.insert(val);
    }

    cout << "Unique element count: " << s.size() << endl;

    return 0;
}


// Is the Set Empty?Create an empty set and checkIs it empty?Then insert 3 values and print the size.

#include <iostream>
#include <set>
using namespace std;

int main() {
    set<int> s;

    if (s.empty()) {
        cout << "Set is empty initially.\n";
    }

    s.insert(5);
    s.insert(10);
    s.insert(15);

    cout << "Set size after inserting 3 values: " << s.size() << endl;

    return 0;
}

---
