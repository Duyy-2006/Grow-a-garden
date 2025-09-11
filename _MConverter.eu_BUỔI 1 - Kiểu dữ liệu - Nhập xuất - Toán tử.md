## BUỔI 1: Compiler, Nhập xuất, Biến, Toán tử {#buổi-1-compiler-nhập-xuất-biến-toán-tử .unnumbered}

### Nội dung buổi học : {#nội-dung-buổi-học}

- Hướng dẫn cài đặt IDE (Dev C) , hỗ trợ sửa các lỗi trong Dev C.

- Hướng dẫn học trên codeforces (cách submit bài, chọn phiên bản trình
  biên dịch,...).

- Giới thiệu về nhập xuất trong C, biến, các kiểu dữ liệu và đặc tả của
  nó.

- Các toán tử trong C (toán tử 1 ngôi, toán tử 2 ngôi).

### Yêu cầu kiến thức cần chuẩn bị : {#yêu-cầu-kiến-thức-cần-chuẩn-bị}

1.  Tải bộ cài dev C https://sourceforge.net/projects/orwelldevcpp/

2.  Lập tài khoản codeforces (Các lead chính invite nick codeforce)

3.  Kiểu dữ liệu cơ bản trong C.

4.  Tìm hiểu về cấu trúc 1 chương trình C

5.  Nếu em không có máy tính

