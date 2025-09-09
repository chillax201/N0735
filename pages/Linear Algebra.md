## Linear map intro :
collapsed:: true
	- $$
	  V \xrightarrow{linear T} W \quad ker(T) = K \\
	  K \mapsto 0 \\
	  \text{fiber over} 0'' \\
	  v + K \mapsto f(v) = w \\
	  \text{fiber over w''} \\
	  \text{(Fiber over }w \notin \text{range of T is empty )}
	  $$
	- ### picture :
		- ![image.png](../assets/image_1757415395232_0.png)
	-
-
- ## Theorem 1.1 (rank nullity) :
	- $$
	  dim(K) + dim(T(V)) = dim(V) \\
	  nullity(T) + rank(T) = dim(domain)
	  $$
	- If underlying scalars are not from $\R$ but from some other filed $F$ even then __everything__ we have done stays valid (To be revisited)
	  collapsed:: true
		- If $|F|$ is finite, say $P$ and if $dimV = n$ then :
		    $$|V|= P^n \quad |K| = P^k \quad |f(v)| = p^r$$
		- then above theorem just becomes
		  $$ P^n = P^r \cdot P^k$$
		  valid by uniformity of fibers
- ## Change of basis :
	- ![image.png](../assets/image_1757416091542_0.png){:height 287, :width 277}
	- Meaning of matrix of T wrt B,C is $A''$
	  $$[T(v]$$