## Sum and Product Rules
Quy tắc tổng và tích
- Giả sử m là số cách thực hiện nhiệm vụ 1 và n là số cách thực hiện nhiệm vụ 2 
	- các cách không phụ thuộc nhau
	- không thực hiện đồng thời
- Quy tắc
	- cộng: hoặc nhiệm vụ 1 hoặc nhiệm vụ 2 => m + n  cách
	- nhân: cả nhiệm vụ 1 và nhiệm vụ 2 => mn cách


VD: nếu mật khẩu gồm 6 hoặc 8 chữ hoặc số (phân biệt chữ hoa thường). có bao nhiêu mk có thể có?
=> $62^6 +62^8$ 


VD (**dạng thi mật khẩu**): Có bao nhiêu mk độ dài 6 -> 8 gồm chữ thường, chữ hoa, chữ số và chữ cái đầu viết hoa
=> $26.(62^5+62^6+62^8)$
=> **trình bày**:
	Số cách chọn của mỗi kí tự là: 26+26+10=62 (cách)
	TH1: MK độ dài là 6
		Số cách tạo mk thỏa mãn đề bài là: 26.62^5 
	TH2
	TH3
	Số MK thỏa mãn đề bài là: $26.(62^5+62^6+62^8)$ 
	(không cần ghi đáp án cụ thể)
	
## Tổ hợp lặp
- Phần tử khác nhau : n
- Chọn k phần tử 

Định nghĩa: Tổ hợp lặp chập k của n là 1 cách lấy đồng thời k phần tử từ tập có n loại phần tử khác nhau, trong đó mỗi loại có $>=k$ phần tử

Mỗi cách chọn r phần tử cho phép chọn lặp từ n loại phần tử khác nhau đgl 1 tổ hợp lặp chập r từ n phần tử

Định lý: Số tổ hợp lặp chập r từ 1 tập có n phần tử là $C(n+r-1, r)$

Tổ hợp lặp chập r từ $n-1+r$ phần tử
=> $C(n+r-1, r) = \frac{(n+r-1)!}{r!(n-1)!}$

#### Dạng sắp xếp vào hộp

#### Dạng phương trình và bất phương trình
Dạng bất phương trình : đặt biến -> chuyển về dạng phương trình
	- >=
	- <  => bù - >=
	- > x => >= x + 1

```
VD: Phương trình dưới đây có bao nhiêu lời giải  x1 + x2 + x3 = 11  
trong đó x1, x2, x3 là các số nguyên không âm?

Giải
C1
Một lời giải <=> một cách chọn 11 phần tử từ tập {a, b, c} sao cho:
	có x1 lần lấy phần tử a
	có x2 lần lấy phần tử b
	có x3 lần lấy phần tử c
=> Số lời giải <=> số tổ hợp lặp chập 11 từ một tập có ba phần tử 
	C(3+11-1, 11) = C(13,11)

C2
Mỗi nghiệm là 1 cách chọn 11 phần tử từ 3 loại phần tử
Mỗi nghiệm ứng với 1 tổ hợp lặp chập 11 từ 3 phần tử
Số nghiệm là C(11+3-1, 11) = C(13,11)
```


```
25. Phương trình x1 + x2 + x3 + x4 + x5 + x6 = 20
a, có bao nhiêu nghiệm nguyên không âm với x2 ≥ 5 ?
b, có bao nhiêu nghiệm nguyên không âm với x2 < 3 ?

Ý tưởng
- dùng tổ hợp lặp
- b. x2 < 3  <=>bù - x2 >= 3

Giải
a. 
Đặt x2 = x2' + 5 (x2' >= 0)
Ta có: x1 + (x2' + 5) + x3 + x4 + x5 + x6 = 20
	<=> x1 + x2' + x3 + x4 + x5 + x6 = 15
Áp dụng tổ hợp lặp: C(15 + 6 - 1, 15) = C(20, 15)

b. 
Xét nghiệm nguyên không âm với x2 >= 3
Đặt x2 = x2' + 3
Ta có : x1 + x2' + 3 + x3 + x4 + x5 + x6 = 20
	<=> x1 + x2' + x3 + x4 + x5 + x6 = 17
Áp dụng tổ hợp lặp: C(17+6-1, 17) = C(22,17)
Tổng số cách chọn không điều kiện là C(20+6-1, 20) = C(25,20)
Vậy số nghiệm nguyên không âm x2 < 3 là C(25,20) - C(22,17)


```

