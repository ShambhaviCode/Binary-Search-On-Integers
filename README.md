🔍 Implementing Binary Search On Integers


💻 Binary Search Code in C



#include <stdio.h>

#include <stdlib.h>

int main(void) 

{

int iaArr[100], iNum, i, iMid, iLow, iHigh, iFound, iKey;

printf("\nEnter the number of elements: ");

scanf("%d", &iNum); 
  
printf("\nEnter the elements in ascending order:\n");

for (i = 0; i < iNum; i++)

scanf("%d", &iaArr[i]);

printf("\nEnter the key element: ");

scanf("%d", &iKey);

iFound = 0;

iLow = 0;

iHigh = iNum - 1;

while (iLow <= iHigh) 

{

iMid = (iLow + iHigh) / 2;

if (iKey == iaArr[iMid]) 

{

iFound = 1;
break;

 } 

else if (iKey < iaArr[iMid]) 

{

 iHigh = iMid - 1;


} 

else

{
            
iLow = iMid + 1;

 }

 }

 if (iFound)

printf("\nKey element %d found at position %d\n", iKey, iMid + 1);

else

printf("\nKey element not found\n");

return 0;

}




📖 Explanation of the Code

🔷 Binary Search Logic:

✔ The program searches for a target number in a sorted array using the binary search algorithm.

✔ It repeatedly divides the search space into two halves until the target is found or the search space is empty.


🔷 How the Binary Search Works:

1. Initialize Search Bounds:

iLow is set to 0 (first index).

iHigh is set to iNum - 1 (last index).



2. Find the Middle Element:

iMid = (iLow + iHigh) / 2 calculates the middle index.



3. Comparison & Search Adjustment:

If iaArr[iMid] == iKey, the key is found, and the position is printed.

If iKey is smaller, search in the left half (iHigh = iMid - 1).

If iKey is larger, search in the right half (iLow = iMid + 1).



4. Repeat Until Found or Search Space is Empty

The process continues until the key is found or iLow > iHigh, meaning the key is not present in the array.




🔷 main() Function:

✔ Accepts user input for the number of elements and array elements (in sorted order).
✔ Reads the key element to search for.
✔ Implements the binary search logic inside a while loop.
✔ Prints whether the key was found (along with its position) or not found.



📝 Example Output

Enter the number of elements

5

Enter the elements in ascending order

12 23 37 46 78

Enter the key element

37

Key element 37 found at position 3

Process returned 0 (0×0)   
execution time : 23.048 s

Press any key to continue.


🎯 Why Use Binary Search?

Binary Search is used because it is a highly efficient searching algorithm for sorted arrays. It significantly reduces the number of comparisons compared to linear search.



1. Faster than Linear Search

Binary Search: O(log N) time complexity

Linear Search: O(N) time complexity


🔹 Example:
Imagine searching for a number in a list of 1 million sorted numbers:

Linear search might need up to 1,000,000 comparisons in the worst case.

Binary search would find the number in at most log₂(1,000,000) ≈ 20 comparisons.



2. Works Efficiently on Large Datasets

Since binary search cuts the search space in half at each step, it is much faster for large datasets compared to scanning each element one by one.


3. Suitable for Sorted Data

Binary search works only on sorted arrays. If the data is already sorted, binary search is a perfect choice.



4. Example Comparison (Linear vs. Binary Search)

Let’s search for 37 in this sorted list:

[10, 15, 22, 30, 37, 45, 50]

🔴 Linear Search Steps (O(N))

1. Compare 10 → Not found


2. Compare 15 → Not found


3. Compare 22 → Not found


4. Compare 30 → Not found


5. Compare 37 → Found (5 comparisons!)



🟢 Binary Search Steps (O(log N))


1. Check middle (30) → 37 is greater, so search right half


2. Check new middle (45) → 37 is smaller, so search left half


3. Check new middle (37) → Found (only 3 comparisons!)



Conclusion

Binary search is used because it is much faster than linear search for sorted data, especially for large datasets. It reduces the number of comparisons to logarithmic time, making it a great choice for quick searching!


















