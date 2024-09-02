# exp-8

Aim:
To study and implement C++ 2D Array - Matrices

Theory:
A 2D array in C++ can be defined as a data structure that deals with two-dimensional grid formats such as matrices wherein every single
element is well identified by two indices: one for rows and another one for columns. It is similar to an array composed of other arrays.
A two-dimensional array could be declared using the syntax type arrayName[rows][columns]; For instance, int matrix[3][4]; indicates three
rows by four columns. All its members occupy successive positions in memory meaning they are laid out linearly following 
row-major order scheme hence it makes it different from accessing them through single index only but rather via two indexes.They may be initialized
while being declared. For static arrays they require listing down values enclosed in nested braces whereas dynamic
arrays size calculation occurs at run-time stage hence this involves dynamic allocation using new’s keyword and deallocation using delete’s keyword in
C++.Elements can be accessed using their respective row and column indexes. The iteration uses mostly a two-fold loop:
the outer one is run for rows while the inner one does columns. It enables you to treat or manipulate one element of an entire array.
a
```
#include <iostream>

//muliplication of matrix
//diagonal addition
// transpose
// compare elements with first row and second row

# include<iostream>
using namespace std;
int main()
{
    //matrix input and display
    int a[2][2];
    int i,j;
    for (i=0 ;i<2; i++)
    {
        for (j=0 ;j<2; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }

    for (i=0 ;i<2; i++)
    {
        for (j=0 ;j<2; j++)
        {
            cout<<a[i][j]<<" ";
        }
        cout<<endl;
    }

}
b
# include<iostream>

//muliplication of matrix
//diagonal addition
// transpose
// compare elements with first row and second row

using namespace std;
int main()
{

    int a[2][2];
    int b[2][2];
    int s[2][2];
    int i,j,r = 0,c=0;
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;

    cout<<"Matrix 2: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>b[i][j];
        }
    }
    cout<<endl;

    
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            s[i][j] = a[i][j] + b[i][j];
        }
    }

    cout<<"Sum: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<s[i][j]<<" ";
        }
        cout<<endl;
    }
        cout<<endl;
}

c
# include<iostream>
using namespace std;
int main()
{
    int i,j,k,r = 0,c=0,s = 0;
    int a[r][c];
    int b[r][c];
    int p[r][c];
    
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;

    cout<<"Matrix 2: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>b[i][j];
        }
    }
    cout<<endl;

    
for (int i = 0; i < r; ++i) 
{
        for (int j = 0; j < r; ++j) 
        {
            p[i][j] = 0;
            for (int k = 0; k <c; ++k) 
            {
                p[i][j] += a[i][k] * b[k][j];
            }
        }
}

    cout<<"Product: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<p[i][j]<<" ";
        }
        cout<<endl;
    }
        cout<<endl;
}
d

# include<iostream>
using namespace std;
int main()
{
    int i,j,k,r = 0,c=0;
    int a[r][c];
    int da = 0;
    
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;


    for (int i = 0; i < r; i++) 
    {
        da = da + a[i][i];
    }

cout<<"Diagonal Sum: "<<da<<endl;


}
e)
# include<iostream>
using namespace std;
int main()
{

    int a[2][2];
    int i,j,r = 0,c=0;
    bool eqr = true;
    cout<<"Enter no. of rows: ";
    cin>>r;
    cout<<"Enter no. of columns: ";
    cin>>c;
    cout<<endl;

    cout<<"Matrix 1: "<<endl;
    for (i=0 ;i<r; i++)
    {
        for (j=0 ;j<c; j++)
        {
            cout<<"Enter the "<<i <<" "<<j<<" element: " ;
            cin>>a[i][j];
        }
    }
    cout<<endl;


    for (int j = 0; j < c; j++) 
    {
        if (a[0][j] != a[1][j]) 
        {
            eqr = false;
            break;
        }
    }
    cout<<"Row equality: "<<eqr;
}
outpute
a)
Enter the 0 0 element: 1
Enter the 0 1 element: 2
Enter the 1 0 element: 3
Enter the 1 1 element: 4

1 2
3 4

b)
Enter no. of rows: 2
Enter no. of columns: 2

Matrix 1: 
Enter the 0 0 element: 1
Enter the 0 1 element: 2
Enter the 1 0 element: 3
Enter the 1 1 element: 4

Matrix 2: 
Enter the 0 0 element: 5
Enter the 0 1 element: 6
Enter the 1 0 element: 7
Enter the 1 1 element: 8

Sum: 
6 8 
10 12 

c
Enter no. of rows: 2
Enter no. of columns: 2

Matrix 1:
Enter the 0 0 element: 1
Enter the 0 1 element: 2
Enter the 1 0 element: 3
Enter the 1 1 element: 4

Matrix 2:
Enter the 0 0 element: 2
Enter the 0 1 element: 0
Enter the 1 0 element: 1
Enter the 1 1 element: 2

Product:
4 4
10 8

d
Enter no. of rows: 3
Enter no. of columns: 3

Matrix:
Enter the 0 0 element: 1
Enter the 0 1 element: 2
Enter the 0 2 element: 3
Enter the 1 0 element: 4
Enter the 1 1 element: 5
Enter the 1 2 element: 6
Enter the 2 0 element: 7
Enter the 2 1 element: 8
Enter the 2 2 element: 9

Diagonal Sum: 15

e)
Enter no. of rows: 3
Enter no. of columns: 3

Matrix:
Enter the 0 0 element: 1
Enter the 0 1 element: 2
Enter the 0 2 element: 3
Enter the 1 0 element: 1
Enter the 1 1 element: 2
Enter the 1 2 element: 3
Enter the 2 0 element: 4
Enter the 2 1 element: 5
Enter the 2 2 element: 6
Row equality (first and second rows): True

conclusion 
In conclusion, a 2D array in C++ serves as an efficient structure for managing grid-based data like matrices, where elements are accessed via two indices representing rows and columns. Understanding its row-major memory layout, initialization methods, and dynamic allocation using pointers is crucial for effective usage. The nested loop structure commonly facilitates element manipulation, making 2D arrays versatile for various computational tasks.




