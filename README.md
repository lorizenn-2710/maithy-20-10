# Thiệp 20/10 Tương Tác 3D — Dành Tặng Mai Thy (12A1) 💐✨

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?style=for-the-badge&logo=github)](https://lorizenn-2710.github.io/maithy-20-10/)
[![Architecture](https://img.shields.io/badge/Architecture-Single--File%20Standalone-blue?style=for-the-badge&logo=html5)](https://lorizenn-2710.github.io/maithy-20-10/)
[![Audio](https://img.shields.io/badge/Audio%20Engine-WebAudio%20API%20%2B%20Soulloom-ff69b4?style=for-the-badge&logo=audio)](https://lorizenn-2710.github.io/maithy-20-10/)
[![Graphics](https://img.shields.io/badge/Render-HiDPI%20Canvas%202D%2F3D-gold?style=for-the-badge)](https://lorizenn-2710.github.io/maithy-20-10/)

Dự án trang thiệp điện tử tương tác 3D cao cấp chào mừng **Ngày Phụ Nữ Việt Nam 20/10**, được thiết kế công phu và trang trọng dành riêng cho **Mai Thy – Cô gái đặc biệt của tập thể 12A1**.

🔗 **Trải nghiệm trực tiếp:** [https://lorizenn-2710.github.io/maithy-20-10/](https://lorizenn-2710.github.io/maithy-20-10/)

---

## 🌟 Triết Lý Thiết Kế & Kiến Trúc Kỹ Thuật

Trang web được thiết kế theo kiến trúc **Single-File Zero-Dependency** (Toàn bộ mã nguồn, dữ liệu ảnh, âm thanh, hiệu ứng hạt và giao diện đều được đóng gói độc lập trong đúng một tệp `index.html` duy nhất):

- **Triệt tiêu 100% lỗi 404 & CORS**: Không tải tệp tĩnh rời (`assets/`). Dữ liệu ảnh kỷ niệm (10 tấm Polaroid) và bài hát gốc **Soulloom** đều được mã hóa Base64 trực tiếp vào mã nguồn.
- **Hoạt động đa môi trường**: Mở trực tiếp ngoại tuyến qua giao thức `file://` trên máy tính hoặc chạy trực tiếp trên máy chủ **GitHub Pages** đều ổn định mượt mà.
- **Tối ưu hóa phần cứng & Tần số quét cao (60–120 FPS)**: Sử dụng hệ thống đa tầng Canvas (Sky Parallax Canvas, Bouquet Canvas, Keepsake Preview Canvas) với thuật toán tính toán ma trận 3D hình học không gian tối ưu cho cả GPU di động lẫn máy tính để bàn.
- **Biểu tượng Vector SVG Thuần Khiết**: Loại bỏ hoàn toàn emoji thô trên thanh công cụ điều khiển, thay thế bằng bộ icon vector SVG thanh lịch phủ nhũ vàng hoàng gia (`pm-foil`).

---

## 🎨 Tính Năng Trọng Tâm

### 1. Bó Hoa Hoàng Gia & Đàn Hạc Tương Tác (Flower Touch Harp)
- Bó hoa Tulip nở rộ, đóa Mẫu đơn phồn hoa và Hồng phấn được kết tinh từ hàng nghìn nét vẽ vector procedural sống động.
- **Flower Touch Harp**: Khi chạm hoặc lướt ngón tay qua từng bông hoa, hệ thống sẽ phát ra âm hưởng gảy đàn hạc ngân nga kèm những đốm sáng lung linh và hiển thị lời chúc gửi riêng cho Mai Thy (*"Rạng rỡ tuổi 18 nhé Mai Thy! 🌷"*, *"Đỗ Nguyện Vọng 1 thật cao nha! 🎓"*, v.v.).

### 2. Vòng Ảnh Polaroid 3D Đa Chiều (3D Bouquet Orbit)
- 10 bức ảnh kỷ niệm thanh xuân chất lượng cao quay quanh bó hoa với hiệu ứng chiều sâu phối cảnh 3D (Z-Index layering & perspective projection).
- **Mặc định: Sóng Ngân Hà (Harmonic 3D Galaxy Wave)** — các bức ảnh tự động nhấp nhô lượn sóng hình sin 3D nhẹ nhàng quanh tán hoa.
- **3 Kiểu bố cục phụ linh hoạt**:
  * *Tiêu Điểm Giữa*: Bức ảnh chính diện phóng to nổi bật nhất.
  * *Quỹ Đạo Vòng Tròn 3D*: Vòng tròn vệ tinh phong cách sao Thổ ôm trọn bó hoa.
  * *Cánh Cung 3D*: Xòe hình bán nguyệt ôm sát mặt trước của hoa.
- **Chức năng bổ trợ**: Hỗ trợ xoay tự do (kéo vuốt cảm ứng), tự động xoay (`AutoSpin`), bộ lọc hiển thị (Xem tất cả 10 ảnh hoặc lọc riêng 4 ảnh kỷ niệm của Mai Thy), mở xem ảnh phóng to chi tiết (**Lightbox**).

### 3. Hệ Thống Âm Thanh Studio & Bài Hát "Soulloom"
- **Bản thu âm gốc Soulloom**: Tích hợp chuỗi âm thanh Base64 nguyên bản, chất âm trong trẻo chuẩn phòng thu.
- **Dải sóng nhạc & Lời chúc thanh xuân (`whisperSpectrumHud`)**:
  * 6 thanh phổ âm thanh (Live Spectrum Bars) chuyển động nhịp nhàng theo biên độ bài hát.
  * Tự động luân chuyển 8 lời nhắn yêu thương, trân trọng từ tập thể 12A1 gửi đến Mai Thy.
- **Cơ chế chống ngắt tiếng thông minh**: Bộ điều khiển âm thanh tự động đánh thức luồng `AudioContext`, khử triệt để tình trạng mất nhạc khi chuyển đổi công tắc Bật/Tắt liên tục.
- **Vòng lặp vô tận (Infinite Loop)**: Tự động tiếp tục phát lại bài hát khi hết thời lượng mà không bị gián đoạn hay ngắt quãng.
- **Mặc định Tắt Beat phụ**: Đảm bảo người xem thưởng thức trọn vẹn giai điệu gốc mà không bị tạp âm trống điện tử chèn đè.

### 4. Studio Hiệu Ứng Hoàng Gia & Chòm Sao Mai Thy (Phím tắt `E`)
- **Chòm sao Mai Thy (Constellation Sky Weaver)**: Vẽ chòm sao chữ cái mang tên Mai Thy nối kết bởi các vì tinh tú lấp lánh trên nền trời đêm.
- **Vòng hào quang hoa (Royal Halo)**: Hiệu ứng ánh sáng huyền ảo tỏa sáng từ tâm bó hoa.
- **Chế độ mật độ hiệu ứng**: Tùy chỉnh 3 mức độ hạt (`eco` cho máy yếu, `balanced` cân bằng mượt mà, `royal` lộng lẫy tối đa).

### 5. Bộ Tạo Thiệp Kỷ Niệm Độ Nét Cao (HD Keepsake Card Generator)
- Công cụ cho phép Mai Thy cá nhân hóa và xuất bức ảnh thiệp chúc mừng 20/10 độ phân giải cao ngay trên trình duyệt.
- Tùy chọn 3 phong cách nghệ thuật: **Hoàng Gia**, **Cực Quang**, và **Cổ Điển**.
- Chạm nút **"Lưu Thiệp Về Máy"** để tải ngay tệp ảnh kỷ niệm PNG sắc nét về điện thoại hoặc máy tính.

### 6. Bức Thư Cổ Điển & Tương Tác Sân Khấu
- Bức thư tay trang trọng gửi Mai Thy với hiệu ứng gõ máy chữ thời gian thực (Typewriter).
- Thẻ thơ chữ lật nghệ thuật (Acrostic Flip Cards) đúc kết những nét đẹp dịu dàng của người con gái 12A1.
- Thả đèn trời ước nguyện (Sky Lanterns) và bắn pháo hoa trái tim rực rỡ chào mừng ngày 20/10.

---

## ⌨️ Bảng Phím Tắt Điều Khiển (Keyboard Shortcuts)

Dành cho người xem trải nghiệm trên máy tính để bàn / laptop:

| Phím Tắt | Chức Năng |
| :--- | :--- |
| `Space` / `Enter` | Mở thiệp (ở màn hình giữ) hoặc Thả đèn trời ước nguyện |
| `E` / `e` | Mở / Đóng Studio Hiệu Ứng Hoàng Gia & Tạo Thiệp Kỷ Niệm |
| `M` / `m` | Bật / Tắt nhạc nền (Soulloom) |
| `V` / `v` | Điều chỉnh âm lượng nhạc (0% → 35% → 70% → 100%) |
| `T` / `t` | Đổi phong cách bầu trời (Cực Quang, Ngân Hà, Dạ Yến, v.v.) |
| `O` / `o` | Bật / Tắt chế độ Vòng ảnh 3D quanh bó hoa |
| `1` - `4` | Chuyển trực tiếp 4 kiểu quỹ đạo (Tiêu điểm, Vòng tròn, Cánh cung, Sóng Ngân Hà) |
| `F` / `f` | Lọc hiển thị giữa "Tất cả ảnh (10)" và "Ảnh của Mai Thy (4)" |
| `P` / `p` | Bật / Tắt chế độ tự động xoay ảnh (AutoSpin) |
| `←` / `→` | Xoay bước sang ảnh trước / ảnh tiếp theo |
| `Esc` | Đóng thư tay / Đóng Lightbox phóng to ảnh / Thoát Studio |

---

## 🚀 Hướng Dẫn Cài Đặt & Triển Khai

### 1. Chạy cục bộ trên máy tính
Không cần cài đặt Node.js hay web server phức tạp:
1. Tải về kho mã nguồn:
   ```bash
   git clone https://github.com/lorizenn-2710/maithy-20-10.git
   ```
2. Nhấp đúp chuột vào tệp `index.html` để mở trực tiếp trên Google Chrome, Apple Safari, Microsoft Edge hoặc Mozilla Firefox.

### 2. Triển khai lên GitHub Pages
1. Đẩy mã nguồn lên nhánh `main` của repository:
   ```bash
   git add index.html README.md
   git commit -m "feat: publish interactive 20/10 keepsake site"
   git push origin main
   ```
2. Vào **Settings** của repository trên GitHub ➔ Chọn mục **Pages**.
3. Tại phần **Branch**, chọn nhánh `main` và thư mục `/ (root)` ➔ Bấm **Save**.
4. Trang web sẽ trực tiếp phát hành tại địa chỉ: `https://<your-username>.github.io/<repo-name>/`.

---

## 📂 Cấu Trúc Kho Lưu Trữ

```text
lorizenn-2710/maithy-20-10/
├── index.html        # Tệp duy nhất chứa 100% mã nguồn, style, scripts, âm thanh & ảnh Base64
└── README.md         # Tài liệu thuyết minh kiến trúc kỹ thuật và hướng dẫn sử dụng
```

---

## 💖 Lời Chúc Gửi Mai Thy

> *"Chúc Mai Thy một ngày 20/10 thật nhiều niềm vui, luôn rạng rỡ, bình an và vững tin bước tới ước mơ tuổi 18 cùng Nguyện Vọng 1 phía trước!"*  
> — **Tập thể 12A1 gửi tặng Mai Thy** 🌷✨
