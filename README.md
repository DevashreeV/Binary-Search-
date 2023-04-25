# Binary-Search-
An effective approach for determining an element's location in a sorted array is binary search. The search period is split in half repeatedly until the target element is located or the interval is empty. As a result, each step removes half of the remaining items, resulting in a logarithmic search time complexity of O(log n), where n is the array's size.


Steps to solve Binary Search:

1.The search interval is first initialised to the full array, which is from index 0 to n-1, where n is the array's size. To represent the left and right ends of the interval, respectively, we declare two variables, left and right. Right is initially set to n-1 while left is first set to 0.

2.The middle index of the search interval is then determined by dividing it by two using the formula mid = (left + right). We determine whether the element at the middle index arr[mid] and the target element x are same. If x equals arr[mid], the target element has been located, and its index mid is returned. We set right to be equal to mid minus one because we know that if x is smaller than arr[mid], x must be found in the left half of the search interval. Otherwise, we know that x must be found in the right half of the search interval if it is bigger than arr[mid], so we set left to be mid + 1.

3.As soon as the search interval is empty or the target element is located, we repeat steps 2 and 3 once more. We know the target element is not in the array if the search interval becomes empty, therefore we return -1.

