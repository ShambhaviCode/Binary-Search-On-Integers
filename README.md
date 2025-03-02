🔍 Binary Search in C 

Binary search is an efficient algorithm for searching an element in a sorted array.
It works using the divide-and-conquer strategy, reducing the search space by half at each step.


📌 How Binary Search Works

1️⃣ Ensure the array is sorted (Binary search only works on sorted arrays).

2️⃣ Find the middle element:
If it's the target value, return its index.

If the target is smaller, search in the left half.

If the target is larger, search in the right half.
3️⃣ Repeat the process until the element is found or the search space becomes empty.


🖥️ Binary Search Code in C



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

🔹 binarySearch function:

✔️ Accepts an array, left & right boundaries, and the target number.

✔️ Finds the middle index.

✔️ Compares the middle element with the target.

✔️ Adjusts the search range accordingly.

🔹 main function:

✔️ Defines a sorted array.

✔️ Takes user input for the target number.

✔️ Calls binarySearch and displays the result.



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

✅ Faster than linear search for large datasets.

✅ Efficient for sorted arrays.

✅ Logarithmic time complexity makes it scalable.
















