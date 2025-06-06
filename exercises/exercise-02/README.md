# Bài tập 2: HTML Nâng cao - Form, Table, Semantic Tags

## 🎯 Mục tiêu

Học cách sử dụng các thẻ HTML nâng cao như form, table, và semantic HTML. Bài tập này xây dựng dựa trên kiến thức từ bài tập 1.

## 📚 Kiến thức cần học trước

- Hoàn thành bài tập 1
- Hiểu cấu trúc HTML cơ bản
- Các thẻ HTML cơ bản (h1-h6, p, ul, ol, a)

## 📋 Yêu cầu bài tập

### **Nhiệm vụ: Tạo trang "CV Online"**

Mở rộng trang giới thiệu từ bài tập 1 thành một CV online hoàn chỉnh với các yêu cầu sau:

### **Phần 1: Cấu trúc Semantic HTML (8 điểm)**
- [ ] Sử dụng `<header>` cho phần đầu trang
- [ ] Sử dụng `<main>` cho nội dung chính
- [ ] Sử dụng `<section>` cho từng phần khác nhau
- [ ] Sử dụng `<footer>` cho phần cuối trang
- [ ] Sử dụng `<article>` cho phần kinh nghiệm (nếu có)

### **Phần 2: Hình ảnh và Media (4 điểm)**
- [ ] Thêm ảnh đại diện với thẻ `<img>`
- [ ] Sử dụng thuộc tính `alt` mô tả ảnh
- [ ] Ảnh có kích thước phù hợp (có thể dùng placeholder)

### **Phần 3: Bảng thông tin (6 điểm)**
- [ ] Tạo bảng `<table>` hiển thị thông tin cá nhân
- [ ] Sử dụng `<thead>`, `<tbody>` đúng cách
- [ ] Có ít nhất 4 hàng thông tin (tên, tuổi, địa chỉ, email, etc.)
- [ ] Sử dụng `<th>` cho header và `<td>` cho data

### **Phần 4: Form liên hệ (7 điểm)**
- [ ] Tạo form `<form>` với các trường:
  - Input text cho tên
  - Input email cho email
  - Textarea cho tin nhắn
  - Select dropdown cho chủ đề
  - Radio buttons cho mức độ ưu tiên
  - Checkbox cho đồng ý điều khoản
- [ ] Sử dụng `<label>` cho tất cả input
- [ ] Có nút submit

## 📁 Cấu trúc file

```
exercise-02/
├── README.md (file này)
├── index.html (file bạn tạo)
├── images/ (folder chứa ảnh)
│   └── avatar.jpg (ảnh đại diện)
└── starter/
    └── template.html (template tham khảo)
```

## 📝 Template khởi tạo

```html
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tên của bạn - CV Online</title>
</head>
<body>
    <header>
        <!-- Thông tin header -->
    </header>
    
    <main>
        <section id="about">
            <!-- Phần giới thiệu -->
        </section>
        
        <section id="info">
            <!-- Bảng thông tin cá nhân -->
        </section>
        
        <section id="contact">
            <!-- Form liên hệ -->
        </section>
    </main>
    
    <footer>
        <!-- Thông tin footer -->
    </footer>
</body>
</html>
```

## ✅ Ví dụ các thành phần

### **Bảng thông tin:**
```html
<table>
    <thead>
        <tr>
            <th>Thông tin</th>
            <th>Chi tiết</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Họ tên</td>
            <td>Nguyễn Văn A</td>
        </tr>
        <tr>
            <td>Tuổi</td>
            <td>22</td>
        </tr>
        <!-- Thêm các hàng khác -->
    </tbody>
</table>
```

