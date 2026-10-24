# DESIGN.md — Lookbook Vải Thô

Thương hiệu thời trang linen Vải Thô — trang lookbook visual-first: ảnh là nội dung chính,
bố cục ảnh lớn, khoảng trắng rộng. Mọi quyết định thiết kế dưới đây là bắt buộc cho bản dựng;
Dev và QA đối chiếu đúng các thông số này, không dùng mô tả chung chung thay thế.

## 1. Bảng màu

| Mã hex | Vai trò |
| --- | --- |
| `#F7F3EC` | Nền chính toàn trang — trắng ngà, tạo cảm giác vải linen thô, ấm và sáng |
| `#22201D` | Chữ chính — tiêu đề, nội dung, giá, điều hướng |
| `#6B7250` | Màu nhấn — xanh olive: nút bấm chính, link, giá khuyến mãi, đường gạch dưới tiêu đề mục |
| `#FFFFFF` | Nền thẻ sản phẩm / khung ảnh nổi trên nền chính (chỉ dùng cho thẻ, không thay nền trang) |
| `#E7DFD0` | Đường kẻ chia mục, viền ảnh, nền khối phụ (footer, thanh lọc nhẹ) |
| `#8A8D7A` | Chữ phụ — ghi chú, mô tả ngắn, placeholder (không dùng cho chữ chính) |

Quy tắc: nền trang luôn `#F7F3EC`, không dùng nền tối; màu nhấn `#6B7250` chỉ chiếm
dưới 10% diện tích một màn hình; không thêm màu rực (đỏ, cam, xanh dương đậm) vào giao diện.

## 2. Font chữ

- **Tiêu đề: Cormorant Garamond** — serif thanh mảnh, dùng cho tên thương hiệu, tên bộ sưu tập,
  tên sản phẩm (cỡ 32–56px desktop, 24–32px mobile), chữ hoa đầu câu, giãn dòng 1.15.
- **Nội dung: Be Vietnam Pro** — sans-serif, dùng cho mô tả, giá, nút bấm, điều hướng, footer
  (cỡ 14–16px, giãn dòng 1.6). Tiếng Việt có dấu phải hiển thị đủ dấu, không lỗi font.
- Không dùng font thứ ba. Nút bấm dùng Be Vietnam Pro in đậm vừa (weight 600), chữ hoa toàn bộ,
  cỡ 13–14px, giãn chữ 0.08em.

## 3. Phong cách tham chiếu

**Lookbook tối giản Nhật – Hàn** (minimalist Japanese–Korean lookbook): phông nền trơn sáng,
người mẫu đứng tự nhiên không tạo dáng cầu kỳ, ánh sáng tự nhiên mềm, ít đạo cụ, mỗi khung hình
chỉ một chủ thể chính. Trang tham chiếu tinh thần này ở mọi section: hero, lưới lookbook,
chi tiết sản phẩm — không dùng phong cách studio tương phản mạnh hay streetwear nhiều lớp.

## 4. Quy tắc hình ảnh

- **Tỉ lệ khung:** ảnh người mẫu lookbook luôn tỉ lệ dọc **3:4** (desktop và mobile thống nhất);
  ảnh chi tiết chất vải (close-up) tỉ lệ **1:1**; ảnh hero toàn màn hình tỉ lệ **16:9** trên desktop,
  **3:4** trên mobile. Không cắt ảnh người mẫu thành ngang, không kéo giãn khung.
- **Tông ảnh:** đồng tông sáng tự nhiên — nền ảnh sáng (trắng, be, ngoài trời nắng nhẹ), độ tương phản
  thấp–vừa, màu vải linen giữ đúng tông thật (trắng ngà, be, olive nhạt), không lọc màu lạnh,
  không tăng bão hòa mạnh.
- **Chất lượng:** ảnh mẫu chất lượng cao, rõ nét, dung lượng tối ưu cho web; mọi ảnh trong một bộ
  sưu tập phải cùng tông sáng và cùng tỉ lệ 3:4, không trộn ảnh tối – sáng, ảnh dọc – ngang lẫn lộn.

## 5. Bố cục (visual-first)

- Ảnh lớn làm nội dung chính: hero chiếm toàn bộ chiều cao màn hình đầu tiên; lưới lookbook
  2 cột desktop / 1 cột mobile, mỗi ảnh chiếm tối thiểu 45% chiều rộng cột.
- Khoảng trắng: lề hai bên tối thiểu 24px mobile / 80px desktop; khoảng cách giữa các section
  tối thiểu 80px desktop / 48px mobile; không xếp ảnh sát nhau.
- Chữ không đè lên ảnh người mẫu; tên sản phẩm + giá đặt dưới ảnh, căn trái, màu `#22201D`,
  giá khuyến mãi (nếu có) màu `#6B7250`.
- Tối đa 3 khối nội dung chữ trên một màn hình cuộn; phần còn lại là ảnh và khoảng trắng.

## 6. Kiểm tra đối chiếu (dành cho QA)

Đối chiếu trực quan: nền `#F7F3EC`, chữ `#22201D`, nhấn `#6B7250`; tiêu đề Cormorant Garamond,
nội dung Be Vietnam Pro; ảnh người mẫu dọc 3:4, tông sáng tự nhiên; bố cục ảnh lớn + khoảng trắng.
Lệch bất kỳ điểm nào trong mục 1–4 là lỗi cần Dev sửa.
