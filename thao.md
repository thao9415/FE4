#Day 1
- Trong 1 trang chỉ dùng 1 thẻ h1
- Thẻ block có width = 100% thẻ chứa nó 
- file reset đặt trên cùng (:D lý do là sau đó còn ghi đè lại file reset chứ, đặt cuối cùng thì code css xong lại load đến file reset, hihihi)
- phân biệt px, %, em, rem: mặc định trình duyệt có font-size 16px = 1rem
    + % phụ thuộc vào thẻ chứa nó
    + rem phụ thuộc vào font-size của thẻ HTML, mặc định 1rem = font-size HTML default = 16px => đo trong file thiết kế 50px đổi sang rem sẽ là 50 : 16 = ??? rem => khó khăn => css trick: ` html { font size: 62.5% } ` 62.5% = 62.5*16/100 = 10 px. Khi đó 1rem = 10px => 5rem = 50px => ez game
    + em phụ thuộc vào thẻ chứa nó gần nhất có chứa thuộc tính font-size hoặc chính nó
- css text:
    + `letter-spacing: value` Khoảng cách giữa các kí tự, `word-spacing: value` Khoảng cách giữa các chữ
    + `white-space: nowrap` Văn bản sẽ hiển thị trên cùng 1 hàng, chỉ xuống dòng khi gặp thẻ br
    + `text-overflow: clip` => text thừa sẽ bị ẩn đi, `text-overflow: ellipsis` => text thừa hiển thị ... => muốn hiển thị 3 dòng sau đó mới ... thêm thuộc tính `-webkit-line-clamp: 3` và `-webkit-box-orient: vertical;`
- `object-fit: cover` 
#Day 2
- opacity: 0 < visibility: hidden < display:none: opacity:0 - trong suốt, vẫn chiếm diện tích, vẫn chạm vào dc, visibility: hidden - trong suốt, vẫn chiếm diện tích, không chạm vào được, display: none - biến mất hoàn toàn, không chiếm diện tích, không chạm vào được
- child vs type: div>p+li*5+div*2
    + Muốn chọn li thứ nhất li:ntn-child(2) - con thứ 2 trong thẻ div hoặc li:fist-of-type - con đầu tiên loại li trong thẻ div. 
    + Chọn li cuối cùng => li:last-of-type...
    + Chọn div con đầu tiên => div:fist-of-type div:ntn-child(7) div:ntn-last-child(2) div:ntn-of-type(2)...
- thẻ p không bọc được thẻ div
- selector: 
    + div p => các thẻ p nằm trong thẻ div, miễn là nằm trong, ko quan trọng p cháu, p chắt j hết
    + div > p => Các thẻ p là con trực tiếp của div (con trực tiếp chứ ko phải con đầu tiên)
    + div + p => Thẻ p hàng xóm, đứng "ngay cạnh" div, nếu div h1 p => cũng ko chọn đc p nhé, vì có thẻ h1 ở giữa rồi.
    + div ~ p => Chọn tất cả thẻ p là hàng xóm, ko cần đứng ngay cạnh, nói chung là cùng đẳng cấp thì chọn thôi.
    
