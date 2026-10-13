# Bài 2 – Cơ chế theo dõi kế hoạch Sprint cho đội RikkeiGo

**Người soạn:** Lan (Scrum Master) – **Dùng cho:** Đức (Product Owner) và Developers, mọi Sprint

**Phạm vi:** Giúp đội (1) biết sớm Sprint Goal có đạt không, (2) bớt tranh luận "nhận bao nhiêu SP" ở Planning, (3) dùng Velocity đúng chỗ. Dữ liệu đầu vào: Velocity 5 Sprint gần nhất (18, 20, 19, 15, 13 SP), Capacity và Burndown của đội.

**Quy tắc chung:** Không quy đổi SP sang giờ; không dùng Velocity hay Burndown làm KPI hoặc để so sánh các đội; Sprint Goal là điểm tham chiếu khi giữ, đổi hay bỏ phạm vi.

| Vấn đề lặp lại | Thành phần xử lý |
|---|---|
| Đến ngày cuối mới biết Goal không đạt | Thành phần 2 và 3 |
| Mỗi Planning lại tranh luận số SP | Thành phần 1 |
| Quản lý muốn xếp hạng đội theo Velocity | Thành phần 4 (quy tắc sử dụng) |

---

## Phần 1 – Thiết kế: 4 thành phần

| # | Thành phần | Dữ liệu đầu vào | Ai cập nhật | Khi nào | Giúp quyết định gì |
|---|---|---|---|---|---|
| 1 | **Bảng dự báo Sprint** | Giờ khả dụng từng Developer (đã trừ nghỉ phép, người mới); khoảng Velocity 5 Sprint gần nhất (chỉ để tham chiếu); danh sách PBI đủ rõ (có AC) | Developers điền Capacity và chọn PBI; Đức cung cấp PBI; Lan điều phối | Đầu buổi Sprint Planning (≤ 15 phút) | Nhận bao nhiêu SP: Developers dự báo thành một **vùng** (thấp–cao) từ 3 dữ kiện (Capacity, Velocity, độ rõ PBI) thay vì tranh luận một con số; PBI chưa đủ rõ thì chưa vào Sprint |
| 2 | **Thẻ Sprint Goal và nhãn Cốt lõi/Linh hoạt** | Sprint Goal 1 câu; mỗi PBI trong Sprint Backlog gắn nhãn *Cốt lõi* (thiếu thì Goal hỏng) hoặc *Linh hoạt* (có thể bỏ) | Đức và Developers cùng chốt; Lan dán lên bảng Sprint | Cuối Planning; xem lại khi có yêu cầu chen vào hoặc khi trễ | Giữ, đổi hay bỏ phạm vi: bỏ phần *Linh hoạt* trước; chỉ đổi phạm vi khi Goal vẫn đạt; nếu Goal không còn ý nghĩa thì Đức cân nhắc hủy Sprint |
| 3 | **Burndown + bảng task, kèm mốc kiểm tra Goal ngày 5** | SP còn lại (chỉ giảm khi PBI Done); số PBI Done / đang làm / bị chặn; bảng task To do–Doing–Done | Developers cập nhật sau mỗi Daily Scrum; Lan nhắc | Hằng ngày; kiểm tra Goal vào **ngày 5** của Sprint 10 ngày | Phát hiện sớm rủi ro: ngày 5 hỏi "phần *Cốt lõi* còn lại có kịp không?" và quyết định cắt, tập trung hay nhờ hỗ trợ ngay, không chờ đến ngày cuối |
| 4 | **Sổ tổng kết Sprint** | SP Done, Capacity kế hoạch so với thực tế, Goal đạt hay không và nguyên nhân | Lan ghi; cả đội xem lại | Sprint Review và Retrospective | Chỉnh dự báo Sprint sau (xu hướng, sai lệch Capacity) và chọn hành động cải tiến. **Quy tắc dùng:** chỉ trong đội; không KPI; không so sánh đội; không đổi SP sang giờ |

---

## Phần 2 – Xử lý tình huống

### Tình huống 1: Ngày 4–6, Burndown nằm ngang dù Developers vẫn làm đủ giờ

**Phát hiện:** Thành phần 3 báo khi Burndown không giảm **2 ngày liền**; Lan nêu ngay ở Daily Scrum. Đường ngang không có nghĩa đội làm ít, mà thường là nhiều PBI được làm dở cùng lúc hoặc PBI quá lớn nên chưa cái nào Done và SP chưa giảm.

**Phản ứng:** Tại Daily, đội xem bảng task: PBI nào gần xong, PBI nào bị chặn. Sau đó dồn sức hoàn thành lần lượt các PBI *Cốt lõi*, chia nhỏ phần còn lại, và đến mốc ngày 5 nếu vẫn không kịp thì Đức và Developers bỏ PBI *Linh hoạt* (thành phần 2) và Đức báo bên liên quan.

### Tình huống 2: Sprint tới, 2 trong 4 Developers nghỉ mỗi người 3 ngày, Capacity giảm ≈ 15%

**Phát hiện:** Bảng Capacity ở thành phần 1 cho thấy 4 người × 10 ngày = 40 người-ngày, trừ 6 → còn 34 (giảm 15%).

**Phản ứng:** Không lấy Velocity nhân 85%, vì Capacity giảm bao nhiêu % không có nghĩa Velocity giảm đúng bấy nhiêu. Developers xem hai người nghỉ có trùng ngày không và có ai giữ kỹ năng riêng không, rồi chọn vùng dự báo thấp hơn, giữ Sprint Goal nhỏ hơn và chỉ để vài PBI *Cốt lõi*; phần còn lại gắn *Linh hoạt*.

### Trả lời đề nghị xếp hạng đội theo Velocity của quản lý

> SP là thang ước lượng riêng của từng đội, nên Velocity của đội ứng dụng khách và đội ứng dụng tài xế không so sánh được với nhau; nếu dùng để xếp hạng thì đội sẽ có động cơ tăng điểm ước lượng và con số mất giá trị dự báo.

**Thông tin phù hợp hơn để quản lý theo dõi đội:**
- Mức độ đạt Sprint Goal qua các Sprint.
- Giá trị đã giao cho khách (ví dụ thời gian chờ tài xế, tỷ lệ huỷ chuyến sau khi phát hành tính năng).
- Thời gian từ khi có yêu cầu đến khi phát hành, và số lỗi lọt ra sau phát hành.
- Phản hồi của bên liên quan tại Sprint Review.