```
26. Bất phương trình x1 + x2 + x3 ≤ 15 (1)
có bao nhiêu nghiệm nguyên không âm?

Giải
Đặt x4 = 15 - (x1 + x2 + x3)  (2)
Từ (1)(2), ta có pt: x1 + x2 + x3 + x4 = 15
Áp dụng tổ hợp lặp: C(15+4-1, 15) = C(18,15)

```

```
27. Bất phương trình x + y + z ≤ 14     (1)
có bao nhiêu nghiệm nguyên không âm? biết x > 5 

Ý tưởng
- x > 5 => x >= 6

Giải
Đặt t = 14 - (x + y + z)   (2)
Từ (1)(2), ta có pt: x + y + z + t = 14
Đặt x' = x - 6
=> pt: x' + 6 + y + z + t = 14
	   x' + y + z + t     = 8
=> C(8 + 4 - 1, 8) = C(11,8)

```

```
VD: Phương trình dưới đây có bao nhiêu lời giải: x1 + x2 + x3 = 11
trong đó x1, x2, x3 là các số nguyên thỏa x1 ≥ 1, x2 ≥ 2, x3 ≥ 3?

Giải
Ta có: 1 cách chọn phần tử a, 2 cách chọn phần tử b, 3 cách chọn phần tử c và 5 lần chọn phần tử tùy ý
=> Số cách chọn 5 phần tử tùy ý là ; C(5+3-1, 5) = C(7,5)
```


## Chỉnh hợp lặp
Định lý: Số chỉnh hợp chập r của 1 tập có n phần tử khi việc lặp cho phép là $n^r$ 

Chỉnh hợp lặp chập k của n là 1 cách lấy có thứ tự **k phần tử** từ tập có **n loại phần tử khác nhau**, trong đó mỗi loại có >= k phần tử
$A(n, k) = N^k$ 

Tự đặt câu hỏi
- Có thứ tự không?
- Có đc lặp không?

Thường có trong bài mật khẩu

Ví dụ
```
VD1: Có bao nhiêu chuỗi có độ dài r có thể được hình thành từ những chữ cái hoa trong bảng chữ cái tiếng Anh?

Giải:
Theo nguyên lý nhân, có 26 chữ cái hoa trong bảng chữ cái  tiếng Anh, và bởi mỗi chữ cái có thể được sử dụng lại
=> có 26^r chuỗi có độ dài r tạo từ các chữ cái hoa tiếng Anh.
```

```
VD2:Nếu mật khẩu gồm 8 chữ hoặc số (không phân biệt chữ hoa và chữ thường). Hỏi có bao nhiêu mật khẩu có thể có?  

Giải
Ta có 26 chữ cái và 10 chữ số, tổng cộng 36 ký tự.  
Mỗi ký tự thứ i có 36 khả năng lựa chọn (chỉnh hợp lặp chập 8 từ 36) 
Số mật khẩu chính là sô chỉnh hợp lặp 36*8
```

```
VD3: Có bao nhiêu chuỗi có độ dài r có thể được hình thành từ những chữ cái hoa trong bảng chữ cái tiếng Anh?  

Giải
Mỗi chữ cái: có 26 lựa chọn.  
=> có 26^r chuỗi có độ dài r
```

## Hoán vị lặp

Hoán vị trong đó có các phần tử như nhau gọi là hoán vị có lặp  

Công thức:  $C^{n_1}_n.C^{n_2}_{n-n_1}...C^{n_k}_{n_k} = \frac{n!}{n_1!n_2!...n_k!}$ 

