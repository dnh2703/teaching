# Bài tập 4: CSS Cơ bản - Selectors, Colors, Fonts

## 🎯 Mục tiêu

Học cách sử dụng CSS để tạo kiểu cho HTML. Đây là bài tập đầu tiên về CSS, tập trung vào các khái niệm cơ bản nhất.

## 📚 Kiến thức cần học trước

- Hoàn thành bài tập 1 và 2 (HTML cơ bản và nâng cao)
- Hiểu cấu trúc HTML
- Biết cách liên kết CSS với HTML

## 📋 Yêu cầu bài tập

### **Nhiệm vụ: Tạo kiểu cho trang CV từ bài tập 2**

Sử dụng trang CV đã tạo ở bài tập 2 (hoặc tạo mới) và thêm CSS để làm đẹp trang web.

### **Phần 1: Thiết lập CSS (3 điểm)**
- [ ] Tạo file `style.css` riêng biệt
- [ ] Liên kết CSS với HTML bằng thẻ `<link>`
- [ ] CSS reset cơ bản (margin, padding = 0)

### **Phần 2: Typography - Fonts và Text (8 điểm)**
- [ ] Chọn và áp dụng Google Font cho toàn trang
- [ ] Thiết lập font-size khác nhau cho h1, h2, h3, p
- [ ] Sử dụng font-weight (bold, normal)
- [ ] Thiết lập line-height cho dễ đọc
- [ ] Căn chỉnh text (text-align) cho các phần khác nhau

### **Phần 3: Colors - Màu sắc (6 điểm)**
- [ ] Chọn bảng màu chủ đạo (2-3 màu chính)
- [ ] Thiết lập màu nền (background-color) cho body
- [ ] Thiết lập màu chữ (color) khác nhau cho các phần
- [ ] Sử dụng màu cho liên kết (a) và hover effect

