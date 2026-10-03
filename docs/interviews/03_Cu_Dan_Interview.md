# SIM-INT-CD — Role-play Interview: Chủ hộ / Cư dân

**Loại:** Simulated Interview / Role-play for Requirement Elicitation (bài tập môn học, không phải phỏng vấn thật).

| Mục | Giá trị |
|---|---|
| Mã biên bản | SIM-INT-CD |
| Người được phỏng vấn | Vai trò giả lập: Chủ hộ / cư dân đang sống tại BlueMoon. Không có danh tính thật. |
| Người phỏng vấn | Analyst (thành viên nhóm đóng vai) |
| Hình thức | Role-play bằng văn bản. **Không phải khảo sát cư dân thực tế.** Không có ngày, giờ, ghi âm, chữ ký hay ảnh. |
| Cơ sở | Đề bài BlueMoon (PS-01), quy trình As-Is giả định WA-01 và WA-02 |

> Toàn bộ câu trả lời dưới đây là **Simulated stakeholder input**, do nhóm viết để phục vụ phân tích yêu cầu. Cư dân **không** là người dùng hệ thống v1.0 (AS-02); biên bản này thu quan điểm của bên đóng phí và bên được quản lý thông tin.

---

## 1. Interview objective

- Hiểu trải nghiệm của cư dân khi biết khoản phải nộp, nộp phí và đối chiếu.
- Tìm nhu cầu về chứng từ, minh bạch khoản phí và quỹ đóng góp.
- Hiểu cách cư dân khai báo thay đổi nhân khẩu, tạm trú, tạm vắng.
- Thu lo ngại về bảo mật dữ liệu cá nhân và các mong muốn ngoài phạm vi v1.0.

## 2. Stakeholder role

Chủ hộ (đại diện hộ gia đình) đóng phí dịch vụ, phí quản lý và có thể góp quỹ tự nguyện. Cung cấp và cập nhật thông tin hộ, nhân khẩu cho Ban quản trị. Không trực tiếp dùng phần mềm ở v1.0.

## 3. Context

Cư dân nhận thông báo khoản phải đóng, nộp tiền mặt tại văn phòng Ban quản trị và nhận biên lai. Các khoản đóng góp được thông báo theo từng đợt, không bắt buộc. Thay đổi nhân khẩu được báo trực tiếp cho Ban.

---

## 4. Interview

### SIM-INT-CD-Q01 — Introduction

**Question:** Anh/chị giới thiệu ngắn về gia đình và việc liên hệ với Ban quản trị?

**Simulated stakeholder answer:**
Mình là chủ hộ một căn hộ ở BlueMoon, sống cùng gia đình. Ít khi lên văn phòng Ban quản trị ngoài lúc đóng phí hoặc khi có việc cần báo, chẳng hạn nhà có thêm người.

**Analyst note:** Cư dân tiếp xúc thưa, nên mọi trải nghiệm gắn với thông báo, nộp phí, khai báo.

**Requirement candidates discovered:** (bối cảnh, chưa có yêu cầu mới)

---

### SIM-INT-CD-Q02 — Current process / As-Is

**Question:** Hiện nay anh/chị biết mình phải đóng bao nhiêu và đóng như thế nào?

**Simulated stakeholder answer:**
Đầu tháng có thông báo, khi thì tờ giấy, khi thì tin nhắn trong nhóm cư dân, ghi số tiền phải đóng. Mình lên văn phòng nộp tiền mặt, được viết biên lai. Quỹ đóng góp thì có thông báo theo đợt, tùy tâm.

**Analyst note:** Khớp WA-01. Thông báo hiện ở ngoài hệ thống (AS-07).

**Requirement candidates discovered:** (bối cảnh, chưa có yêu cầu mới)

---

### SIM-INT-CD-Q03 — Pain Points

**Question:** Anh/chị gặp khó khăn gì khi đóng phí?

**Simulated stakeholder answer:**
Có tháng mình không hiểu số tiền được tính thế nào, chỉ thấy một tổng. Có tháng quên mất đã đóng chưa, tìm lại biên lai không thấy. Muốn hỏi thì lại ngại phải lên văn phòng.

**Analyst note:** Pain point: thiếu minh bạch cách tính, khó đối chiếu lịch sử. Người dùng là BQT, nhưng phần mềm phải xuất được thông tin giúp BQT trả lời cư dân.

