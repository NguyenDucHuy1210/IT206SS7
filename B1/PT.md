# Bài 1 – Dự báo Sprint 6 của đội RikkeiGo

**Người soạn:** Vy (Developer), cùng Lan (Scrum Master) – **Dùng cho:** Sprint Planning với Đức (Product Owner)

## Dữ liệu đầu vào

| Dữ liệu | Giá trị | Nhận xét |
|---|---|---|
| Velocity 5 Sprint gần nhất | 18, 20, 19, 15, 13 SP | Trung bình 17 SP, nhưng xu hướng giảm; 3 Sprint gần nhất trung bình ≈ 15,7 SP |
| Capacity | Sprint 5: 212 giờ → Sprint 6: 186 giờ | Giảm ≈ 12% (đã tính Minh làm nửa giờ, Hà nghỉ 3 ngày) |
| PBI đủ rõ (có Acceptance Criteria) | #1 (5), #3 (3), #4 (5), #5 (2) = **15 SP** | #2 (13 SP) thiếu AC cho trường hợp mất GPS nên chưa đủ rõ |
| Sprint Goal mong muốn | Khách chủ động hơn khi chờ tài xế | Đức đề xuất |

---

## Phần 1 – Đề xuất: 2 cách dự báo

### Cách A – Dự báo từ Velocity (top-down)

Lấy Velocity Sprint gần nhất làm cơ sở, điều chỉnh theo tỷ lệ Capacity, rồi lấy PBI từ trên xuống theo thứ tự Backlog cho đến khi gần đủ con số.

- **Con số dự báo:** 13 SP × (186 / 212) ≈ 11,4 → **11 SP**
- **PBI chọn:** #1 (5) + #3 (3) + #5 (2) = **10 SP**
  - Bỏ #2: chưa đủ rõ và quá lớn.
  - #4 (5 SP) không vừa vì sẽ lên 15 SP, vượt 11.

### Cách B – Dự báo từ Sprint Goal và Capacity (bottom-up)

Chốt Sprint Goal với Đức trước, chọn các PBI đủ rõ phục vụ Goal, rồi Developers chia nhỏ thành task và ước giờ để đối chiếu với 186 giờ. SP là kết quả của việc chọn, Velocity chỉ dùng để kiểm tra xem con số có hợp lý không.

- **Con số dự báo:** **8 SP** cho Sprint Goal, và nếu chia task xong còn dư giờ thì kéo thêm #1 (5 SP) → tối đa **13 SP**
- **PBI chọn:** #3 (3) + #4 (5) = **8 SP**; #1 (5) là PBI kéo thêm

---

## Phần 2 – So sánh

| Tiêu chí | Cách A – Từ Velocity | Cách B – Từ Sprint Goal + Capacity |
|---|---|---|
| **Phản ánh thay đổi Capacity** | **(–)** Chỉ co theo tỷ lệ 12%, nhưng Capacity giảm bao nhiêu % không có nghĩa Velocity giảm đúng bấy nhiêu; không thấy được việc Minh làm nửa giờ hay Hà nghỉ vào ngày nào. | **(+)** Dùng đúng 186 giờ thực tế, ước giờ theo task nên thấy rõ ai làm được gì trong 10 ngày. |
| **Bảo vệ Sprint Goal** | **(–)** Chọn theo thứ tự Backlog để lấp cho đủ số, ra tập PBI rời rạc (hẹn giờ, SMS, giao diện Tết), không gắn với Goal "chờ tài xế". | **(+)** Goal đi trước, PBI nào không phục vụ Goal thì xếp sau; nếu trễ thì cắt phần kéo thêm, Goal vẫn giữ. |
| **Dễ giải thích với Product Owner** | **(+)** Một con số, một phép tính, dựa trên lịch sử, giải thích trong 1 phút. | **(–)** Cần thêm bước chia task và ước giờ nên Planning lâu hơn; bù lại, cách giải thích bằng Goal dễ hiểu với Đức. |

---

## Phần 3 – Lựa chọn: Cách B

**Căn cứ:**
- **Velocity:** 8–13 SP nằm ở mức thận trọng so với 13 SP của Sprint 5 (khi Capacity cao hơn) và xu hướng giảm gần đây; không chạy theo mức trung bình 17 SP vì Average chỉ mô tả quá khứ.
- **Capacity:** 186 giờ, thấp hơn 12%, và Minh mới vào nên cần chừa đệm.
- **Độ rõ của PBI:** chỉ có 15 SP đủ rõ; #2 chưa vào được.

**Sprint Goal đề xuất:**
> *"Khách biết khi nào tài xế sắp đến và liên lạc được với tài xế trong lúc chờ."*

**Danh sách PBI mang vào Sprint Planning:**

| Thứ tự | PBI | SP | Vai trò trong Sprint 6 | Lý do |
|---|---|---|---|---|
| 1 | #3 Gửi SMS khi tài xế sắp đến | 3 | Dự báo chính | Trực tiếp phục vụ Goal; hợp đồng SMS đã ký nên không bị chặn |
| 2 | #4 Chat với tài xế | 5 | Dự báo chính | Phục vụ Goal; AC đầy đủ |
| 3 | #1 Hẹn giờ đặt xe trước | 5 | Kéo thêm nếu còn Capacity | AC đầy đủ, Đức xếp thứ 1 trong Backlog, nhưng không cần cho Goal |
| – | #5 Giao diện chủ đề Tết | 2 | Không vào | Không phục vụ Goal |
| – | #2 Theo dõi vị trí tài xế | 13 | Không vào | Quá lớn và thiếu AC cho trường hợp mất GPS; cần tách nhỏ và viết AC trong Sprint 6 để cân nhắc cho Sprint 7 |

**Cách kiểm tra trong Planning:** Developers chia #3 và #4 thành task, cộng giờ ước tính và so với 186 giờ (trừ phần đệm cho việc Minh làm quen dự án). Nếu còn dư rõ ràng thì mới kéo #1.

**Phản hồi đề nghị 20 SP của quản lý:**

> Velocity là số đo quá khứ để đội dự báo Sprint tới, không phải chỉ tiêu phải đạt; 20 SP nằm trong khoảng cũ nhưng Sprint 6 có Capacity giảm khoảng 12%, có người mới, và chỉ có 15 SP PBI đủ rõ, nên muốn đạt 20 SP phải nhét #2 (13 SP, chưa có AC) vào Sprint. Nếu biến con số thành chỉ tiêu thì đội sẽ cắt chất lượng hoặc ước lượng phình lên để "tăng", và Velocity sẽ không còn dùng để dự báo được nữa. Đội sẽ báo cáo mức độ đạt Sprint Goal tại Sprint Review; Velocity sẽ tự ổn định lại khi đội ổn định và PBI rõ hơn.
