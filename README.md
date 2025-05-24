# LinkedListDeque – Double-Ended Queue in Java

🧠 **Project:** Linked List-Based Deque Implementation  
🧰 **Language:** Java (Generics, Inner Classes)  
🎯 **Focus:** Data Structures, OOP, Test-Driven Development

---

## 📌 Overview

This project implements a **double-ended queue (deque)** using a custom **doubly-linked list** structure in Java. The deque allows insertion and removal of elements from both ends in constant time and is generic, supporting any data type.

Rather than relying on Java’s built-in data structures, this implementation was built completely from scratch, focusing on object-oriented design, manual memory handling (via reference unlinking), and full unit test coverage.

---

## 🚀 Features Implemented

### Core Deque Operations:
| Method | Description |
|--------|-------------|
| `addFirst(T item)` | Adds item to the front |
| `addLast(T item)` | Adds item to the back |
| `removeFirst()` | Removes and returns the item at the front |
| `removeLast()` | Removes and returns the item at the back |
| `get(int index)` | Gets item at index using iteration |
| `getRecursive(int index)` | Gets item at index using recursion |
| `isEmpty()` | Returns whether the deque is empty |
| `size()` | Returns the number of items in the deque |
| `toList()` | Returns contents as a `List<T>` for testing/inspection |

---

## ⚙️ Internal Structure

The deque is implemented using a **circular sentinel-based doubly-linked list**, which simplifies edge case handling (like inserting/removing from empty or single-element lists).

```java
private class Node {
    T item;
    Node prev;
    Node next;
}
