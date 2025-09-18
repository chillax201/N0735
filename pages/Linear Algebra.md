public:: true

- ## Linear map intro
	- $$
	  V \xrightarrow{linear T} W \quad ker(T) = K \\
	  K \mapsto 0 \\
	  \text{fiber over} 0'' \\
	  v + K \mapsto f(v) = w \\
	  \text{fiber over w''} \\
	  \text{(Fiber over }w \notin \text{range of T is empty )}
	  $$
	- ### picture :
	  collapsed:: true
		- ![image.png](../assets/image_1757415395232_0.png){:height 648, :width 356}
-
- ## Theorem 1.1 (rank nullity)
	- $$
	  dim(K) + dim(T(V)) = dim(V) \\
	  nullity(T) + rank(T) = dim(domain)
	  $$
	- If underlying scalars are not from $\R$ but from some other filed $F$ even then __everything__ we have done stays valid (To be revisited)
		- If $|F|$ is finite, say $P$ and if $dimV = n$ then :
		    $$|V|= P^n \quad |K| = P^k \quad |f(v)| = p^r$$
		- then above theorem just becomes
		  $$ P^n = P^r \cdot P^k$$
		  valid by uniformity of fibers
-
- ## Change of basis
	- ### Change of basis :
	  $$ M_{B',C'}(T) = Q^{-1}M_{B,C}(T)P$$
	- __fill in proof for above__
	-
	- Diagram:
	  collapsed:: true
		- ![image.png](../assets/image_1757416091542_0.png){:height 287, :width 277}
	- Meaning of matrix of T wrt B,C is $A''$:
	  $$[T(v)]_C = A [V]_B$$
	- <ins> Notation </ins>
		- $$
		  M_{B,C}(T) = \text{this A} \\
		  [V]_B = \text{coordination vector of V wrt B} \\
		  [V]_{B'} = P^{-1}[V]_B \\
		  $$
-
- ## Determinant
	- sum of $n!$ terms, each of which each is a product of n entries of $A$ chosen such that :
		- each column contributes exactly one factor
		  logseq.order-list-type:: number
		- each row contributes exactly one factor
		  logseq.order-list-type:: number
	- $$det(A)  = \sum (-1)^{l(\sigma)}a_{1\sigma(1)}a_{2\sigma(2)} \dots a_{n\sigma(n)}$$
	  where $\sigma$ is any permutation of column indices 1,2,...,n
	- $l(\sigma) =$ number of inversions in $\sigma$ i.e
		- number of pairs $(i,j)$ such that $\quad i<j \quad$ & $\quad \sigma(i) > \sigma(j)$
		- observe:
			- $l(\sigma) = l(\sigma^{-1})$
			- $\sigma \xrightarrow{switch \; two \; adjacent \; entries, \; say \; in\; slots \; i,\; i+1} \mu$
			  $\Rightarrow \quad l(\mu) = l(\sigma) \pm 1$
			- $\mu = \sigma \circ S_i \quad \text{(where } s_i \text{ is a permutation that switches i and i+1)}$
			- $det(P^{-1}AP) = det(A)$ implies that determinant is an intrinsic property of operator itself and doesn't depend on basis
		-
-
- ## Multilinear Functions
	- Domain $V_1 \times V_2 \times \dots \times V_k$
	- Co-domain W
	- where $V_i$ and $W$ are V.spaces
	- f is called multilinear is fixing all arguments except $i^{th}$ argument gives a linear function in $i^{th}$ argument. this holds for each i
	- multilinear + alternating :
		- if adjacent arguements of f are swapped then f becomes minus of what it was 
		  e.g : $f(V_1,V_2\dots V_k) = -f(V_2,V_1\dots V_k)$
		- consider :
		  $$ f(V_1 + V_2, V_2 + V_2, V_3 \dots)  = 0 \quad \text{(b/c f alternating)}$$
-
- ## Direct Sum
	- ### internal
		- Let $W_{\alpha} \quad \alpha \in I$ be a family of a vector space $V$
		- definitions:
			- span {$W_{\alpha}$} = set of all sums of vectors from $\underset{\alpha \in I}{\cup}W_{\alpha}$
				- we say {$W_{\alpha}$} spans $V$ is $\sum W_{\alpha} = V$
			- {$W_{\alpha}$} is a linear independent family of subspaces means $\sum W_{\alpha} \Rightarrow$ each $W_{\alpha} = 0$
			- If $W_1, \dots W_n$ subspaces of V are linearly independent, then we say V is (internal)direct sum of $W_1, \dots, W_n$ and write
			  $$V= W_1 \oplus \dots \oplus W_n \quad \text{(internal)}$$
			- special case 
			  n = $W_1,W_2$ subspaces of $V$
				- we saw $V= W_1 \oplus W_2 \Leftrightarrow$ (any 2 of the following 3)
					- $W_1 \cap W_2 = 0$
					  logseq.order-list-type:: number
					- $W_1+W_2 = V$
					  logseq.order-list-type:: number
					- $dim(W_i) + dim(W_2) = dim(V)$
					  logseq.order-list-type:: number
	- ### external
		- External direct sum of any vector spaces $W_1, \dots ,W_n$ is the set $W_1\times \dots \times W_n$ made into a vector space with component wise + and scalar multiplication we denote this v.space by :
		  $$W_1\oplus \dots\oplus W_n \quad \text{external}$$
		- Note 
		  $$\R^n = \R \oplus \dots \oplus \R \quad \text{n times}$$
	- ### Theorem
	  $dim(W_1) + dim(W_2) - dim (W_1\cap W_2) = dim(W_1+W_2)$
	  where $W_1$ and $W_2$ are both subspaces of some vector space
		- proof :
			- let {$X_1, \dots, X_k$} be a basis for $W_1 \cap W_2$
			- extend to {$X_1, \dots, X_k,Y_1,\dots,Y_l$} for a basis for $W_1$
			- extend to {$X_1, \dots, X_k,Z_1,\dots,Z_l$} for a basis for $W_2$
			- LHS = $$(k+l) + (k+m) - k = k+l+m$$
			- now we need to show that RHS is $k+l+m$ (i)
			- now our claim is that $S=$ {$X_1, \dots, X_k,Y_1,\dots,Y_l,Z_1,\dots,Z_l$} is a basis for $W_1+W_2$
			- Let $\sum a_p X_p + \sum b_q Y_q + \sum c_r Z_r = 0$
			  $\Rightarrow \sum a_p X_p + \sum b_q Y_q = \sum -c_r Z_r = u \quad (u \in W_1 \cap W_2)$
			  note : $\sum a_p X_p + \sum b_q Y_q \in W_1 \quad \sum -c_r Z_r  \in W_2$
			- from above we get 
			  Each $b_q = 0$ looking at LHS as element of $W_1$
			  Each $c_r = 0$ looking at RHS as element of $W_2$
			  So $LHS = RHS = 0$
			  $\Rightarrow a_p = 0 \quad \forall p$
			- this shows $s$ spans $W_1+W_2$ and elements are linearly independent
			  hence, we show (i)
- ## Extending functions
	- we know that is $B \subset U$ is a basis and there is a function $f$ from $B$ to $V$ then there is always a natural extension of the function $f$ such that it maps all vectors in $U$ to vectors in $V$
	- similarly we can do the following for linearly independent subspaces $W_1, \dots W_n$:
		- given any linear map $f_i : W_i \rightarrow U \exists!$ simultaneous extension 
		  $f:V\rightarrow U$ of all $f_i$ (i.e $f|_{W_i} = f_i$)
-
- ## Fields
  Informally a set with well behaved arithmetic of 4 operations $+,-,\cdot,\div$
	- examples are $\R, \mathbb{C}$ and $\mathbb{Q}$
	- If F is a subfield of $E$ , then in particular $E$ is a vector space over $F$.
	  $dim E$ as a bector space over $F$
	  is denoted $[E:F]$ is (called degree of $E$ over $F$)
	- examples of finite fields 
	  numbers$\mod p \quad \text{(for P prime)}$
	-