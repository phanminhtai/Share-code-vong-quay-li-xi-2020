# Share code vòng quay lì xì 2020
Tết thấy vui vui nên ngẫu hứng nên viết một con web tặng mọi người.
Mình dùng `Winwheel.js` để làm vòng quay và `sweetalert.js` để làm popup 
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
### Chỉnh sửa ảnh
`index.html`: 
