## 1. Relations and their properties
#### Binary relations - Quan hệ hai ngôi 
Ký hiệu: aRb


#### Relations on a set - Quan hệ trên một tập hợp
- Reflexivity - Phản xạ
	> A relation on a set A is a relation from A to A.
	- aRa, $\forall a \in A$
- Irreflexive - Phi phản xạ
	- quan hệ bù của nó $\not R$ là phản xạ
- Symmetry - Đối xứng
	> A relation R on a set A is called symmetric if (b, a) ∈ R whenever (a, b) ∈ R, for all a, b ∈ A.
- Antisymmetry - Phản xứng
	> A relation R on a set A such that for all a, b ∈ A, if (a, b) ∈ R and (b, a) ∈ R, then a = b is called antisymmetric.
- Transitivity - Bắc cầu
	- $(a,b) \in R \wedge (b, c) \in R \to (a,c) \in R$,  $\forall a, b, c$ 

#### Combining relations
Let R be a relation from a set A to a set B and S a relation from B to a set C. The composite of R and S is the relation consisting of ordered pairs (a, c), where a ∈ A, c ∈ C, and for which there exists an element b ∈ B such that (a, b) ∈ R and (b, c) ∈ S. We denote the composite of R and S by S ◦ R.


## 2. n-ary Relations and their applications

## 3. Representing relations
#### Using matrices

#### Using digraphs




## 4. Closures of relations - Bao đóng của quan hệ
"Bao đóng X" của quan hệ R được định nghĩa là tập cha nhỏ nhất của R mà có tính chất đó
#### Reflexive closure - Bao đóng phản xạ
- Bổ sung (a, a) vào R với mỗi $a \in A$

- Tức $R \cup I_A$
#### Symmetric closure - Bao đóng đối xứng
- Bổ sung (b, a) vào R cho mỗi (a, b) trong R

- Tức $R \cup R^{-1}$

#### Transitive closures - Bao đóng bắc cầu
>The connectivity relation R* consists of the pairs (a, b) such that there is a path of length at least one from a to b in R.

- Bổ sung (a, c) vào R cho mỗi (a, b), (b, c) trong R

#### Connectivity relation R*
![simpleTransitiveClosure.png](https://github.com/thou05/discrete-mathematics/blob/main/img/simpleTransitiveClosure.png)


**A FASTER TRANSITIVE CLOSURE ALGORITHM**

>	**Procedure**: transClosure($M_R$ : zero-one $n \times n$ matrix)
>	
>	A := $M_R$
>	
>	for i := 1 to $\lceil log_2n \rceil$
>	
>		A := A $\odot$ (A + $I_n$)
>		
>	return A


> The transitive closure of a relation R = the connectivity relation R* 

> Let $M_R$ be the zero–one matrix of the relation R on a set with n elements. Then the zero–one matrix of the transitive closure R* is 
>     $M_{R*} = M_R \vee M^2_R \vee M^3_R \vee ... \vee M^n_R$  

**VD**: 
A = {a, b, c, d} => n = 4

R = {(a, b), (b, d), (c, c), (d, b), (d, a)}

Tìm R* ?

![](https://github.com/thou05/discrete-mathematics/blob/main/img/exampleTransitiveClosure.png)


=> R* = ${(a, a), (a, b), (a, d)...}$


#### Warshall Algorithm
![warshall.png](https://github.com/thou05/discrete-mathematics/blob/main/img/warshall.png)

- B1: Tìm $W_0 = M_R$ 
- B2: Tìm $W_k$ (k = 1 -> n) theo quy tắc
	- Giữ lại hàng k cột k từ $W_{k-1}$ -> $W_k$ 
	- Giữ lại các phần tử = 1 từ $W_{k-1}$ -> $W_k$ 
	- Các phần tử còn lại xác định bằng phép hội gióng lên hàng k cột k tương ứng 
	=> $R* = W_n$ 

VD:
![](https://github.com/thou05/discrete-mathematics/blob/main/img/exampleWarShall.png)

=> $R_{BC} ={(a,a), (a,c), (a,e), (b,e), (c,a), (c,c), (c,e), (d,d)}$


## 5. Equivalence relations - Quan hệ tương đương
- Quan hệ tương đương trên A là quan hệ hai ngôi bất kì mà phản xạ, đối xứng và bắc cầu
#### Equivalence classes

#### Partitions - Phân hoạch
- Phân hoạch của tập A là tập mọi lớp tương đương của 1 quan hệ tương đương nào đó
- Chúng chia tập A thành các mảnh rời nhau, mỗi mảnh chứa mọi phần tử tương đương với nhau

## 6. Partial Orderings - Thứ tự bộ phận


