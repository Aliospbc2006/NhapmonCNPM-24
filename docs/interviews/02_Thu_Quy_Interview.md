# SIM-INT-TQ — Phỏng vấn role-play: Thủ quỹ / Người thu phí

**Loại:** Phỏng vấn theo kịch bản (role-play) phục vụ Requirement Elicitation (bài tập môn học, không phải phỏng vấn thật).

| Mục | Giá trị |
|---|---|
| Mã biên bản | SIM-INT-TQ |
| Người được phỏng vấn | Thủ quỹ / người thu phí. Không có danh tính thật. |
| Người phỏng vấn | Analyst (thành viên nhóm đóng vai) |
| Hình thức | Role-play bằng văn bản. **Không phải buổi gặp thực tế.** Không có ngày, giờ, ghi âm, chữ ký hay ảnh. |
| Cơ sở | Đề bài BlueMoon (PS-01), quy trình As-Is giả định WA-01, biểu mẫu giả định DA-02 |

> Toàn bộ câu trả lời dưới đây là thông tin stakeholder theo kịch bản, do nhóm viết để phục vụ phân tích yêu cầu.

---

## 1. Mục tiêu phỏng vấn

- Hiểu chi tiết thao tác thu phí hằng ngày và các tình huống ngoại lệ.
- Tìm pain point khi tìm hộ, tính tiền, ghi nhận, đối chiếu, lập biên lai.
- Thu nhu cầu tra cứu công nợ và nhu cầu về tốc độ, số người dùng đồng thời.
- Làm rõ điểm khác biệt có thể có so với Ban quản trị (ví dụ miễn giảm).

## 2. Vai trò người được phỏng vấn

Thủ quỹ / người thu phí: thao tác thu tiền, ghi sổ và lập biên lai tại văn phòng Ban quản trị. Là người dùng cuối tiếp xúc nhiều nhất với phần mềm ở v1.0 (phần thu phí, tra cứu). Chịu trách nhiệm đối chiếu số liệu thu với Ban quản trị cuối tháng.

## 3. Bối cảnh

Hằng tháng thủ quỹ nhận danh sách khoản phải thu từ Ban. Hộ nộp tại văn phòng. Thủ quỹ ghi sổ giấy, gõ lại Excel và viết biên lai tay. Có hộ nộp thiếu, nộp gộp, nộp nhầm. Chung cư có vài trăm hộ (AS-13).

---

## 4. Nội dung phỏng vấn

### SIM-INT-TQ-Q01 — Giới thiệu

**Câu hỏi:** Anh/chị giới thiệu vai trò của mình khi thu phí ở chung cư?

**Trả lời:**
Mình là thủ quỹ, lo việc thu tiền, ghi sổ và viết biên lai cho các hộ. Thường thu ở văn phòng Ban. Cuối tháng mình tổng hợp số đã thu để đưa lại cho Ban. Mình ghi chép cẩn thận nhưng việc tay chân nhiều nên cũng hay sót.

**Ghi chú của Analyst:** Xác định TQ là người dùng thao tác nhiều nhất (thu phí, tra cứu).

**Yêu cầu phát hiện được:** (bối cảnh, chưa có yêu cầu mới)

---

### SIM-INT-TQ-Q02 — Quy trình hiện tại: thu tiền

**Câu hỏi:** Anh/chị mô tả một lần thu phí điển hình, từ lúc hộ đến nộp tiền?

**Trả lời:**
Đầu tháng mình nhận danh sách từ Ban. Hộ đến nộp thì mình tìm tên hộ trên Excel hoặc sổ, thu tiền, ghi ngày nộp với số tiền, rồi viết biên lai tay hai liên, đưa một liên cho hộ. Có người nhờ người khác nộp hộ. Mình ghi vào sổ trước, tối gõ lại vào Excel. Mình muốn gõ một lần thôi: chọn hộ, chọn khoản, nhập số tiền và ngày là xong.

**Ghi chú của Analyst:** Khớp WA-01. Ghi hai lần là nguồn sai sót. Có người nộp hộ nên ghi nhận *người nộp* là thông tin phụ (chưa thành yêu cầu riêng, ghi vào Notes RAW-013).

**Yêu cầu phát hiện được:**
- Ghi nhận nộp tiền nhanh (hộ, khoản, số tiền, ngày, người thu) → RAW-013 (WISH-12)

---

### SIM-INT-TQ-Q03 — Khó khăn hiện tại

**Câu hỏi:** Điều gì khó khăn hoặc dễ nhầm nhất khi thu phí?

