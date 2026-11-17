# VNR202 – Ôn thi Lịch sử Đảng Cộng sản Việt Nam

Bộ tài liệu và công cụ ôn thi trắc nghiệm toàn diện cho học phần **VNR202 (Lịch sử Đảng Cộng sản Việt Nam)** với ngân hàng **415 câu hỏi trắc nghiệm**, được trích xuất và chuẩn hóa từ đề gốc, tách riêng tệp dữ liệu độc lập, kèm 2 web app ôn luyện offline và bài mẹo học thuộc bao quát 100% đề thi.

---

## 📁 Cấu trúc thư mục dự án

```text
D:\Documents\Book\Semester_9\VNR\
├── .nojekyll                   # Cấu hình hỗ trợ triển khai GitHub Pages
├── index.html                  # Trang chủ trung tâm điều hướng
├── meo-hoc-thuoc.html          # Web bí kíp mẹo học thuộc trực quan có tìm kiếm
├── VNR202.pdf                  # Đề gốc PDF 118 trang (415 câu trắc nghiệm)
├── VNR202_meo_hoc_thuoc.md     # Bản Markdown chi tiết của bí kíp mẹo học thuộc
├── VNR202_thi_thu.html         # Web app thi thử (có bấm giờ, chấm điểm, xem câu sai)
├── VNR202_flashcard.html       # Web app luyện chọn đáp án SM-2 (Anki, ôn gấp 2-4 ngày)
├── README.md                   # Hướng dẫn sử dụng dự án
└── data\
    ├── questions.js            # Dữ liệu 415 câu hỏi (JS load offline không bị lỗi CORS)
    └── questions.json          # Dữ liệu chuẩn JSON thuần dùng cho API/lập trình
```

---

## 🚀 Cách sử dụng

**Chạy trực tiếp 100% offline**: Nhấp đúp chuột mở trực tiếp bất kỳ tệp `.html` nào bằng trình duyệt (Chrome, Edge, Cốc Cốc, Safari, Firefox). Không cần kết nối mạng, không cần cài đặt nodejs hay máy chủ web.

### 1. 📝 Web Thi thử (`VNR202_thi_thu.html`)
- **Tùy chọn linh hoạt:** Chọn số lượng câu (20, 40 câu như thi thật, 60, 100 hoặc toàn bộ 415 câu).
- **Lọc theo chủ đề:** Chọn ôn theo từng giai đoạn lịch sử hoặc theo dạng câu hỏi (Con số, Thời gian, Nhân vật, Đại hội/Hội nghị TW).
- **Hẹn giờ:** Tùy chọn 15s, 30s, 60s mỗi câu hoặc tắt hẹn giờ.
- **Chế độ làm bài:**
  - *Xem kết quả ngay*: Bấm chọn là biết ngay đúng/sai, hiện đáp án chuẩn và ghi chú giải thích.
  - *Nộp bài xong mới chấm*: Làm như thi thật trong phòng thi, hết giờ/nộp bài sẽ chấm điểm thang 10, hiển thị tỷ lệ % và danh sách xem lại câu sai.
- **Ôn lại câu sai:** Kết quả các câu làm sai được tự động lưu trong trình duyệt; có nút riêng để luyện lại duy nhất các câu làm sai ở lượt trước.

### 2. ✅ Web Luyện chọn đáp án SM-2 (`VNR202_flashcard.html`)
- **Thuật toán Spaced Repetition (SM-2 kiểu Anki):** Mỗi câu bạn chọn đáp án rồi bấm **✔️ Kiểm tra**. Sau đó tự đánh giá mức độ nhớ theo 4 nút:
  - **Lại** (quên): Lặp lại sau 10 phút.
  - **Khó**: Khoảng cách lặp lại × 1.2.
  - **Được**: Khoảng cách lặp lại × hệ số dễ (Ease).
  - **Dễ**: Tốt nghiệp, khoảng cách tăng vọt.
- **Cảnh báo câu nhiều đáp án:** Toàn bộ 415 câu có 3 câu phải chọn 2 đáp án (Q20, Q36, Q116). App sẽ hiện dải banner màu cam **⚠️ CÂU NÀY CHỌN NHIỀU ĐÁP ÁN** để bạn không bị tick thiếu.
- **Chế độ ôn cấp tốc (Trong ⚙️ Cài đặt):**
  - **⏳ Ôn gấp 4 ngày:** Tự động tăng lượng câu mới lên ~120 câu/ngày, nén khoảng cách ôn tập không vượt quá ngày thi.
  - **🔥 Ôn gấp 2 ngày:** Nén cường độ cao ~220 câu/ngày cho bạn nào cần "chữa cháy" sát giờ thi.
