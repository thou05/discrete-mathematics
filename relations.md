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

<img src="https://github.com/thou05/discrete-mathematics/blob/main/img/simpleTransitiveClosure.png" width="500" height=auto>
<img src="https://github.com/thou05/discrete-mathematics/blob/main/img/fasterTranstiveClosure.png" width="500" height=auto>


-  The transitive closure of a relation R = the connectivity relation R* 

- Let $M_R$ be the zero–one matrix of the relation R on a set with n elements. Then the zero–one matrix of the transitive closure R* is 
>$M_{R*} = M_R \vee M^2_R \vee M^3_R \vee ... \vee M^n_R$  

```
Ví dụ
A = {a, b, c, d} => n = 4
R = {(a, b), (b, d), (c, c), (d, b), (d, a)}
Tìm R* ?
```
<img src="https://github.com/thou05/discrete-mathematics/blob/main/img/exampleTransitiveClosure.png" width="500" height=auto>

=> R* = ${(a, a), (a, b), (a, d)...}$


#### Warshall Algorithm
<img src="https://github.com/thou05/discrete-mathematics/blob/main/img/warshall.png" width="500" height=auto>

- B1: Tìm $W_0 = M_R$ 
- B2: Tìm $W_k$ (k = 1 -> n) theo quy tắc
	- Giữ lại hàng k cột k từ $W_{k-1}$ -> $W_k$ 
	- Giữ lại các phần tử = 1 từ $W_{k-1}$ -> $W_k$ 
	- Các phần tử còn lại xác định bằng phép hội gióng lên hàng k cột k tương ứng 
	=> $R* = W_n$ 
	
Ví dụ:

<img src="https://github.com/thou05/discrete-mathematics/blob/main/img/exampleWarShall.png" width="500" height=auto>



## 5. Equivalence relations - Quan hệ tương đương
- Quan hệ tương đương trên A là quan hệ hai ngôi bất kì mà phản xạ, đối xứng và bắc cầu
- Equivalence classes
-  Partitions - Phân hoạch
	- Phân hoạch của tập A là tập mọi lớp tương đương của 1 quan hệ tương đương nào đó
	- Chúng chia tập A thành các mảnh rời nhau, mỗi mảnh chứa mọi phần tử tương đương với nhau

```
VD Câu 16: Cho quan hệ R chứa tất cả các cặp (x,y) trong đó x và y là các xâu bít có chiều dài lớn hơn hoặc bằng 3 và có 3 bít đầu tiên như nhau.
a, Hỏi R có phải là một quan hệ tương đương trên tập các xâu bít có chiều dài lớn hơn hoặc bằng 3 không? Vì sao?
b, Nếu có hãy xác định lớp tương đương của các xâu bít: 011, 11111, 10110100

Giải
a.
- Mọi cặp (x, x) thuộc R => R phản xạ
- Nếu (x, y) thuộc R thì x và y có 3 bit đầu tiên như nhau => y và x cũng có 3 bit đầu tiên như nhau => (y, x) thuộc R => R đối xứng
- Nếu (x, y) thuộc R => x và y có 3 bit đầu tiên như nhau
	  (y, z) thuộc R => y và z có 3 bit đầu tiên như nhau
	=> x và z có 3 bit đầu tiên như nhau
=> R là quan hệ tương đương

b.
[011]      = {x | x là xâu bit có 3 phần tử đầu là 011}
[11111]    = {x | x là xâu bit có 3 phần tử đầu là 111}
[10110100] = {x | x là xâu bit có 3 phần tử đầu là 101}
```


### Equivalence classes


### Partitions - Phân hoạch
- Phân hoạch của tập A là tập mọi lớp tương đương của 1 quan hệ tương đương nào đó
- Chúng chia tập A thành các mảnh rời nhau, mỗi mảnh chứa mọi phần tử tương đương với nhau

## 6. Partial Orderings - Thứ tự bộ phận
Quan hệ R trên S được gọi là thứ tự bộ phận (par- tial order) nếu nó phản xạ, phản đối xứng, và bắc cầu.

`VD Câu 15`: Cho tập A = {S| S $\subseteq$ Z}, và quan hệ thứ tự $\subseteq$ trên A. Cho S1 = {-4, 2, 4, 6, 0} và S2 = {0, 2, 5, 6, -3}. Hãy tìm cận trên nhỏ nhất và cận dưới lớn nhất của S1 và S2


- Cận trên nhỏ nhất: là một cận trên và nhỏ hơn mọi cận trên khác $S_1 \cup S_2$
- Cận dưới lớn nhất : là một cận dưới và lớn hơn mọi cận dưới khác $S_1 \cap S_2$ 
- Dàn đẩy đủ: mọi tập con đều có cận dưới lớn nhât và cận trên nhỏ nhất trong tập đó

## Đề thi mẫu - Câu 3

