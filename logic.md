## 1. Logic mệnh đề
#### 1.1 ĐN mệnh đề
- Mệnh đề đơn gồm
	- 1 khẳng định
	- có giá trị chân lý true or false
#### 1.2 Phép toán
- Negation - Phép phủ định của 1 mệnh đề đơn p
	- KH: $\bar{p}$ or $\neg{p}$
	- nhận giá trị chân lý ngược với giá trị chân lý của p
- Conjunction - Phép hội: hội của 2 mệnh đề đơn p và q là mệnh đề phức
	- KH: $p \wedge q$
	- chỉ nhận giá trị **đúng khi p và q cùng đúng**
- Disjunction - Phép tuyển: tuyển của 2 mệnh đề đơn p và q là mệnh đề phức
	- KH: $p \vee q$
	- chỉ nhận giá trị **sai khi p và q cùng sai**
	- khi p và q cùng đúng: tuyển bao trùm
- XOR - Phép tuyển loại trừ: tuyển loại trừ của 2 mệnh đề đơn p và q là mệnh đề phức
	- KH: $p \oplus q$
	- chỉ **đúng** khi p và q nhận **giá trị chân lý ngược nhau**
- Implication - Phép kéo theo: Mệnh đề đơn p kéo theo q là mệnh đề phức
	- KH: $p \rightarrow q$
	- **chỉ sai khi p đúng q sai**
	- các câu mệnh đề có thể diễn tả
		- p là dkien của q $\to$ dkien đủ của q là p
		- q là dkien cần của p $\to$ dkien cần của p là q
- Phép toán điều kiện 2 phía
	- KH: $p \leftrightarrow q$
	- chỉ nhận giá trị **đúng** khi p và q có **giá trị chân lý giống nhau**
	- khi và chỉ khi, ddkien cần và đủ

- Thứ tự ưu tiên phép toán : theo thứ tự từ trên xuống dưới
	- () 
	- $\neg$ 
	- $\vee \wedge \oplus$
	- $\leftrightarrow$

