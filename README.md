# 📂 Tree Structure Console Application

This project is a **C# console application** that demonstrates how to build and traverse a **generic tree data structure** to represent a file system hierarchy. The program prints directories and files in an **ASCII tree format**, allows searching for specific nodes, and highlights the results.

---

## 📌 Features
- Build a tree structure with parent/child relationships.  
- Print the hierarchy in ASCII style (`+--`, `|--`).  
- Search for a specific file/folder in the tree.  
- Highlight the found node in square brackets `[ ]`.

---

## 🛠️ Technologies Used
- **Language**: C#  
- **Framework**: .NET (Console Application)  
- **Libraries / Namespaces**:
  - System → Console I/O  
  - System.Collections.Generic → Tree nodes and child lists  
  - System.Linq, System.Text, System.Threading.Tasks → included by default  

---

## 🖥️ Example Output

C:
+-- Users
| +-- Alice
| | +-- Documents
| | | +-- report.docx
+-- Program Files
| +-- Microsoft
| +-- Google
+-- Windows

--- After Highlight ---
C:
+-- Users
| +-- Alice
| | +-- Documents
| | | +-- [report.docx]
+-- Program Files
| +-- Microsoft
| +-- Google
+-- Windows


---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/prjTreeExample2.git
2. Open the project in Visual Studio or VS Code.
3. Build and run the console application.


---
## 📖 Learning Outcomes

- Understanding of tree data structures in C#.
- Recursive traversal and search in hierarchical data.
- ASCII-based visualization of trees.

## 📊 UML Class Diagram

```mermaid
classDiagram
    class TreeNode~T~ {
        +T Data
        +TreeNode~T~ Parent
        +List~TreeNode<T>~ Children
    }

    class Tree~T~ {
        +TreeNode~T~ Root
        +void PrintTree(TreeNode~T~ node, string indent, bool last)
        +TreeNode~T~ FindNode(TreeNode~T~ node, T value)
        +void PrintTree(TreeNode~T~ node, TreeNode~T~ highlightNode, string indent, bool last)
    }

    Tree~T~ "1" --> "1" TreeNode~T~ : Root
    TreeNode~T~ "1" --> "*" TreeNode~T~ : Children
    TreeNode~T~ --> TreeNode~T~ : Parent


