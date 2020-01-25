# Share code vòng quay lì xì 2020
Tết thấy vui vui nên ngẫu hứng viết một con web tặng mọi người.
Mình dùng `Winwheel.js` để làm vòng quay và `sweetalert.js` để làm popup 
## Demo
Anh em xem demo ở đây: [Vòng quay lì xì](https://sharescript.net/demo/vong-quay-li-xi-2020-by-GrouSrlpPrsc/)

Lưu ý pass mở khoá vòng quay là "mycode"
## Ý tưởng và chức năng
Ý tưởng thực ra là dành cho điện thoại. Sau khi truy cập vào web, nhập pass rồi mình sẽ đưa cho mấy đứa con nít quay, mỗi đứa sẽ được quay một số lần nhất định mình đã setup trước, sau khi quay hết sẽ yêu cầu nhập pass(thực ra view source là thấy cmn pass luôn, có thể obfuscated tí cho vui). Phần cài đặt bên dưới có lịch sử lì xì và tổng số tiền đã mất...

**Túm cái váy lại là như này:**
- Mới vào trang, reload trang, hết lượt quay và làm mới vòng quay đều phải nhập mật khẩu
- Sau khi quay thì số tiền đã quay trước đó sẽ mất
- Khi đối phương muốn nhận tiền phải nhấp vào nút nhận tiền bên trái, khi đó lịch sử sẽ được lưu lại và yêu cầu nhập mật khẩu. Sau khi nhập mật khẩu vòng quay sẽ được reset như mới(Lịch sử không reset)
- Lịch sử sẽ mất khi reload trang
## Hướng dẫn setup
Bộ html nên ae up lên host hoặc save vô máy rồi bật ra

Tuỳ chỉnh css ở `css/custom.css`
### Chỉnh sửa vòng quay "`index.html`"
Anh em có thể sửa ảnh 2020 để dùng cho nhiều năm sau, đường dẫn của nó là `img/hea2.png` ở dòng 28 `index.html`

Tiếp đến có thể sửa nhạc "Vỗ tay", "Mất lượt", "Đang quay" ở dòng 70 71 72 `index.html`

Sửa mật khẩu vòng quay ở dòng 76 `index.html`, anh em có thể thêm mã hoá hay cái quần đùi gì đó để bảo mật tối ưu

Sửa số lần quay ở dòng 77 `index.html`

**Sửa vòng quay:**(Từ dòng 148 `index.html`)

Một đối tượng(một ô trong vong quay) sẽ được định nghĩa bằng code dưới đây
~~~
{
     'fillStyle': '#910f06',                // Màu ô(fill)
     'text': 'Ô mất lượt',                  // Chữ trên ô
     'size': winwheelPercentToDegrees(24),  // 24 là % quay trúng
     'textFontSize': 30,                    // Size chữ
     'textFillStyle': '#ffffff'             // Màu chữ
}
~~~
Ngoài ra thì anh em nghịch trong `index.html` nhá mình chú thích hết rồi, có thể chế ra nhiều kiểu khác :D

Nếu không làm được cứ inbox mình nhé, chúc anh em đầu năm vui vẻ không quạu!
