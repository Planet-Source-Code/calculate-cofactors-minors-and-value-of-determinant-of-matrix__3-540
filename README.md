<div align="center">

## Calculate Cofactors, Minors, and value of Determinant of Matrix


</div>

### Description

This piece of code calculates the cofactors, the minors, and the value of the determinant of a 3x3 matrix with just one line of code each within a loop! Can't make it any shorter!
 
### More Info
 
matrix[3][3] - containg the values of the matrix

cofactor[3][3] - containing the value of cofactors corresponding to the values in matrix array.

minor[3][3] - containing the value of minors

determinant - containing the value of the determinant.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[N/A](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/empty.md)
**Level**          |Beginner
**User Rating**    |3.7 (22 globes from 6 users)
**Compatibility**  |C, C\+\+ \(general\)
**Category**       |[Math](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math__3-12.md)
**World**          |[C / C++](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/calculate-cofactors-minors-and-value-of-determinant-of-matrix__3-540/archive/master.zip)





### Source Code

```
/*	The author of this piece of code is Rahul Khanna
	<rahulk@techie.com>
	Use this code at your own risk.
*/
/*	This piece of code demonstrates how you can calculate
	the cofactors, minors and the value of a 3x3 determinant
	itself with the smallest possible code. The cofactor, and
	minors are calculated in one line of code each! Can you
	make it any smaller?
*/
/*	Assuming there is an array "matrix[3][3]" that contains
	the values of the matrix in the format rows x columns.
	The cofactors of the repective matrix element is stored
	in its position values in the array "cofactor". Eg, cofactor
	of array element matrix[1][1] will be stored in cofactor[1][1].
	Same as above with minors.
*/
long row, col;
long matrix[3][3];
long cofactor[3][3], minor[3][3];
long determinant = 0;
for (row = 0; row < 3; row++)
{
	for (col = 0; col < 3; col++)
	{
		cofactor[row][col] = matrix[(row + 1) % 3][(col + 1) % 3] * matrix[(row + 2) % 3][(col + 2) % 3] - matrix[(row + 1) % 3][(col + 2) % 3] * matrix[(row + 2) % 3][(col + 1) % 3];
		minor[row][col] = (row + col) % 2 == 0 ? cofactor : -cofactor;
		if (row == 0)
			determinant += matrix[0][col] * cofactor;
	}
}
```

