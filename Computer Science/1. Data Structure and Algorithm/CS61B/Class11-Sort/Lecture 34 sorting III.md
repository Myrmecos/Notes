### 1. quicksort versus mergesort
	1. quicksortL3S: scan three times for items larger than, equal to and smaller than
	2. quicksortLHTS: Tony Hoarse's in-place partitioning. left pointer loves small items while right pointer loves large items.
	3. quicksortPickTH: picking exactly median for pivot (median finding: BFPRT or PICK)
	performances:
	![[Pasted image 20230925205149.png]]
	P.S. replacing Pick with QuickSelect below will also be slow
### 2. selection quick sort
1. quick select for finding median:
		1. PARTITIONING, pivot pushing smaller items to its left and the operation after one partition is on the median's side (to the geometric center)
			worst case performance: theta(N^2) if in sorted order
			![[Pasted image 20230925205404.png]]
			would normally not "overrun" across the median and requires returning:
			![[Pasted image 20230925205620.png]]
			summary:
			![[Pasted image 20230925205941.png]]
### 3. stability
 1. if items remain original relative order after sorting
	2. stable (Insertion sort and MergeSort) versus unstable (heapSort and QuickSort) (as QuickSort requires ==shuffling==![[Pasted image 20230925210024.png]]
	3. another random image to help you understand![[Pasted image 20230925210406.png]]
### 4. shuffling
 1. generate N random number, 
 2. attach to each array item,
 3. sort according to number