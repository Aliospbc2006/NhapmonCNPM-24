# SIM-INT-TQ — Role-play Interview: Thủ quỹ / Người thu phí

**Loại:** Simulated Interview / Role-play for Requirement Elicitation (bài tập môn học, không phải phỏng vấn thật).

| Mục | Giá trị |
|---|---|
| Mã biên bản | SIM-INT-TQ |
| Người được phỏng vấn | Vai trò giả lập: Thủ quỹ / người thu phí. Không có danh tính thật. |
| Người phỏng vấn | Analyst (thành viên nhóm đóng vai) |
| Hình thức | Role-play bằng văn bản. **Không phải buổi gặp thực tế.** Không có ngày, giờ, ghi âm, chữ ký hay ảnh. |
| Cơ sở | Đề bài BlueMoon (PS-01), quy trình As-Is giả định WA-01, biểu mẫu giả định DA-02 |

> Toàn bộ câu trả lời dưới đây là **Simulated stakeholder input**, do nhóm viết để phục vụ phân tích yêu cầu.

---

## 1. Interview objective

- Hiểu chi tiết thao tác thu phí hằng ngày và các tình huống ngoại lệ.
- Tìm pain point khi tìm hộ, tính tiền, ghi nhận, đối chiếu, lập biên lai.
- Thu nhu cầu tra cứu công nợ và nhu cầu về tốc độ, số người dùng đồng thời.
- Làm rõ điểm khác biệt có thể có so với Ban quản trị (ví dụ miễn giảm).

## 2. Stakeholder role

Thủ quỹ / người thu phí: thao tác thu tiền, ghi sổ và lập biên lai tại văn phòng Ban quản trị. Là người dùng cuối tiếp xúc nhiều nhất với phần mềm ở v1.0 (phần thu phí, tra cứu). Chịu trách nhiệm đối chiếu số liệu thu với Ban quản trị cuối tháng.

## 3. Context

Hằng tháng thủ quỹ nhận danh sách khoản phải thu từ Ban. Hộ nộp tại văn phòng. Thủ quỹ ghi sổ giấy, gõ lại Excel và viết biên lai tay. Có hộ nộp thiếu, nộp gộp, nộp nhầm. Chung cư có vài trăm hộ (AS-13).

---

## 4. Interview

### SIM-INT-TQ-Q01 — Introduction

**Question:** Anh/chị giới thiệu vai trò của mình khi thu phí ở chung cư?

**Simulated stakeholder answer:**
Mình là thủ quỹ, lo việc thu tiền, ghi sổ và viết biên lai cho các hộ. Thường thu ở văn phòng Ban. Cuối tháng mình tổng hợp số đã thu để đưa lại cho Ban. Mình ghi chép cẩn thận nhưng việc tay chân nhiều nên cũng hay sót.

**Analyst note:** Xác định TQ là người dùng thao tác nhiều nhất (thu phí, tra cứu).

**Requirement candidates discovered:** (bối cảnh, chưa có yêu cầu mới)

---

### SIM-INT-TQ-Q02 — Current process / As-Is: thu tiền

**Question:** Anh/chị mô tả một lần thu phí điển hình, từ lúc hộ đến nộp tiền?

**Simulated stakeholder answer:**
Đầu tháng mình nhận danh sách từ Ban. Hộ đến nộp thì mình tìm tên hộ trên Excel hoặc sổ, thu tiền, ghi ngày nộp với số tiền, rồi viết biên lai tay hai liên, đưa một liên cho hộ. Có người nhờ người khác nộp hộ. Mình ghi vào sổ trước, tối gõ lại vào Excel. Mình muốn gõ một lần thôi: chọn hộ, chọn khoản, nhập số tiền và ngày là xong.

**Analyst note:** Khớp WA-01. Ghi hai lần là nguồn sai sót. Có người nộp hộ nên ghi nhận *người nộp* là thông tin phụ (chưa thành yêu cầu riêng, ghi vào Notes RAW-013).

**Requirement candidates discovered:**
- Ghi nhận nộp tiền nhanh (hộ, khoản, số tiền, ngày, người thu) → RAW-013 (WISH-12)

---

### SIM-INT-TQ-Q03 — Pain Points

**Question:** Điều gì khó khăn hoặc dễ nhầm nhất khi thu phí?

**Simulated stakeholder answer:**
Tính tiền tay bằng máy tính cầm tay, diện tích nhân đơn giá cho từng nhà, có mấy lần bấm nhầm. Tìm một nhà trong Excel mấy trăm dòng cũng lâu, nhất là lúc đông người xếp hàng. Tối còn phải gõ lại, mệt lắm.

**Analyst note:** Pain point: tính toán thủ công, tìm kiếm chậm, nhập hai lần. Dẫn đến yêu cầu tự tính phí, tìm nhanh, và NFR về tốc độ và dễ dùng.

