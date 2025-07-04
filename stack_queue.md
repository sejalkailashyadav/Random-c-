⚔️ Let's go, Samurai! Time to unlock your next C++ weapon.

You’ve mastered:
✅ `map`, `unordered_map`, `set`, `unordered_set`

---

### 🧱 Next Logical Topic: **Stack & Queue**

Let’s start with:

---

## 🔄 1. **Stack in C++**

### 📌 What is it?

* **LIFO**: Last In, First Out
* Like a **stack of plates** — last one placed is the first removed.

### 💡 Common Use Cases:

* Valid Parentheses `(){}[]`
* Undo feature
* Backtracking (like maze, recursion trace)
* DFS (Depth-First Search)

---

### 🛠️ C++ Code Example:

```cpp
#include <iostream>
#include <stack>
using namespace std;

int main() {
    stack<int> s;

    s.push(10);
    s.push(20);
    s.push(30);

    cout << "Top element: " << s.top() << endl; // 30

    s.pop(); // removes 30

    cout << "New top: " << s.top() << endl; // 20

    cout << "Is stack empty? " << (s.empty() ? "Yes" : "No") << endl;

    return 0;
}
```

---

### 🔍 Stack Functions:

| Operation | Meaning                 |
| --------- | ----------------------- |
| `push(x)` | Insert element          |
| `pop()`   | Remove top element      |
| `top()`   | Get top element         |
| `empty()` | Check if stack is empty |
| `size()`  | Stack size              |

---
Absolutely bro! ⚔️ Here's your clean, ready-to-save **C++ STL Resume for `stack` and `queue`**, with:

✅ All methods
✅ Example usage
✅ Easy-to-read layout

---

## 📄 C++ STL Stack & Queue Cheat Sheet (Samurai Resume Style)

```cpp
#include <iostream>
#include <stack>
#include <queue>
using namespace std;

int main() {
    // ---------- STACK ----------
    stack<int> s;

    // ✅ Push elements
    s.push(10);
    s.push(20);
    s.push(30);

    // ✅ Top element (last pushed)
    cout << "Stack Top: " << s.top() << endl; // 30

    // ✅ Pop element
    s.pop(); // removes 30

    // ✅ Check if empty
    cout << "Is stack empty? " << (s.empty() ? "Yes" : "No") << endl;

    // ✅ Size of stack
    cout << "Stack Size: " << s.size() << endl;

    cout << "------" << endl;

    // ---------- QUEUE ----------
    queue<int> q;

    // ✅ Push elements
    q.push(1);
    q.push(2);
    q.push(3);

    // ✅ Front element
    cout << "Queue Front: " << q.front() << endl; // 1

    // ✅ Back element
    cout << "Queue Back: " << q.back() << endl; // 3

    // ✅ Pop element (from front)
    q.pop(); // removes 1

    // ✅ Check if empty
    cout << "Is queue empty? " << (q.empty() ? "Yes" : "No") << endl;

    // ✅ Size of queue
    cout << "Queue Size: " << q.size() << endl;

    return 0;
}
```

---

## 🧠 Stack Methods Summary:

| Method    | Description                     |
| --------- | ------------------------------- |
| `push(x)` | Insert element on top           |
| `pop()`   | Remove top element              |
| `top()`   | Access top element              |
| `empty()` | Check if stack is empty         |
| `size()`  | Number of elements in the stack |

---

## 🧠 Queue Methods Summary:

| Method    | Description                     |
| --------- | ------------------------------- |
| `push(x)` | Add element to back             |
| `pop()`   | Remove front element            |
| `front()` | Access front element            |
| `back()`  | Access last element             |
| `empty()` | Check if queue is empty         |
| `size()`  | Number of elements in the queue |

---
Absolutely bro! ⚔️ Here’s your **LeetCode Warrior List** — handpicked problems based on what you’ve learned with `stack` and `queue` so far.

---

## 📚 **LeetCode Problems: Stack + Queue Based**

### ✅ **Beginner – Core Stack Problems**

| Problem                                                                         | Name                                     |
| ------------------------------------------------------------------------------- | ---------------------------------------- |
| [20](https://leetcode.com/problems/valid-parentheses/)                          | Valid Parentheses                        |
| [155](https://leetcode.com/problems/min-stack/)                                 | Min Stack                                |
| [682](https://leetcode.com/problems/baseball-game/)                             | Baseball Game                            |
| [844](https://leetcode.com/problems/backspace-string-compare/)                  | Backspace String Compare                 |
| [1047](https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string/) | Remove All Adjacent Duplicates In String |

---

### ✅ **Beginner – Core Queue Problems**

| Problem                                                               | Name                            |
| --------------------------------------------------------------------- | ------------------------------- |
| [933](https://leetcode.com/problems/number-of-recent-calls/)          | Number of Recent Calls          |
| [346](https://leetcode.com/problems/moving-average-from-data-stream/) | Moving Average from Data Stream |
| [641](https://leetcode.com/problems/design-circular-deque/)           | Design Circular Deque           |
| [225](https://leetcode.com/problems/implement-stack-using-queues/)    | Stack using Queues              |
| [232](https://leetcode.com/problems/implement-queue-using-stacks/)    | Queue using Stacks              |

---

### 🔁 **Stack + Queue Combo Problems**

| Problem                                                                | Name                             |
| ---------------------------------------------------------------------- | -------------------------------- |
| [239](https://leetcode.com/problems/sliding-window-maximum/)           | Sliding Window Maximum           |
| [496](https://leetcode.com/problems/next-greater-element-i/)           | Next Greater Element I           |
| [503](https://leetcode.com/problems/next-greater-element-ii/)          | Next Greater Element II          |
| [150](https://leetcode.com/problems/evaluate-reverse-polish-notation/) | Evaluate Reverse Polish Notation |

---

