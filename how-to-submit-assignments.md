# Hướng dẫn tạo Branch và nộp bài tập

## 📋 Tổng quan quy trình

Trong khóa học này, chúng ta sẽ sử dụng Git để quản lý bài tập theo quy trình sau:

1. **Teacher** đăng bài tập lên nhánh `main`
2. **Member** tạo nhánh mới để làm bài tập
3. **Member** nộp bài qua Pull Request
4. **Teacher** review và feedback

## 🚀 Bước 1: Chuẩn bị môi trường

### 1.1. Clone repository về máy (chỉ làm 1 lần)
```bash
git clone [URL_REPOSITORY]
cd [TEN_FOLDER_PROJECT]
```

### 1.2. Cấu hình thông tin cá nhân (chỉ làm 1 lần)
```bash
git config user.name "Tên của bạn"
git config user.email "email@example.com"
```

## 📚 Bước 2: Lấy bài tập mới từ teacher

### 2.1. Đảm bảo đang ở nhánh main
```bash
git checkout main
```

### 2.2. Cập nhật code mới nhất từ repository
```bash
git pull origin main
```

### 2.3. Kiểm tra bài tập mới
```bash
# Xem danh sách file/folder mới
ls -la

# Đọc hướng dẫn bài tập (thường trong file README hoặc instructions)
cat README.md
```

## 🌿 Bước 3: Tạo nhánh mới cho bài tập

### 3.1. Quy tắc đặt tên nhánh
Sử dụng format: `baitap-[số-bài]-[tên-member]`

**Ví dụ:**
- `baitap-01-nguyenvana`
- `baitap-02-tranthib`
- `baitap-03-lethic`

### 3.2. Tạo và chuyển sang nhánh mới
```bash
# Thay [TEN_NHANH] bằng tên nhánh theo quy tắc trên
git checkout -b [TEN_NHANH]

# Ví dụ:
git checkout -b baitap-01-nguyenvana
```

### 3.3. Kiểm tra nhánh hiện tại
```bash
git branch
# Dấu * sẽ hiển thị nhánh bạn đang làm việc
```

## 💻 Bước 4: Làm bài tập

### 4.1. Đọc kỹ yêu cầu bài tập
- Đọc file hướng dẫn (README.md, instructions.txt, etc.)
- Hiểu rõ yêu cầu và tiêu chí chấm điểm
- Xem ví dụ mẫu (nếu có)

### 4.2. Tạo/chỉnh sửa file theo yêu cầu
```bash
# Tạo file mới
touch index.html style.css script.js

# Hoặc chỉnh sửa file có sẵn
code . # Mở VS Code
```

### 4.3. Kiểm tra tiến độ thường xuyên
```bash
# Xem file nào đã thay đổi
git status

# Xem chi tiết thay đổi
git diff
```

## 💾 Bước 5: Lưu tiến độ (Commit)

### 5.1. Thêm file vào staging area
```bash
# Thêm tất cả file đã thay đổi
git add .

# Hoặc thêm từng file cụ thể
git add index.html
git add style.css
```

### 5.2. Commit với message rõ ràng
```bash
# Format: [Loại] Mô tả ngắn gọn
git commit -m "feat: Hoàn thành HTML cơ bản cho bài tập 1"
git commit -m "style: Thêm CSS cho header và navigation"
git commit -m "fix: Sửa lỗi responsive trên mobile"
```

**Các loại commit phổ biến:**
- `feat`: Thêm tính năng mới
- `fix`: Sửa lỗi
- `style`: Thay đổi giao diện/CSS
- `docs`: Cập nhật tài liệu
- `refactor`: Tái cấu trúc code

### 5.3. Commit thường xuyên
- Commit sau mỗi phần nhỏ hoàn thành
- Không chờ đến khi hoàn thành toàn bộ bài tập
- Giúp dễ dàng quay lại phiên bản trước nếu có lỗi

## 📤 Bước 6: Nộp bài tập

### 6.1. Đẩy nhánh lên repository
```bash
# Lần đầu tiên đẩy nhánh mới
git push -u origin [TEN_NHANH]

# Ví dụ:
git push -u origin baitap-01-nguyenvana

# Các lần sau chỉ cần:
git push
```