```
VD1: Có bao nhiêu xâu khác nhau có thể lập từ tất cả các ký tự trong
từ: MISSISSIPPI

Giải
M = 1 => C(11,1) 
I = 4 => C(10,4)
S = 4 => C(6,4)
P = 2 => C(2,2)
=> nhân lại với nhau = ...
```

`Note` : $C^4_{10}$  = C(10,4)

```
VD2: phân bố đồ vật vào hộp
Có bao nhiêu cách chia một cỗ bài chuẩn 52 quân cho 4 người chơi, mỗi người một xấp 5 quân. (thứ tự các quân bài không quan trọng)

Giải
Số cách chia cho:
Người 1 : C(52, 5)
Người 2 : C(47, 5)
Người 3 : C(42, 5)
Người 4 : C(37, 5)
=> Tổng cách chia: C(52, 5).C(47, 5).C(42, 5).C(37, 5)
```

```
VD3: Có bao nhiêu chuỗi khác nhau có thể được tạo ra khi sắp xếp lại các chữ cái của từ SUCCESS

Giải
Ta có độ dài xâu là 7
Số cách lựa chọn vị trí cho:
S = 3 => C(7,3)
U = 1 => C(4,1)
C = 2 => C(3,2)
E = 1 => C(1,1)
=> Số chuỗi thỏa mãn đề bài: C(7,3).C(4,1).C(3,2).C(1,1)
```

## Nguyên lý bao - loại trừ (Inclusion-Exclusion Principle)

**Nguyên lý**:  Nếu một công việc có thể được thực hiện bằng một trong hai phương án, phương án một có $n_1$ cách thực hiện và phương án hai có $n_2$ cách thực hiện => số  cách thực hiện công việc là $n_1 + n_2$ trừ đi số cách thực hiện chung cho hai phương án.

**Biểu diễn dưới dạng tập:** 
Giả sử A và B là các tập
Có $|A|$ cách chọn một phần tử từ tập A
Có $|B|$ cách chọn một phần tử từ tập B
=> Số cách chọn một phần tử từ tập A hoặc B: $|A \cup B| = |A| + |B| - |A \cap B|$


```
VD(dạng thi bit): Có bao nhiêu xâu tam phân độ dài 12 bit hoặc 2 bit đầu là 01 hoặc 3 bit cuối là 020

Gợi ý:
	tam phân: 0,1,2
	tứ phân: 0,1,2,3 
	=> n phân: 0,1,.., n-1
	
Giải
TH1: số xâu tam phân có độ dài là 12 và 2 bit đầu là 01 là: 3^10
TH2: số xâu tam phân có độ dài là 12 và 3 bit cuối là 020 là: 3^9
TH3: số xâu tam phân có độ dài là 12 và 2 bit đầu là 01 và 3 bit cuối là 020 là: 3^7
Theo nguyên lý bao loại trừ, số xâu thỏa mãn đề bài là: 3^10 + 3^9 - 3^7
```


```
VD2: Một số qui tắc giả thiết của mật khẩu:  
- Mật khẩu dài 2 ký tự.  
- Mỗi ký tự là một chữ từ a-z, hoặc là một số 0-9, hoặc là 1 trong 10 ký tự phân cách sau !@#$%^&*().  
- Mỗi mật khẩu chứa ít nhất 1 số hoặc 1 ký tự phân cách.

Giải
Mật khẩu hợp lệ có chữ số hoặc ký tự ngăn cách ở vị trí 1 hoặc 2.  
TH1: mật khẩu với ký hiệu OK ở vị trí 1)= (10+10)-(10+10+26)  
TH2: mật khẩu với ký hiệu OK ở vị trí #2): also 20.46  
TH3: mật khẩu với cả hai ký hiệu OK ở 2 vị trí): 20-20  
Theo nguyên lý bao loại trừ: 920+920–400 = 1440
```