- **Tab 📋 Danh sách:** Xem toàn bộ câu hỏi và đáp án cùng lúc, có thanh tìm kiếm nhanh, nút ẩn/hiện đáp án.
- **Sao lưu tiến độ:** Hỗ trợ xuất và nhập tiến độ ôn tập ra file JSON.

### 3. 💡 Bí kíp mẹo học thuộc (`meo-hoc-thuoc.html` & `VNR202_meo_hoc_thuoc.md`)
- **Nhóm 1 - Con số & Bộ số ma thuật:** Bộ 2 (khai thác thuộc địa, nhiệm vụ chiến lược, kế hoạch giải phóng), Bộ 3 (văn kiện thành lập Đảng, nhiệm vụ cấp bách 3/9/1945, đặc điểm Đại hội IV, 3 đợt Điện Biên Phủ, 3 đột phá chiến lược), Bộ 4 (4 chiến lược của Mỹ), Bộ 6 (6 đặc trưng Cương lĩnh 1991), Bộ 8 (Cương lĩnh 2011), Bộ 36 (36 nước công nhận KTTT năm 2012).
- **Thần chú mục tiêu Đại hội XIII:** *"25 Thấp, 30 Cao, 45 Phát triển"*.
- **Nhóm 2 - Dòng thời gian lịch sử chuẩn xác:** Chuỗi thời gian liên hoàn từ 1858 đến 2021.
- **Nhóm 3 - Bảng Tổng Bí thư & Lãnh tụ:** Trần Phú, Lê Hồng Phong, Nguyễn Văn Cừ, Trường Chinh, Lê Duẩn, Nguyễn Văn Linh, Lê Khả Phiêu, Nông Đức Mạnh, Nguyễn Phú Trọng.
- **Nhóm 4 - Bảng từ khóa 13 kỳ Đại hội Đảng:** Thấy từ khóa cốt lõi là khoanh trúng ngay Đại hội.
- **Nhóm 5 - Các Hội nghị Trung ương & Quyết sách:** HNTW 6 (Mở đầu chuyển hướng), HNTW 8 (Hoàn chỉnh chuyển hướng), HNTW 15 (Bạo lực cách mạng miền Nam), HNTW 6 khóa IV (Bung ra), Khoán 100, Khoán 10, HNTW 5 khóa VIII (Tuyên ngôn văn hóa).
- **Nhóm 6 - Bảng phân biệt 4 chiến lược chiến tranh của Mỹ:** Đơn phương, Đặc biệt, Cục bộ, Việt Nam hóa chiến tranh.
- **Nhóm 7 - Các bẫy tử thần:** 3 câu nhiều đáp án, 6 câu phủ định ("Không phải / Không đúng"), 6 cặp câu trùng lặp nguyên văn (học 1 được 2).

---

## 📌 Bảng thống kê quan trọng trước khi vào phòng thi

| Chỉ số | Kết quả | Ý nghĩa & Chiến thuật phòng thi |
|---|---|---|
| **Tổng số câu** | **415 câu** | Ngân hàng câu hỏi trọn vẹn của môn học |
| **Câu 1 đáp án** | **412 câu** | Chiếm 99.3% đề |
| **Câu chọn NHIỀU ĐÁP ÁN** | **3 câu** (Q20: AD, Q36: AB, Q116: BC) | **Bắt buộc chọn đủ 2 đáp án**; tick thiếu là 0 điểm |
| **Tỷ lệ đáp án A** | **152 câu (~36.9%)** | Khi bí hoặc hết giờ, ngả về **A** cho xác suất trúng cao nhất |
| **Câu có "Tất cả các đáp án trên"** | **2 câu** (Đúng 1/2 câu = 50%) | **Không** mặc định chọn khi gặp cụm từ này |
| **Câu phủ định ("Không phải / Không đúng")**| **6 câu** (Q29, Q32, Q85, Q357, Q390, Q411) | Cần đọc kỹ yêu cầu để tìm câu sai |
| **Cặp câu trùng lặp nguyên văn** | **6 cặp câu** | [139-170], [157-189], [168-179], [214-226], [288-289], [373-374] |

---

## ⌨️ Bảng phím tắt tiện lợi

- **1 – 4** hoặc **A – D**: Chọn phương án tương ứng.
- **Space / Enter**: Xác nhận đáp án / Sang câu tiếp theo.
- **1, 2, 3, 4** (Sau khi kiểm tra ở Flashcard): Đánh giá tương ứng **Lại, Khó, Được, Dễ**.
- **Z**: Hoàn tác thẻ vừa đánh giá.
- **← / →**: Chuyển câu trước / câu sau.

---

Chúc các bạn ôn thi hiệu quả và đạt điểm A+ môn Lịch sử Đảng Cộng sản Việt Nam (VNR202)!
