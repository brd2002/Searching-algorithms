# Searching-algorithms 
 *Searching_Algorithms:
 1 . Linear_Search_Algorithms
 2. Binary_Search_Algorithms
 

                1 . Linear_Search_algorithms 
                example_with_code_in_c++

//CODE_IN_C++
                 
          #include<iostream>
using namespace std;
 int linearsearch(int arr[] , int n , int x)
 {
     int i ;
      for(i = 0 ; i<n ; i++)
        if(arr[i] == x)
        return i;
      return -1;
 }
  int main(void)
  {
      int arr[] = {1,2,3,4,5,6,7};
      int x = 7;
      int n = sizeof(arr)/sizeof(arr[0]) ;
      int result = linearsearch(arr , n , x);
      (result ==-1)? cout<< "Element is not found in Arrry "
      :cout<< "Element is found in Array "<< result;
      return 0;
       // brdcoder007
  }
  
   output: 6.
   Time_complexity :O(n)
 
 
 
               2  . Binary_Search_algorithms
               example_with_code_in_c++
               
//CODE_IN_C++               
               
        #include<bits/stdc++.h>
using namespace std;
int binarySearch(int arr[] , int l , int r , int x)
{
    if(r>=l)
    {
        int mid = l+(r-l)/2;
        if(arr[mid]==x)
            return mid;
        if(arr[mid]>x)
            return binarySearch(arr ,l ,mid-1 , x);
        else
            return binarySearch(arr , mid+1 , r ,x);

    } return -1;
}
 int main(void)
 {
     int arr[] ={1,2,3,4,5,6,7,8};
     int x = 5;
     int n = sizeof(arr)/sizeof(arr[0]);
     int result = binarySearch(arr ,0 ,n-1 ,x);
     (result == -1)?cout<< "Element is not found in array "
                   :cout<< "Element is found in Array "<< result;
                   return 0;

                   
                   //brdcoder007

 }
 output: 4.
 Time_complexity:O(logn).
 