```
VD3: Có bao nhiêu chuỗi bit có độ dài 8 hoặc bắt đầu bằng chữ số 1 hoặc kết thúc bằng 00?

Giải
TH1: Số chuỗi bit có độ dài 8 bắt đầu bằng chữ số 1 là 2^7
TH2: Số chuỗi bit có độ dài 8 kết thúc bằng 00 là 2^6
TH3: Số chuỗi bit có độ dài 8 bắt đầu bằng chữ số 1 và kết thúc bằng 00 là 2^5 
Theo nguyên lý bao loại trừ, số chuỗi bit thỏa mãn đề bài: 2^7 + 2^6 - 2^5
```

```
VD4: Một công ty máy tính nhận 350 đơn xin việc từ các ứng viên cho một công việc lên kế hoạch cho một web server mới. Giả sử rằng có 220 ứng viên ngành khoa học máy tính, 147 ngành kinh doanh và 51 ứng viên có cả ngành khoa học máy tính và kinh doanh. Có bao nhiêu ứng viên không có ngành khoa học máy tính hoặc không có ngành kinh doanh?

Giải: 
Theo nguyên lý bao loại trừ, số ứng viên ngành khoa học máy tính hoặc kinh doanh là: 220 + 147 - 51 = 316
=> Số ứng viên không có ngành khoa học máy tính hoặc không có ngành kinh doanh là: 350 - 316 = 34
```

## Nguyên lý Dirichlet
Hay còn là nguyên lý chim bồ câu

**Định lý Dirichlet**: Giả sử k là một số nguyên dương, nếu cho k + 1 (nhiều hơn) đồ vật được đặt vào  trong k hộp, thì có ít nhất một hộp chứa hai đồ vật.

**Nguyên lý Dirichle tổng quát** :  Nếu N đồ vật được đặt vào k hộp, thì có ít nhất một hộp chứa ít nhất $\lceil N / k \rceil$  đồ vật.

**Bài tập**
1. Dạng bài xuôi
	```
	VD Có N = 280 sinh viên trong lớp này. Trong đó có k=52 tuần trong năm.  
	Như vậy, có ít nhất một tuần mà trong tuần đó có ít nhất [280/52|[5.38] = 6 sinh viên có cùng ngày sinh nhật.
	```

	```
	VD2: Trong 100 người tùy ý, có thể khẳng định có bao nhiêu người cùng tháng sinh nhật ? 
	Giải
	Trong 100 người có ít nhất [100/12] = [8.33] = 9 người có cùng tháng sinh
	```

2. Dạng bài ngược
	- N ít nhất = k.(x-1) + 1
	```
	VD : Cần ít nhất bao nhiêu sv cùng quê để đảm bảo 8 bạn cùng quê, biết có 63 tỉnh
	=> N = 63.7 + 1
	```

	```
	VD2: Cần tối thiểu bao nhiêu sinh viên trong lớp học để đảm bảo rằng có ít nhất sáu sinh viên nhận cùng kết quả đánh giá, nếu có năm điểm chữ dùng để đánh giá A, B, C, D và F?
	
	Giải
	Số sinh viên tối thiểu cần để đảm bảo rằng có ít nhất sáu sinh viên nhận cùng điểm đánh giá là số nguyên nhỏ nhất N sao cho [N/5] = 6.
	=> N = (6-1).5 + 1 = 26
	```

## Hệ thức truy hồi - Recurrence Relations

```
VD: Có bao nhiêu xâu nhị phân độ dài 10 mà không chứa 2 số 1 kề nhau  
Giải
Gọi  là xâu nhị phân độ dài n thỏa mãn đề bài  
TH1: Xâu kết thúc = 0 an-1  
TH2: Xâu kt = 1  
TH2.1: 11 => k xét  
TH2.2: 01 => an-2  
(nếu tam phân: TH3: xâu kt = 2)  
=> an = an-1 + an-2 (n>=2)  
a10=?  
a0 = 1 (xâu rỗng)  
a1 = 2 (0, 1)  
a2 = 3 (00, 01, 10)  
a3 = a2 + a1 = 3 + 2 = 5  
...  
a10
```