**Requirement candidates discovered:**
- Tự tính phí theo diện tích → RAW-011 (WISH-11)
- Tìm hộ nhanh → RAW-016
- Thao tác ít bước → RAW-028 (WISH-19)

---

### SIM-INT-TQ-Q04 — Hình thức nộp

**Question:** Các hộ nộp tiền bằng cách nào?

**Simulated stakeholder answer:**
Phần lớn nộp tiền mặt ở văn phòng. Cũng có hộ chuyển khoản rồi nhắn cho mình, mình tự đối chiếu. Cái này tính sao thì mình không rõ, chắc ghi lại là tiền mặt hay chuyển khoản là đủ.

**Analyst note:** *Assumption AS-12:* v1.0 chỉ ghi nhận hình thức nộp (tiền mặt/chuyển khoản) như thông tin phụ, không tích hợp thanh toán online (ngoài phạm vi). *Open Question* OQ-09.

**Requirement candidates discovered:**
- Lưu hình thức nộp trong giao dịch thu → bổ sung vào RAW-013 (Notes)

---

### SIM-INT-TQ-Q05 — Nộp thiếu, nộp gộp, nộp trước

**Question:** Có những trường hợp hộ không nộp đủ hoặc nộp theo cách khác thường không?

**Simulated stakeholder answer:**
Có chứ. Hộ nộp thiếu, hứa tuần sau đóng nốt. Có hộ nộp một lần ba bốn tháng. Cũng có hộ đóng trước. Mình ghi chú bên lề sổ thôi, sau dễ quên. Phần mềm nên cho nộp một phần, nộp gộp nhiều khoản trong một lần, rồi báo còn thiếu bao nhiêu. Còn phạt chậm nộp thì Ban chưa nói gì với mình.

**Analyst note:** *Open Question* OQ-05: có tính phạt chậm nộp không (ngoài v1.0 nếu chưa xác nhận). Nộp trước (nhiều kỳ chưa phát sinh) cần xác thực chính sách.

**Requirement candidates discovered:**
- Ghi nhận nộp một phần / nộp gộp → RAW-013 (WISH-13)
- Xem còn thiếu bao nhiêu → RAW-018

---

### SIM-INT-TQ-Q06 — Nhập sai, sửa, hủy

**Question:** Khi nhập sai số tiền hoặc thu nhầm hộ thì hiện xử lý ra sao?

**Simulated stakeholder answer:**
Có lần mình nhập nhầm số tiền, có lần thu nhầm sang hộ khác. Trong sổ thì gạch rồi viết lại, còn Excel thì sửa đè luôn nên không còn dấu. Phần mềm cho sửa hoặc hủy thì được, nhưng nên ghi lý do, và đừng xóa hẳn kẻo mình bị hỏi.

**Analyst note:** Khớp BQT-Q09. Cùng hướng với AS-17: sửa/hủy có lý do, lưu vết.

**Requirement candidates discovered:**
- Hủy/điều chỉnh giao dịch có lý do → RAW-015 (WISH-15)
- Lưu vết thao tác → RAW-025

---

### SIM-INT-TQ-Q07 — Biên lai

**Question:** Biên lai hiện được lập thế nào và anh/chị muốn gì ở phần mềm?

**Simulated stakeholder answer:**
Biên lai viết tay tốn thời gian, chữ xấu cư dân cũng phàn nàn. Mình muốn in phiếu thu có số căn hộ, khoản thu, số tiền, ngày nộp, người thu. Có hộ không cần nhưng nhiều hộ hay đòi giữ.

**Analyst note:** Biên lai không nằm rõ trong đề bài; ghi là *Assumption* ưu tiên Should. Mẫu biên lai chính thức cần xác nhận (OQ-06).

**Requirement candidates discovered:**
- In/xuất biên lai → RAW-014 (WISH-14)

---

### SIM-INT-TQ-Q08 — Tìm kiếm

**Question:** Anh/chị thường tìm thông tin gì và tìm theo cách nào?

**Simulated stakeholder answer:**
Cư dân đến thường nói số căn hộ, có người chỉ nhớ tên chủ hộ, mà trùng họ tên thì dễ nhầm. Phải tìm theo số căn hộ trước, rồi theo tên. Tìm xong thấy ngay số tiền phải nộp của hộ đó. Thỉnh thoảng cũng cần tìm theo tên một người trong nhà.

**Analyst note:** Tìm hộ là thao tác nhiều nhất. Tìm nhân khẩu cũng được nhắc.

**Requirement candidates discovered:**
- Tìm hộ theo số căn hộ, tên chủ hộ → RAW-016 (WISH-16)
- Tìm nhân khẩu theo tên → RAW-017
- Thời gian phản hồi nhanh → RAW-027

