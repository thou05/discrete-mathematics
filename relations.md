<link rel="stylesheet" type="text/css" href="file:///Users/pat/Library/Application Support/abnerworks.Typora/themes/newsprint.css">

<style>
   img{
   	width: 300px;
   	height: auto;
   }
</style>


## 1. Relations and their properties
### 1.1 Binary relations - Quan hệ hai ngôi 
- Quan hệ 2 ngôi R từ A và B là tập con của A x B
- Ký hiệu: aRb <=> $(a, b) \in R$
- aRb ta nói a quan hệ với b
- Quan hệ 2 ngôi R tương ứng với hàm vị từ $P_R: AxB$ -> ${T, F}$ xác định trên tích đề các của A, B
- VD:
	- Quan hệ cùng lớp: a cùng lớp với b
	- Quan hệ ước số: a | b

### 1.2 Complementary relations - Quan hệ bù
- $\not R$ = (A x B) - R

### 1.3 Inverse relations - Quan hệ ngược
- Quan hệ 2 ngôi $R: A x B$ có quan hệ ngược $R^{-1}: B x A$
### 1.4 Relations on a set - Quan hệ trên một tập hợp
- Quan hệ hai ngôi từ A vào chính nó đgl quan hệ trên A

- **Reflexivity** - Phản xạ: aRa, $\forall a \in A$
- **Irreflexive** - Phi phản xạ: quan hệ bù của nó $\not R$ là phản xạ
- Symmetry - Đối xứng: $R = R^{-1}$, $(a, b) \in R$ <-> $(b, a) \in R$
- Antisymmetry - Phản xứng: $\forall a $
- Transitivity - Bắc cầu
	- $(a,b) \in R \wedge (b, c) \in R \to (a,c) \in R$,  $\forall a, b, c$ 

### 1.5 Composite relations - Tích quan hệ


## 2. n-ary Relations and their applications


![](https://i.imgur.com/waxVImv.png)
## 3. Representing relations
### Using matrices

### Using digraphs



====================================================================
## 4. Closures of relations - Bao đóng của quan hệ
"Bao đóng X" của quan hệ R được định nghĩa là tập cha nhỏ nhất của R mà có tính chất đó
### 4.1 Reflexive closure - Bao đóng phản xạ
- Bổ sung (a, a) vào R với mỗi $a \in A$

- Tức $R \cup I_A$
### 4.2 Symmetric closure - Bao đóng đối xứng
- Bổ sung (b, a) vào R cho mỗi (a, b) trong R

- Tức $R \cup R^{-1}$

### 4.3 Transitive closures - Bao đóng bắc cầu
>The connectivity relation R* consists of the pairs (a, b) such that there is a path of length at least one from a to b in R.

- Bổ sung (a, c) vào R cho mỗi (a, b), (b, c) trong R

#### Connectivity relation R*

![simpleTransitiveClosure.png](https://github.com/thou05/discrete-mathematics/blob/main/img/simpleTransitiveClosure.png)

![](https://github.com/thou05/discrete-mathematics/blob/main/img/fasterTranstiveClosure.png)

<img src="https://github.com/thou05/discrete-mathematics/blob/main/img/simpleTransitiveClosure.png" >
<img src="https://github.com/thou05/discrete-mathematics/blob/main/img/fasterTranstiveClosure.png">


-  The transitive closure of a relation R = the connectivity relation R* 

- Let $M_R$ be the zero–one matrix of the relation R on a set with n elements. Then the zero–one matrix of the transitive closure R* is 
>$M_{R*} = M_R \vee M^2_R \vee M^3_R \vee ... \vee M^n_R$  



<details><summary>Xem ví dụ</summary>
<p>
A = {a, b, c, d} => n = 4

R = {(a, b), (b, d), (c, c), (d, b), (d, a)}

Tìm R* ?

![](https://github.com/thou05/discrete-mathematics/blob/main/img/exampleTransitiveClosure.png)

=> R* = ${(a, a), (a, b), (a, d)...}$
</p>
</details>

s

#### Warshall Algorithm
![warshall.png](https://github.com/thou05/discrete-mathematics/blob/main/img/warshall.png)

- B1: Tìm $W_0 = M_R$ 
- B2: Tìm $W_k$ (k = 1 -> n) theo quy tắc
	- Giữ lại hàng k cột k từ $W_{k-1}$ -> $W_k$ 
	- Giữ lại các phần tử = 1 từ $W_{k-1}$ -> $W_k$ 
	- Các phần tử còn lại xác định bằng phép hội gióng lên hàng k cột k tương ứng 
	=> $R* = W_n$ 

<details><summary>Xem ví dụ</summary>
<p>

![](https://github.com/thou05/discrete-mathematics/blob/main/img/exampleWarShall.png)

</p>
</details>



======================================================================
## 5. Equivalence relations - Quan hệ tương đương
- Quan hệ tương đương trên A là quan hệ hai ngôi bất kì mà phản xạ, đối xứng và bắc cầu
### Equivalence classes

### Partitions - Phân hoạch
- Phân hoạch của tập A là tập mọi lớp tương đương của 1 quan hệ tương đương nào đó
- Chúng chia tập A thành các mảnh rời nhau, mỗi mảnh chứa mọi phần tử tương đương với nhau

=======================================================================
## 6. Partial Orderings - Thứ tự bộ phận


