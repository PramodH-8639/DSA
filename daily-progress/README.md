# DSA Daily Progress

## LeetCode 237 — Delete Node in a Linked List

**Topic:** Linked List  
**Difficulty:** Medium

### 🧩 Problem

Given a node in a singly linked list, delete that node.

The important point is that we are **not given the head of the linked list**.

### 💡 Approach

We cannot directly remove the given node because we don't have access to the previous node.

Instead:

1. Copy the value of the next node into the current node.
2. Make the current node point to the node after the next node.

### 🔍 Example

Before:

`5 → 9 → 7`

If we need to delete `5`:

`9 → 7`

We achieve this by:

```java
node.val = node.next.val;
node.next = node.next.next;
```
