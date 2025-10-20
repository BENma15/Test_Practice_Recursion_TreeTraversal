# Binary Tree Traversal Example

This folder contains a simple Binary Tree Traversal implementation

## Files

- `tree_traversal_example.cpp` - TODO: Implement the recursive `Traversal` function
- `tree_traversal_example_answer.cpp` - Complete solution
- `Makefile` - Build configuration for easy compilation
- `.vscode/` - VS Code debugging configuration

## Usage

### Compilation
```bash
make
```

### Running
```bash
./tree_traversal_example
```

### Debugging in VS Code

1. Open the `tree_traversal` folder in VS Code
2. Set breakpoints in the code by clicking in the left margin
3. Press F5 or go to Run → Start Debugging
4. The debugger will build and run the program

## Function
The `Traversal(TreeNode* node)` function performs inorder traversal of a binary tree using recursion.

### Step-by-Step Implementation Instructions

1. **Base Case**:  
   - If the current node (`node`) is `nullptr`, return (end of branch).

2. **Inorder Traversal Pattern**:  
   - Recursively traverse the **left** subtree.
   - Process the current node: `std::cout << node->data << " ";`
   - Recursively traverse the **right** subtree.

## Example

The program builds this binary tree:
```
       4
      / \
     2   6
    / \ / \
   1  3 5  7
```

### Expected Output
```
Inorder Traversal (recursive):
=============================
1 2 3 4 5 6 7
```

### Example Trace: Inorder traversal

```
Traversal(4):
├─ Traversal(2):
│  ├─ Traversal(1):
│  │  ├─ Traversal(nullptr) → return
│  │  ├─ print(1) → "1 "
│  │  └─ Traversal(nullptr) → return
│  ├─ print(2) → "2 "
│  └─ Traversal(3):
│     ├─ Traversal(nullptr) → return
│     ├─ print(3) → "3 "
│     └─ Traversal(nullptr) → return
├─ print(4) → "4 "
└─ Traversal(6):
   ├─ Traversal(5):
   │  ├─ Traversal(nullptr) → return
   │  ├─ print(5) → "5 "
   │  └─ Traversal(nullptr) → return
   ├─ print(6) → "6 "
   └─ Traversal(7):
      ├─ Traversal(nullptr) → return
      ├─ print(7) → "7 "
      └─ Traversal(nullptr) → return
```
