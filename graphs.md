## Chu trình Euler
- Chu trình Euler: chu trình đơn đi qua tất cả các cạnh của đồ thị G đúng một lần
- Đường đi Euler: đường đi đơn đi qua tất cả các cạnh của đồ thị G đúng một lần
- **Điều kiện cần và đủ:**
	- Định lý 1: Một đa đồ thị liên thông có **chu trình** Euler khi và chỉ khi mỗi **đỉnh của nó đều có bậc chẵn**.
	- Định lý 2: Một đa đồ thị liên thông có **đường đi** Euler nhưng không có chu trình Euler khi và chỉ khi nó có đúng **hai đỉnh bậc lẻ.**
- Ví dụ: ![](https://github.com/thou05/discrete-mathematics/blob/main/img/vdeuler.png)

- Trình bày tìm đường đi và chu trình Euler
	- KĐ là chu trình không ? 
	- Giải thích
- BT: ![](https://github.com/thou05/discrete-mathematics/blob/main/img/bai4euler.png)
	```
	Giải:
	G1: 
	- Có chu trình euler vì tất cả các đỉnh đều bậc chẵn: a, e, c, d, e, b, a
	- Không có đường đi euler vì không có 2 đỉnh bậc lẻ
	G2:
	- Không có chu trình euler vì các đỉnh a, b, c, d bậc lẻ
	- Không có đường đi euler vì có 4 đỉnh bậc lẻ
	G3:
	- Không có chu trình euler vì có 2 đỉnh bậc lẻ
	- Có đường đi euler vì có 2 đỉnh bậc lẻ : a, c, d, e, b, d, a, b
	```
- Ví dụ đề thi
	![](https://github.com/thou05/discrete-mathematics/blob/main/img/dethitrrcau4.png)
	```
	Giải
	a. 
	- Đồ thị G có đường đi Euler vì có 2 đỉnh h, e bậc lẻ
	- Đường đi: e d g e b a c b h c d h g a h
	(còn nhiều đường khác, nên bắt đầu từ đỉnh lẻ)
	
   ```
## Tìm đường ngắn nhất Dijkstra
- Bài toán: Tìm đường đi ngắn nhất từ đỉnh a đến z của đồ thị có trọng số liên thông G = (V,E)
- Gọi L(v) là độ dài đường đi ngắn nhất từ đỉnh a đến đỉnh v
- S là tập các đỉnh đã tìm được đường đi ngắn nhất từ a đến nó
- Ý tưởng:
  - B1: L(a) = 0, S = $\varnothing$, $\forall v \in V$, $v \neq a$ : L(v) = $\infty$
  - B2: Nếu $z \in S$ thì kết thúc
  - B3: Chọn $v \notin S$ sao cho L(v) là nhỏ nhất. Đưa v vào S
  - B4: Với mỗi đỉnh x liền kề v thì $x \notin S$ thì đặt: `L(x) = min{L(x), L(v) + w(v,x)}`. Quay lại bước 2

## Tìm cây khung nhỏ nhất
- Tổng trọng số trên cách cạnh của nó nhỏ nhất 
- Chú ý trình bày:
	- Kẻ bảng
	- Tổng trọng số
	- Vẽ cây khung
#### Thuật toán Prim

Đồ thị G = (V,E) liên thông, có n đỉnh.
- Bước 1: Chọn một cạnh bất kỳ có trọng số nhỏ nhất, đặt nó vào cây khung.
- Bước 2: Lần lượt ghép vào cây các cạnh có trọng số nhỏ nhất **liên thuộc** với **một đỉnh của cây và không tạo ra chu trình** trong cây.
- Bước 3: Thuật toán dừng lại khi (n-1) cạnh được ghép vào cây. (tức ghép đc tất cả các đỉnh)

---
Prim ghép vào cây có trongj số nhỏ nhất liên thuộc với cây khung đang có

![](https://github.com/thou05/discrete-mathematics/blob/main/img/vdPrim.png)

#### Thuật toán Kruskal
Đồ thị G = (V,E) liên thông, có n đỉnh.
➢ Bước 1: Chọn một cạnh bất kỳ có trọng số nhỏ nhất, đặt nó vào cây khung.
➢ Bước 2: Lần lượt ghép vào cây các cạnh có trọng số nhỏ nhất mà không tạo ra chu trình trong cây.
➢ Bước 3: Thuật toán dừng lại khi (n-1) cạnh được ghép vào cây.

![](https://github.com/thou05/discrete-mathematics/blob/main/img/vdKruskal.png)


---
## Tìm theo chiều sâu
![](https://github.com/thou05/discrete-mathematics/blob/main/img/timchieusau.png)

## Tìm theo chiều rộng
![](https://github.com/thou05/discrete-mathematics/blob/main/img/timchieurong.png)


## Đề thi mẫu - câu 4

1. Cho đồ thị vô hướng có trọng số G sau biết thứ tự lựa chọn các đỉnh ưu tiên theo thứ tự trong bảng chữ cái. Hãy trình bày thuật toán Dijkstra dưới dạng bảng để tìm đường đi ngắn nhất  từ đỉnh g đến định b và cho biết độ dài của đường đi đó.

	![](https://github.com/thou05/discrete-mathematics/blob/main/img/dothidethi1.png)
	
Giải

|  k  |       a       |       b       |       c       |       d       |       e       |   g    |       h       |
| :-: | :-----------: | :-----------: | :-----------: | :-----------: | :-----------: | :----: | :-----------: |
|  1  | $(\infty, g)$ | $(\infty, g)$ | $(\infty, g)$ | $(\infty, g)$ | $(\infty, g)$ | (0,g)* | $(\infty, g)$ |
|  2  |     (2,g)     | $(\infty, g)$ | $(\infty, g)$ |    (1,g)*     |     (2,g)     |   __   |     (7,g)     |
|  3  |    (2,g)*     | $(\infty, g)$ |     (3,d)     |      __       |     (2,g)     |   __   |     (5,d)     |
|  4  |      __       |     (4,a)     |    (3,d)*     |      __       |      __       |   __   |     (3,a)     |
|  5  |      __       |     (4,a)     |      __       |      __       |      __       |   __   |    (3,a)*     |
|  6  |      __       |    (4,a)*     |      __       |      __       |      __       |   __   |      __       |

Đường đi ngắn nhất: g -> a -> b \\
Độ dài = 6


2. Cho đồ thị vô hướng có trọng số G sau:  
	a. Đồ thị G có đường đi Euler không, vì sao? Nếu có, hãy tìm 1 đường đi Euler của  G.  
	b. Hãy trình bày thuật toán Kruskal để tìm cây khung nhỏ nhất của G, biết thứ tự  lựa chọn các đỉnh ưu tiên theo thứ tự trong bảng chữ cái (chú ý: thể hiện được ý tưởng của  thuật toán).
	
	![](https://github.com/thou05/discrete-mathematics/blob/main/img/dothidethi2.png)
	
```
Giải
a. 
-  Đồ thị G có đường đi Euler vì có 2 đỉnh h, e bậc lẻ
- Đường đi: e d g e b a c b h c d h g a h

b.

| Bước chọn | Cạnh | Trọng số |	
|     1     |  ah  |    1     |
|     2     |  bc  |    1     |
|     3     |  ch  |    1     |
|     4     |  dg  |    1     |
|     5     |  ag  |    2     |
|     6     |  ge  |    2     |

Tổng trọng số là 8

Cây: 
	    a
	  /   \
	 h     g
	/     / \ 
       c     d   e
      / 
     b  

hoặc biểu diễn vẽ theo các cạnh

```

3. Cho đồ thị vô hướng có trọng số G sau. Hãy trình bảy thuật toán Prim dưới dạng bảng đế  tìm cây khung nhỏ nhất của G, biết thứ tự lựa chọn các đỉnh ưu tiên theo thứ tự trong bảng chữ cái. 

![](https://github.com/thou05/discrete-mathematics/blob/main/img/dothidethi3.png)

```
Note:
- có 7 đỉnh -> cần tìm 6 cạnh
```
	
Giải
	

	| Bước chọn | Cạnh | Trọng số |
	| :-------: | :--: | :------: |
	|     1     |  ah  |    1     |
	|     2     |  hc  |    1     |
	|     3     |  bc  |    1     |
	|     4     |  ag  |    2     |
	|     5     |  gd  |    1     |
	|     6     |  ge  |    2     |
	
	Tổng trọng số là 8
```
Cây: 
	    a
	  /   \
	 h     g
	/     / \ 
       c     d   e
      / 
     b  
		
```

4. Cho đồ thị vô hướng có trọng số G sau biết thứ tự lựa chọn các đỉnh ưu tiên theo thứ tự trong bảng chữ cái. Hãy trình bày thuật toán Dijkstra dưới dạng bảng để tìm đường đi ngắn nhất  từ đỉnh h đến đỉnh e và cho biết độ dài của đường đi đó.

	![](https://github.com/thou05/discrete-mathematics/blob/main/img/dothidethi1.png)
Giải

|  k  |       a       |       b       |       c       |       d       |       e       |       g       |    h    |
| :-: | :-----------: | :-----------: | :-----------: | :-----------: | :-----------: | :-----------: | :-----: |
|  1  | $(\infty, h)$ | $(\infty, h)$ | $(\infty, h)$ | $(\infty, h)$ | $(\infty, h)$ | $(\infty, h)$ | (0, h)* |
|  2  |    (1,h)*     |     (6,h)     |     (1,h)     |     (4,h)     | $(\infty, h)$ |     (7,h)     |   __    |
|  3  |      __       |     (3,a)     |    (1,h)*     |     (4,h)     | $(\infty, h)$ |     (3,a)     |   __    |
|  4  |      __       |    (2,c)*     |      __       |     (4,h)     | $(\infty, h)$ |     (3,a)     |   __    |
|  5  |      __       |      __       |      __       |     (4,h)     |     (9,b)     |    (3,a)*     |   __    |
|  6  |      __       |      __       |      __       |    (4,h)*     |     (5,g)     |      __       |   __    |
|  7  |      __       |      __       |      __       |      __       |    (5,g)*     |      __       |   __    |

Đường đi ngắn nhất: h -> a -> g -> e

Độ dài = 5

5. Cho đồ thị vô hướng có trọng số G sau biết thứ tự lựa chọn các đỉnh ưu tiên theo thứ tự trong bảng chữ cái. Hãy trình bày thuật toán Dijkstra dưới dạng bảng để tìm đường đi ngắn nhất  từ đỉnh c đến đỉnh e và cho biết độ dài của đường đi đó.

	![](https://github.com/thou05/discrete-mathematics/blob/main/img/dothidethi1.png)
Giải

|  k  |       a       |       b       |   c    |       d       |       e       |       g       |       h       |
| :-: | :-----------: | :-----------: | :----: | :-----------: | :-----------: | :-----------: | :-----------: |
|  1  | $(\infty, c)$ | $(\infty, c)$ | (0,c)* | $(\infty, c)$ | $(\infty, c)$ | $(\infty, c)$ | $(\infty, c)$ |
|  2  | $(\infty, c)$ |    (1,c)*     |   __   |     (3,c)     | $(\infty, c)$ | $(\infty, c)$ |     (1,c)     |
|  3  |     (3,b)     |      __       |   __   |     (3,c)     |     (8,b)     | $(\infty, c)$ |    (1,c)*     |
|  4  |    (2,h)*     |      __       |   __   |     (3,c)     |     (8,b)     |     (8,h)     |      __       |
|  5  |      __       |      __       |   __   |    (3,c)*     |     (8,b)     |     (4,a)     |      __       |
|  6  |      __       |      __       |   __   |      __       |     (8,b)     |    (4,a)*     |      __       |
|  7  |      __       |      __       |   __   |      __       |    (6,e)*     |      __       |      __       |

Đường đi ngắn nhất: c -> h -> a -> g -> e

Độ dài : 6



-----
## References
1. Slide bài giảng
2. https://cuuduongthancong.com/atc/2569/chu-trinh-va-duong-di-euler/chu-trinh-va-duong-di-hamilton/thuat-toan-dijkstra


