* slide has notes but requires adobe to see them
### 1. quicksort (partition sort)
	1. idea: partitioning
	2. processes
		1. find an item called pivot
		2. move items greater than pivot to one side, and smaller items to the other side (3 scan approach, scan and copy red -> white -> blue)
		3. repeat for each side
			
![[Pasted image 20230925082745.png]]
### 2. runtime
	1. best case: pivot does not land on either side: theta(NlogN)
	2. worst case (for sorted arrays or array with one repeated item): theta(N^2)
	3. compare with mergesort: best case and worst case theta(NlogN)
	4. but most cases theta(NlogN), as long as most pivot don't land on either side, and empirically faster than any other sort
### 3. quicksort is: BST (binary search tree) sort
	1. proof: comparison in quicksort exactly the same as constructing a BST tree

### 4. review before moving on!
![[Pasted image 20230925083409.png]]

### 5. avoiding worst case
	1. randomness: pick random pivot or shuffle before sorting
	2. smarter pivot selection: calculate median (eg choosing median of first three items); exact median quicksort is safe but slower than mergesort
	3. introspection: switch to a safer sort if recursion goes too deep
	4. * preprocess array, no obvious reason (can't check if it's sorted, almost sorted arrays will also be slow)
	