```
1. Cho quan hệ R = {(1,1), (1,3), (2,2), (3,1), (3,3), (4,4)} trên tập A = {1, 2, 3 ,4}
a. R là quan hệ tương đương hay quan hệ thứ tự ? Vì sao ?
b. Nếu R là quan hệ tương đương, hãy tìm một phân hoạch trên tập A tương ứng với R. Nếu R là quan hệ thứ tự, hãy tìm cận dưới lớn nhất và cận trên nhỏ nhất theo R của 2 phần tử (7, 9)

Giải
a. 
- Mọi cặp (x, x) thuộc R : (1,1) (2,2) (3,3) (4,4) => R có tính phản xạ
- Mọi (x,y) thuộc R đều có (y,x) thuộc R => R đối xứng
- Vì có cặp (1, 3) và (3,1) => R không phản xứng
- Mọi (x,y) thuộc R và mọi (y,z) thuộc R đều có (x,z) thuộc R => R có tính bắc cầu
=> R là quan hệ tương đương
b. Lớp tương đương
[1] = {1, 3}
[2] = {2}
[3] = {3, 1}
[4] = {4}
```

```
2. Cho tập A = {1,3,5,9,15,30} và quan hệ hai ngôi R trên A định nghĩa như sau: 
				R = {(a,b)| a|b}
Hãy tìm cận dưới lớn nhất và cận trên nhỏ nhất theo R của 2 phần tử (5, 15). Tập (A,R) có phải là một dàn đầy đủ không?

Giải:
Ta có R = {(1,1), (3,3), (5,5), (9,9), (15,15), (30,30), (1,3), (1,5), (1,9), (1,15), (1,30), (3,9), (3,15), (3,30), (5,15), (5,30), (15,30)}
- Cận dưới lớn nhất của (5,15) = UCLN(5,15) = 1
- Cận trên nhỏ nhất của (5,15) = BCNN(5,15) = 15

Tập (A,R) không là dàn đầy đủ vì cặp (9,15) không có BCNN trên A 

Lưu ý:
- a | b : a là ước của b hay b chia hết cho a
- Tập (A, R): tập A với quan hệ R định nghĩa thứ tự phân hoạch.
	Với mọi cặp (a,b) thuộc a, ta luôn có thể tìm đc UCLN hoặc BCNN thuộc a 
```

```
3. Cho quan hệ R trên tập A chứa tất cả các xâu tam phân có độ dài 5 sao cho:
	R = {(s,t) | xâu s và xâu t chứa cùng một số các chữ số 2}
a. R là quan hệ tương đương hay quan hệ thứ tự ? Vì sao ?
b. Nếu R là quan hệ tương đương, hãy tìm một phân hoạch trên tập A tương ứng với R. Nếu R là quan hệ thứ tự thì tập (A,R) có phải alf một dàn đầy đủ không vì sao?

Giải
a. 
- Mọi cặp (s,s) thuộc R => R phản xạ
- Nếu (s,t) thuộc R thì s và t có cùng số chữ số 2 => t và s cùng số chữ số 2 => (t, s) thuộc R => có tính đối xứng
- Nếu (s,t) thuộc R => s và t có cùng số chữ số 2
	  (t,z) thuộc R => t và z có cùng số chữ số 2
	=> (s,z) có cùng số chữ số 2
	=> có bắc cầu
=> R là quan hệ tương đương
b. Phân hoạch của tập A theo số chữ số 2 là:
[0] = {00000, 000001, 11111, ...}
[1] = {20000, 21111, 00002, ...}
[2] = {22000, 22111, 11122, ...}
[3] = {22200, 22211, 11122...}
[4] = {22220, 22221, 12222...}
[5] = {22222}
```

```
4. Cho tập A = {x,y,z,t,u} và quan hệ 2 ngôi R trên A

	R = {(x,x),(x,z),(y,t),(z,u),(u,u),(u,x),(t,z),(t,t)}
	
Sử dụng thuật toán Warshall tìm bao đóng bắc cầu của R (thể hiện thuật toán dưới sự biến đối của ma trận 0-1 biểu diễn quan hệ)
```

```
5. Cho tập A = {a,b,c,d,e} và quan hệ 2 ngôi R trên A

	R = {(a,c),(a,e),(b,d),(c,c),(c,a),(d,b),(e,d)}
	
Sử dụng thuật toán đơn giản tìm bao đóng bắc cầu của R (thể hiện thuật toán dưới sự biến đối của ma trận 0-1 biểu diễn quan hệ)
```

```
6. Cho tập A = {a,b,c,d,e} và quan hệ 2 ngôi R trên A
	R = {(a,d),(a,a),(b,c),(b,e),(c,c),(c,a),(d,e),(e,c)}

a. R có các tính chất phi phản xạ, phản đối xứng không? Vì sao?
b. Sử dụng thuật toán Warshall tìm bao đóng bắc cầu của R (thể hiện thuật toán dưới sự biến đối của ma trận 0-1 biểu diễn quan hệ)

Giải
a. 
- Vì (a,a) và (c,c) thuộc R => không phi phản xạ
- Mọi (x,y) thuộc R và (y,x) không thuộc R với x khác y => phản đối xứng
b.
```

-----
## References
1. https://caolacvc.blogspot.com/2018/11/full-ky-tu-latex.html
2. https://www.studocu.com/vn/document/truong-dai-hoc-sai-gon/cau-truc-roi-rac/ctrr-chuong-5-quan-he-bai-tap/28486521
3. https://phamtyn.wordpress.com/2016/06/29/quan-he-thu-tuorder-relation/
4. https://cuuduongthancong.com/atc/2481/quan-he-(relation)/dinh-nghia-quan-he/cac-tinh-chat-cua-quan-he

