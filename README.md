# Sắp Xếp Họ Tên Trong Excel

**Tác giả:** Dương Tấn Chánh

Phần mềm giúp bạn sắp xếp danh sách họ tên trong file Excel theo đúng thứ tự bảng chữ cái tiếng Việt (A → Z), nhanh chóng và chính xác.

---

## Phần mềm này dùng để làm gì?

Khi bạn có một file Excel chứa danh sách học sinh, nhân viên, đoàn viên… với cột "Họ tên" lộn xộn, phần mềm sẽ giúp bạn:

- Tự động tìm cột họ tên trong file
- Sắp xếp lại danh sách theo tên (A → Z), đúng chuẩn tiếng Việt
- Giữ nguyên các cột khác (ngày sinh, lớp, địa chỉ…) đi kèm với từng người
- Xuất ra một file Excel mới đã sắp xếp xong

**Ví dụ:**

Trước khi sắp xếp:

| STT | Họ tên | Lớp |
|-----|--------|-----|
| 3 | Trần Văn Cường | 10A1 |
| 1 | Nguyễn Thị Bình | 10A1 |
| 4 | Đặng Quốc Dũng | 10A1 |
| 2 | Lê Thị Hoa | 10A1 |

Sau khi sắp xếp:

| STT | Họ tên | Lớp |
|-----|--------|-----|
| 1 | Nguyễn Thị Bình | 10A1 |
| 3 | Trần Văn Cường | 10A1 |
| 4 | Đặng Quốc Dũng | 10A1 |
| 2 | Lê Thị Hoa | 10A1 |

Các cột STT, Lớp… vẫn đi theo đúng người. Chỉ có thứ tự dòng thay đổi.

---

## Cách sử dụng

### Bước 1 — Mở phần mềm

Nhấp đúp vào file `sapxep.html`. Phần mềm sẽ mở trong trình duyệt web (Chrome, Edge, Firefox… đều được).

### Bước 2 — Chọn file Excel

Có 3 cách để chọn file:

- **Cách 1:** Kéo file Excel từ thư mục và thả vào khung có viền nét đứt.
- **Cách 2:** Bấm vào khung đó, rồi chọn file từ máy tính.
- **Cách 3:** Mở file trong Windows, bấm Ctrl+C để copy, rồi bấm Ctrl+V trong trang phần mềm.

**Định dạng file được hỗ trợ:** `.xlsx`, `.xls`, `.csv`

### Bước 3 — Chọn tùy chọn (nếu cần)

Trong khối "2. Tùy chọn xử lý":

- **Sheet**: Nếu file có nhiều sheet, chọn sheet bạn muốn sắp xếp.
- **Chuẩn hóa về dạng Chữ Hoa Đầu Mỗi Từ**: Tick vào nếu bạn muốn "NGUYỄN VĂN AN" hoặc "nguyễn văn an" thành "Nguyễn Văn An".
- **Đánh lại cột STT từ 1 đến hết**: Tick vào nếu bạn muốn cột STT được đánh lại từ 1, 2, 3… theo thứ tự mới. Nếu không tick, cột STT cũ sẽ đi theo từng người.

### Bước 4 — Sắp xếp

Bấm nút **"Sắp xếp dữ liệu"**.

Chờ vài giây (thanh tiến trình chạy). Khi xong, danh sách đã sắp xếp sẽ hiện ra ở khối "4. Kết quả".

### Bước 5 — Xuất file

Bấm nút **"Xuất file Excel"**. File mới sẽ tự động được tải về máy, có tên dạng:

```
<tên file gốc>_sapxep_YYYYMMDD_HHmm.xlsx
```

Ví dụ: `DanhSachHocSinh_sapxep_20260925_1430.xlsx`

---

## Lưu ý quan trọng — File Excel nên có cột số thứ tự

Để phần mềm hoạt động chính xác, **file Excel của bạn nên có cột Số thứ tự (STT) ở cột đầu tiên (cột A)**.

### Cách kiểm tra

1. Mở file Excel.
2. Nhìn vào cột A (cột đầu tiên bên trái).
3. Nếu cột A có các số 1, 2, 3, 4… tăng dần cho từng người → file đã đúng.
4. Nếu cột A là "Họ tên", "Mã số", "Ngày sinh" hoặc các thông tin khác → file chưa đúng.

### Nếu file chưa có cột STT

Bạn hãy mở file Excel, **chèn thêm một cột ở vị trí đầu tiên (bên trái cột hiện tại)**, đặt tiêu đề là "TT" hoặc "STT", rồi đánh số 1, 2, 3… từ trên xuống cho từng người. Sau đó lưu file và dùng phần mềm.

