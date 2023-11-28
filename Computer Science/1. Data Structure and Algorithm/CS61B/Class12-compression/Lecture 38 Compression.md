### 1. prefix free codes
1. How do zip files work? ![[Pasted image 20230928075220.png]]
2. avoiding ambiguity:
	1. Morse code: pausing between characters
	2. PREFIX-FREE CODES, no codeword is a prefix of any other ![[Pasted image 20230928075416.png]]can be made less spindly: ![[Pasted image 20230928075501.png]]
	3. ==Shannon-Fano coding: top down==![[Pasted image 20230928075547.png]]![[Pasted image 20230928075619.png]]efficiency (average characters per text) = frequency * codeLength	![[Pasted image 20230928075749.png]]
	
### 4. Huffman Coding: optimal![[Pasted image 20230928075852.png]]
1. prefix-free codes and data structures to use
		1. encoding: array of BitSequence (observe that chars are just integers, eg 'A' = 65. we can use character as index to retrieve), better than hashMap: faster, smaller
		2. decoding: use trie (analogous to finding longest prefix)
2. application:
	1. for each input type (eg English or Chinese), assemble huge numbers of sample input for the category and use each corpus to create a standard code
	2. ==for every input file, create a unique code just for it ==(better in many case)
3. Process ![[Pasted image 20230928081304.png]]
### 3. Theory of compression
1. not possible to find an algorithm zip everything to 50% (or will go down to 1 bit and 0.5?!)
2. treat algorithm and compressed bitstream as a single sequence of bits
3. * major operating systems have no idea what to do with a .huf file
4. a simpler view ![[Pasted image 20230928081656.png]]

### 4. LZW

### 5. Lossy Compression
