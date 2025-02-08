Longest palindrome in an array
Here we find the longest palindrome number from the given array.

so here we need to sort the array in ascending order and later check from the last that the given number is palindrome or not.

the reason behind to sort an array is, we want the longest palindrome number so, in the sorted array, we got the largest number from the last element of the array, and check this is a palindrome or not and check till starting element. If there is no palindrome number so return -1 and print that there is no palindrome number.

Example
Input a[] = {1, 232, 54545, 999991};

Output: 54545

Input: arr[] = {1, 2, 3, 4, 5, 50};

Output: 5
now we will see the java program and working to find the largest number of the array.

Longest palindrome
Working
Step 1. Initialize arrays.

Step 2. Declare the scanner class for taking input.

Step 3. take array size from the user.

Step 4. Take an element of the array from the user.

Step 5.  store the return value of function largest in a larger variable.

largest(int a[], int size)

Step 1. Initialise temp variable.

Step 2.  Initialise the two-loop for sorting.

Step 3.  perform sorting.

Step 4. Initialise backward for loop for checking the large palindrome number.

Step 5. Check the current index value is a palindrome or not to call the ispalindrome Function. and return the current element.

Step 6. if there is not any palindrome number so return -1.

boolean isPalindrome(int n)

Step1. Copy the original number which is passed from the main function.

Step 2. Initialise while loop to find the reverse of the number.

Step 3. If the reverse of the number is equal to the original number then return true otherwise, return false. 

C	JAVA	Python
#include <stdio.h>  
int main()  
{
    int n, i , j, temp, rem, num;
    printf("enter size of both array : ");
    scanf("%d",&n);
    int arr1[n];
    printf("enter elements of array 1 : ");
    for(i=0; i<n; i++)
    {
        scanf("%d",&arr1[i]);
    }
    //sorting of array in ascending order
    for(i=0; i<n; i++)
    {
        for(j=i+1; j<n; j++)
        {
           if(arr1[i]>arr1[j])
            {
                temp = arr1[i];
                arr1[i] = arr1[j];
                arr1[j] = temp;
            }
        }
    }
    for(i=n; i>=0; i--)
    {
        num = 0;
        temp = arr1[i];
        while(arr1[i]!=0)
        {
            rem = arr1[i] % 10;
            num = num*10 + rem;
            arr1[i] = arr1[i]/10;
        }
        if(num==temp)
        {
            printf("%d",num);
            break;
        }
    }
    return 0;
}  
Output
case 1:
enter size 
5
enter element
12
3
11
212
345
Longest palindrome number in the array 212
case 2:
enter size
4
enter element
21
32
41
27
there is no palindrome in the array
