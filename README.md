# AIM
To create a matrix by taking inputs from user and doing operations on it.

# Software Used
VS Code and Cpp Online Compiler

# Problem Statement
1.) To make a matrix by taking number of rows and column from user.

2.) To make a matrix by taking number of rows and column from user and do their addition and multiplication.

3.) To add the diagonal elements of the matrix.

4.) To make the transpose of a matrix.

# Theory
An array is a type of data structure used to store the collection of the same data type items held at contiguous memory locations. Arrays can be one-dimensional or multidimensional based on the number of directions in which the array can grow. In this article, we will study multidimensional arrays such as two-dimensional arrays and three-dimensional arrays.

To multiply two matrices, the number of columns of first matrix should be equal to the number of rows to second matrix. This program displays the error until the number of columns of first matrix is equal to the number of rows of second matrix.

Matrix addition is a basic C++ procedure that merges two matrices to create a new matrix. Matrices are two-dimensional numerical arrays with rows and columns.

# Program Codes
```javascript

//MATRIX FROM USER
#include<iostream>
using namespace std;
int main()
{
    int r,c , i , j;
    cout<< " Enter number of rows: ";
    cin>> r ;
    cout<<" Enter number of columns: ";
    cin>> c;
    int arr[r][c];
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
        cout<< " "<< arr[i][j];
    }
    cout<<endl;
}

}

//MATRIX ADDITION & MULTIPLICATION
#include<iostream>
using namespace std;
int main()
{
    int a,b,c,d , i , j ,k , e, f;
    cout<< " Enter matrix-1 rows: ";
    cin>> a ;
    cout<<" Enter matrix-1 columns: ";
    cin>> b;
    cout<< " Enter matrix-2 rows: ";
    cin>> c ;
    cout<<" Enter matrix-2 columns: ";
    cin>> d;

    int mat1[a][b];
    int mat2[c][d];
    int add [a][b];
    int mul [a][d];
    
 
//Taking elements of the matrix   
for (i=0 ; i < a ; i++)
    {
        for(j = 0 ; j < b ; j++)
        {
            cout<< "Enter elements ("<<i<< "," <<j<<"): "  ;
            cin>>mat1[i][j];
        }
    }


    for (i=0 ; i < c ; i++)
    {
        for(j = 0 ; j < d ; j++)
        {
            cout<< "Enter elements ("<<i<< "," <<j<<"): "  ;
            cin>>mat2[i][j];
        }
    }
//Checking condition for addition of matrices using if-else loop.
    if ( a !=c || b!=d)
    {
        cout<< "Matrix cannot be added as dimension do not match."<<endl;
    }
    
else
{for (i=0 ; i < a ; i++)
    {
        for(j = 0 ; j < b ; j++)
        {
            add[i][j] = mat1[i][j] + mat2 [i][j];

        }
    }
//Printing the sum of matrices.
cout<<"ADDITION OF MATRIX: "<<endl;
for (i=0 ; i< a ; i++)
{
    for(j = 0; j< b ; j++ )
    { 
        cout<< " " <<add[i][j];
    }
    cout<<endl;
}}
//Checking condition for multiplication of matrices.
    if( b != c)
{
    cout<< "Matrices cannot be multiplied as dimensions do not match." <<endl;
    return 1;
}
for(i = 0; i<a ; i++)
{
    for( j = 0; j<d ; j++)
    {
        mul[i][j] = 0;
        for( k=0; k<b ; k++)
        {
            mul[i][j] += mat1[i][k] * mat2[k][j];
        }
    }
}
//Printing the product of matrices.
cout << "MULTIPLICATION OF MATRIX: "<<endl;
for (i=0 ; i< a ; i++)
{
    for(j = 0; j<d ; j++ )
    { 
        cout<< " " <<mul[i][j];
    }
    cout<<endl;
}
}



//ADDITION OF DIAGONAL ELEMENTS
#include<iostream>
using namespace std;
int main()

{ int i,j, r1, c1, sum=0, sum2=0;
 cout<<"Enter number of rows and cloumns of matrix: ";
cin>>r1>>c1;
int mat1[r1][c1];
//Checking if square matrix or not
if(r1!=c1)
{
    cout<<"ONLY SQUARE MATRIX ARE TO BE ENTERED!"<<endl;
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
    cout<< "Sum of diagoal elements is: "<<sum<<endl;
    cout<<"Sum of diagonal elements is: "<<sum2<<endl;
}

}

//TRANSPOSE OF MATRIX
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
        cout<< " "<< arr[i][j];
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
# Output
## Matrix from User 
![Exp 8 - Matrix from user](https://github.com/user-attachments/assets/b31e0c51-8a05-4bd2-887e-4bb2e06698a5)

## Matrix Addition and Multiplication
![Exp 8 - Add Multi](https://github.com/user-attachments/assets/7d56c4af-719e-47ad-bdac-44957ab7d2fb)
![Sum Multi 2](https://github.com/user-attachments/assets/8177734c-7e2f-4286-a3ca-6eec5d27f514)
![Add Multi 3](https://github.com/user-attachments/assets/065651ae-dfd0-405a-bf6b-6a3fc668472e)



## Diagonal Sum of Matrix 
![Diagonal Sum of elements](https://github.com/user-attachments/assets/000227f3-b636-4376-8f46-3a09022fd9bb)

## Matrix Transpose
![Transpose of elements](https://github.com/user-attachments/assets/4c7bb0fa-14b1-4b85-b54e-8967cbc665f6)

# Conclusion
We learnt to take inputs from user and print the matrix from it, adding and multiplying two matrices using for loop, adding the diagonal elements of the matrix and transpose of a matrix.
