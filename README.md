# Writeups-technique
Viết writeups ko chỉ cho người khác đọc mà còn cho chính bản thân mình trong tương lai xem lại khi kiến thức bị bão hòa theo thời gian. Vì vậy, việc nắm vững các kỹ thuật trình bày, phát biểu và tính mạch lạc là điều vô cùng quan trọng

Viết writeup ko chỉ viết văn, nó còn là cả một nghệ thuật của công đoạn học hỏi. Vậy nên nếu biết đặt câu hỏi cho chiều sâu và tính thực dụng của tri thức, thì việc trình bày giúp ta tiếp thu nó tốt hơn

---

## 1.Phần details

Là thứ quan trọng nhất, vấn đề là chúng thu gọn thông tin được truyền đặt vào một khung nhỏ, đọc giả hễ muốn đọc thì cứ việc mở ra và tránh làm nhiễu vấn đề trọng tâm có trong writeup. Nhưng cũng để ý nó còn có một điểm yếu chí mạng, nếu ta chủ quan ko thiết lập ranh giới rõ ràng cho nó, nó có thể gây ra nhầm lẫn rối loạn thông tin (kiểu nó như hòa là một với thông tin trọng tâm) nên việc đặt ranh giới với kỹ thuật `---` bên trên lẫn dưới và `<sub>--đã hết phần giải thích--</sub>` bên dưới cùng phần details khi kết thúc trình bày lại vô cùng quan trọng.

Nó cho biết đọc giả đã nhận thức mình đã thực sự đọc xong phần này chưa, ngoài ra cần thêm `> phần detail trả lời câu hỏi trên` hay `> phần details giải thích về FPU` cho đọc giả biết mình có quan tâm chủ đề này không.

---

## 2.Nghệ thuật đặt ranh giới cho các chủ đề

khi mục lục được thiết lập sẵn, nhưng với các chủ đề như `## 1.tổng quan mã bù hai` và `## 2.nghệ thuật khử nhiễu trong dịch ngược` cần phải cách ly bằng cách thiết lập ranh giới `---` gạch ngang cho từng chủ đề. Đối với chủ đề con như `#### 1.1.Mã bù hai là gì?` thì chúng ta ko cần thiết lập ranh giới, vì nó thuộc chủ đề `## 1` nên việc đặt ranh giới vừa phá vỡ trình tự logic, vừa tăng rối mắt cho đọc giả

---

## 3.Nghệ thuật thiết lập mục lục

mục lục thoáng qua hơi tầm thường, nhưng với sách hay tài liệu giá trị cao thường rất hay dùng. Có mục lục, đọc giả biết trang thông tin này nó có những điều gì, điều gì mình cần học và mình học được những gì trong này. Mục lục hay, đọc giả siêu lòng có hứng đọc tiếp, mục lục tầm thường đọc giả bỏ qua bài luôn.

trình bày rõ và khoảng cách với các mục con của mục chính, ví dụ :

```
- 1.Tổng quan về IEEE754
    - 1.1.IEEE754 là gì
      - 1.1.1.<thông tin tiếp>
```

tac dụng của nó sẽ giúp đọc giả phân biệt phần nào là phần con thuộc phần cha, tránh soi từng số gây tốn time và mỏi mắt. Quan trọng ko kém là đính kèm link redirect vào trong mục lục luôn, họ ấn là dịch tới chính xác cái họ cần, khỏi phải lướt tay tìm kiếm tốn thời gian

---

## 4.Nghệ thuật reading checkpoint

Writeup tốt ko chỉ cho đọc giả biết ranh giới và phân biệt của tầng thông tin vật lý, nó cần phải cho đọc giả biết ranh giới và nhìn thấu nhận thức của mình hiện tại với kiến thức. Một reading checkpoint có thể giúp đạt sự truyền tải thông tin tốt hơn vì nó cho biết đọc giả cần chuẩn bị những gì trước khi đi qua vấn đề này và học hỏi. Ví dụ :

```
> **Reading checkpoint**
>
> Đến đây, bạn cần hiểu:
>
> - Actual exponent là gì
> - Exponent field là gì
> - Bias dùng để làm gì
> - Chuẩn hóa số thực ra sao
> - Sign là gì
> - số âm, dương actual exponent của vị trí dấu chấm nhị phân
>
> Nếu đã rõ thì có thể tiếp tục.
```

thêm vào trước chủ đề hay ở chỗ người đọc có thể nhìn thấy trước khi đi vào phần introduce của chương kế tiếp.

## 5.Nghệ thuật phép toán học

Dùng các cú pháp phân số, căn bậc, nhân chia, lũy thừa như `$$\large2^{2} = 4` góp phần làm cho tính dễ đọc thăng cao và chuyên nghiệp hơn. Cú pháp toán học phải **TO, Rõ ràng** để thấy, ở đây mình khuyến nghị dùng `\large hay \Large (Muốn to hơn nữa)` trước cú pháp như trên. Ngoài ra, các mũi tên như `2+1 \xrightarrow{\text{thông tin 1}} 3` hay việc đóng khung bên dưới từng biểu thức như `\underbrace{1\times2^{-126}}*{\text{thông tin 2}}` giúp góp thêm không gian nêu rõ các ý nghĩa của biểu thức và trực quan hơn, góp phần giúp mức độ hiểu biết cao hơn và sâu hơn 

ví dụ với `\underbrace{1\times2^{-126}}*{\text{thông tin 2}}` thì sẽ ra thế này :

$$\large
\underbrace{1\times2^{2}}*{\text{thông tin 2}}=
\underbrace{1\times2\times2}*{\text{thông tin 2}}
$$

hay với `\xrightarrow{\text{thông tin 1}}` :

$$\large
2 + 1 \xrightarrow{\text{thông tin 1}} 3
$$
