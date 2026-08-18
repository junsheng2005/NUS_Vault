# Basic Matrix Commands

| **Command**  | **Description**               |
| ------------ | ----------------------------- |
| `>> A+B`     | matrix addition               |
| `>> A-B`     | matrix subtraction            |
| `>> c*A`     | scalar multiplication         |
| `>> A*B`     | matrix multiplication         |
| `>> A^n`     | n-th power of A               |
| `>> A'`      | transpose of A                |
| `>> inv(A)`  | inverse of A                  |
| `>> det(A)`  | determinant of A              |
| `>> rref(A)` | reduced row echelon form of A |

# Matrix Manipulation

| **Command**                   | **Description**                              |
| ----------------------------- | -------------------------------------------- |
| `>> A(2, 3)`                  | Extracting entries from a matrix             |
| `>> A(2, :)`                  | Extracting rows from a matrix                |
| `>> A(:, 3)`                  | Extracting columns from a matrix             |
| `>> A([1:2], [2:3])`          | Submatrix                                    |
| <br>`>> [A B]`<br>`>> [A; B]` | Merging matrices<br>Left-Right<br>Top-Bottom |

> [!NOTE] Note
> `>>rref([A B])` to find reduced row echelon form of augmented matrix $(\boldsymbol{A}|\boldsymbol{B})$


