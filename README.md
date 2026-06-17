# Gia đình 5 biết — Website tuyên truyền

Website tĩnh giới thiệu mô hình **"Gia đình 5 biết"** — chương trình trang bị 5 nhóm kỹ năng số thiết yếu cho gia đình:

1. **Biết thanh toán số** — Thanh toán không tiền mặt an toàn
2. **Biết quản lý số** — Tổ chức cuộc sống bằng công cụ số
3. **Biết hỗ trợ số** — Đồng hành cùng ông bà, cha mẹ
4. **Biết bảo vệ số** — Nhận diện và phòng tránh lừa đảo
5. **Biết sử dụng AI có trách nhiệm**

Mô hình phối hợp giữa BCH Đoàn Trường ĐH Công nghệ Thông tin, ĐHQG-HCM và Hội LHPN phường Thủ Dầu Một (Mùa Hè Xanh 2026).

## Cấu trúc

```
.
├── index.html              # Trang chủ
├── thanh-toan-so.html
├── quan-ly-so.html
├── ho-tro-so.html
├── bao-ve-so.html
├── ai-co-trach-nhiem.html
├── css/style.css
├── js/main.js
├── netlify.toml            # Cấu hình Netlify
└── README.md
```

## Chạy local

Đây là website tĩnh thuần HTML/CSS/JS — không cần build:

```bash
# Mở trực tiếp
open index.html

# Hoặc chạy local server (khuyến nghị)
python3 -m http.server 8000
# truy cập http://localhost:8000
```

## Deploy lên Netlify qua GitHub

### Bước 1: Đẩy code lên GitHub

```bash
cd "Website_GD5B"
git init
git add .
git commit -m "Initial commit — Gia dinh 5 biet website"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

### Bước 2: Kết nối Netlify

1. Truy cập [app.netlify.com](https://app.netlify.com) → **Add new site** → **Import from Git**.
2. Chọn GitHub, cấp quyền và chọn repository vừa tạo.
3. **Build settings** — Netlify đọc cấu hình từ `netlify.toml`:
   - Build command: *(để trống)*
   - Publish directory: `.`
4. Bấm **Deploy site**.

Netlify sẽ tự deploy lại mỗi khi bạn `git push` lên branch `main`.

### Tên miền tuỳ chỉnh

Trong Netlify dashboard: **Domain settings** → **Add custom domain** → trỏ DNS theo hướng dẫn.

## Tuỳ chỉnh nội dung

- **Đổi video YouTube**: tìm `youtube.com/embed/` trong các file `.html` và thay ID video.
- **Đổi link chatbot**: thay URL `notebooklm.google.com/notebook/...` trong tất cả file `.html` (gợi ý dùng find/replace).
- **Đổi màu chủ đạo**: chỉnh các biến CSS trong `css/style.css` (block `:root`).

## Công nghệ

- HTML5 + CSS3 (Custom Properties, Grid, Flexbox)
- JavaScript thuần (IntersectionObserver cho hiệu ứng scroll)
- Font: Inter (Google Fonts)
- Không phụ thuộc framework — load nhanh, dễ bảo trì

---

© 2026 · UIT × Hội LHPN phường Thủ Dầu Một
