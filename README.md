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

Dùng các cú pháp phân số, căn bậc, nhân chia, lũy thừa như `$$\large2^{2} = 4` góp phần làm cho tính dễ đọc thăng cao và chuyên nghiệp hơn. Cú pháp toán học phải **TO, Rõ ràng** để thấy, ở đây mình khuyến nghị dùng `\large hay \Large (Muốn to hơn nữa)` trước cú pháp như trên. Ngoài ra, các mũi tên như `2+1 \xrightarrow{\text{thông tin 1}} 3` hay việc đóng khung bên dưới từng biểu thức như `\underbrace{1\times2^{2}}*{\text{thông tin 2}}=\underbrace{1\times2\times2}*{\text{thông tin 2}}` giúp góp thêm không gian nêu rõ các ý nghĩa của biểu thức và trực quan hơn, góp phần giúp mức độ hiểu biết cao hơn và sâu hơn 

ví dụ với `\underbrace{1\times2^{2}}*{\text{thông tin 2}}=\underbrace{1\times2\times2}*{\text{thông tin 2}}` thì sẽ ra thế này :

$$\large
\underbrace{1\times2^{2}}*{\text{thông tin 2}}=
\underbrace{1\times2\times2}*{\text{thông tin 2}}
$$

hay với `\xrightarrow{\text{thông tin 1}}` :

$$\large
2 + 1 \xrightarrow{\text{thông tin 1}} 3
$$

## 6.Nghệ thuật phân bổ tiêu đề theo từng giai cấp

việc phân bổ tiêu đề ít góp phần gì nhiều, nhưng việc nó làm thay đổi kích cỡ cho các tiêu đề cha và con sẽ khiến đọc giả có mạch tự nhiên hơn và sẽ cảm nhận được đây là tiêu đề con theo kích cỡ của chữ, thay vì phải kéo lên mục lục xem lại. Dùng các `#` cho tiêu đề chính, thường giới thiệu ví dụ :

```
# Writeup : chủ đề writeup
```

dùng `##` cho tiêu đề cha ví dụ :

```
## 1.Tổng quan về số thực chuẩn IEEE754
```

dùng `###` cho tiêu đề con ví dụ :

```
### 1.1.IEEE754 là gì?
```

dùng `####` cho tiêu đề cháu, ví dụ :

```
#### 1.1.1.Các vấn đề thường gặp phải trong IEEE754
```

Khuyến nghị nên dùng `#` tới `####` cho từng tiêu đề, vì nếu dùng nhiều hơn kích cỡ sẽ rất nhỏ gây khó khăn cho người đọc

## 7.Nghệ thuật phân mảnh văn phong dài

dùng nút enter để xuống dòng theo nhịp của các đoạn văn dài, ví dụ từ đoạn sau :

```
- không phải mọi số thập phân đều biểu diễn chính xác trong nhị phân, nên IEEE 754 phải làm tròn (rounding). Đây là nguyên nhân của những kết quả như `0.1 + 0.2 != 0.3` trong nhiều ngôn ngữ lập trình. Phần chương này sẽ biểu diễn và tổng quát về việc này. Vì sao lại phải rounding?: Trong hệ thống máy tính, bit nhị phân là hữu hạn nhưng biểu diễn số thực một cách chính xác lại phải vô hạn nên khi đến một ngưỡng nào đó đụng tới rào cản hữu hạn sẽ xem như làm tròn của bit nhị phân đó ví dụ 4 bit $$\large0000_{2}$$ thì số thực chỉ được biểu diễn ở phạm vi bit này, bit được cấp cho trường fraction và các trường khác lại rất ít nên độ chính xác vì thế mà giảm rất đáng kể
```

ta có thể xuống dòng thành như vậy :

```
- không phải mọi số thập phân đều biểu diễn chính xác trong nhị phân, nên IEEE 754 phải làm tròn (rounding). Đây là nguyên nhân của những kết quả như `0.1 + 0.2 != 0.3` trong nhiều ngôn ngữ lập trình. Phần chương này sẽ biểu diễn và tổng quát về việc này

**Vì sao lại phải rounding?:** Trong hệ thống máy tính, bit nhị phân là hữu hạn nhưng biểu diễn số thực một cách chính xác lại phải vô hạn nên khi đến một ngưỡng nào đó đụng tới rào cản hữu hạn sẽ xem như làm tròn của bit nhị phân đó ví dụ 4 bit $$\large0000_{2}$$ thì số thực chỉ được biểu diễn ở phạm vi bit này, bit được cấp cho trường fraction và các trường khác lại rất ít nên độ chính xác vì thế mà giảm rất đáng kể
```

điều này giúp người đọc đỡ ngộp hơn

## 8.Nghệ thuật chèn các ký hiệu đặc biệt vào mục tiêu đề (mục lục)

Ta găp vấn đề khi dùng `$$\large1_{2}$$` nó lại hiện nguyên hình cú pháp khi đóng khung như `[ ]` để index link redirect vào? , ko sao ta có cách giải quyết là ta cần push lên github hay các nền tảng gì để nó in ra và ta copy nó dán vào là xong. Chỉ có thể dùng và hoạt động với một số kiểu nhất định như dương vô cực, âm vô cực $$\large+\infty$$, $$\large-\infty$$ ...

ví dụ :

```
[3.4.Round toward positive infinity $$\large+\infty$$]() // bị hiện nguyên cú pháp $$\large+\infty$$

thay vào đó, copy ký hiệu luôn

[3.4.Round toward positive infinity +∞]() //ổn thỏa, redirect link thoải mái
```

## 9.Khuôn viền và mô tả hình ảnh

Nghệ thuật này rất hữu ích, ví dụ trường hợp khi các ảnh trùng màu nền. Chẳng hạn, khi ta chụp màn hình ảnh nền của github để lấy cái thông tin quan trọng cho đọc giả đỡ phải bấm link redirect quay lại gây bất tiện, nhưng vấn đề màu nền github hay các màu nền trùng rất cao khiến 90% đọc giả phải hiểu nhầm đó là một loại văn bản ví dụ cụ thể:

```
![định lý 3.1](image/image.png)
> định lý được đề cập tới tại chương 3.1
```

thì kết quả sẽ ra

<kbd>
    
<img src="image/image.png" alt="trùng màu"/>

</kbd>

> ta thấy nó bị trùng màu
