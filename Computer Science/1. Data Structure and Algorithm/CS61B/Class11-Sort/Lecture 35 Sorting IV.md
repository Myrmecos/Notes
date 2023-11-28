### 1. sorting summary
1. application: 
	1. put things in order
	2. other tasks, eg finding duplicates, improving 3SUM performance from N^3 to N^2
	3. ![[Pasted image 20230926083836.png]]==why mergeSort does not need to keep track of recursive calls==

### 2. math problems
1. (N!) ∈ Omega((N/2)^(N/2)), prove by spreading N and (N/2)^(N/2) out
2. log(N!) ∈ Omega (NlogN), just take log on each side of the above expression, and take out constant terms
3. NlogN ∈ Omega (log(N!)), just tuck N inside log N
4. thus, NlogN ∈ Theta (log(N!)) and vise versa

### 3. Theoretical bounds on sorting
1. upper bound: O(N log N), as in mergesort. heapsort and insertion sort
2. lower bond: Omega(log(N!))
	1. game of puppy, cat, dog
	2. solution (comparing N animals):
		1. N animals have a tree with N! leaves
		2. the tree has a height of ceiling(log2(N!))
		3. thus the required questions (the number of branches we have to come across) is ceiling(log(N!))
		4. therefore the runtime is Omega(log(N!))
3. the asymptotic optimality
	1. achieved by mergesort, quicksort and heapsort

### 4. empirical testing: 
1. use excel/ Python etc
2. better asymptotic performance may not imply better real world performance
3. asymptotically optimal sort; avoiding yes or no questions
	1. sleepSort. runtime: N + max(A)
	2. bucketSort. insert at the array order corresponding to the number; runtime Theta(N)
4. key-index counting
### 5. Counting Sort
6. question: < 1000 element - array, which is quicker:
	1. quickSort (it wins!)
	2. counting sort
		1. assume r = 10 000, which means largest integer in it is 10,000![[Pasted image 20230926203717.png]] if N gets big enough, counting sort is faster
		2. create an array of size R to store count: Theta(R) (alphabet)
		3. counting number of each item: Theta(N)
		4. calculating target positions of each item: Theta(R)
		5. creating an array of size N to store ordered data: Theta(N)
		6. copy items from original array to ordered array: Theta(N)
		7. copying items from ordered array back to original array: Theta (N); thus memery usage: Theta (N+R)
	3. ![[Pasted image 20230926204339.png]]

		
### 6. LSD Radix Sort (least significant digit)
1. alphabet only needs one digit.
2. for numbers with different lengths (different ditits): replace missing digits with 0s.
3. example: ![[Pasted image 20230926205019.png]]
4. annoying feature: theta (WN + WR) runtime (W: number of digits of the largest num)
5. MSD sort (most significant digit.). messier
	1. ![[Pasted image 20230926205826.png]]
6. radix sort vs compare sort. 
	1. MergeSort better for large long digits and not similar
	2. LSD better for similar strings
	3. real data: merge sort will usually win, as we only need to examine first few chars of most strings
7. radix mostly only used in digits sorting
8. ![[Pasted image 20230926210233.png]]