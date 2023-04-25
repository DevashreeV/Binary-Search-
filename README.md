# Binary-Search-
An effective approach for determining an element's location in a sorted array is binary search. The search period is split in half repeatedly until the target element is located or the interval is empty. As a result, each step removes half of the remaining items, resulting in a logarithmic search time complexity of O(log n), where n is the array's size.

![image](https://user-images.githubusercontent.com/91966097/234353532-58a16f68-c184-4bb0-bb2d-2f6432dff935.png)


Steps to solve Binary Search:

1.The search interval is first initialised to the full array, which is from index 0 to n-1, where n is the array's size. To represent the left and right ends of the interval, respectively, we declare two variables, left and right. Right is initially set to n-1 while left is first set to 0.

2.The middle index of the search interval is then determined by dividing it by two using the formula mid = (left + right). We determine whether the element at the middle index arr[mid] and the target element x are same. If x equals arr[mid], the target element has been located, and its index mid is returned. We set right to be equal to mid minus one because we know that if x is smaller than arr[mid], x must be found in the left half of the search interval. Otherwise, we know that x must be found in the right half of the search interval if it is bigger than arr[mid], so we set left to be mid + 1.

3.As soon as the search interval is empty or the target element is located, we repeat steps 2 and 3 once more. We know the target element is not in the array if the search interval becomes empty, therefore we return -1.

Example of Binary Search:

          #include <stdio.h>
          int main()
          {
            int arr[6]={10,20,30,40,50,60};
            printf("Enter the number to be searched	: ");int a,i,l;
            scanf("%d",&a);

            l=6;
            int b=0;
            int e=l-1;
            int mid,result=-1;
            while(b<=e)
          {
            mid=(b+e)/2;
            if (arr[mid]==a)
            {

            result=mid;	break;
            }	
            else if(arr[mid]>a)
            {
              e=mid-1;
            }
            else if(arr[mid]<a)
            {
              b=mid+1;
            }
          }
          printf("%d",result);
          }

1. A 6-dimensional integer array with the values 10, 20, 30, 40, 50, and 60 is declared.
 
2. We use the scanf() method to save the searchable number that the user must provide in the variable 'a'.

3. The array's size, 6, is the initial value for l'. The value of 'b' is set to 0, which denotes the start of the search interval. The value of 'e' is set to l-1, indicating the end of the search interval.

4.The procedure is repeated using a while loop until either the number is located or the search time has run out. The variable'mid' contains the middle index of the search interval, which is determined as (b+e)/2. The index "mid" is saved in the variable "result" and the loop is ended with the "break" expression if the middle member of the array "arr[mid]" equals the integer "a". The search interval is limited to the left half of the array if "arr[mid]" is bigger than "a," in which case "e" is updated to mid-1. The search interval is limited to the right half of the array if 'arr[mid]' is smaller than 'a', in which case 'b' is updated to mid+1.

5.The last line of code prints the index of the number in the array if it was found, and -1 if it was not found.
![Screenshot (730)](https://user-images.githubusercontent.com/91966097/234355647-eb7eb9ec-d67c-40ab-bd83-a6338e17be68.png)


