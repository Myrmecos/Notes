### 1. commonly used number bases
	1. decimal
	2. binary: 0b, eg. 0b11110 = 1*2^4 + ... = 30
	3. hexadecimal: 0X, 0-F nibble
### 2. representing everything with bits
	 1. cahr: 5 bits for 26 letters
	 2. ASCII: 7 bits
### 3. unsigned integers
	000 = 0
	001 = 1
	010 = 2
	...
	111 = 7
### 4. signed integers
1. method 1. fist bit as sign (but: largest neg num + 1 -> largest pos num)
2. method 2. biased notation: shifted so 0 in middle. 
		conventional bias: 2^(n-1) - 1
		but: 0 is not 0b0
		![[Pasted image 20230929082523.png]]
1. method 3: one's complement: 0-0; most neg: 100...0 = -(2^(n-1)-1); most pos: 01...1 = 2^(n-1)-1 ![[Pasted image 20230929075942.png]]
2. method 4: two's complement: shifting negative by 1
		1. used by modern hardare
		2. use most significant bit as sign bit
		3. to negate: flip bits and add 1
			1. 7= 0b 0000 0111; -7 = 0b 1111 1001
![[Pasted image 20230929081038.png]]

### 5. overflow
1. most and least signifiant bit: MSB and LSB
2. result of arithmetic operation can't be represented by finite hardware bit -> overflow. 0b11111 + 1 = 0b00000
limited bits and overflow: ![[Pasted image 20230929081436.png]]
2's complement and overflow situations: ![[Pasted image 20230929081740.png]]

### 6. sign extension
	1. representing number using more bits than before
	eg. signed: 0b11 = 0b1001
	one or two complement: 0b11 = 0b1111
### 7. translation. 
hex <-> binary <-> decimal
2^10 kibi
2^20 Mebi
2^30 Gibi
2^40 Tebi
2^50 Pebi
2^60 Exbi
2^70 Zebi
2^80 Yobi
1. going from a smaller base to a larger base
	2 -> 10: 0b1001 = 8+1 = 9
2. a larger base to a smaller base
	10 -> 2: 
		14/2 = 7 ...0 (4th)
		7/2 = 3 ...1 (3rd)
		3/2 = 1 ... 1 (2nd)
		1/2 = 1 ... 1 (1st)
		0b1110 (mode from bottom to top)
		(or use 16 to subtract by 2)
3. binary to hex: 4 per group
	1. 0b 1001 1111 = 0x 9F
4. hex to binary: similar
![[Pasted image 20230929075339.png]]![[Pasted image 20230929075552.png]]
![[Pasted image 20230929075718.png]]
![[Pasted image 20230929075809.png]]

		

	
 
