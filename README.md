# CM2035 Algorithms and Data Structures II - University of London

Coursework for **CM2035 Algorithms and Data Structures II** (BSc Computer Science, University of London). The project is a command-line **postfix calculator** in JavaScript (Node.js) that uses the same problem to compare several classic data structures and algorithms.

| Assessment | Project | Key topics |
|---|---|---|
| Mid Term | Postfix calculator with symbol tables | Stacks, expression trees, BST, direct addressing, hash tables, sorting algorithms |

**Tech:** JavaScript · Node.js (`readline` for interactive menus)

---

## Postfix Calculator with Symbol Tables

An interactive console program with a main menu that leads into two parts.

### Part 1: Arithmetic operations
- Evaluates **postfix (Reverse Polish) expressions** with a stack
- Shows the stack contents sorted with the user's choice of **five sorting algorithms**:
  - Bubble sort
  - Insertion sort
  - Selection sort
  - Merge sort
  - Quick sort
- Sorting runs on a copy of the stack, so it's for display only and never affects the calculation

### Part 2: Symbol tables
Variables (`A`–`Z`) can be assigned, searched, deleted, and used inside postfix expressions. The same symbol table is built four different ways:

| Program | Data structure | What it shows |
|---|---|---|
| Inorder traversal | **Expression tree** | Builds a tree from postfix input and prints the fully parenthesised infix form |
| Binary search | **Binary search tree** | Insert, search, and delete (including finding the minimum for two-child deletes), with sorted output |
| Direct addressing | **Array indexed A–Z** | O(1) lookup by mapping each letter straight to an index |
| Hash table | **Hash table** | Hash-based insert, search, and delete, with sorted display of the stored variables |

### Robustness
- Validates operators and variable names, and rejects anything that isn't `A`–`Z`
- Error messages for invalid input, with the menu shown again instead of crashing
- Each program links back to the main menu

---

## How to run

```bash
cd endterm
node main.js
```
Requires Node.js. There are no external packages to install.