## Bài tập
Các bài ôn thi : 5, 7, 8, 14, 15, 20, 25, 26, 27, 31, 36, 37, 38, 40, 41, 42
```
5. Có bao nhiêu xâu gồm 3 chữ số thập phân mà:
a, Không chứa cùng một chữ số đúng ba lần
b, Bắt đầu bằng một chữ số lẻ.
c, Có đúng hai chữ số 5

Giải
a. 
	Tổng số xâu gồm 3 chữ số thập phân là: 10^3
	Số xâu có cùng 1 chữ số thập phân là: 10
	=> Số xâu không chứa cùng 1 chữ số đúng 3 lần là: 10^3 - 10
b.
	Chữ số đầu tiên có 5 cách chọn: 1,3,5,7,9
	Chữ số thứ 2 và 3 có 10^2 cách chọn
	=> Xâu bit bắt đầu bằng 1 chữ số lẻ là: 5.10^2
c.
	Số cách chọn 2 vị trí trong 3 vị trí để điền số 5 là C(3,2)
	
```

```
7. 
a. Có bao nhiêu hàm số từ tập có 6 phần tử vào tập có 5 phần tử?
b. Có bao nhiêu hàm số đơn ánh từ tập có 5 phần tử đến tập có 6 phần tử?
c. Có bao nhiêu hàm số đơn ánh từ tập có 6 phần tử đến tập có 5 phần tử?

Note:
Từ tập m->n, nếu m > n -> không có hàm đơn ánh

Giải
a. 
	Mỗi phần tử trong A có 5 lựa chọn để ánh xạ
	=> Số hàm đơn ánh thỏa mãn là: 5^6
b.
	Số cách chọn phần tử thứ 1 có 6 cách
	Số cách chọn phần tử thứ 2 có 5 cách
	Số cách chọn phần tử thứ 3 có 4 cách
	Số cách chọn phần tử thứ 4 có 3 cách
	Số cách chọn phần tử thứ 5 có 2 cách
	=> Tổng số cách chọn: 6.5.4.3.2 cách
c.
	Vì 6 > 5 => không tồn tại hàm đơn ánh từ tập 6 phần tử -> tập 5 phần tử
```

```
8. Có bao nhiêu xâu nhị phân có độ dài bằng 10 hoặc bắt đầu bằng 3 số 0, hoặc kết thúc bằng hai số 1?

Giải
```

```
14. Một ngăn tủ có 10 quả bóng màu đen, 10 quả bóng màu trắng và 10 quả bóng màu đỏ. Một người lấy các quả bóng một cách ngẫu nhiên trong bóng tối. Hỏi người đó phải lấy ít nhất bao nhiêu quả bóng để đảm bảo có ít nhất 4 quả cùng mầu?
```
```
15. Cho tập A= {1,2,3,…, 12}, hỏi cần phải chọn ít nhất bao nhiêu số từ tập A để đảm bảo có ít nhất 1 cặp có tổng bằng 13?
```

```
20. Có bao nhiêu cách chia 3 quyển sách cho 5 người, nếu:
a, 3 quyển sách giống hệt nhau?
b, 3 quyển sách khác nhau?

Note
Xác định dùng tổ hợp lặp, chỉnh hợp lặp:
- Chia sách có quan trọng thứ tự không?
- Có được lặp không?

Giải
a. Áp dụng công thức tổ hợp lặp với n = 5, k = 3:
=> C(5+3-1, 3) = C(7,3)

b. Áp dụng chỉnh hợp lặp, số cách chia 3 quyển khác nhau là: 5^3
```

```
31. Có thể tạo được bao nhiêu xâu tam phân khác nhau nếu dùng 3 chữ số 2, 5 chữ số 1 và 9 chữ số 0?
```

```
36. Hãy giải hệ thức truy hồi an = 8an-1 – 16an-2 ; với a0 = 2, a1= 5
```

```
37.
```

