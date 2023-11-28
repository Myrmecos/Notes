#### -weighted quick union ![[Pasted image 20230918095620.png]]
max depth: log N
(increase 1 depth means at least doubling in size )
Worst case:
![[Pasted image 20230918100353.png]]
![[Pasted image 20230918100057.png]]
![[Pasted image 20230918100255.png]]
MN: M connect
N: constructor
### -Path compression
very close to amortized constant time!![[Pasted image 20230918100642.png]]
![[Pasted image 20230918100706.png]]
path compression only needs slight modification of the find()function:

```cpp
string find(unordered_map<string,string>& root,string s){
        if(root[s]!=s) 
            root[s]=find(root,root[s]); //挂到根节点下
        return root[s];
    }
```
and man it's fast:
(alpha: inverse Akerman funciton)
![[Pasted image 20230918100909.png]]




