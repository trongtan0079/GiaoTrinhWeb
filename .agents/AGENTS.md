# Quy tắc Agent cho Dự án Đại Giáo Trình Web Frontend

## ⛔ QUY TẮC BẢO TOÀN NỘI DUNG (MỨC ƯU TIÊN CAO NHẤT)

1. **TUYỆT ĐỐI KHÔNG được xóa, ghi đè, hoặc viết lại toàn bộ nội dung** bất kỳ file `.tex` nào.
2. **Chỉ được sửa từng đoạn cụ thể** bằng `replace_file_content` hoặc `multi_replace_file_content`.
3. **Trước khi chỉnh sửa**, PHẢI đọc (`view_file`) nội dung hiện tại để hiểu rõ cấu trúc.
4. **Sau mỗi chỉnh sửa**, PHẢI biên dịch XeLaTeX → commit → push lên GitHub ngay.
5. **Trước mỗi phiên chỉnh sửa lớn**, tạo tag backup: `git tag -a backup-YYYY-MM-DD-safe`.

## Các file quan trọng nhất (CẤM overwrite)

- `ch03_semantic_html5.tex` (~511KB, 7245 dòng)
- `ch06_css_foundations.tex` (~447KB, 7175 dòng)
- `ch04_forms_accessibility.tex` (~238KB, 3149 dòng)
- `ch01_web_architecture.tex` (~91KB, 1207 dòng)
- `main.tex` (file gốc cấu trúc giáo trình)

## Quy trình chỉnh sửa bắt buộc

```
1. view_file → Đọc đầy đủ vùng nội dung liên quan
2. Xác định chính xác StartLine/EndLine cần sửa
3. replace_file_content (KHÔNG dùng write_to_file Overwrite trên file lớn)
4. xelatex -interaction=nonstopmode main.tex (2 lượt)
5. git add + git commit + git push origin main
```

## Tham khảo

- Đọc `QUY_TẮC_THIẾT_KẾ.MD` để hiểu quy cách format LaTeX.
- Giáo trình hiện tại: **614 trang**, 24 file `.tex`.
