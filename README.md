Circular Rotation of an Array by K Position in C
In this article, we will brief in on how to perform Circular rotation of an array by K positions in C programming. In circular rotation we will rotate the elements in the array where one rotation operation moves the last element of the array to the first position and shifts all remaining elements to the right.


Keypoints:-
In this section we will learn about basic knowledge which we need to know before coding the above Program. So we must have knowledge of what is an array? 

What is an array?
An array is a data structure, it is collection of similar data elements which is stored at contiguous memory locations in which each data element can be accessed directly by only using its index number.
 
How to declare an array?
To declare an array in C,a programmer specifies the type of the elements and the number of elements required by an array as follows − This is called a single-dimensional array. The arraySize must be an integer constant greater than zero and type can be any valid C data type. For example, to declare a 10-element array called balanceof type double, use this statement − Here balanceis a variable array which is sufficient to hold up to 10 double numbers.
Algorithm
Declare and initialize the array
Enter index value for circular rotation
Perform circular rotation
Now using two for loops and a temp variable for  circular rotation
Store last element of the array in temp variable
Using second loop start shifting the elements of  the array  by one
Than last element of the array will be added to the starting of the array
Than display the array at the end.
Circular Rotations Of Array By K Positions
Code of Circular rotation of an array by K positions
#include<stdio.h>        
int main()    
{             
    int size;
    printf("Size of array: ");
    scanf("%d",&size);    
    int arr[size];
    printf("Enter the elements ");
    for(int a=0;a<size;a++)   
    scanf("%d",&arr[a]);    
    int n;
    printf("Enter the index from where you want your array to rotate ");
    scanf("%d",&n);        
    printf("Array: \n");    
    for (int a = 0; a < size; a++) {     
        printf("%d ", arr[a]);     
    }             
    for(int a = 0; a < n; a++) { int b, temporary; temporary = arr[size-1]; for(b = size-1; b > 0; b--)
            {    
                    arr[b] = arr[b-1];    
             }    
            arr[0] = temporary;    
    }            
    printf("\n");            
    printf("New Array: \n");    
    for(int a = 0; a< size; a++){    
        printf("%d ", arr[a]);    
    }    
    return 0;    
}
Input

Size of array: 6
Enter the elements: 2 3 4 5 6 7
Enter the index from where you want your array to rotate : 3

 Output
Array:
2 3 4 5 6 7
New Array:
5 6 7 2 3 4
