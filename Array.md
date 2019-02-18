 #Problem-1
#Problem statement
We are given an array (or a list) of data. We are also given a way to “order” the elements present in the data. Now, we are asked to arranged the data as per the given order.

As an example, we are given an array of integers: [5, 1, 4, 2, 3]. We are given the “order” as “smaller than”. So, we are asked to arrange the elements of this array in such a way that each element is smaller than its successor. Basically, we need to find a way to sort this array so that the final array obtained is [1, 2, 3, 4, 5].

#Bubble Sort Algorithm in C – Introduction
As an example, for the array mentioned above – [5, 1, 4, 2, 3] we can see that 5 should not be on the left of 1 and so, we swap them to get: [1, 5, 4, 2, 3]. Next, we see that 5 should again not be on the left of 4. We swap 5 and 4 to get [1, 4, 5, 2, 3]. We repeat this for 5 and 2 and subsequently for 5 and 3 to get [1, 4, 2, 3, 5].

As can be seen – after one “pass” over the array, the largest element (5 in this case) has reached its correct position – extreme right. Let us try to repeat this process.

Algorithm :

Step 1: Repeat Step 2 For i = 0 to N-1
Step 2: Repeat For J = i + 1 to N - I
Step 3: IF A[J] > A[i]
SWAP A[J] and A[i]
[END OF INNER LOOP]
[END OF OUTER LOOP
Step 4: EXIT
Complexity

Scenario	Complexity
Space	O(1)
Worst case running time	O(n2)
Average case running time	O(n)
Best case running time	O(n2)

#Example of Bubble Sort.


#include<stdio.h>
void bubble_sort(int[],int);
void display(int[],int);
int main() {
int arr[] ={2,1,3,4,5};
int len = sizeof(arr)/sizeof(arr[0]);
bubble_sort(arr,len);
display(arr,len);
return 0;
}
void bubble_sort(int arr[],int len)
{
int i,j,temp;
for(i=0;i<len;i++) {
    for(j=i+1;j<len;j++) {
        if(arr[i]>arr[j]) {
           temp = arr[i];
           arr[i] =arr[j];
           arr[j] =temp;
        }
    }
}

}


void display(int arr[],int len) {
int i;
for(i=0;i<len;i++) {
    printf("arr[%d]:%d\n",i,arr[i]);
}

}
#================================================================================================================#



