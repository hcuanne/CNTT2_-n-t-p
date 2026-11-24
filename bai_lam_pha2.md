# BÀI LÀM PHA 2

- **Họ tên:** [Điền họ tên]
- **Lớp:** [Điền lớp]
- **Link repository Pha2:** [Điền link GitHub]
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** ChatGPT (kết quả mô phỏng để ôn tập)

> **Lưu ý:** Đây là đáp án mẫu phục vụ ôn tập. Các link trò chuyện phải được tạo từ các cuộc hội thoại thực tế chạy nguyên văn prompt ở Pha 1; không thể tạo link hợp lệ bằng cách điền giả.

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```json
[
  {
    "ma_goi": "SVT",
    "ngay_su_kien": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "FZ",
    "ngay_su_kien": "2027-01-05",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_ve": "thuong",
    "ghi_chu": "một người cần hỗ trợ xe lăn"
  },
  {
    "ma_goi": "VIP",
    "ngay_su_kien": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_ve": "vip",
    "ghi_chu": "một người khiếm thị cần hỗ trợ tìm chỗ"
  }
]
```

**Link trò chuyện:** [Điền link Share sau khi chạy prompt thực tế]

## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

```text
B1. Tiền người lớn: 5 × 1.200.000 = 6.000.000 đồng.
B2. Tiền trẻ em: hai bé 8 và 10 tuổi: 2 × 1.200.000 × 70% = 1.680.000 đồng; bé 3 tuổi: 0 đồng. Tổng tiền trẻ em = 1.680.000 đồng.
B3. Tiền vé trước giảm: 6.000.000 + 1.680.000 = 7.680.000 đồng.
B4. Giảm giá nhóm (5 người lớn): 7.680.000 × 5% = 384.000 đồng. Tiền vé sau giảm = 7.680.000 − 384.000 = 7.296.000 đồng.
B5. Phụ thu khu ghế ưu tiên: 1 × 300.000 = 300.000 đồng (không giảm).
B6. Tổng tiền: 7.296.000 + 300.000 = 7.596.000 đồng.
[RESULT: 7.596.000 đồng]
```

**Link trò chuyện:** [Điền link Share sau khi chạy prompt thực tế]

### b) Kiểm tra kết quả AI

AI tính **đúng** cả 6 bước theo bảng giá và quy tắc. Tổng tiền đúng là **7.596.000 đồng**.

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```json
{
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_hiep_bi_anh_huong": 2,
  "tom_tat": "Hai khán giả bị xếp khu không mái che trong hai hiệp đầu"
}
```

**Link trò chuyện:** [Điền link Share sau khi chạy prompt thực tế]

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
|---|---:|---|---|
| Đúng thông tin (5đ) | 0/5 | “Vé Sân Vận Động bên em giá 1.000.000đ/người” sai giá 1.200.000đ. “Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh” sai vì chỉ hoàn 50%. | “Vé SVT giá 1.200.000 đồng/người lớn. Huỷ trước trận 3 ngày được hoàn 50% tiền vé.” |
| Đầy đủ (3đ) | 2/3 | Đã đề cập giá và huỷ vé nhưng cung cấp sai; thiếu đề nghị khách cho biết ngày trận và số lượng vé. Câu “Anh cần gì cứ nhắn em nhé!” quá chung chung. | “Anh vui lòng cho em biết ngày trận đấu và số lượng vé cần đặt ạ.” |
| Giọng điệu (2đ) | 1/2 | “xem rất đã luôn ạ”, “nha anh” mang tính suồng sã, thiếu chuyên nghiệp. | “Trải nghiệm xem trận đấu tại sân vận động rất hấp dẫn ạ.” |

**Tổng điểm: 3/10.**

**Link trò chuyện:** [Điền link Share sau khi chạy prompt thực tế]
