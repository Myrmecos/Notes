Review:
![[Pasted image 20230927073821.png]]
### 1. Tries
1. search using digits (compared with: trees, using compareTo; hashTable using hashcode)
2. digit-by-digit search![[Pasted image 20230927074228.png]]
3. runtime
	1. Insert a key with L digits into a Trie with N keys 
		1. worst case: Theta(L)
	2. search. key with L digits and Trie with N keys
		1. best case: Theta(1) , no match
		2. worst case: Theta(N)
	3. compare with hash table search
		1. best case: Theta(L)
		2. typical case: Theta(L)
		3. worst case: Theta(NL)![[Pasted image 20230927074748.png]]
4. usage
	1. prefix matching
	2. approximate matching

### 2. Trie implementation
1. storage:
	1. storing letters implicitly on each link![[Pasted image 20230927074943.png]]like the above image, instead of storing in each node![[Pasted image 20230927075017.png]]
2. implementation of searching for longest prefix
	1. check each digit in turn, walk down the tree
	2. keep track of the most recent blue(marked) thing
	3. at some point next is null
	4. return most recent blue thing
3. problem
	1. mapping from node to its childern is done with a data-indexed array of size R. 
	2. that means each node uses R memory
	3. improvement: tracking children in a better way; ternary search tries; patricia/radix tries; DAWG; suffix/prefix array
### 3. Child link optimization
1. array based trie![[Pasted image 20230927075349.png]]
2. BST based trie![[Pasted image 20230927075407.png]]
3. replace array with a map (for links)![[Pasted image 20230927075629.png]]
4. trade-off
	1. data-indexed array: max speed, large memory required
	2. treeMap/hashMap: slower query performance, less memory wasted
		1. mitigate performance issues: initializing HashMap to be small

### 4. Ternary search tries
1. solutions to above problems: trie nodes with a fixed number of links
	1. each node: 3 links. left link for next key val smaller than node's character; middle link for == , right link for larger![[Pasted image 20230927080100.png]]
	2. a bit awkward as: we move one character further to an unmatched node before linking new character
2. summary![[Pasted image 20230927080541.png]]
