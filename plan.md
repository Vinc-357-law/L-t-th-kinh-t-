# Game "Lật thẻ thuật ngữ kinh tế": Kế hoạch và nhật ký

Game ôn thuật ngữ Kinh tế vi mô (theo giáo trình *Nguyên lý Kinh tế học* của N. Gregory Mankiw) cho sinh viên năm nhất, dùng trong 5 phút đầu giờ.

**Quy trình làm việc:** nhóm nêu ý tưởng → AI trình bày hướng đi → nhóm duyệt → AI làm → AI ghi báo cáo vào file này và đẩy lên GitHub.

## Tiến độ

| # | Giai đoạn | Trạng thái |
|---|---|---|
| 1 | Lập kế hoạch | ✅ Xong (14/11/2026) |
| 2 | Phân tích: chốt yêu cầu | 🟡 Đã chốt 11 điểm, còn chờ duyệt 8 thuật ngữ và 2 điểm phát sinh |
| 3 | Thiết kế giao diện | 🟡 Đã gửi khung giao diện, chờ duyệt |
| 4 | Viết code (v1.0) | ⬜ Chưa làm |
| 5 | Chạy thử và sửa lỗi | ⬜ Chưa làm |
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

### Điểm phát sinh, chờ nhóm xác nhận

- **A. Nhập tên và ràng buộc "không thu thập tên":** đề xuất dùng *biệt danh* (không bắt buộc tên thật). Biệt danh chỉ lưu trong trình duyệt của máy đang chơi (localStorage), không gửi đi đâu.
- **B. Cách xếp hạng:** đề xuất chỉ xếp hạng ván ghép đủ 8 cặp trước khi hết giờ. Ít lượt hơn xếp trên; bằng lượt thì ván nhanh hơn xếp trên. Lưu 10 ván tốt nhất trên máy.

## Giải pháp kỹ thuật

- Một file `index.html`, viết bằng HTML, CSS và JavaScript thuần. Không dùng thư viện, CDN hay font tải từ mạng, nên chạy được khi offline.
- Dữ liệu 8 cặp thuật ngữ đặt ở đầu file để dễ thay.
- Xáo thẻ bằng Fisher–Yates. Khi hai thẻ sai đang chờ úp lại thì khóa bàn. Đồng hồ dừng khi ghép xong hoặc khi hết giờ.

## Nhật ký phiên bản

| Phiên bản | Ngày | Thay đổi / lỗi đã sửa | Ai phát hiện |
|---|---|---|---|
| (chưa có) | | | |

## Tài liệu trong repo

- `Huong_di_game_lat_the.docx`: bản hướng đi gửi nhóm
- `plan.md`: kế hoạch và nhật ký (file này)
