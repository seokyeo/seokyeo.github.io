---
title: "c++ 이진탐색 알고리즘"
categories: 
    - cpp
tags:
    - [cpp, 이진탐색, 이분탐색, algorithm]
---

```cpp
//arr의 sort 필요

//기본
int BinSearch(int arr[], int target)
{
	int low = 0;
	int high = arr.length - 1;
	int mid;
	
	while(low <= high){
		mid = (low+high) /2;
		
		if(arr[mid] == target) return mid;
		else if(arr[mid] > target) high = mid -1;
		else //arr[mid]<target
	        low = mid + 1; 
	}
	return -1;
}
//재귀
int RecursiveBinSearch(int arr[], int target, int low, int high)
{
	if(low > high) return -1;
	
	int mid = (low + high) /2;
	if(arr[mid]==target) return mid;
	else if(arr[mid] > target) return RecursiveBinSearch(arr, target,low, mid-1);
	else //(arr[mid] < tartget)
		 return RecursiveBinSearch(arr, target, mid+1, high);
}

 

```