### 6.2. Tạo Pull Request trên GitHub/GitLab

1. Truy cập repository trên web
2. Nhấn nút "New Pull Request" hoặc "Create Merge Request"
3. Chọn:
   - **From**: nhánh bài tập của bạn
   - **To**: nhánh `main`
4. Điền thông tin:
   - **Title**: `[Bài tập X] - [Tên member]`
   - **Description**: Mô tả những gì đã làm, khó khăn gặp phải (nếu có)

**Ví dụ Pull Request:**
```
Title: [Bài tập 1] - Nguyễn Văn A

Description:
## Đã hoàn thành:
- ✅ Tạo cấu trúc HTML cơ bản
- ✅ Thiết kế CSS responsive
- ✅ Thêm JavaScript tương tác cơ bản

## Khó khăn gặp phải:
- Gặp khó khăn với CSS Grid layout
- Cần hỗ trợ thêm về JavaScript Event Handling

## Câu hỏi:
- Có cách nào tối ưu hóa CSS tốt hơn không?
```

## 🔄 Bước 7: Xử lý feedback từ teacher

### 7.1. Đọc feedback và yêu cầu chỉnh sửa
- Kiểm tra comment trong Pull Request
- Ghi chú những điểm cần sửa

### 7.2. Thực hiện chỉnh sửa
```bash
# Đảm bảo đang ở đúng nhánh bài tập
git checkout [TEN_NHANH]

# Thực hiện chỉnh sửa theo feedback
# ... chỉnh sửa code ...

# Commit các thay đổi
git add .
git commit -m "fix: Sửa theo feedback của teacher"

# Đẩy lên repository
git push
```

### 7.3. Thông báo đã sửa xong
- Comment trong Pull Request: "Đã sửa theo yêu cầu, mong thầy/cô review lại"

## 🎯 Bước 8: Chuẩn bị cho bài tập tiếp theo

### 8.1. Sau khi bài tập được approve
```bash
# Chuyển về nhánh main
git checkout main

# Cập nhật code mới nhất
git pull origin main

# Xóa nhánh bài tập cũ (tùy chọn)
git branch -d [TEN_NHANH_CU]
```

### 8.2. Sẵn sàng cho bài tập mới
- Lặp lại quy trình từ Bước 2

## ⚠️ Lưu ý quan trọng

### ❌ Những điều KHÔNG nên làm:
- **KHÔNG** làm bài tập trực tiếp trên nhánh `main`
- **KHÔNG** push code chưa hoàn thành lên nhánh `main`
- **KHÔNG** xóa hoặc sửa file bài tập của người khác
- **KHÔNG** copy code từ bạn khác mà không hiểu

### ✅ Những điều nên làm:
- **LUÔN** tạo nhánh mới cho mỗi bài tập
- **LUÔN** commit thường xuyên với message rõ ràng
- **LUÔN** kiểm tra code trước khi push
- **LUÔN** đọc kỹ feedback và thực hiện chỉnh sửa

## 🆘 Xử lý tình huống thường gặp

### Tình huống 1: Quên tạo nhánh mới, đã làm bài trên main
```bash
# Tạo nhánh mới từ main hiện tại
git checkout -b [TEN_NHANH]

# Reset main về trạng thái ban đầu
git checkout main
git reset --hard origin/main

# Quay lại nhánh bài tập để tiếp tục
git checkout [TEN_NHANH]
```

### Tình huống 2: Cần cập nhật code mới từ main vào nhánh bài tập
```bash
# Ở nhánh bài tập
git checkout [TEN_NHANH]

# Merge code mới từ main
git merge main

# Hoặc rebase (nâng cao)
git rebase main
```

### Tình huống 3: Làm nhầm nhánh
```bash
# Xem đang ở nhánh nào
git branch

# Chuyển sang nhánh đúng
git checkout [TEN_NHANH_DUNG]
```

### Tình huống 4: Muốn hoàn tác commit cuối cùng
```bash
# Hoàn tác commit nhưng giữ lại thay đổi
git reset --soft HEAD~1

# Hoàn tác commit và xóa luôn thay đổi (cẩn thận!)
git reset --hard HEAD~1
```

**Chúc bác Ngân học tập hiệu quả! 🎓** 