```
38. Tìm hệ thức truy hồi cho số các xâu nhị phân độ dài n chứa 3 số 0 liên tiếp
- Tìm điều kiện đầu?
- Có bao nhiêu xâu nhị phân độ dài 5 chứa 3 số 0 liên tiếp?

Note
- hệ thức truy hồi là 1 pt biểu diễn sự tương quan để có thể biểu diễn phần tử an thông qua các phần tử trước nó
- đầu tiên tạo dãy số => lời giải nằm trong dãy số
- ví dụ bài này: tạo 1 dãy số mà trong dãy số có 1 phần tử là lời giải
- điều kiện đầu là những phần tử đầu trong dãy
- xâu rỗng: xâu không chứa phần tử nào = xâu có độ dài = 0
  tập rỗng: tập không chứa phần tử nào = tập có lực lượng = 0 
- Xác định các giá trị đầu của dãy a: 
	- a_0 là số xâu nhị phân độ dài 0 chứa 3 số 0 liên tiếp => a_0 = 0
	- a_1 là số xâu nhị phân độ dài 1 chứa 3 số 0 liên tiếp => a_1 = 0
	- a_2 là số xâu nhị phân độ dài 2 chứa 3 số 0 liên tiếp => a_2 = 0
	- a_3 là số xâu nhị phân độ dài 3 chứa 3 số 0 liên tiếp => a_3 = 1 (000)
	- a_3 là số xâu nhị phân độ dài 4 chứa 3 số 0 liên tiếp => a_4 = 3 (1000, 0001, 0000)
- Phân trường hợp xâu xuất hiện số 0 và không xuất hiện số 0 cư xử khác nhau
- Xâu tam phân hoặc tứ phân, thì có 2 TH: a KT bởi 0 họăc KT bởi số khác 0

Giải
Gọi a_n là số xâu nhị phân độ dài n chứa 3 số 0 liên tiếp
=> Dãy số (a)_n = (a_0, a_1, ... ,a_n)
=> Số xâu nhị phân độ dài 5 chứa 3 số 0 liên tiếp là a_5
Xâu nhị phân độ dài n thỏa mãn đề bài thuộc 1 trong 2 trường hợp
- Xâu kết thúc bởi số 0 có 2 TH = A
	- Xâu kết thúc bởi 00 có 2 TH
		- Xâu kết thúc bởi 000 
		- Xâu kết thúc bởi 100
	- Xâu kết thúc bởi 10
- Xâu kết thúc bởi số 1 = B
=> a_n = số A + số B

- Xác định các giá trị đầu của dãy a: a_0 = 0, a_1 = 0, a_2 = 0, a_3 = 1, a_4 = 3



```

```
40. Tìm hệ thức truy hồi tính số xâu tam phân độ dài n và có một số chẵn bit 0.

Giải
Gọi a_n là số các xâu có độ dài n thỏa mãn chẵn bit 0
	a_n-1 là số các xâu có độ dài n-1 bit thỏa mãn lẻ bit 0
TH1: Xâu có độ dài n-1 bit có số bit 0 chẵn và thêm 1 bit khác 0
	=> có 2.a_n-1 xâu
TH2: Xâu có độ dài n-1 bit có số bit 0 lẻ và số xâu n-1 = số xâu n - 1 lẻ 
	=> 3^n-1 - a_n-1
```

```
41. Một máy bán tem tự động chỉ nhận các đồng xu 1$ và tờ tiền 1$ và tờ tiền 5$.
a, Hãy tìm hệ thức truy hồi tính số cách đặt n$ vào trong máy bán hàng, biết thứ tự các đồng xu và các
tờ tiền là quan trọng.
b, Tìm các điều kiện đầu.
c, có bao nhiêu cách đặt 10$ vào máy để mua một bộ tem?
```
```
42. Có bao nhiêu số tự nhiên có 3 chữ số hoặc chia hết cho 5 hoặc là số chẵn?

Giải
Ta có: số tự nhiên có 3 chữ số từ 100 -> 999 là 900 số
TH1: Số tự nhiên có 3 chữ số chia hết cho 5
- Số cuối có 2 cách chọn 0 hoặc 5
- Số đầu tiên có 9 cách chọn
- Số thứ 2 có 10 cách chọn
=> tổng số cách chọn: 10.9.2 = 180 

TH2: Số tự nhiên có 3 chữ số là số chẵn
- Số đầu tiên có 9 cách chọn từ 1 -> 9
- Số thứ 2 có 10 cách chọn từ 0 -> 9
- Số cuối có 5 cách chọn 0, 2, 4, 6, 8
=> tổng số cách chọn: 9.10.5 = 450

TH3: Số tự nhiên có 3 chữ số chia hết cho 5 và là số chẵn
- Số đầu tiên có 9 cách chọn từ 1 -> 9
- Số thứ 2 có 10 cách chọn từ 0 -> 9
- Số cuối có 1 cách chọn là số 0
=> tổng số cách chọn: 9.10.1 = 90

Theo nguyên lý bao loại trừ, số số thỏa mãn yêu cầu đề bài: 
	180 + 450 - 90 = 540
```