### Tại sao cần cột STT?

Phần mềm dùng cột STT làm **mốc để biết dữ liệu học sinh kết thúc ở đâu**. Khi gặp dòng mà cột STT không còn là số (ví dụ dòng "Tổng cộng", dòng ghi chú, dòng chữ ký…), phần mềm sẽ tự biết dừng lại — không sắp xếp nhầm các dòng đó.

Nếu file không có cột STT, phần mềm có thể dừng ngay từ dòng đầu tiên và không sắp xếp được.

---

## Những việc phần mềm KHÔNG làm

- **Không giữ được màu nền, font chữ, viền ô** của file gốc — đây là giới hạn của thư viện miễn phí. File xuất ra chỉ giữ **giá trị** và **cấu trúc** (ô gộp, chiều rộng cột).
- **Không sắp xếp được nếu cột họ tên không nằm trong 50 dòng đầu của file.** Nếu tiêu đề "Họ tên" ở dòng 51 trở đi, phần mềm sẽ không tự tìm thấy.
- **Không tính lại công thức** của cột công thức. Khi bạn mở file xuất ra bằng Excel, Excel sẽ tự tính lại và hiển thị giá trị đúng.

---

## Các câu hỏi thường gặp

### 1. Tôi chọn file rồi mà nút "Sắp xếp" vẫn bị mờ, không bấm được?

Nguyên nhân có thể do:

- File không có cột "Họ tên" trong 50 dòng đầu → phần mềm hiện khối "Xác nhận cột họ và tên" ở giữa trang. Bạn hãy chọn cột họ tên và nhập dòng bắt đầu dữ liệu, rồi bấm "Xác nhận".
- File đang chọn là sheet rỗng → hãy chọn sheet khác trong dropdown "Sheet".
- Đang trong quá trình đọc file → chờ vài giây.

### 2. Sắp xếp xong nhưng kết quả không đúng thứ tự tiếng Việt?

- Kiểm tra xem tên có ký tự đặc biệt hoặc số không (ví dụ "An2", "An*").
- Kiểm tra các ô họ tên có khoảng trắng thừa ở đầu/cuối không.
- Phần mềm dùng chuẩn sắp xếp chính thức của tiếng Việt (Đ đứng sau D, dấu sắc/huyền/hỏi/ngã/nặng được phân biệt). Nếu kết quả khác với mong đợi của bạn, hãy kiểm tra lại dữ liệu gốc.

### 3. File xuất ra mất màu, mất định dạng?

Đây là giới hạn của phần mềm (đã ghi ở mục trên). Nếu cần giữ định dạng hoàn toàn, bạn cần dùng phần mềm khác hoặc sửa trực tiếp trong Excel.

### 4. Tôi muốn sắp xếp nhiều sheet cùng lúc?

Phần mềm chỉ xử lý **một sheet mỗi lần**. Hãy chọn từng sheet và sắp xếp riêng, xuất riêng.

### 5. Danh sách có dòng trống ở giữa, phần mềm có bỏ qua không?

Có. Phần mềm tự động bỏ qua các dòng trống nằm giữa danh sách (tối đa 3 dòng trống liên tiếp). Nếu có 4 dòng trống liên tiếp trở lên, phần mềm coi như danh sách đã hết và dừng lại.

### 6. Có dòng học sinh mới chưa có STT ở cuối danh sách, phần mềm xử lý thế nào?

Phần mềm dừng sắp xếp tại dòng đó (vì cột STT không còn là số). Dòng học sinh mới đó sẽ **giữ nguyên vị trí**, không bị đưa vào danh sách sắp xếp.

Nếu bạn muốn dòng đó cũng được sắp xếp, hãy mở file Excel, đánh STT cho dòng đó rồi chạy lại phần mềm.

---

## Mẹo sử dụng

- **Kiểm tra kỹ trước khi xuất**: Xem kết quả ở khối "4. Kết quả" trước, nếu thấy sai thì bấm "Hủy" và chạy lại.
- **Xem nhật ký**: Khối "5. Nhật ký / Cảnh báo" ghi lại mọi việc phần mềm đã làm — hữu ích khi bạn cần biết vì sao kết quả ra như vậy.
- **Sao lưu file gốc**: Nên giữ nguyên file Excel gốc, không sửa trực tiếp. Phần mềm luôn tạo file mới.

---

## Cần hỗ trợ?

Liên hệ tác giả: **Dương Tấn Chánh**