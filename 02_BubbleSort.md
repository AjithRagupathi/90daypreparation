## Bubble Sort it





``` java



//{ Driver Code Starts
//Initial Template for Java

import java.util.*;
import java.io.*;


// } Driver Code Ends
//User function Template for Java

class Solution
{
    //Function to sort the array using bubble sort algorithm.
	public static void bubbleSort(int arr[], int n)
    {
        //code here
        for(int i=0;i<n-1;i++){// the couter loop will run for n-1 times 
           
            for(int j=0;j<n-i-1;j++){ // here on each itteration of the outer loop completes the last element is sorted on its correct position so the conditions should be n-1-i;
                if(arr[j]>arr[j+1]){
                    swap(arr,j,j+1);
                }
               
            }
            
        }
    }
    public static void swap(int arr[], int i, int j){
        int temp= arr[i];
        arr[i]=arr[j];
        arr[j]=temp;
    } 
}

//{ Driver Code Starts.

class Sorting
{
    //method to print the Elements of the array
    static void printArray(int arr[])
    {
        int n = arr.length;
        for (int i=0; i<n; ++i)
            System.out.print(arr[i] + " ");
        System.out.println();
    }
	public static void main(String args[])
	{
	    //taking input using Scanner class
		Scanner sc = new Scanner(System.in);
		
		//taking total testcases
		int t = sc.nextInt();
		while(t>0)
		{
		    //taking total elements
			int n = sc.nextInt();
			
			//creating a new array of length n
			int arr[] = new int[n];
			
			//inserting elements to the array
			for(int i=0;i<n;i++)
			{
				arr[i] = sc.nextInt(); 
			}
			
			
			//calling bubbleSort() method
			new Solution().bubbleSort(arr,n);
			
			//calling printArray() method
			printArray(arr);
			
		t--;	
		}
	}

}

```

## Time and space complexity
Time Complexity: O(N2)
Auxiliary Space: O(1)

### Advantages of Bubble Sort:
- Bubble sort is easy to understand and implement.
- It does not require any additional memory space.
- It is a stable sorting algorithm, meaning that elements with the same key value maintain their relative order in the sorted output.
###  Disadvantages of Bubble Sort:
- Bubble sort has a time complexity of O(N2) which makes it very slow for large data sets.
- Bubble sort is a comparison-based sorting algorithm, which means that it requires a comparison operator to determine the relative order of elements in the input data set. It can limit the efficiency of the algorithm in certain cases.