## Đề thi - câu 2
```
1. Một ngăn tủ có 50 bút bi đen, 20 bút bi xanh và 30 bút bi đỏ. Một người lấy những chiếc bút  một cách ngẫu nhiên trong bóng tối. Hỏi người đó phải lấy ít nhất bao nhiêu chiếc bút để đảm bảo có ít nhất 12 chiếc bút cùng mầu?

Gợi ý:  hỏi ít nhất bao nhiêu => dirichle

Giải
Gọi x là số bút bi ít nhất phải lấy để có ít nhất 12 chiếc bút cùng màu. 
Theo nguyên lý Dirichlet:  ⌈x / 3⌉ = 12  
=>  x = (12 - 1) × 3 + 1 = 34 (bút)
```

```
2. Có thể xây dựng được bao nhiêu hàm f từ tập A đến tập B biết
a. |A| = 6, |B| = 9
b. f là hàm đơn ánh và |A| = 9, |B| = 12
```

```
3.
a. Có bao nhiêu số tự nhiên có 3 chữ số mà hoặc chia hết cho 5 hoặc là số chẵn?
b. Cho tập A={x,y,z,t}, A có bao nhiêu tổ hợp lặp chập 7? Lấy ví dụ 5 tổ hợp lặp chập 7 của A.
```

```
4. Có bao nhiều cách chia 10 cái máy tính xách tay cho 3 phòng thí nghiệm, biết  
a.10 máy tính đó giống hệt nha  
b.10 máy tính đó khác nhau

Giải
```

```
5. Tìm hệ thức truy hồi và điều kiện đầu tính số xâu tử phân độ dài n không chứa số 1 liền kề  nhau. Có bao nhiêu xâu như vậy độ dài 8?

Giải
Gọi an là xâu tứ phân độ dài n không chứa số 1 liền kề nhau
TH1: Xâu kết thúc bởi số 1
TH2:
```



```
6. Tìm hệ thức truy hồi và điều kiện đầu tính số xấu thập phân độ dải n chứa số chẵn lần chữ số 2. Có bao nhiêu xâu như vậy độ dài 8?

Giải
Gọi an là số các xâu thập phân độ dài n chứa chẵn số 2
	an-1 là số các xâu thập phân độ dài n chứalẻ số 2
TH1: Xâu có độ dài n-1 bit chứa chẵn số 2 và thêm 1 bit khác 2
=> có 9.an-1
TH2: xâu có độ dài n-1 bit chứa lẻ số 2 với 1 bit bằng 2
=> có 10^n-1 - an-1
=> an = 9.an-1 + 10^n-1 - an-1 = 10^n-1 + 8an-1
Vậy HTTH : an =  10^n-1 + 8an-1 (n >= 1)
Điều kiện đầu: a0 = 0, a1 = 0, a2 = 1
a3 = ...
a4 = ...


```

```
7.
a. Có bao nhiêu xâu tam phân độ dài 15 hoặc có 2 phần tử đều là 1 hoặc có 3 phần tử cuối đều là 0
b. Có bao nhiêu hàm đơn ánh từ tập có 6 phần tử đến 5 phần tử? Vì sao?
```


