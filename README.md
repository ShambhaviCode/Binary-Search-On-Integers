


Binary search is an efficient algorithm for searching an element in a sorted array. It works using the divide-and-conquer strategy, reducing the search space by half in each step.


---

How Binary Search Works

Step 1: Ensure the array is sorted (Binary search only works on sorted arrays).

Step 2: Find the middle element:

If it's the target value, return its index.

If the target is smaller, search in the left half.

If the target is larger, search in the right half.


Step 3: Repeat the process until the element is found or the search space becomes empty.



---

Binary Search Code in C

#include <stdio.h>

// Function to perform binary search
int binarySearch(int arr[], int left, int right, int target) {
    while (left <= right) {
        int mid = left + (right - left) / 2;

        // Check if the middle element is the target
        if (arr[mid] == target)
            return mid;

        // If target is smaller, search the left half
        if (arr[mid] > target)
            right = mid - 1;
        // Else, search the right half
        else
            left = mid + 1;
    }
    return -1; // Element not found
}

int main() {
    int arr[] = {2, 5, 8, 12, 16, 23, 38, 56, 72, 91}; // Sorted array
    int n = sizeof(arr) / sizeof(arr[0]); // Find array size
    int target;

    // Get input from user
    printf("Enter the number to search: ");
    scanf("%d", &target);

    // Call binary search function
    int result = binarySearch(arr, 0, n - 1, target);

    // Print the result
    if (result != -1)
        printf("Element found at index %d\n", result);
    else
        printf("Element not found in the array\n");

    return 0;
}


---

Explanation of the Code

binarySearch function:

Accepts an array, left & right boundaries, and the target number.

Finds the middle index.

Compares the middle element with the target.

Adjusts the search range accordingly.


main function:

Defines a sorted array.

Takes user input for the target number.

Calls binarySearch and displays the result.




---

Example Output

Enter the number to search: 23
Element found at index 5

Enter the number to search: 100
Element not found in the array


---

Complexity Analysis

Best Case:  → If the middle element is the target.

Worst/Average Case:  → Since the search space is halved at each step.



---

Why Use Binary Search?

✅ Faster than linear search for large datasets.
✅ Efficient for sorted arrays.
✅ Logarithmic time complexity makes it scalable.