**Trả lời:**
Tính tiền tay bằng máy tính cầm tay, diện tích nhân đơn giá cho từng nhà, có mấy lần bấm nhầm. Tìm một nhà trong Excel mấy trăm dòng cũng lâu, nhất là lúc đông người xếp hàng. Tối còn phải gõ lại, mệt lắm.

**Ghi chú của Analyst:** Pain point: tính toán thủ công, tìm kiếm chậm, nhập hai lần. Dẫn đến yêu cầu tự tính phí, tìm nhanh, và NFR về tốc độ và dễ dùng.

**Yêu cầu phát hiện được:**
- Tự tính phí theo diện tích → RAW-011 (WISH-11)
- Tìm hộ nhanh → RAW-016
- Thao tác ít bước → RAW-028 (WISH-19)

---

### SIM-INT-TQ-Q04 — Hình thức nộp

**Câu hỏi:** Các hộ nộp tiền bằng cách nào?

**Trả lời:**
Phần lớn nộp tiền mặt ở văn phòng. Cũng có hộ chuyển khoản rồi nhắn cho mình, mình tự đối chiếu. Cái này tính sao thì mình không rõ, chắc ghi lại là tiền mặt hay chuyển khoản là đủ.

**Ghi chú của Analyst:** *Assumption AS-12:* v1.0 chỉ ghi nhận hình thức nộp (tiền mặt/chuyển khoản) như thông tin phụ, không tích hợp thanh toán online (ngoài phạm vi). *Open Question* OQ-09.

**Yêu cầu phát hiện được:**
- Lưu hình thức nộp trong giao dịch thu → bổ sung vào RAW-013 (Notes)

---

### SIM-INT-TQ-Q05 — Nộp thiếu, nộp gộp, nộp trước

**Câu hỏi:** Có những trường hợp hộ không nộp đủ hoặc nộp theo cách khác thường không?

**Trả lời:**
Có chứ. Hộ nộp thiếu, hứa tuần sau đóng nốt. Có hộ nộp một lần ba bốn tháng. Cũng có hộ đóng trước. Mình ghi chú bên lề sổ thôi, sau dễ quên. Phần mềm nên cho nộp một phần, nộp gộp nhiều khoản trong một lần, rồi báo còn thiếu bao nhiêu. Còn phạt chậm nộp thì Ban chưa nói gì với mình.

**Ghi chú của Analyst:** *Open Question* OQ-05: có tính phạt chậm nộp không (ngoài v1.0 nếu chưa xác nhận). Nộp trước (nhiều kỳ chưa phát sinh) cần xác thực chính sách.

**Yêu cầu phát hiện được:**
- Ghi nhận nộp một phần / nộp gộp → RAW-013 (WISH-13)
- Xem còn thiếu bao nhiêu → RAW-018

---

### SIM-INT-TQ-Q06 — Nhập sai, sửa, hủy

**Câu hỏi:** Khi nhập sai số tiền hoặc thu nhầm hộ thì hiện xử lý ra sao?

**Trả lời:**
Có lần mình nhập nhầm số tiền, có lần thu nhầm sang hộ khác. Trong sổ thì gạch rồi viết lại, còn Excel thì sửa đè luôn nên không còn dấu. Phần mềm cho sửa hoặc hủy thì được, nhưng nên ghi lý do, và đừng xóa hẳn kẻo mình bị hỏi.

**Ghi chú của Analyst:** Khớp BQT-Q09. Cùng hướng với AS-17: sửa/hủy có lý do, lưu vết.

**Yêu cầu phát hiện được:**
- Hủy/điều chỉnh giao dịch có lý do → RAW-015 (WISH-15)
- Lưu vết thao tác → RAW-025

---

### SIM-INT-TQ-Q07 — Biên lai

**Câu hỏi:** Biên lai hiện được lập thế nào và anh/chị muốn gì ở phần mềm?

**Trả lời:**
Biên lai viết tay tốn thời gian, chữ xấu cư dân cũng phàn nàn. Mình muốn in phiếu thu có số căn hộ, khoản thu, số tiền, ngày nộp, người thu. Có hộ không cần nhưng nhiều hộ hay đòi giữ.

**Ghi chú của Analyst:** Biên lai không nằm rõ trong đề bài; ghi là *Assumption* ưu tiên Should. Mẫu biên lai chính thức cần xác nhận (OQ-06).

**Yêu cầu phát hiện được:**
- In/xuất biên lai → RAW-014 (WISH-14)

---

### SIM-INT-TQ-Q08 — Tìm kiếm

**Câu hỏi:** Anh/chị thường tìm thông tin gì và tìm theo cách nào?

