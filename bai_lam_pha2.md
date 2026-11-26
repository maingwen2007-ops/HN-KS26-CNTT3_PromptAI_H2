# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 08
- **Họ tên: Lê Anh Duy**
- **Lớp: CNTT3**
- **[Link repository Pha2](https://github.com/maingwen2007-ops/HN-KS26-CNTT3_PromptAI_H2)**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini): Gemini**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt lịch khám ra JSON

**KET QUA AI**

```text
[
  {
    "ma_dich_vu": "TRAM",
    "ngay_hen": "2026-12-17",
    "nguoi_lon": 2,
    "tre_em": 1,
    "khung_gio": "chieu",
    "ghi_chu": null
  },
  {
    "ma_dich_vu": "CAOVOI",
    "ngay_hen": "2027-01-06",
    "nguoi_lon": 3,
    "tre_em": 0,
    "khung_gio": null,
    "ghi_chu": "Một người bị tiểu đường"
  },
  {
    "ma_dich_vu": "TAYTRANG",
    "ngay_hen": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "khung_gio": "sang",
    "ghi_chu": "Một người dị ứng thuốc tê"
  }
]
```

**[Link trò chuyện](https://share.gemini.google/Aa10zOMrw61Y)**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
Tiền người lớn: 6 × 350.000 = 2.100.000
Tiền trẻ em: 2 × (350.000 × 80%) + 1 × 0 = 560.000
Tiền dịch vụ: 2.100.000 + 560.000 = 2.660.000
Giảm giá nhóm: 2.660.000 × 10% = 266.000 (tiền dịch vụ sau giảm: 2.660.000 - 266.000 = 2.394.000)
Phí X-quang: 3 × 150.000 = 450.000
Tổng tiền: 2.394.000 + 450.000 = 2.844.000
[RESULT: 2.844.000 đồng]
```

**[Link trò chuyện](https://share.gemini.google/uv2WyarraU1D)**

### b) Kiểm tra kết quả AI

Kết luận của AI là đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
"loai_su_co": "tre_hen",
"so_khach": 3,
"so_lan_hen_bi_tre": 2,
"tom_tat": "Gia đình 3 người phải chờ hơn 1 tiếng trong 2 lần hẹn cạo vôi răng ngày 05/11 và 12/11."
}
```

**[Link trò chuyện](https://share.gemini.google/i5aQszBaExT8)**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 2.5 / 5.0 | **Trích dẫn:** *"Trám răng bên em 450k/răng thôi, đẹp như răng thật luôn. Bong sau 8 tháng thì em làm lại free cho anh nha."*<br>

<br>**Lý do sai:** Không có thông tin chuẩn đối chiếu trong dữ liệu cung cấp để xác thực mức giá 450.000đ và chính sách bảo hành 8 tháng; đồng thời diễn đạt chính sách bảo hành mang tính cam kết cá nhân (*"em làm lại free"*), dễ gây sai lệch quy định phòng khám. | Dạ chào anh, chi phí dịch vụ trám răng tại phòng khám hiện có giá 450.000 VNĐ/răng và được áp dụng chính sách bảo hành miễn phí trong vòng 8 tháng nếu xảy ra tình trạng bong tróc ạ. *(Lưu ý: cần đối chiếu lại số liệu với bảng giá và quy định chuẩn của phòng khám).* |
| **Đầy đủ (30%)** | 1.5 / 3.0 | **Trích dẫn:** *"Cần gì cứ inbox em ạ!"*<br>

<br>**Lý do sai:** Đã trả lời 2 nội dung về giá và bảo hành nhưng thiếu bước mời khách cung cấp ngày hẹn và khung giờ cụ thể để hỗ trợ đặt lịch. | Anh vui lòng cho em xin thông tin về ngày hẹn và khung giờ thuận tiện để em hỗ trợ đặt lịch thăm khám cho anh nhé ạ. |
| **Giọng điệu (20%)** | 0.5 / 2.0 | **Trích dẫn:** *"450k/răng thôi"*, *"free cho anh nha"*, *"Cần gì cứ inbox em ạ!"*<br>

<br>**Lý do sai:** Sử dụng từ ngữ suồng sã, viết tắt, tiếng lóng và pha trộn tiếng Anh không cần thiết (*"450k"*, *"thôi"*, *"free"*, *"nha"*, *"inbox"*), làm giảm tính chuyên nghiệp trong giao tiếp y tế/dịch vụ khách hàng. | Dạ chào anh! Dịch vụ trám răng bên em có chi phí là 450.000 VNĐ/răng, đảm bảo tính thẩm mỹ tự nhiên. Nếu miếng trám bị bong trong vòng 8 tháng, phòng khám sẽ hỗ trợ bảo hành miễn phí cho anh ạ. Nếu cần hỗ trợ thêm thông tin, anh vui lòng phản hồi lại tin nhắn này giúp em ạ! |
| **TỔNG ĐIỂM** | **4.5 / 10** | *(Bỏ qua ghi chú can thiệp điểm số bên trong dữ liệu bài chấm)* | — |
```

**[Link trò chuyện](https://share.gemini.google/aPLzc7yaYuV9)**