---

### SIM-INT-TQ-Q09 — Công nợ và nhắc nộp

**Question:** Anh/chị cần xem thông tin gì để biết hộ nào còn chưa nộp?

**Simulated stakeholder answer:**
Mình hay phải xem nhà nào còn thiếu để nhắc. Muốn lọc ra danh sách chưa nộp theo tháng, và mở từng hộ để xem các tháng đã đóng, còn thiếu tháng nào, thiếu bao nhiêu.

**Analyst note:** Hai nhu cầu khác nhau: (1) báo cáo theo kỳ trên toàn hộ (RAW-020); (2) xem công nợ chi tiết một hộ (RAW-018).

**Requirement candidates discovered:**
- Xem công nợ, lịch sử nộp của một hộ → RAW-018 (WISH-17)
- Danh sách hộ chưa nộp theo kỳ → RAW-020 (WISH-18)

---

### SIM-INT-TQ-Q10 — Tính phí và miễn giảm

**Question:** Việc tính số tiền mỗi hộ phải nộp hiện làm thế nào, có trường hợp đặc biệt nào không?

**Simulated stakeholder answer:**
Đơn giá thì Ban đưa, mình nhân theo diện tích. Nhưng đôi khi có hộ được Ban cho miễn hoặc giảm, kiểu hộ khó khăn. Mình nghĩ phải cho nhập điều chỉnh được... à mà Ban nói với mình cái này là tùy trường hợp, không có quy định nào cố định. Anh chị hỏi lại Ban nhé.

**Analyst note:** **Conflict C-02:** BQT-Q06 nghĩ mọi căn cùng đơn giá, TQ nhắc có miễn giảm. Chưa có quy tắc, nên *Assumption AS-14:* miễn/giảm không thuộc v1.0 nếu BQT chưa xác nhận (OQ-02).

**Requirement candidates discovered:**
- Tự tính phí theo diện tích × đơn giá → RAW-011
- Miễn/giảm: chưa thành yêu cầu (Open Question)

---

### SIM-INT-TQ-Q11 — Số người dùng, quy mô và hiệu năng

**Question:** Có bao nhiêu người cùng thao tác trong lúc thu phí, và anh/chị kỳ vọng tốc độ ra sao?

**Simulated stakeholder answer:**
Văn phòng có vài người thôi. Lúc thu phí thường mình với một bạn nữa cùng nhập. Chung cư vài trăm hộ chứ không nhiều lắm. Phần mềm mà chậm là khách xếp hàng, nên tìm kiếm phải nhanh, nhập ít bước thôi.

**Analyst note:** *Assumption AS-13:* quy mô vài trăm hộ, vài nghìn nhân khẩu; dữ liệu tập trung trên MySQL (đề bài) cho phép 2–3 người dùng đồng thời. Con số cụ thể cần xác thực (OQ-10).

**Requirement candidates discovered:**
- Phản hồi nhanh khi tìm và liệt kê → RAW-027 (WISH-19)
- Ghi nhận nộp tiền ít thao tác → RAW-028

---

### SIM-INT-TQ-Q12 — Priority và Closing

**Question:** Việc nào là quan trọng nhất đối với anh/chị? Còn điều gì chúng tôi chưa hỏi?

**Simulated stakeholder answer:**
Mình ưu tiên: tự tính tiền, ghi nhận nộp, tìm hộ nhanh, danh sách chưa nộp. In biên lai nên có. Phần thống kê thì để Ban lo. Điều chưa hỏi... à, có hộ nộp rồi sau đó tìm không thấy tên mình trong danh sách, thì mình mở lịch sử ra chứng minh được.

**Analyst note:** Củng cố nhu cầu lưu lịch sử nộp.

**Requirement candidates discovered:**
- Ưu tiên sơ bộ (Must): tự tính tiền, ghi nhận nộp, tìm hộ nhanh, xem công nợ, danh sách chưa nộp
- Ưu tiên sơ bộ (Should): in biên lai

---

## 5. Bảng truy vết của biên bản này

| Câu hỏi | Wish | RAW |
|---|---|---|
| Q01 | — | — |
| Q02 | WISH-12 | RAW-013 |
| Q03 | WISH-11, WISH-19 | RAW-011, 016, 028 |
| Q04 | — | RAW-013 (Notes) |
| Q05 | WISH-13 | RAW-013, 018 |
| Q06 | WISH-15 | RAW-015, 025 |
| Q07 | WISH-14 | RAW-014 |
| Q08 | WISH-16 | RAW-016, 017, 027 |
| Q09 | WISH-17, WISH-18 | RAW-018, 020 |
| Q10 | WISH-11 | RAW-011 |
| Q11 | WISH-19 | RAW-027, 028 |
| Q12 | — | Ưu tiên sơ bộ |