**Requirement candidates discovered:**
- Hiển thị cách tính (diện tích, đơn giá) trên chứng từ → RAW-011, RAW-014 (WISH-20)
- Tra lịch sử nộp của một hộ → RAW-018

---

### SIM-INT-CD-Q04 — Chứng từ nộp tiền

**Question:** Khi nộp phí, anh/chị mong muốn nhận được gì?

**Simulated stakeholder answer:**
Mình muốn có giấy xác nhận đã nộp, ghi rõ nộp khoản gì, tháng nào, bao nhiêu, ngày nào. Tốt nhất có cả diện tích và đơn giá để mình hiểu số đó ra sao. Biên lai hiện tại có khi thiếu mất tháng.

**Analyst note:** Chứng từ rõ ràng là nhu cầu chung của cư dân và thủ quỹ (TQ-Q07).

**Requirement candidates discovered:**
- Biên lai có đủ khoản, kỳ, số tiền, ngày → RAW-014 (WISH-20)
- Hiển thị cách tính (diện tích, đơn giá) → RAW-011 (WISH-20)

---

### SIM-INT-CD-Q05 — Khoản đóng góp tự nguyện

**Question:** Anh/chị nghĩ gì về các khoản đóng góp theo đợt?

**Simulated stakeholder answer:**
Các khoản đóng góp mình hay đóng nhưng không biết cuối cùng thu được bao nhiêu, bao nhiêu hộ góp. Mình muốn rõ ràng. Mà đây là tự nguyện, đừng ghi tên hộ nào chưa đóng rồi nhắc, người ta khó chịu.

**Analyst note:** Cần minh bạch tổng thu (thống kê) nhưng không coi hộ chưa đóng khoản tự nguyện là nợ (AS-19). **Conflict C-07** với CQ-Q07 (CQ muốn danh sách hộ tham gia).

**Requirement candidates discovered:**
- Khoản tự nguyện theo đợt, không bắt buộc → RAW-012 (WISH-21)
- Tổng thu từng đợt → RAW-019

---

### SIM-INT-CD-Q06 — Khai báo thay đổi nhân khẩu

**Question:** Khi gia đình có thay đổi (thêm người, người ở tạm, vắng mặt), anh/chị báo cho Ban thế nào?

**Simulated stakeholder answer:**
Nhà mình có thêm em bé, và có người thân ở tạm vài tháng. Mình chỉ báo miệng với Ban hoặc đưa giấy, không biết có ghi lại không. Lúc đi vắng dài ngày mình cũng báo. Mong Ban ghi nhận đúng và có thời gian rõ ràng.

**Analyst note:** Cư dân khai báo qua Ban quản trị (BQT nhập). Cần ghi thời gian bắt đầu, kết thúc của tạm trú và tạm vắng.

**Requirement candidates discovered:**
- Thêm/sửa nhân khẩu → RAW-006
- Ghi nhận biến động nhân khẩu → RAW-007
- Tạm trú / tạm vắng có thời gian → RAW-008 (WISH-22)

---

### SIM-INT-CD-Q07 — Bảo mật dữ liệu cá nhân

**Question:** Anh/chị có lo ngại gì về thông tin cá nhân khi lưu vào phần mềm?

**Simulated stakeholder answer:**
Mình lo thông tin như số giấy tờ, số điện thoại của cả nhà bị lộ. Chỉ Ban quản trị biết thôi, đừng ai cũng xem được. Còn đưa cho cơ quan thì phải theo yêu cầu thật. Mình cũng không muốn người nào trong Ban cũng xem tùy ý.

**Analyst note:** Yêu cầu bảo vệ dữ liệu cá nhân và phân quyền. **Conflict C-03:** CQ-Q09 cần giấy tờ đầy đủ khi gửi cơ quan; giải pháp đề xuất: che bớt khi hiển thị thường ngày, chỉ người có quyền mới thấy và xuất.

**Requirement candidates discovered:**
- Bảo vệ dữ liệu cá nhân → RAW-024 (WISH-23)
- Phân quyền → RAW-023
- Chỉ người đăng nhập mới truy cập → RAW-001, RAW-022

---

### SIM-INT-CD-Q08 — Mong muốn tự xem thông tin

**Question:** Anh/chị có muốn tự xem thông tin phí của mình không, và bằng cách nào?

