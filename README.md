# LeetCode 206 - Reverse Linked List

## Problem Description

Given the head of a singly linked list, reverse the linked list and return the new head.

For example, if the linked list is:

1 → 2 → 3 → 4 → 5

After reversing it becomes:

5 → 4 → 3 → 2 → 1

## Example

Input:

head = [1,2,3,4,5]

Output:

[5,4,3,2,1]

## Approach

We reverse the linked list by changing the direction of each node's `next` pointer.

Two pointers are used:

- `previous` stores the previous node.
- `current` stores the node currently being processed.

Before changing the `next` pointer, we store the next node in `next_node`. This prevents losing the remaining part of the linked list.

Then we make the current node point to the previous node and move both pointers forward.

When the traversal is complete, `previous` becomes the new head of the reversed linked list.

## Algorithm

1. Set `previous` to `None`.
2. Set `current` to `head`.
3. Store the next node before changing the link.
4. Reverse the current node's pointer.
5. Move `previous` and `current` one step forward.
6. Continue until `current` becomes `None`.
7. Return `previous` as the new head.

## Time Complexity

**O(n)**

Each node is visited exactly once.

## Space Complexity

**O(1)**

Only a few pointer variables are used, so no extra space is required based on the size of the linked list.

## Key Concepts

- Linked List
- Pointers
- Traversal
- In-place Reversal
- `next` Pointer

## Author

T.nandhini
