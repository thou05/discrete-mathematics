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
	![[Pasted image 20240901112837.png]]
	![[Pasted image 20240901113143.png]]
	![[Pasted image 20240902173816.png]]
	![[Pasted image 20240902173847.png]]
	![[Pasted image 20240904012350.png]]

#### 1.4 Hằng đúng và hằng sai
- Hằng đúng (sai) là mệnh đề phức mà luôn là đúng (sai) không phụ thuộc vào giá trị chân lý của các mệnh đề nguyên tố thành phần
- (không thi) Thỏa được là có thể vừa đúng vừa sai 

- Cách kiểm tra mệnh đề
	- C1: Bảng chân lý
		![[Pasted image 20240903015444.png]]
		
	- C2: Sử dụng phép biến đổi tương đương logic
		![[Pasted image 20240903015508.png]]
		
	- C3: Lập luận
		![[Pasted image 20240903015524.png]]
#### 1.5 Chuẩn tắc tuyển
- Hội sơ cấp: hội hoặc phủ định của các mệnh đề đơn
- Dạng CCT: **tuyển của các hội** sơ cấp

- (khong thi) Chuẩn tắc hội
	- Tuyển sơ cấp: tuyển hoặc phủ định của các mệnh đề đơn
	- Dạng CTH: hội của các tuyển sơ cấp

#### 1.6 Chuẩn tắc tuyển hoàn toàn
- CTTHT là dạnh chuẩn tắc tuyển mà ở đó mọi tuyển sơ cấp đều chứa đầu đủ các biến mệnh đề đơn
- chỉ lấy bộ giá trị làm A đúng

	![[Pasted image 20240904012819.png]]

- (khong thi) Chuẩn tắc hội 
	![[Pasted image 20240904012926.png]]
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
- $\forall$ (FOR$\forall$LL)
	$\forall x P(x)$ : vói mọi x trong ..., P thỏa mãn
	
	![[Pasted image 20240904034051.png]]
- $\exists$ ($\exists$XITS)
	$\exists x P(x)$ : tồn tại x trong ... (có 1 hoặc nhiều hơn) sao cho P(x) là đúng
	
	![[Pasted image 20240904034124.png]]

-  Biến bị trói buộc và tự do

-  Lồng lượng tử

#### 3.4 Luật suy diễn
----
src
- [Bài 3 Chuẩn tắc tuyển, chuyển tắc hội, tối thiếu hóa]( https://www.youtube.com/watch?v=MyGyI27UhsU)
- [ Tối thiểu hóa biểu thức logic mệnh đề bằng Thuật toán Quine_McCluskey](https://youtu.be/8YbbV42UX7Q?si=IPh87YLa2YLgIBMh)
- [Biểu thức lượng tử - Dr.Luong Thai Le](https://drive.google.com/file/d/1yAAI3wQp8XQuTBQKbdAYQ6jgZTcp6sJD/view?t=19)
- 