### **Form liên hệ:**
```html
<form>
    <label for="name">Tên của bạn:</label>
    <input type="text" id="name" name="name" required>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <label for="subject">Chủ đề:</label>
    <select id="subject" name="subject">
        <option value="general">Tổng quát</option>
        <option value="work">Công việc</option>
        <option value="collaboration">Hợp tác</option>
    </select>
    
    <label for="message">Tin nhắn:</label>
    <textarea id="message" name="message" rows="4" required></textarea>
    
    <fieldset>
        <legend>Mức độ ưu tiên:</legend>
        <input type="radio" id="low" name="priority" value="low">
        <label for="low">Thấp</label>
        
        <input type="radio" id="medium" name="priority" value="medium">
        <label for="medium">Trung bình</label>
        
        <input type="radio" id="high" name="priority" value="high">
        <label for="high">Cao</label>
    </fieldset>
    
    <input type="checkbox" id="agree" name="agree" required>
    <label for="agree">Tôi đồng ý với điều khoản sử dụng</label>
    
    <button type="submit">Gửi tin nhắn</button>
</form>
```

## 🎯 Tiêu chí chấm điểm

| Tiêu chí | Điểm | Mô tả |
|----------|------|--------|
| **Semantic HTML** | 8 | Sử dụng header, main, section, footer đúng |
| **Hình ảnh** | 4 | Thẻ img với alt text phù hợp |
| **Bảng** | 6 | Table với thead, tbody, th, td đúng cách |
| **Form** | 7 | Form hoàn chỉnh với các input types khác nhau |
| **Tổng cộng** | **25** | |

### Thang điểm:
- **23-25 điểm:** Xuất sắc ⭐⭐⭐
- **20-22 điểm:** Tốt ⭐⭐
- **17-19 điểm:** Khá ⭐
- **Dưới 17 điểm:** Cần cải thiện

## 🚀 Hướng dẫn thực hiện

### Bước 1: Tạo nhánh mới
```bash
git checkout main
git pull origin main
git checkout -b exercise-02-[ten-cua-ban]
```

### Bước 2: Chuẩn bị file
```bash
cd exercises/exercise-02
touch index.html
mkdir images
```

### Bước 3: Thêm ảnh đại diện
- Tìm một ảnh đại diện (hoặc dùng placeholder)
- Đặt vào folder `images/`
- Hoặc sử dụng placeholder: `https://picsum.photos/200/200`

### Bước 4: Viết HTML
- Bắt đầu với cấu trúc semantic
- Thêm từng section một
- Test form trong trình duyệt

### Bước 5: Kiểm tra và commit
```bash
git add .
git commit -m "feat: Hoàn thành bài tập 2 - HTML nâng cao"
git push -u origin exercise-02-[ten-cua-ban]
```

## 💡 Tips hữu ích

1. **Semantic HTML:** Sử dụng đúng thẻ cho đúng mục đích
2. **Form validation:** Sử dụng `required`, `type="email"` cho validation cơ bản
3. **Accessibility:** Luôn có `label` cho mọi input
4. **Table structure:** Sử dụng `thead` và `tbody` để cấu trúc rõ ràng
5. **Alt text:** Mô tả ảnh một cách có ý nghĩa

## 📚 Tài liệu tham khảo

- [MDN HTML Forms](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)
- [MDN HTML Tables](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)
- [MDN Semantic HTML](https://developer.mozilla.org/en-US/docs/Glossary/Semantics#semantic_elements)
- [HTML Form Elements](https://www.w3schools.com/html/html_form_elements.asp)

## ❓ Câu hỏi thường gặp

**Q: Form có cần xử lý submit không?**
A: Không, chỉ cần HTML. Xử lý form sẽ học với JavaScript sau.

**Q: Bảng có cần styling không?**
A: Chưa cần. CSS sẽ được học từ bài tập 4.

**Q: Tôi có thể thêm nhiều section hơn không?**
A: Có, bạn có thể thêm section kinh nghiệm, học vấn, kỹ năng, etc.

**Q: Ảnh phải là ảnh thật không?**
A: Không, có thể dùng placeholder hoặc ảnh bất kỳ.

---

**Trước đó:** [Bài tập 1: HTML Cơ bản](../exercise-01/README.md)
**Tiếp theo:** [Bài tập 3: Tổng hợp HTML](../exercise-03/README.md)

**Deadline:** [Teacher sẽ thông báo] 