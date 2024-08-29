
## Aim
Create a matrix by taking user inputs and perform various operations on it.

## Software Used
- VS Code

## Problem Statement

1. **Matrix Creation**
   - Prompt the user to enter the number of rows and columns.
   - Generate a matrix based on the provided dimensions.

2. **Matrix Addition and Multiplication**
   - Create two matrices by taking user inputs.
   - Perform addition and multiplication of these matrices.
   - Ensure that the number of columns in the first matrix equals the number of rows in the second matrix for multiplication.

3. **Diagonal Elements**
   - Calculate and return the sum of the diagonal elements of a matrix.

4. **Matrix Transpose**
   - Compute and return the transpose of a matrix, which involves swapping its rows and columns.

## Theory

- **Arrays**: Arrays are data structures that store a collection of items of the same data type at contiguous memory locations. They can be one-dimensional or multidimensional. This project focuses on two-dimensional arrays (matrices).

- **Matrix Multiplication**: For two matrices to be multiplied, the number of columns in the first matrix must equal the number of rows in the second matrix. An error is displayed if this condition is not met.

- **Matrix Addition**: Matrix addition involves combining two matrices of the same dimensions to form a new matrix where each element is the sum of corresponding elements from the input matrices.

## Program Codes

```javascript
//Mukesh Rothe  //23070123089  //EXP8
#include <iostream>
using namespace std;

int main() {
    int rows, cols, i, j;

    cout << "Enter number of rows: ";
    cin >> rows;
    cout << "Enter number of columns: ";
    cin >> cols;

    int matrix[rows][cols];

    cout << "Enter elements of matrix:" << endl;
    for (i = 0; i < rows; i++) {
        for (j = 0; j < cols; j++) {
            cout << "Enter element [" << i + 1 << "," << j + 1 << "]: ";
            cin >> matrix[i][j];
        }
    }

    cout << "Entered Matrix:" << endl;
    for (i = 0; i < rows; i++) {
        for (j = 0; j < cols; j++) {
            cout << matrix[i][j] << " ";
            if (j == cols - 1)
                cout << endl;
        }
    }

    return 0;
}

//Mukesh Rothe  //23070123089  //EXP8
#include<iostream>
using namespace std;
int main()
{
    int a,b,c,d , i , j ,k , e, f;
    cout<< "Enter Matrix-1 rows: ";
    cin>> a ;
    cout<<"Enter Matrix-1 columns: ";
    cin>> b;
    cout<<"Enter Matrix-2 rows: ";
    cin>> c ;
    cout<<"Enter Matrix-2 columns: ";
    cin>> d;

    int mat1[a][b];
    int mat2[c][d];
    int add[a][b];
    int multi[a][d];
    
 if ( a!=c || b!=d)
    {  cout<< "Matrix cannot be added as dimension do not match."<<endl;
    }
  else
{cout<<"Enter Matrix-1 elements"<<endl;
 for (i=0 ; i < a ; i++)
    {
        for(j = 0 ; j < b ; j++)
        {   cout<< "Enter elements- ("<<i<< "," <<j<<"): "  ;
            cin>>mat1[i][j];
        }
    }

cout<<"Enter Matrix-2 elements"<<endl;
    for (i=0 ; i < c ; i++)
    {
        for(j = 0 ; j < d ; j++)
        {   cout<< "Enter elements- ("<<i<< "," <<j<<"): "  ;
            cin>>mat2[i][j];
        }
    }

for (i=0 ; i < a ; i++)
    {
        for(j = 0 ; j < b ; j++)
        {  add[i][j] = mat1[i][j] + mat2 [i][j];
        }
    }
cout<<"Addition of Matrix: "<<endl;
for (i=0 ; i< a ; i++)
{
    for(j = 0; j< b ; j++ )
    { cout<< " " <<add[i][j];
    }
    cout<<endl;
}}

    if( b != c)
{   cout<< "Matrices cannot be multiplied as dimensions do not match." <<endl;
    return 1;
}
for(i = 0; i<a ; i++)
{
    for( j = 0; j<d ; j++)
    {
        multi[i][j] = 0;
        for( k=0; k<b ; k++)
        {
            multi[i][j] += mat1[i][k] * mat2[k][j];
        }
    }
}
cout << "Multiplication of Matrix: "<<endl;
for (i=0 ; i< a ; i++)
{
    for(j = 0; j< b ; j++ )
    {  cout<< " " <<multi[i][j];
    }
    cout<<endl;
}
}

//Mukesh Rothe  //23070123089  //EXP8
#include<iostream>
using namespace std;
int main()

{ int i,j, r1, c1, sum=0, sum2=0;
 cout<<"Enter number of rows and columns of first matrix: ";
cin>>r1>>c1;
int mat1[r1][c1];

if(r1!=c1)
{
    cout<<"Only square matrices are to be entered!"<<endl;
}
else
{
for(i=0; i<r1; i++)
{
    for (j=0 ; j<c1 ; j++)
    {
        cout<<"Enter elements ("<<i<< "," <<j<<"): ";
        cin>>mat1[i][j];
    }
}


for(i=0; i<r1; i++)
{
    for (j=0 ; j<c1 ; j++)
    { if(i==j)
    {
        sum +=mat1[i][j];
    }
    if (i+j == r1-1)
    sum2 += mat1[i][j];
    }
    }
    cout<<"Sum of diagonal elements is: "<<sum<<endl;
    cout<<"Sum of diagonal elements is: "<<sum2<<endl;
}

}

//Mukesh Rothe  //23070123089  //EXP8
#include<iostream>
using namespace std;
int main()
{
    int r,c , i , j;
    cout<< " Enter number of rows: ";
    cin>> r;
    cout<<" Enter number of columns: ";
    cin>> c;
    int arr[r][c], arr2[c][r];
    for (i=0 ; i < r ; i++)
    {
        for(j = 0 ; j < c ; j++)
        {
            cout<< "Enter elements ("<<i<< "," <<j<<"): "  ;
            cin>>arr[i][j];
        }
    }
for (i=0 ; i<r ; i++)
{
    for(j = 0; j< c ; j++ )
    { 
        cout<< "  "<< arr[i][j];
    }
    cout<<endl;
}
for (i=0 ; i<c ; i++)
{
    for(j = 0; j< r ; j++ )
    { 
        arr2[i][j]= arr[j][i];
    }

    
}
cout<<endl;
for (i=0 ; i<c ; i++)
{
    for(j = 0; j< r ; j++ )
    { 
        cout<< " "<< arr2[i][j];
    }
    cout<<endl;
}

}
```


## Output
Matrix-

Matrix Add-Multiply-

Matrix Diagonal Sum-

Matrix Transpose-



## Conclusion

In this project, we:
- Took user input to create matrices.
- Implemented matrix addition and multiplication using loops.
- Computed the sum of the diagonal elements of a matrix.
- Calculated the transpose of a matrix.

