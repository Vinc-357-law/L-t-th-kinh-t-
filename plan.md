# Game "Lật thẻ thuật ngữ kinh tế": Kế hoạch và nhật ký

Game ôn thuật ngữ Kinh tế vi mô (theo giáo trình *Nguyên lý Kinh tế học* của N. Gregory Mankiw) cho sinh viên năm nhất, dùng trong 5 phút đầu giờ.

**Quy trình làm việc:** nhóm nêu ý tưởng → AI trình bày hướng đi → nhóm duyệt → AI làm → AI ghi báo cáo vào file này và đẩy lên GitHub.

## Tiến độ

| # | Giai đoạn | Trạng thái |
|---|---|---|
| 1 | Lập kế hoạch | ✅ Xong (14/11/2026) |
| 2 | Phân tích: chốt yêu cầu | ✅ Xong, đã duyệt 8 thuật ngữ và 2 điểm phát sinh (nhóm còn dò lại định nghĩa với sách) |
| 3 | Thiết kế giao diện | ✅ Đã duyệt; bản Word `Thiet_ke_giao_dien.docx` gửi nhóm góp ý |
| 4 | Viết code (v1.0) | ✅ Xong (14/11/2026): `index.html`, link chia sẻ https://claude.ai/artifact/PhhJxuAJgr97w6EUCL1jvm |
| 5 | Chạy thử và sửa lỗi | 🟡 Đang chờ nhóm chơi thử và góp ý |
| 6 | Hoàn thiện tài liệu | ⬜ Chưa làm |

## Yêu cầu đã chốt (giai đoạn 2)

| # | Câu hỏi | Quyết định của nhóm |
|---|---|---|
| 1 | Môn học | Kinh tế vi mô, theo giáo trình Mankiw |
| 2 | Cách tính lượt | Mỗi lần lật 2 thẻ tính 1 lượt, kể cả đúng hay sai |
| 3 | Đồng hồ | Đếm ngược 5 phút |
| 4 | Thời gian thẻ sai còn ngửa | 1 giây |
| 5 | Màn chúc mừng | Chỉ hiện số lượt và thời gian |
| 6 | Kỷ lục | Nhập tên nhân vật lúc bắt đầu để tính điểm (xem điểm phát sinh A) |
| 7 | Âm thanh | Không có |
| 8 | Thiết bị | Laptop và điện thoại |
| 9 | Ngôn ngữ | Tiếng Việt |
| 10 | Hình thức nộp | File HTML và link trang web chia sẻ |
| 11 | Repo | https://github.com/Vinc-357-law/L-t-th-kinh-t- |

### Điểm phát sinh (đã duyệt)

- **A. Nhập tên và ràng buộc "không thu thập tên":** dùng *biệt danh*, không bắt buộc tên thật. Biệt danh chỉ lưu trong trình duyệt của máy đang chơi (localStorage), không gửi đi đâu.
- **B. Cách xếp hạng:** chỉ xếp hạng ván ghép đủ 8 cặp trước khi hết giờ. Ít lượt hơn xếp trên; bằng lượt thì ván nhanh hơn xếp trên. Lưu 10 ván tốt nhất trên máy.

### 8 thuật ngữ (đã duyệt)

| # | Thuật ngữ | Định nghĩa |
|---|---|---|
| 1 | Chi phí cơ hội | Thứ bạn phải từ bỏ để có được một thứ khác |
| 2 | Lợi thế so sánh | Khả năng sản xuất một hàng hóa với chi phí cơ hội thấp hơn người khác |
| 3 | Quy luật cầu | Khi các yếu tố khác không đổi, giá hàng hóa tăng thì lượng cầu giảm |
| 4 | Trạng thái cân bằng | Tình huống giá đạt mức mà lượng cung bằng lượng cầu |
| 5 | Độ co giãn của cầu theo giá | Mức độ phản ứng của lượng cầu khi giá hàng hóa thay đổi |
| 6 | Thặng dư tiêu dùng | Mức sẵn lòng chi trả của người mua trừ đi số tiền họ thực trả |
| 7 | Ngoại tác | Tác động của hành động một người lên phúc lợi của người ngoài cuộc |
| 8 | Hàng hóa công cộng | Hàng hóa không có tính loại trừ và không có tính cạnh tranh trong tiêu dùng |

## Giải pháp kỹ thuật

- Một file `index.html`, viết bằng HTML, CSS và JavaScript thuần. Không dùng thư viện, CDN hay font tải từ mạng, nên chạy được khi offline.
- Dữ liệu 8 cặp thuật ngữ đặt ở đầu file để dễ thay.
- Xáo thẻ bằng Fisher–Yates. Khi hai thẻ sai đang chờ úp lại thì khóa bàn. Đồng hồ dừng khi ghép xong hoặc khi hết giờ.

## Nhật ký phiên bản

| Phiên bản | Ngày | Thay đổi / lỗi đã sửa | Ai phát hiện |
|---|---|---|---|
| 1.0 | 14/11/2026 | Bản đầu tiên: màn bắt đầu (biệt danh, cách chơi, bảng xếp hạng), lưới 4×4 trên laptop và 2 cột trên điện thoại, đếm ngược 5 phút, màn kết quả khi thắng và khi hết giờ, bảng xếp hạng top 10 trên máy | — |

### Kiểm tra trên bản 1.0

- Cú pháp JavaScript: không lỗi (`node --check`).
- Không có đường dẫn `http://` hay `https://` nào trong `index.html`, nên game không gọi ra Internet.
- Đã xử lý trong code: khóa bàn khi 2 thẻ sai đang chờ úp lại; bấm lại thẻ đang ngửa hoặc thẻ đã ghép thì bỏ qua; Chơi lại hủy các bộ hẹn giờ của ván cũ; đồng hồ tính theo giờ thực nên không lệch khi chuyển tab.
- Chưa chạy thử trên trình duyệt thật. Nhóm chạy 8 tình huống trong phần 4 của `Huong_di_game_lat_the.docx` và báo lỗi theo mẫu.

## Tài liệu trong repo

- `index.html`: game (mở bằng trình duyệt là chơi)
- `Huong_di_game_lat_the.docx`: bản hướng đi gửi nhóm
- `Thiet_ke_giao_dien.docx`: thiết kế giao diện và đối chiếu đề bài, gửi nhóm góp ý
- `plan.md`: kế hoạch và nhật ký (file này)