**Trả lời:**
Cư dân đến thường nói số căn hộ, có người chỉ nhớ tên chủ hộ, mà trùng họ tên thì dễ nhầm. Phải tìm theo số căn hộ trước, rồi theo tên. Tìm xong thấy ngay số tiền phải nộp của hộ đó. Thỉnh thoảng cũng cần tìm theo tên một người trong nhà.

**Ghi chú của Analyst:** Tìm hộ là thao tác nhiều nhất. Tìm nhân khẩu cũng được nhắc.

**Yêu cầu phát hiện được:**
- Tìm hộ theo số căn hộ, tên chủ hộ → RAW-016 (WISH-16)
- Tìm nhân khẩu theo tên → RAW-017
- Thời gian phản hồi nhanh → RAW-027

---

### SIM-INT-TQ-Q09 — Công nợ và nhắc nộp

**Câu hỏi:** Anh/chị cần xem thông tin gì để biết hộ nào còn chưa nộp?

**Trả lời:**
Mình hay phải xem nhà nào còn thiếu để nhắc. Muốn lọc ra danh sách chưa nộp theo tháng, và mở từng hộ để xem các tháng đã đóng, còn thiếu tháng nào, thiếu bao nhiêu.

**Ghi chú của Analyst:** Hai nhu cầu khác nhau: (1) báo cáo theo kỳ trên toàn hộ (RAW-020); (2) xem công nợ chi tiết một hộ (RAW-018).

**Yêu cầu phát hiện được:**
- Xem công nợ, lịch sử nộp của một hộ → RAW-018 (WISH-17)
- Danh sách hộ chưa nộp theo kỳ → RAW-020 (WISH-18)

---

### SIM-INT-TQ-Q10 — Tính phí và miễn giảm

**Câu hỏi:** Việc tính số tiền mỗi hộ phải nộp hiện làm thế nào, có trường hợp đặc biệt nào không?

**Trả lời:**
Đơn giá thì Ban đưa, mình nhân theo diện tích. Nhưng đôi khi có hộ được Ban cho miễn hoặc giảm, kiểu hộ khó khăn. Mình nghĩ phải cho nhập điều chỉnh được... à mà Ban nói với mình cái này là tùy trường hợp, không có quy định nào cố định. Anh chị hỏi lại Ban nhé.

**Ghi chú của Analyst:** **Conflict C-02:** BQT-Q06 nghĩ mọi căn cùng đơn giá, TQ nhắc có miễn giảm. Chưa có quy tắc, nên *Assumption AS-14:* miễn/giảm không thuộc v1.0 nếu BQT chưa xác nhận (OQ-02).

**Yêu cầu phát hiện được:**
- Tự tính phí theo diện tích × đơn giá → RAW-011
- Miễn/giảm: chưa thành yêu cầu (Open Question)

---

### SIM-INT-TQ-Q11 — Số người dùng, quy mô và hiệu năng

**Câu hỏi:** Có bao nhiêu người cùng thao tác trong lúc thu phí, và anh/chị kỳ vọng tốc độ ra sao?

**Trả lời:**
Văn phòng có vài người thôi. Lúc thu phí thường mình với một bạn nữa cùng nhập. Chung cư vài trăm hộ chứ không nhiều lắm. Phần mềm mà chậm là khách xếp hàng, nên tìm kiếm phải nhanh, nhập ít bước thôi.

**Ghi chú của Analyst:** *Assumption AS-13:* quy mô vài trăm hộ, vài nghìn nhân khẩu; dữ liệu tập trung trên MySQL (đề bài) cho phép 2–3 người dùng đồng thời. Con số cụ thể cần xác thực (OQ-10).

**Yêu cầu phát hiện được:**
- Phản hồi nhanh khi tìm và liệt kê → RAW-027 (WISH-19)
- Ghi nhận nộp tiền ít thao tác → RAW-028

---

### SIM-INT-TQ-Q12 — Ưu tiên và kết thúc

**Câu hỏi:** Việc nào là quan trọng nhất đối với anh/chị? Còn điều gì chúng tôi chưa hỏi?

**Trả lời:**
Mình ưu tiên: tự tính tiền, ghi nhận nộp, tìm hộ nhanh, danh sách chưa nộp. In biên lai nên có. Phần thống kê thì để Ban lo. Điều chưa hỏi... à, có hộ nộp rồi sau đó tìm không thấy tên mình trong danh sách, thì mình mở lịch sử ra chứng minh được.

**Ghi chú của Analyst:** Củng cố nhu cầu lưu lịch sử nộp.

**Yêu cầu phát hiện được:**
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
