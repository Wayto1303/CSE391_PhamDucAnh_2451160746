# Phần A: Đọc Hiểu

_Câu A1_

Khi gõ https://shopee.vn vào trình duyệt và nhấn Enter, thứ tự 5 bước xảy ra là:

1. Gửi Request: trình duyệt hỏi DNS Server "shopee.vn là IP nào?" và nhận về địa chỉ IP sau đó gửi yêu cầu đến Server thông qua mạng Internet
2. Server xử lý: "Trường muốn xem trang chủ shopee"
3. HTTP Response: Server sẽ gửi các file như html, css, js cho bên trình duyệt cũng thông qua mạng Internet
4. Parse html, css & execute js: Trình duyệt sẽ đọc các file html như bản kiến trúc, css như bản nội thất và xử lý js như lắp đặt hệ thống điện nước
5. Paint & render: Trình duyệt sẽ hoàn thiện và hiển thị giao diện lên trên màn hình cho Trường xem

Tab Network cho thấy toàn bộ các request mà trình duyệt gửi đi khi tải trang


_Câu A2_
Lỗi 3 — Thẻ `<img>` thiếu thuộc tính alt
Google đọc alt để hiểu ảnh nói về cái gì. Thiếu alt thì ảnh vô nghĩa với cả Google lẫn người dùng dùng screen reader.

Lỗi 4 — Menu điều hướng không dùng `<nav>`
Google ưu tiên `<nav>` để xác định cấu trúc điều hướng của trang. Dùng `<div class="menu">` thì Google không nhận ra đây là menu.
## Sửa lại lỗi

```html
<header>
  <div class="logo">ShopTLU</div>
  <nav>
    <ul>
      <li><a href="/">Trang chủ</a></li>
      <li><a href="/products">Sản phẩm</a></li>
    </ul>
  </nav>
</header>

<main>
  <article class="product">
    <h1>iPhone 16 Pro</h1>
    <p class="price">25.990.000đ</p>
    <img src="iphone.jpg" alt="iPhone 16 Pro" />
  </article>
</main>

<footer>© 2026 ShopTLU</footer>
```