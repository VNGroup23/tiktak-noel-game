# Hứng quà Noel · Tiktak Co-working Space

Bản demo mini-game Giáng sinh 2026 cho chuỗi Tiktak Co-working Space. Mỗi lượt 45 giây: khách lái xe trượt tuyết T!KTAK hứng hộp quà và ngôi sao, né cục than. Đạt đủ điểm thì được mở hộp quà nhận ưu đãi dịch vụ của Tiktak.

## Chạy thử

Không cần build: mở trực tiếp `index.html` trên trình duyệt, hoặc chạy:

```bash
python3 -m http.server 8765
# rồi mở http://127.0.0.1:8765
```

Game tối ưu cho điện thoại (dọc). Trên máy tính dùng chuột hoặc phím ← → / A D, phím P để tạm dừng. Thêm `?cs=TT3` vào link để chọn sẵn cơ sở (TT1, TT2, TT3, TT5, TT8), dùng cho mã QR đặt tại từng cơ sở.

## Cơ chế

| Vật phẩm | Hiệu ứng |
|---|---|
| Hộp quà | +10 điểm |
| Ngôi sao | +30 điểm |
| Đồng hồ | +5 giây |
| Cục than | −20 điểm, mất combo |

Hứng liên tiếp 5 món thì điểm nhân 2, liên tiếp 10 món thì nhân 3. Để rơi quà hoặc dính than là mất combo.

**Lượt chơi và quà:** 3 lượt mỗi ngày cho mỗi số điện thoại. Đạt từ 300 điểm trong một lượt thì được chọn 1 trong 3 hộp quà (tối đa 1 hộp mỗi ngày). Quà có mã riêng, lưu trong Ví quà; lễ tân nhập mã để xác nhận đã trao. Top 3 mỗi cơ sở nhận quà tại tiệc Giáng sinh 24/12.

Bộ quà, tỉ lệ trúng và mốc điểm trong demo là số tạm, chưa chốt với vận hành.

## Lưu ý về bản demo

- Dữ liệu (lượt chơi, mã quà, bảng xếp hạng) chỉ lưu trên trình duyệt đang mở (localStorage). Bảng xếp hạng có tên người chơi mẫu.
- Trang lễ tân dùng PIN demo `2412`.
- Bản chạy thật cần máy chủ để lưu dữ liệu chung, chống gian lận điểm và quản lý kho quà.
