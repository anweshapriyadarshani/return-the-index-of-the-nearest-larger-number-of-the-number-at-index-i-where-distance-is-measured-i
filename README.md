# return-the-index-of-the-nearest-larger-number-of-the-number-at-index-i-where-distance-is-measured-i
Given an array of numbers and an index i, return the index of the nearest larger number of the number at index i, where distance is measured in array indices.  For example, given [4, 1, 3, 5, 6] and index 0, you should return 3.  If two distances to larger numbers are the equal, then return any one of them. If the array at i doesn't have a nearest larger integer, then return null.  Follow-up: If you can preprocess the array, can you do this in constant time?


#include<iostream> 
using namespace std; 
  
/* prints element and NGE pair  
for all elements of arr[] of size n */
void printNGE(int arr[], int n) 
{ 
    int next, i, j; 
    for (i = 0; i < n; i++) 
    { 
        next = -1; 
        for (j = i + 1; j < n; j++) 
        { 
            if (arr[i] < arr[j]) 
            { 
                next = arr[j]; 
                break; 
            } 
        } 
        cout << arr[i] << " -- " 
             << next << endl; 
    } 
} 
  
// Driver Code 
int main() 
{ 
    int arr[] = {11, 13, 21, 3}; 
    int n = sizeof(arr)/sizeof(arr[0]); 
    printNGE(arr, n); 
    return 0; 
} 