**Simulated stakeholder answer:**
Nếu xem được số tiền và lịch sử đóng trên điện thoại thì tiện lắm, khỏi lên văn phòng.

**Analyst note:** **Conflict C-04:** đề bài mô tả ứng dụng desktop cho Ban quản trị (AS-02). Ghi nhận là mong muốn của cư dân, **ngoài phạm vi v1.0** (Won't-have), có thể đưa vào roadmap sau.

**Requirement candidates discovered:**
- Cư dân tự xem phí, lịch sử qua điện thoại → WISH-24 (Out of v1.0; không tạo RAW)

---

### SIM-INT-CD-Q09 — Nhắc nộp phí

**Question:** Anh/chị có mong muốn được nhắc khi đến hạn nộp không?

**Simulated stakeholder answer:**
Có tin nhắn nhắc trước hạn thì đỡ quên.

**Analyst note:** Gửi thông báo hoặc nhắc tự động ngoài phạm vi v1.0 (AS-07). Ban có thể dùng danh sách hộ chưa nộp (RAW-020) để nhắc thủ công. **Conflict C-05** với kỳ vọng nhắc tự động.

**Requirement candidates discovered:**
- Nhắc nộp phí tự động → WISH-25 (Out of v1.0; không tạo RAW)

---

### SIM-INT-CD-Q10 — Phí gửi xe, điện, nước, internet

**Question:** Anh/chị đóng phí gửi xe và điện, nước, internet hiện nay thế nào?

**Simulated stakeholder answer:**
Gửi xe thì mình trả riêng, điện nước internet cũng trả riêng. Nếu gộp một chỗ thì tiện, nhưng chắc để sau cũng được, giờ cứ lo phí chung cư cho ổn đã.

**Analyst note:** Củng cố roadmap v2.0, **Won't-have v1.0**. Mô tả hiện trạng ở đây là giả lập.

**Requirement candidates discovered:**
- Gộp phí xe, điện, nước, internet → RAW-029, RAW-030 (Roadmap v2.0)

---

### SIM-INT-CD-Q11 — Sửa sai và điều chỉnh

**Question:** Nếu thông tin hoặc số tiền của gia đình bị ghi sai thì anh/chị muốn xử lý thế nào?

**Simulated stakeholder answer:**
Có lần Ban ghi diện tích nhà mình sai, may mình để ý. Nếu sai thì phải sửa được và tính lại phần bị sai, đừng để ảnh hưởng nhiều tháng. Cũng phải biết mình đã nộp thừa hay thiếu bao nhiêu.

**Analyst note:** Cần chính sách tính lại khi sửa diện tích hoặc hủy giao dịch (OQ-14). Cùng hướng với RAW-004, RAW-015.

**Requirement candidates discovered:**
- Sửa thông tin hộ khi sai → RAW-004
- Hủy/điều chỉnh giao dịch → RAW-015
- Biết nộp thừa/thiếu → RAW-018

---

### SIM-INT-CD-Q12 — Priority và Closing

**Question:** Điều gì quan trọng nhất với anh/chị? Còn điều gì chúng tôi chưa hỏi?

**Simulated stakeholder answer:**
Quan trọng nhất là tính đúng, có biên lai rõ, và thông tin của nhà mình được giữ kín. Còn lại tính sau. Chưa hỏi gì thêm, mình chỉ mong đỡ phải lên lui nhiều lần.

**Analyst note:** Ưu tiên của cư dân: chính xác, chứng từ, riêng tư.

**Requirement candidates discovered:**
- Ưu tiên sơ bộ: tính đúng, có biên lai rõ, giữ kín thông tin cá nhân

---

## 5. Bảng truy vết của biên bản này

| Câu hỏi | Wish | RAW |
|---|---|---|
| Q01 | — | — |
| Q02 | — | RAW-011, 012 (bối cảnh) |
| Q03 | WISH-20 | RAW-011, 014, 018 |
| Q04 | WISH-20 | RAW-014 |
| Q05 | WISH-21 | RAW-012, 019 |
| Q06 | WISH-22 | RAW-006, 007, 008 |
| Q07 | WISH-23 | RAW-001, 022, 023, 024 |
| Q08 | WISH-24 | Out of v1.0 |
| Q09 | WISH-25 | Out of v1.0 |
| Q10 | — | RAW-029, 030 (roadmap) |
| Q11 | — | RAW-004, 015, 018 |
| Q12 | — | Ưu tiên sơ bộ |