### **Phần 4: CSS Selectors (8 điểm)**
- [ ] Sử dụng element selector (h1, p, etc.)
- [ ] Sử dụng class selector (.class-name)
- [ ] Sử dụng ID selector (#id-name)
- [ ] Sử dụng descendant selector (div p)
- [ ] Sử dụng pseudo-class (:hover, :first-child)

## 📁 Cấu trúc file

```
exercise-04/
├── README.md (file này)
├── index.html (copy từ bài tập 2 hoặc tạo mới)
├── style.css (file CSS chính)
└── starter/
    ├── template.html
    └── template.css
```

## 📝 Template CSS cơ bản

```css
/* CSS Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Import Google Font */
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');

/* General Styles */
body {
    font-family: 'Roboto', sans-serif;
    line-height: 1.6;
    color: #333;
    background-color: #f4f4f4;
}

/* Typography */
h1 {
    /* Thêm styles cho h1 */
}

h2 {
    /* Thêm styles cho h2 */
}

p {
    /* Thêm styles cho p */
}

/* Colors */
.primary-color {
    /* Định nghĩa màu chính */
}

.secondary-color {
    /* Định nghĩa màu phụ */
}

/* Links */
a {
    /* Styles cho liên kết */
}

a:hover {
    /* Hover effect cho liên kết */
}
```

## ✅ Ví dụ CSS cụ thể

### **Typography:**
```css
/* Google Font */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');

body {
    font-family: 'Inter', sans-serif;
    font-size: 16px;
    line-height: 1.6;
}

h1 {
    font-size: 2.5rem;
    font-weight: 700;
    margin-bottom: 1rem;
}

h2 {
    font-size: 2rem;
    font-weight: 600;
    margin-bottom: 0.8rem;
}

p {
    font-size: 1rem;
    margin-bottom: 1rem;
}
```

### **Colors:**
```css
:root {
    --primary-color: #3498db;
    --secondary-color: #2c3e50;
    --accent-color: #e74c3c;
    --background-color: #ecf0f1;
    --text-color: #2c3e50;
}

body {
    background-color: var(--background-color);
    color: var(--text-color);
}

h1, h2 {
    color: var(--primary-color);
}

a {
    color: var(--accent-color);
    text-decoration: none;
}

a:hover {
    color: var(--secondary-color);
    text-decoration: underline;
}
```

### **Selectors:**
```css
/* Element selector */
header {
    background-color: var(--primary-color);
    color: white;
    padding: 2rem 0;
}

/* Class selector */
.highlight {
    background-color: yellow;
    padding: 0.2rem 0.4rem;
}

/* ID selector */
#main-title {
    text-align: center;
    border-bottom: 2px solid var(--accent-color);
}

/* Descendant selector */
header h1 {
    margin: 0;
    text-align: center;
}

/* Pseudo-class */
li:first-child {
    font-weight: bold;
}

table tr:nth-child(even) {
    background-color: #f9f9f9;
}
```

## 🎯 Tiêu chí chấm điểm

| Tiêu chí | Điểm | Mô tả |
|----------|------|--------|
| **Thiết lập CSS** | 3 | File CSS riêng, liên kết đúng, reset cơ bản |
| **Typography** | 8 | Font, size, weight, line-height, alignment |
| **Colors** | 6 | Bảng màu nhất quán, background, text colors |
| **Selectors** | 8 | Sử dụng đa dạng các loại selector |
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
git checkout -b exercise-04-[ten-cua-ban]
```

### Bước 2: Chuẩn bị file
```bash
cd exercises/exercise-04
# Copy HTML từ bài tập 2 hoặc tạo mới
cp ../exercise-02/index.html .
touch style.css
```

### Bước 3: Liên kết CSS
Thêm vào `<head>` của HTML:
```html
<link rel="stylesheet" href="style.css">
```

### Bước 4: Chọn bảng màu
- Sử dụng [Coolors.co](https://coolors.co/) để tạo bảng màu
- Hoặc chọn từ [Material Design Colors](https://materialui.co/colors)

### Bước 5: Chọn font
- Truy cập [Google Fonts](https://fonts.google.com/)
- Chọn 1-2 font phù hợp
- Copy import URL vào CSS

### Bước 6: Viết CSS từng phần
1. CSS Reset và general styles
2. Typography (fonts, sizes)
3. Colors (background, text)
4. Specific selectors

### Bước 7: Test và commit
```bash
git add .
git commit -m "feat: Hoàn thành bài tập 4 - CSS cơ bản"
git push -u origin exercise-04-[ten-cua-ban]
```

## 💡 Tips hữu ích

1. **CSS Variables:** Sử dụng `:root` để định nghĩa màu sắc tái sử dụng
2. **Font pairing:** Chọn tối đa 2 fonts (1 cho heading, 1 cho body)
3. **Color contrast:** Đảm bảo màu chữ và nền có độ tương phản tốt
4. **Naming convention:** Đặt tên class có ý nghĩa (`.header-title`, `.contact-form`)
5. **Browser DevTools:** Sử dụng F12 để test CSS trực tiếp

## 📚 Tài liệu tham khảo

- [MDN CSS Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics)
- [CSS Selectors Reference](https://www.w3schools.com/cssref/css_selectors.asp)
- [Google Fonts](https://fonts.google.com/)
- [Coolors - Color Palette Generator](https://coolors.co/)
- [CSS Color Values](https://www.w3schools.com/css/css_colors.asp)

## ❓ Câu hỏi thường gặp

**Q: Tôi có thể sử dụng CSS framework như Bootstrap không?**
A: Không, bài tập này yêu cầu viết CSS thuần để hiểu cơ bản.

**Q: Có cần responsive design không?**
A: Chưa cần, responsive sẽ học ở bài tập 8.

**Q: Tôi có thể thêm animations không?**
A: Chưa cần, animations sẽ học ở bài tập 9.

**Q: Làm sao biết màu nào đẹp?**
A: Tham khảo các trang như Dribbble, Behance, hoặc dùng color palette generators.

---

**Trước đó:** [Bài tập 3: Tổng hợp HTML](../exercise-03/README.md)
**Tiếp theo:** [Bài tập 5: CSS Box Model](../exercise-05/README.md)

**Deadline:** [Teacher sẽ thông báo] 