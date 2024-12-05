## 1. Sum and Product Rules
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
	
## Inclusion-Exclusion Principle
Nguyên lý bao - loại trừ

Giả sử có $k <= m$ cách thực hiện nhiệm vụ 1 đồng thời với việc thực hiện nhiệm vụ 2 (tức những cách giống nhau)

Khi đó, số cách hoàn thành "Thực hiện nhiệm vụ 1 hoặc nhiệm vụ 2" là `m+n-k`

Lý thuyết tập hợp: Nếu A và B
- không rời nhau => $|A \cup B| = |A| + |B| - |A \cap B|$
- rời nhau => $|A| + |B|$

VD(**dạng thi bit**): Có bao nhiêu xâu tam phân độ dài 12 bit hoặc 2 bit đầu là 01 hoặc 3 bit cuối là 020
=> 
	tam phân: 0,1,2
	tứ phân: 0,1,2,3 
	=> n phân: 0,1,.., n-1
=> trình bày
	TH1: số xâu tam phân có độ dài là 12 và 2 bit đầu là 01 là: $3^{10}$ 
	TH2: số xâu tam phân có độ dài là 12 và 3 bit cuối là 020 là: $3^9$ 
	TH3: số xâu tam phân có độ dài là 12 và 2 bit đầu là 01 và 3 bit cuối là 020 là: $3^7$
	Theo nguyên lý bao loại trừ, số xâu thỏa mãn đề bài là: $3^{10} + 3^9 - 3^7$ 