[[https://play.google.com/store/apps/details?id=com.kvassyu.coding2.cpp]{.underline}](https://play.google.com/store/apps/details?id=com.kvassyu.coding2.cpp)

### Chi tiết bài giảng:

#### 1. Tại sao lại chọn C để training? {#tại-sao-lại-chọn-c-để-training .unnumbered}

- Trong lịch sử, C từng là 1 ngôn ngữ bậc cao, và đến ngày nay C là 1
  ngôn ngữ cấp thấp, để luyện tư duy lập trình cơ bản

- C là nền tảng để có thể nắm bắt các ngôn ngữ khác dễ dàng hơn: C++,
  Java, ...

#### 2. Cấu trúc của 1 chương trình C: (00:00 - 00:30) {#cấu-trúc-của-1-chương-trình-c-0000---0030 .unnumbered}

\*Ví dụ về một chương trình C :

*//Khai báo các thư viện*

\#include \<stdio.h\> // standard in out . header các hàm nhập xuất cơ
bản

*// Hàm Main*

**int** main(){

    printf(\"Chao mung den voi CLB Lap Trinh PTIT\");

return 0;

}

\*Các câu hỏi có thể hỏi và bài tập đưa ra:

- **Các em có biết thêm thư viện nào khác hay không? Chức năng của
  chúng**

**+Math.h**

**+stdlib.h**

- **Thử in ra một câu chào trong cmd**

*// Người dạy tự đưa ra ví dụ giúp các em hiểu*

**2.1.Khái niệm:**

Một chương trình C cơ bản gồm có :

- Các lệnh tiền xử lý : khai báo thư viện stdio.h (Standard in out.h)

- Các biến (các em sẽ được học ở buổi sau )

- Các lệnh và biểu thức (như hàm main là nơi mà chương trình bắt đầu,
  printf là một chức năng khác của ngôn ngữ C).

- Cách comment

#### 3. Biến và Kiểu dữ liệu trong C : (00:30 - 01:00) {#biến-và-kiểu-dữ-liệu-trong-c-0030---0100 .unnumbered}

Giới thiệu về kiểu dữ liệu trong C .

|           |                                            |        |
|-----------|--------------------------------------------|--------|
| char      | 0 ... 255                                  | 1 byte |
| int       | -2147483648..2147483647. 2\^32 - (2\^32-1) | 4 byte |
| float     | 3\. 4e-38 . . 3.4e + 38                    | 4 byte |
| double    | 1.7e-308 . . 1.7e + 308                    | 8 byte |
| long long | -9223372036854775808...9223372036854775807 | 8 byte |

**3.1.** **Khái niệm:** [Nó được sử dụng để lưu trữ dữ liệu. Giá trị của
nó có thể được thay đổi và nó có thể được sử dụng lại nhiều lần.]{.mark}

[Mỗi biến có một loại dữ liệu cụ thể. Nhắc nhở các em biến trong C có
phân biệt chữ hoa chữ thường (chưa cần nói nhiều về quy tắc đặt tên
biến).]{.mark}

**[3.2. Cách khai báo một biến:]{.mark}**

[\< Kiểu_dữ_liệu \> \<tên_biến\>;]{.mark}

[VD :]{.mark} ![](media/image1.png){width="5.0625in" height="1.53125in"}

- Nói cho các em mỗi dòng lệnh trong C kết thúc bằng dấu ";".

- Một số quy tắc khai báo biến, bảo các em có thể tự tìm hiểu ??

  - Khai báo tên biến ko có số ở đầu, ko có dấu cách, ko trùng với các
    từ khóa đặc biệt (int,float,break,...)

  3.  **Biến toàn cục và biến cục bộ trong C :**

|                 |                                 |                                              |
|-----------------|---------------------------------|----------------------------------------------|
|                 | Biến toàn cục                   | Biến cục bộ                                  |
| Vị trí khai báo | Được khai báo ngoài hàm main    | Được khai báo trong các khối lệnh, trong hàm |
| Phạm vi sử dụng | ở bất kỳ đâu trong chương trình | Chỉ dung được trong hàm, khối lệnh đó        |

- Khác nhau giữa biến kiểu int và float là gì ? (nói về độ chính xác của
  số thực)

- Nói về cách gán giá trị cho 1 biến? nếu khởi tạo biến mà không gán giá
  trị thì biến sẽ nhận giá trị gì, sự khác nhau giữa global và local ra
  sao (biến global auto bằng 0 khi khởi tạo).

- Nói về tự khóa const :

Được sử dụng để định nghĩa hằng số trong C.

Vd : **const** []{.mark}**float** []{.mark}PI = 3.14;

Và bây giờ biến PI không thể thay đổi, nếu cố gắng thay đổi sẽ gặp lỗi.

#### 4. Toán tử nhập xuất trong C: (01:00 - 01:30) {#toán-tử-nhập-xuất-trong-c-0100---0130 .unnumbered}

\- Hàm printf() được sử dụng để in lệnh đã cho ra màn hình.

\- Hàm scanf() được dùng để đọc dữ liệu đầu vào từ bàn phím.

**4.1 Đặc tả :**

|           |      |
|-----------|------|
| int       | %d   |
| long long | %lld |
| float     | %f   |
| double    | %lf  |
| char      | %c   |

- Cách in chiều rộng đặc tả ( %.2f, %2d)

- (Ví dụ về %2.2f : 2 số phần nguyên, 2 số sau dấu phẩy)

- Cho các em làm bài tập theo từng phần để giúp các em hiểu bài hơn, bài
  tập tùy vào người dạy chính quyết định.

- Bài tập: Nhập vào nguyên / thực a, in ra số nguyên a / in ra số thập
  phân có 10 chữ số đằng sau dấu phẩy.

### 5. Biểu thức {#biểu-thức .unnumbered}

#### 5.1Toán tử số học: {#toán-tử-số-học .unnumbered}

|             |                                  |                                                                                                                                                                                                                    |
|-------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Toán tử** | **Miêu tả**                      | **Ví dụ**                                                                                                                                                                                                          |
| **+**       | Cộng 2 toán hạng                 | A + B sẽ cho kết quả là 11                                                                                                                                                                                         |
| **-**       | Trừ 2 toán hạng                  | A - B sẽ cho kết quả là -1                                                                                                                                                                                         |
| **\***      | Nhân 2 toán hạng                 | A \* B sẽ cho kết quả là 30                                                                                                                                                                                        |
| **/**       | Chia 2 toán hạng                 | B / A sẽ cho kết quả là 0 (2 toán hạng đều là số nguyên thì kết quả là phần nguyên của thương) A / C sẽ cho kết quả là 4.166667 (1 trong 2 toán hạng là số thực dấu phẩy động thì thương là số thực dấu phẩy động) |
| **%**       | Chia lấy phần dư                 | B % A sẽ cho kết quả là 1                                                                                                                                                                                          |
| **++**      | Tăng giá trị thêm 1 cho một biến | A++ sẽ khiến A tăng thêm 1                                                                                                                                                                                         |
| **----**    | Giảm giá trị thêm 1 cho 1 biến   | A--- sẽ khiến A giảm đi 1                                                                                                                                                                                          |

#### 5.2 Toán tử gán: {#toán-tử-gán .unnumbered}

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 27%" />
<col style="width: 47%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Toán tử</strong></td>
<td><strong>Ví dụ</strong></td>
<td><strong>Tương đương với</strong></td>
</tr>
<tr class="even">
<td><strong>=</strong></td>
<td><p><strong>C = A + B</strong></p>
<p><strong>C = B</strong></p></td>
<td><p><strong>C = A + B</strong></p>
<p><strong>C = B</strong></p></td>
</tr>
<tr class="odd">
<td><strong>+=</strong></td>
<td><strong>C += A</strong></td>
<td><strong>C = C + A</strong></td>
</tr>
<tr class="even">
<td><strong>-=</strong></td>
<td><strong>C -= A</strong></td>
<td><strong>C = C - A</strong></td>
</tr>
<tr class="odd">
<td><strong>*=</strong></td>
<td><strong>C *= A</strong></td>
<td><strong>C = C * A</strong></td>
</tr>
<tr class="even">
<td><strong>/=</strong></td>
<td><strong>C /= A</strong></td>
<td><strong>C = C / A</strong></td>
</tr>
<tr class="odd">
<td><strong>%=</strong></td>
<td><strong>C %= A</strong></td>
<td><strong>C = C % A</strong></td>
</tr>
</tbody>
</table>

=\> Có thể nói thêm về phân biệt giữa a++ và ++a

(a++ là thực hiện phép toán rồi mới tăng biến a lên 1 đơn vị)

(++a là tăng biến a lên 1 đơn vị rồi mới thực hiện phép toán)

VD:

int a = 4; printf("%d", a++); printf("%d", a); =\> In ra 4 5

int a = 4; printf("%d", ++a); printf("%d", a); =\> In ra 5 5

#### 6. Ép kiểu {#ép-kiểu .unnumbered}

Đôi khi chúng ta cần chuyển đổi giá trị một biểu thức sang kiểu dữ liệu
khác. Ví dụ trong trường hợp ta muốn thực hiện phép toán chia lấy phần
dư của 2 số nguyên, nhưng lại được lưu trong **2 biến kiểu float, ta
không thể áp dụng trực tiếp toán tử % cho 2 biến đó**. Bạn chạy chương
trình thế này sẽ báo lỗi:

1#include \<stdio.h\>

2int main(void)

3{

4 int a = 5, c;

5 float b = 6;

6 c = a % b;

7 printf(\"%d\", c);

8 return 0;

9}

**Vì thế cần ép kiểu theo cú pháp: (\<kiểu dữ liệu\>) \<biểu thức\>**

để lấy giá trị từ biến b, đổi sang số nguyên để thực hiện phép %. Code
đúng như sau:

1#include \<stdio.h\>

2int main(void)

3{

4 int a = 5, c;.

5 float b = 6;

6 **c = a % (int)b;**

7 printf(\"%d\", c);

8 return 0;

9}

**Nêu ví dụ về thay đổi giá trị của hai biến**

- Có thể dùng biến thứ 3 tạm bằng toán tử gán

- Có thể dùng toán tử toán học để thay đổi giá trị. VD = a = a + b, b =
  a - b, a = a - b

### 7.Luyện tập: (Thời gian ngoài còn lại) {#luyện-tập-thời-gian-ngoài-còn-lại .unnumbered}

Câu hỏi có thể đưa ra :

- Đổi giá trị của 2 biến ?

- Thử nhập vào một số và in ra nó ?

Bài tập :

**Bài 1**: Nhập 1 số nguyên r ( 0 \< r \< 10\^9), tính chu vi và diện
tích của hình tròn bán kính r.

*Example*

<table>
<colgroup>
<col style="width: 45%" />
<col style="width: 54%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Input:</td>
<td>Output:</td>
</tr>
<tr class="even">
<td>3</td>
<td><p>18.85</p>
<p>28.27</p></td>
</tr>
</tbody>
</table>

**Bài 2:** Nhập vào 3 số nguyên d, m, y( 0 \< d \< 32, 0 \< m \< 13, 0
\< y \< 10000 ) lần lượt là ngày, tháng và năm. In ra màn hình dưới dạng
dd/mm/yyyy.

*Example*

|           |            |
|-----------|------------|
| Input:    | Output:    |
| 5 12 2021 | 05/12/2021 |

**Bài 3:** Nhập 2 số nguyên l, r. Tính tổng các số nguyên trong đoạn
\[l; r\]. 

*Example*

|        |             |
|--------|-------------|
| Input: | Output:  bc |
| 5 10   | 45          |
