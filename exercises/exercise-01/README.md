# Bài tập 1: HTML Cơ bản - Cấu trúc và thẻ đơn giản

## 🎯 Mục tiêu

Làm quen với cấu trúc cơ bản của HTML và các thẻ thường dùng nhất. Đây là bài tập đầu tiên giúp bạn hiểu nền tảng của HTML.

## 📚 Kiến thức cần học trước

- Hiểu HTML là gì
- Cấu trúc cơ bản của một tài liệu HTML
- Các thẻ HTML cơ bản

## 📋 Yêu cầu bài tập

### **Nhiệm vụ: Tạo trang "Giới thiệu bản thân"**

Tạo một trang HTML đơn giản giới thiệu về bản thân với các yêu cầu sau:

### **Phần 1: Cấu trúc cơ bản (8 điểm)**
- [ ] Tạo file `index.html` với cấu trúc HTML5 đúng chuẩn
- [ ] Có đầy đủ: `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`
- [ ] Thiết lập `<meta charset="UTF-8">`
- [ ] Thiết lập `<title>` phù hợp

### **Phần 2: Nội dung trong `<head>` (2 điểm)**
- [ ] Title hiển thị: "Tên của bạn - Giới thiệu"
- [ ] Meta description (tùy chọn)

### **Phần 3: Nội dung trong `<body>` (10 điểm)**

#### **3.1. Tiêu đề (2 điểm)**
- [ ] Sử dụng `<h1>` cho tên của bạn
- [ ] Sử dụng `<h2>` cho "Giới thiệu về tôi"

#### **3.2. Đoạn văn (3 điểm)**
- [ ] Ít nhất 2 đoạn văn `<p>` giới thiệu về bản thân
- [ ] Mỗi đoạn ít nhất 2-3 câu

#### **3.3. Danh sách (3 điểm)**
- [ ] Một danh sách không có thứ tự `<ul>` về sở thích (ít nhất 4 mục)
- [ ] Một danh sách có thứ tự `<ol>` về mục tiêu học tập (ít nhất 3 mục)

#### **3.4. Liên kết và nhấn mạnh (2 điểm)**
- [ ] Ít nhất 1 liên kết `<a>` đến trang web yêu thích
- [ ] Sử dụng `<strong>` hoặc `<em>` để nhấn mạnh một số từ quan trọng

## 📁 Cấu trúc file

```
exercise-01/
├── README.md (file này)
├── index.html (file bạn tạo)
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
    <title><!-- Thêm title ở đây --></title>
</head>
<body>
    <!-- Thêm nội dung ở đây -->
</body>
</html>
```

## ✅ Ví dụ mẫu (chỉ tham khảo cấu trúc)

```html
<h1>Nguyễn Văn A</h1>
<h2>Giới thiệu về tôi</h2>

<p>Xin chào! Tôi là Nguyễn Văn A, hiện đang là sinh viên năm 2...</p>
<p>Tôi có niềm đam mê với <strong>công nghệ</strong> và luôn muốn...</p>

<h3>Sở thích của tôi</h3>
<ul>
    <li>Đọc sách</li>
    <li>Nghe nhạc</li>
    <li>Lập trình</li>
    <li>Du lịch</li>
</ul>

<h3>Mục tiêu học tập</h3>
<ol>
    <li>Học thành thạo HTML và CSS</li>
    <li>Tìm hiểu về JavaScript</li>
    <li>Xây dựng website cá nhân</li>
</ol>

<p>Bạn có thể tìm hiểu thêm về lập trình tại 
<a href="https://developer.mozilla.org">MDN Web Docs</a>.</p>
```

## 🎯 Tiêu chí chấm điểm

| Tiêu chí | Điểm | Mô tả |
|----------|------|--------|
| **Cấu trúc HTML** | 8 | DOCTYPE, html, head, body đúng chuẩn |
| **Head section** | 2 | Title và meta tags |
| **Tiêu đề** | 2 | Sử dụng h1, h2 đúng |
| **Đoạn văn** | 3 | Ít nhất 2 đoạn p có nội dung |
| **Danh sách** | 3 | Có ul và ol với đủ items |
| **Liên kết & nhấn mạnh** | 2 | Có a, strong/em |
| **Tổng cộng** | **20** | |

### Thang điểm:
- **18-20 điểm:** Xuất sắc ⭐⭐⭐
- **15-17 điểm:** Tốt ⭐⭐
- **12-14 điểm:** Khá ⭐
- **Dưới 12 điểm:** Cần cải thiện

## 🚀 Hướng dẫn thực hiện

### Bước 1: Tạo nhánh mới
```bash
git checkout main
git pull origin main
git checkout -b exercise-01-[ten-cua-ban]
```

### Bước 2: Tạo file
```bash
cd exercises/exercise-01
touch index.html
```

### Bước 3: Viết HTML
- Bắt đầu với template cơ bản
- Thêm từng phần một
- Kiểm tra trong trình duyệt thường xuyên

### Bước 4: Kiểm tra
- Mở file trong trình duyệt
- Kiểm tra tất cả yêu cầu đã hoàn thành
- Validate HTML tại [W3C Validator](https://validator.w3.org/)

### Bước 5: Commit và push
```bash
git add .
git commit -m "feat: Hoàn thành bài tập 1 - HTML cơ bản"
git push -u origin exercise-01-[ten-cua-ban]
```

## 💡 Tips hữu ích

1. **Sử dụng indentation:** Thụt lề code để dễ đọc
2. **Comment code:** Thêm comment để giải thích
3. **Kiểm tra thường xuyên:** Mở file trong trình duyệt để xem kết quả
4. **Đặt tên file:** Luôn dùng `index.html` cho trang chính

## 📚 Tài liệu tham khảo

- [MDN HTML Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [W3Schools HTML Tutorial](https://www.w3schools.com/html/)
- [HTML5 Semantic Elements](https://www.w3schools.com/html/html5_semantic_elements.asp)

## ❓ Câu hỏi thường gặp

**Q: Tôi có thể thêm CSS không?**
A: Bài tập này chỉ tập trung vào HTML. CSS sẽ được học ở bài tập 4.

**Q: Nội dung có thể là tiếng Anh không?**
A: Có, bạn có thể viết bằng tiếng Anh hoặc tiếng Việt.

**Q: Tôi có thể thêm ảnh không?**
A: Chưa cần thiết cho bài này. Thẻ `<img>` sẽ được học ở bài tập 2.

---

**Tiếp theo:** [Bài tập 2: HTML Nâng cao](../exercise-02/README.md)

**Deadline:** [Teacher sẽ thông báo] 