#### 1.3 Các mệnh đề tương đương
Các luật tương đương

	![](https://github.com/thou05/discrete-mathematics/blob/main/img/logicalequivalences.png.png)
	![](https://github.com/thou05/discrete-mathematics/blob/main/img/hangdangthuc1.png.png)
	![](https://github.com/thou05/discrete-mathematics/blob/main/img/hangdangthuc2.png.png)
	![](https://github.com/thou05/discrete-mathematics/blob/main/img/hangdangthuc3.png.png)
	![](https://github.com/thou05/discrete-mathematics/blob/main/img/tuongduong3.png.png)

#### 1.4 Hằng đúng và hằng sai
- Hằng đúng (sai) là mệnh đề phức mà luôn là đúng (sai) không phụ thuộc vào giá trị chân lý của các mệnh đề nguyên tố thành phần
- (không thi) Thỏa được là có thể vừa đúng vừa sai 

- Cách kiểm tra mệnh đề
	- C1: Bảng chân lý
	
		![](https://github.com/thou05/discrete-mathematics/blob/main/img/dungsaibangchanly.png.png)
		
	- C2: Sử dụng phép biến đổi tương đương logic
	
		![](https://github.com/thou05/discrete-mathematics/blob/main/img/dungsaituongduong.png.png)
		
	- C3: Lập luận
	
		![](https://github.com/thou05/discrete-mathematics/blob/main/img/dungsailapluan.png.png)
#### 1.5 Chuẩn tắc tuyển
- Hội sơ cấp: hội hoặc phủ định của các mệnh đề đơn
- Dạng CCT: **tuyển của các hội** sơ cấp

- (khong thi) Chuẩn tắc hội
	- Tuyển sơ cấp: tuyển hoặc phủ định của các mệnh đề đơn
	- Dạng CTH: hội của các tuyển sơ cấp

#### 1.6 Chuẩn tắc tuyển hoàn toàn
- CTTHT là dạnh chuẩn tắc tuyển mà ở đó mọi tuyển sơ cấp đều chứa đầu đủ các biến mệnh đề đơn
- chỉ lấy bộ giá trị làm A đúng

	![](https://github.com/thou05/discrete-mathematics/blob/main/img/chuantactuyenhoantoan.png.png)

- (khong thi) Chuẩn tắc hội 

	![](https://github.com/thou05/discrete-mathematics/blob/main/img/chuantachoihoantoan.png.png)
#### 1.7 Tối thiểu hóa Quine Mc-Cluskey
Các bước
- B1: Biểu diễn thành các **xâu bít 0, 1**
- B2: **Sắp xếp** xâu bít theo chiều tăng dần các số 1 và phân chia thành các lớp
- B3: Làm **giảm độ dài** xâu bít : Nếu cặp bít chỉ khác ở đúng 1 vị trí thì ghép cặp và bỏ bit ở vị trí khác đó
	- chỉ xét 2 lớp liên tiếp với nhau
	- xét cùng vị trí số 1 
	- những lần sau nhìn bit bỏ đi và số 1
- B4: **Đánh dấu** xâu bít tham gia B3
- B5: Lặp lại b2-> 4 cho đến khi không giảm độ dài xâu được nữa
- B6: Biểu diễn xâu bít **không bị đánh dấu thành HSC** 
- B7: Từ HSC thu được tìm tập con nhỏ nhất phủ toàn bộ biểu thức cần tối thiểu (**lập bảng phủ**)
	=> Tuyển của các HSC là biểu thức tối thiểu cần tìm

## 3. Logic vị từ - Predicate Logic
#### 3.1 Khái niệm
- Logic vị từ là mở rộng logic mệnh đề, cho phép suy luận chính xác về cả lớp các thực thể (kho hieu vl)
	- Logic mệnh đề coi các mệnh đề đơn giản như các thực thể nguyên tố (atomic entities)
	- Logic vị từ phân biệt chủ ngữ (subjects) khỏi vị ngữ (predicates)
- Quy ước
	- x, y, z: đối tượng/ thực thể
	- P, Q, R: hàm mệnh đề (vị ngữ)

#### 3.2 Hàm mệnh đề - Propositional Functions
- Logic vị từ khái quát hóa các định nghĩa ngữ pháp của vị ngữ thành các hàm có một số đối số tùy ý

#### 3.3 Biểu thức lượng tử
- Lượng tử là các ký hiệu để ta ước lượng có bao nhiêu đối tượng trong vũ trụ khẳng định thỏa mãn vị ngữ đã cho
- $\forall$ (FOR $\forall$ LL)

	$\forall x P(x)$ : vói mọi x trong ..., P thỏa mãn
	
- $\exists$ ( $\exists$ XITS)

	$\exists x P(x)$ : tồn tại x trong ... (có 1 hoặc nhiều hơn) sao cho P(x) là đúng
	

-  Biến bị trói buộc và tự do

-  Lồng lượng tử

#### 3.4 Luật suy diễn

## Bài tập 
Các bài ôn thi: 1gi , 2, 3cd, 4,5,14,19 

```
Note: Khi gặp hằng đúng sai thỏa được, kẻ bảng chân lý ra nháp check là loại nào -> chứng minh  
```

`1.`
g. $\neg ((p \space \oplus \space r \to (q \vee \neg r)) \to \neg(p \leftrightarrow r)$ 
   
$\Leftrightarrow \space \neg(\neg(p \oplus r) \vee (q \vee \neg r) \to \neg \neg(p \oplus r)$ 

$\Leftrightarrow \space \neg(p \oplus r) \vee (q \vee \neg r) \vee (p \oplus r)$

$\Leftrightarrow \space (q \vee \neg r) \vee 1$

$\Leftrightarrow \space 1 (đpcm)$ 


i. $((p \vee q) \wedge (p \to r) \wedge (q \to r)) \to r$ 

$\Leftrightarrow \space ((p \vee q) \wedge (\neg p \vee r) \wedge (\neg q \vee r)) \to r$

$\Leftrightarrow \space ((p \vee q) \wedge (r \vee (\neg p \wedge \neg q))) \to r$

$\Leftrightarrow \space ((p \vee q) \wedge (r \vee \neg (p \vee q))) \to r$ 

$\Leftrightarrow \space (((p \vee q) \wedge r) \vee ((p \vee q) \wedge \neg (p \vee q))) \to r$

$\Leftrightarrow \space (((p \vee q) \wedge r) \vee 0) \to r$  

$\Leftrightarrow \space ((p \vee q) \wedge r) \to r$ 

$\Leftrightarrow \space \neg ((p \vee q) \wedge r) \vee r$ 

$\Leftrightarrow \space (\neg (p \vee q) \vee \neg r) \vee r$ 

$\Leftrightarrow \space \neg (p \vee q) \vee (\neg r \vee r)$ 

$\Leftrightarrow \space (\neg (p \vee q) \vee 1$

$\Leftrightarrow \space 1 \space (đpcm)$

`4. Trong các phát biểu sau, phát biểu nào là mệnh đề? Nếu là mệnh đề, hãy biểu diễn nó thành công thức logic tương ứng.`

a. Hà Nội là thủ đô của Mỹ 

	=> là mệnh đề , biểu thức logic: a
	
b. Hãy biết tận dụng tài nguyên thời gian của bạn

	=> Không phải mệnh đề vì là câu lời khuyên
	
c. Linh học toán có giỏi không?

	=> không phải mệnh đề vì là câu hỏi
	
d. Nếu bạn đi học bằng xe máy thì hãy mang theo bằng lái.

	=> Không phải mệnh đề vì là câu cầu khiến
	
e. Bạn sẽ đến lớp đúng giờ khi và chỉ khi bạn đi bằng xe máy.

	=> là mệnh đề a <-> b
	
f. Mọi học sinh khoa Công nghệ thông tin đều học môn Toán rời rạc

	=> là mệnh đề
	
	P(x, y) = "x khoa y"
	
	Q(x, y) = "x học môn y"
	
	=> $\forall x((x, CNTT) \to Q(x, TRR))$

g. Số nguyên x là số dương.

	=> Không phải mệnh đề vì x chưa rõ, chưa xác định được chân lý

h. Số nguyên lẻ không chia hết cho 2.

i. Mọi số nguyên đều chia hết cho số nguyên y

j. Tồn tại số nguyên chia hết cho số y

k. Có những sinh viên khoa Công nghệ thông tin không học môn Xử lý ảnh.

	P(x,y) = "x khoa y"
	
	Q(x,y) = "x học môn y"
	
	=> $\exists x(P(x, CNTT) \wedge \neg Q(x, XLA))$ 
	
l. Điều kiện cần để Nam được chọn đi học là Nam phải biết tiếng Anh hoặc tiếng Nhật.

m. $\exists x \forall y P(x,y) \to \exists z Q(z)$

	=> Là mệnh đề vì đầy đủ biến ràng buộc
	
n. $\forall x \exists y(Q(x, y, z) \wedge P(x))$ 

	=> Không phải mệnh đề vì biến z là biến tự do


`5.`
c. C = $(p \wedge q \to u) \to ((q \vee \overline{p}) \to u \wedge p)$

|  p  |  q  |  u  | $p \wedge q$ | $p \wedge q \to u$ | $\overline{p}$ | $q \vee \overline{p}$ | $u \wedge p$ | $(q \vee \overline{p}) \to u \wedge p)$ |  C  |
| :-: | :-: | :-: | :----------: | :----------------: | :------------: | :-------------------: | :----------: | :-------------------------------------: | :-: |
|  0  |  0  |  0  |      0       |         1          |       1        |           1           |      0       |                    0                    |  0  |
|  0  |  0  |  1  |      0       |         1          |       1        |           1           |      0       |                    0                    |  0  |
|  0  |  1  |  0  |      0       |         1          |       1        |           1           |      0       |                    0                    |  0  |
|  0  |  1  |  1  |      0       |         1          |       1        |           1           |      0       |                    0                    |  0  |
|  1  |  0  |  0  |      0       |         1          |       0        |           0           |      0       |                    1                    |  1  |
|  1  |  0  |  1  |      0       |         1          |       0        |           0           |      1       |                    1                    |  1  |
|  1  |  1  |  0  |      1       |         0          |       0        |           1           |      0       |                    0                    |  1  |
|  1  |  1  |  1  |      1       |         1          |       0        |           1           |      1       |                    1                    |  1  |

Vậy C = $p\overline{qu} + p\overline{q}u + pq\overline{u} + pqu$ 

`12.` Cho L(x,y) = "x yêu y", với không gian là tập hợp mọi người trên thế giới

a. Mọi người đều yêu hoa    
    
	=> $\forall x L(x,Hoa)$ 
	
b. Có một người mà Hạnh không yêu 
      
	=> $\exists x \neg L(Hanh, x)$
	
c. Không có ai yêu tất cả mọi người   
       
	=> $\neg (\exists x \forall y(L(x,y))$ 
	
d. Tồn tại một người yêu tất cả mọi người nhưng không yêu mình   

	=> $\exists x \forall y(P(x, y) \wedge \neg P(x,x))$  

`15.`
```
Note: 
- phân tích xem có bao nhiêu câu đơn, mỗi câu đơn biểu diễn thành 1 vị từ - tách chủ ngữ và vị ngữ
- với mọi thì dùng phép kéo theo
- tồn tại thì dùng phép hội
```

a. Tất cả các sinh viên tin học đều cần phải học môn toán rời rạc

b. Có một sinh viên ở lớp này đã có máy vi tính

c. Tất cả các **sinh viên ở lớp này** đều đã **học ít nhất một *môn** về tin học*

	Chọn không gian xác định là U = tập vũ trụ khẳng định
	
	Định nghĩa các vị từ:
	
		P(x,y) = "x ở lớp y"
		
		Q(x,y) = "x học môn y"
		
		F(x,y) = "môn x về lĩnh vực y"
		
	C = $\forall x(P(x,lớp \space này) \to \exists y (Q(x,y) \wedge F(y, tin \space học)))$ 

d, Có một sinh viên của lớp này đã học ít nhất một môn về tin học
	
e, Mỗi sinh viên của lớp này ở một nhà trong ký túc xá

	P(x,y) = "x lớp y"
	
	Q(y,x) = "y ở nhà x"
	
	R(x,y) = "nhà x nằm trong khu y"
	
	=> E = $\forall x(P(x, lớp \space này) \to \exists y(P(x,y) \wedge R(y, KTX)$ 

f, Có một sinh viên của lớp này đã ở tất cả các phòng của ít nhất một nhà trong ký túc xá

g, Tất cả sinh viên của lớp này ít nhất đã ở một phòng trong tất cả các nhà của ký túc xá

## Đề thi - câu 1
1. Trong các phát biểu sau, phát biểu nào không là mệnh đề, phát biểu nào là mệnh đề? Vì sao?
	- Không nên đi xe máy khi bạn chưa đủ 16 tuổi
	- $\forall x(P(x) \to \exists yQ(x,y))$
	- Mọi số nguyên đều chia hết cho số nguyên x
	- Có ít nhất một bạn sinh viên khoa CNTT đạt học bổng Honda Yes
	- $\forall x(P(x,z) \to \exists yQ(x,y))$

	Giải
	
	a. Không là mệnh đề vì đây là câu lời khuyên
	
	b. Là mệnh đề vì đầy đủ các biến ràng buộc
	
	c. Không là mệnh đề vì x là biến tự do, không biết đúng sai
	
	d. Là mệnh đề 
	
	e. Không là mệnh đề vì biến z là biến tự do

2. Tìm dạng chuẩn tắc tuyển hoàn toàn của biểu thức logic mệnh đề là B, sau đó tối thiểu hóa biểu thức nhận được bằng phương pháp Quine-Mc Cluskey
		B = $((p \oplus q) \vee (u \to \neg p \to q)) \leftrightarrow \neg u$ 
```
Note:
Các bước giải
Bảng chân lý -> lấy giá trị 1
Chuyển về dangj 01
Bảng rút gọn
Bảng phủ

```
 
Giải

Đặt B1 = $(p \oplus q) \vee (u \to \overline{p} \to q)$

Bảng chân lý

|  p  |  q  |  u  | $p \oplus q$ | $\overline{p}$ | $u \to \overline{p}$ | $u \to \overline{p} \to q$ | B1  | $\overline{u}$ |  B  |
| :-: | :-: | :-: | :----------: | :------------: | :------------------: | :------------------------: | :-: | :------------: | :-: |
|  0  |  0  |  0  |      0       |       1        |          1           |             0              |  0  |       1        |  0  |
|  0  |  0  |  1  |      0       |       1        |          1           |             0              |  0  |       0        |  1  |
|  0  |  1  |  0  |      1       |       1        |          1           |             1              |  1  |       1        |  1  |
|  0  |  1  |  1  |      1       |       1        |          1           |             1              |  1  |       0        |  0  |
|  1  |  0  |  0  |      1       |       0        |          1           |             0              |  1  |       1        |  1  |
|  1  |  0  |  1  |      1       |       0        |          0           |             1              |  1  |       0        |  0  |
|  1  |  1  |  0  |      0       |       0        |          1           |             1              |  1  |       1        |  1  |
|  1  |  1  |  1  |      0       |       0        |          0           |             1              |  1  |       0        |  0  |

=> B = $\overline{pq}u + \overline{p}q\overline{u} + p\overline{qu} + pq\overline{u}$

B(0,1) = 001 + 010 + 100 + 110

```
Bảng rút gọn
(1) 001      (2,4) _10
(2) 010 v    (3,4) 1_0
(3) 100 v
---
(4) 110 v
```
=> Hội sơ cấp rút gọn: $\overline{pq}u + q\overline{u} + p\overline{u}$


Bảng phủ

|                  | $\overline{pq}u$ | $\overline{p}q\overline{u}$ | $p\overline{qu}$ | $pq\overline{u}$ |
| :--------------: | :--------------: | :-------------------------: | :--------------: | :--------------: |
| $\overline{pq}u$ |        +         |                             |                  |                  |
| $q\overline{u}$  |                  |          $\oplus$           |                  |        +         |
| $p\overline{u}$  |        +         |                             |     $\oplus$     |        +         |
|                  |        v         |              v              |        v         |        v         |

=> B(p,q,u) = $q\overline{u} + p\overline{u}$

3. Tìm dạng chuẩn tắc tuyển hoàn toàn của biểu thức logic mệnh đề là B, sau đó tối thiểu hóa biểu thức nhận được bằng phương pháp Quine-Mc Cluskey

		B = $((p \oplus q) \vee (u \to \neg p \wedge q)) \leftrightarrow \neg u$ 
		

4. Hãy tối thiểu hóa biểu thức sau bằng phương pháp Quine-Mc Cluskey

		B = $\overline{x}yz\overline{t} + x\overline{y}zt + xt\overline{zt} + \overline{xy}zt + x\overline{yz}t + \overline{xyzt} + \overline{x}y\overline{zt} +  x\overline{y}z\overline{t}$

5. Cho không gian của $U_1$ là tập tất cả các sinh viên trong trường ĐH GTVT, $U_2$ là tập gồm các khoa trong trường ĐH GTVT, $U_3$ là tập các môn học. Q(x,y) là vị từ: “x học môn y”, P(x,y) là vị từ “x là sinh viên khoa y". Hãy sử dụng các vị từ trên để biểu diễn các câu sau:  
	- Có ít nhất một sinh viên khoa Cơ khí không học môn tiếng Nhật  
	- Nam là sinh viên khoa CNTT khi và chỉ khi Nam học môn Cấu trúc dữ liệu và giải thuật.

	Giải
	
	a. $\exists x(P(x, cơ \space khí) \wedge \neg Q(x, tiếng \space nhật))$
	
	b. Q(nam, CNTT) <-> P(Nam, CTDLGT)

6. Hãy kiểm tra tính hằng đúng, sai, thỏa được của biểu thức logic mệnh đề sau (không dùng bảng chân lý)

		A = $(((p \wedge \overline{r}) \vee q) \wedge (q \to r)) \to (p \vee r)$ 

	Giải
	
	A = $(((p \wedge \overline{r}) \vee q) \wedge (q \to r)) \to (p \vee r)$\\
	<=> $(((p \wedge \overline{r}) \vee q) \wedge (q \to r)) \to (p \vee r)$\\
	
	<=> $(\overline{((p \wedge \overline{r}) \vee q) \wedge (\overline{q} \vee r)}) \vee (p \vee r)$ 
	
	<=> $((\overline{(p \wedge \overline{r}) \vee q)} \vee \overline{(\overline{q} \vee r)}) \vee (p \vee r)$ 
	
	<=> $((\overline{(p \wedge \overline{r})} \wedge \overline{q}) \vee \overline{(\overline{q}} \wedge \overline{r})) \vee (p \vee r)$ 
	
	<=> $((\overline{p} \vee r) \wedge \overline{q}) \vee (q \wedge \overline{r})) \vee (p \vee r)$ 
	
	<=> $(((\overline{p} \wedge \overline{q}) \vee (r \wedge  \overline{q}) \vee (q \wedge \overline{r})) \vee (p \vee r)$ 
	
	<=> $(\overline{p} \wedge \overline{q}) \vee (r \wedge  \overline{q}) \vee (q \wedge \overline{r}) \vee p \vee r$ 
	
	<=> $((\overline{p} \wedge \overline{q}) \vee p) \vee (r \wedge  \overline{q}) \vee ((q \wedge \overline{r})  \vee r)$ 
	
	<=> $((\overline{p} \vee p) \wedge (\overline{q} \vee p)) \vee (r \wedge  \overline{q}) \vee ((q \vee r) \wedge (\overline{r} \vee r))$ 
	
	<=> $(1 \wedge (\overline{q} \vee p)) \vee (r \wedge  \overline{q}) \vee ((q \vee r) \wedge 1)$ 
	
	<=> $(\overline{q} \vee p) \vee (r \wedge  \overline{q}) \vee (q \vee r)$ 
	
	<=> $\overline{q} \vee p \vee (r \wedge  \overline{q}) \vee q \vee r$ 
	
	<=> $(\overline{q} \vee q) \vee p \vee (r \wedge  \overline{q}) \vee r$ 
	
	<=> $1 \vee p \vee (r \wedge  \overline{q}) \vee r$ 
	
	<=> $1 \space (đpcm)$ 
	


----
## References
1. [Bài 3 Chuẩn tắc tuyển, chuyển tắc hội, tối thiếu hóa]( https://www.youtube.com/watch?v=MyGyI27UhsU)
2. [ Tối thiểu hóa biểu thức logic mệnh đề bằng Thuật toán Quine_McCluskey](https://youtu.be/8YbbV42UX7Q?si=IPh87YLa2YLgIBMh)
3. [Biểu thức lượng tử - Dr.Luong Thai Le](https://drive.google.com/file/d/1yAAI3wQp8XQuTBQKbdAYQ6jgZTcp6sJD/view?t=19)
4. https://cuuduongthancong.com/atc/2888/logic-bac-nhat,-cu-phap-va-ngu-nghia-cac-luong-tu,-hop-giai-voi-logic-vi-tu


