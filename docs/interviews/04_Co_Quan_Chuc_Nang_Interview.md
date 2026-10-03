# SIM-INT-CQ — Role-play Interview: Đại diện cơ quan chức năng

**Loại:** Simulated Interview / Role-play for Requirement Elicitation (bài tập môn học, không phải phỏng vấn thật).

| Mục | Giá trị |
|---|---|
| Mã biên bản | SIM-INT-CQ |
| Người được phỏng vấn | Vai trò giả lập chung: đại diện chính quyền địa phương / tổ dân phố phối hợp với Ban quản trị. Không có danh tính hay đơn vị cụ thể. |
| Người phỏng vấn | Analyst (thành viên nhóm đóng vai) |
| Hình thức | Role-play bằng văn bản. **Không phải buổi gặp thực tế.** Không có ngày, giờ, ghi âm, chữ ký hay ảnh. |
| Cơ sở | Đề bài BlueMoon (PS-01: cung cấp thông tin cho cơ quan chức năng, thu đóng góp phối hợp chính quyền và tổ dân phố), WA-02 |

> Toàn bộ câu trả lời dưới đây là **Simulated stakeholder input**, do nhóm viết để phục vụ phân tích yêu cầu. Nội dung về trường thông tin hoặc biểu mẫu mà cơ quan yêu cầu là **giả định chung**, không trích dẫn quy định pháp luật cụ thể; cần xác thực với nguồn chính thức nếu triển khai thật (OQ-07).

---

## 1. Interview objective

- Hiểu khi nào và vì sao cơ quan chức năng cần thông tin hộ, nhân khẩu từ Ban quản trị.
- Xác định các trường thông tin, dạng báo cáo và độ chính xác cần có.
- Hiểu vai trò phối hợp trong các khoản đóng góp tự nguyện.
- Thu yêu cầu về bảo mật và trách nhiệm khi cung cấp dữ liệu cá nhân.

## 2. Stakeholder role

Đại diện chính quyền địa phương / tổ dân phố, vai trò chung. Yêu cầu Ban quản trị cung cấp thông tin hộ và nhân khẩu khi cần; phối hợp thu các khoản đóng góp theo đợt. **Không** dùng phần mềm; Ban quản trị là đầu mối duy nhất (AS-16).

## 3. Context

Đề bài nêu Ban quản trị cần cung cấp thông tin chi tiết hộ gia đình, nhân khẩu, biến đổi nhân khẩu, tạm vắng, tạm trú cho cơ quan chức năng khi được yêu cầu, và có các khoản đóng góp phối hợp với chính quyền và tổ dân phố.

---

## 4. Interview

### SIM-INT-CQ-Q01 — Introduction

**Question:** Anh/chị giới thiệu vai trò của mình khi làm việc với Ban quản trị chung cư?

**Simulated stakeholder answer:**
Mình đại diện bên chính quyền địa phương, phối hợp với Ban quản trị về việc nắm thông tin cư trú và một số khoản đóng góp. Mình không dùng phần mềm của Ban, chỉ nhận thông tin khi cần.

**Analyst note:** Xác định CQ không phải người dùng hệ thống; ảnh hưởng tới yêu cầu xuất thông tin.

**Requirement candidates discovered:** (bối cảnh, ủng hộ AS-16)

---

### SIM-INT-CQ-Q02 — Current process / As-Is

**Question:** Khi cần thông tin về hộ dân, quy trình hiện nay diễn ra thế nào?

**Simulated stakeholder answer:**
Khi cần thống kê hộ dân hay kiểm tra thông tin cư trú, bên mình gửi yêu cầu cho Ban quản trị, Ban tổng hợp danh sách rồi gửi lại. Thường là file hoặc bản in. Có khi mất vài ngày vì Ban phải ngồi gom.

**Analyst note:** Khớp WA-02. Thời gian chờ do tổng hợp thủ công.

**Requirement candidates discovered:**
- Xuất nhanh danh sách hộ và nhân khẩu → RAW-009 (WISH-26)

---

### SIM-INT-CQ-Q03 — Pain Points

**Question:** Điều gì gây khó khăn khi nhận thông tin từ Ban quản trị?

**Simulated stakeholder answer:**
Thông tin hay thiếu, mỗi lần gửi mỗi khác, nhất là người ở tạm hoặc đang vắng. Có hộ đã chuyển đi mà danh sách vẫn còn tên.

**Analyst note:** Pain point: dữ liệu không nhất quán, không cập nhật. Dẫn đến nhu cầu lịch sử biến động và tình trạng cư trú rõ ràng.

**Requirement candidates discovered:**
- Tình trạng cư trú rõ ràng → RAW-008
- Lịch sử biến động → RAW-007

---

### SIM-INT-CQ-Q04 — Trường thông tin cần có

**Question:** Anh/chị thường cần những thông tin nào của hộ và nhân khẩu?

**Simulated stakeholder answer:**
Thường cần họ tên, ngày sinh, giới tính, quan hệ với chủ hộ, số giấy tờ tùy thân, và tình trạng cư trú là thường xuyên, tạm trú hay tạm vắng, kèm thời hạn. Còn biểu mẫu cụ thể thì tùy từng lần yêu cầu, mình cũng không nhớ hết.

**Analyst note:** *Assumption AS-18:* v1.0 lưu các trường cơ bản trên; biểu mẫu và trường chính xác theo quy định hiện hành cần xác thực (OQ-07). Việc lưu số giấy tờ tùy thân là điểm cần thận trọng về bảo mật (OQ-08).

**Requirement candidates discovered:**
- Thông tin nhân khẩu cơ bản và quan hệ chủ hộ → RAW-006
- Tình trạng cư trú, thời hạn tạm trú/tạm vắng → RAW-008 (WISH-27)

---

### SIM-INT-CQ-Q05 — Dạng cung cấp và tra cứu nhanh

**Question:** Thông tin nên được cung cấp dưới dạng nào, và khi có yêu cầu kiểm tra một người cụ thể thì sao?

**Simulated stakeholder answer:**
Danh sách theo căn hộ, in ra hoặc file bảng tính, Ban đóng dấu xác nhận. Khi cần kiểm tra một người thì phải tra nhanh được theo tên, đừng để mình chờ cả buổi.

**Analyst note:** Việc đóng dấu xác nhận nằm ngoài hệ thống (AS-16). Tra cứu nhanh một người ứng với tìm nhân khẩu.

**Requirement candidates discovered:**
- In/xuất danh sách → RAW-009 (WISH-26)
- Tìm nhân khẩu theo tên → RAW-017

---

### SIM-INT-CQ-Q06 — Biến động nhân khẩu

**Question:** Anh/chị cần biết những biến động nhân khẩu nào?

**Simulated stakeholder answer:**
Mình cần biết ai chuyển đến, chuyển đi, sinh, mất, vào ngày nào, để đối chiếu. Giữ lịch sử, đừng xóa người đã đi, vì sau này có khi hỏi lại.

**Analyst note:** Khớp đề bài (biến đổi nhân khẩu). Không xóa cứng (AS-17). Danh sách loại biến động cần chốt với Ban (OQ-13).

**Requirement candidates discovered:**
- Biến động nhân khẩu có ngày và lý do, giữ lịch sử → RAW-007 (WISH-28)

---

### SIM-INT-CQ-Q07 — Quỹ đóng góp phối hợp

**Question:** Anh/chị cần thông tin gì liên quan đến các khoản đóng góp phối hợp thu?

**Simulated stakeholder answer:**
Các quỹ đóng góp thì Ban phối hợp với bên mình. Mình cần biết tổng thu từng đợt và danh sách hộ đã đóng để báo cáo. Nhưng đây là tự nguyện, đừng ghi hộ chưa đóng thành hộ nợ.

**Analyst note:** **Conflict C-07:** CQ muốn danh sách hộ đã đóng, CD không muốn bị nhắc tên khi chưa đóng. Đề xuất: báo cáo đợt ghi tổng thu và danh sách hộ đã đóng, không có khái niệm "nợ" đối với khoản tự nguyện (AS-19).

**Requirement candidates discovered:**
- Tổng thu và danh sách hộ đã đóng theo đợt → RAW-012, RAW-019 (WISH-30)

---

### SIM-INT-CQ-Q08 — Truy cập hệ thống

**Question:** Cơ quan có cần truy cập trực tiếp vào phần mềm không?

**Simulated stakeholder answer:**
Không, bên mình không vào phần mềm. Ban là đầu mối duy nhất, mình hỏi thì Ban trả lời.

**Analyst note:** Củng cố AS-02 và AS-16: không có tài khoản cho cơ quan chức năng ở v1.0.

**Requirement candidates discovered:** (không có yêu cầu mới; củng cố AS-16)

---

### SIM-INT-CQ-Q09 — Bảo mật và trách nhiệm khi cung cấp

**Question:** Khi Ban cung cấp thông tin cá nhân, anh/chị có yêu cầu gì về bảo mật và trách nhiệm?

**Simulated stakeholder answer:**
Thông tin cá nhân chỉ nên cung cấp khi có yêu cầu hợp lệ. Ban nên ghi lại đã cung cấp gì, cho ai, lúc nào, và chỉ người được phân công mới được xuất. Số giấy tờ thì gửi cơ quan cần đầy đủ, nhưng hiển thị thường ngày che bớt cho an toàn.

**Analyst note:** **Conflict C-03** (nhưng cùng hướng giải pháp với CD-Q07): lưu đủ, che khi hiển thị, giới hạn quyền xuất, ghi log việc xuất.

**Requirement candidates discovered:**
- Bảo vệ dữ liệu cá nhân, giới hạn quyền xuất → RAW-024
- Ghi nhận lần xuất dữ liệu → RAW-025

---

### SIM-INT-CQ-Q10 — Độ chính xác và cập nhật kịp thời

**Question:** Anh/chị kỳ vọng dữ liệu được cập nhật kịp thời đến mức nào?

**Simulated stakeholder answer:**
Biến động nên cập nhật sớm, tốt nhất khi vừa phát sinh. Thời hạn cụ thể thì tùy Ban tự quy định. Tạm trú hay tạm vắng mà hết thời hạn thì phần mềm nên đánh dấu để Ban biết.

**Analyst note:** Quy tắc thời hạn cập nhật là quy trình nội bộ của Ban, ngoài phạm vi phần mềm (OQ-13). Đánh dấu tạm trú/tạm vắng hết hạn: hỗ trợ RAW-008.

**Requirement candidates discovered:**
- Đánh dấu tạm trú/tạm vắng hết hạn → RAW-008 (Notes)

---

### SIM-INT-CQ-Q11 — Thống kê theo thời điểm

**Question:** Anh/chị có cần báo cáo tổng hợp theo thời điểm không?

**Simulated stakeholder answer:**
Có yêu cầu tổng hợp số hộ, số nhân khẩu, bao nhiêu người tạm trú, tạm vắng tại một thời điểm, ví dụ hết quý. Số liệu phải ghi rõ tính đến ngày nào.

**Analyst note:** Thống kê theo thời điểm đòi hỏi dữ liệu biến động có ngày (RAW-007).

**Requirement candidates discovered:**
- Thống kê số hộ, nhân khẩu, tạm trú, tạm vắng tại thời điểm → RAW-021 (WISH-29)

---

### SIM-INT-CQ-Q12 — Priority và Closing

**Question:** Điều gì quan trọng nhất với anh/chị? Còn điều gì chúng tôi chưa hỏi?

**Simulated stakeholder answer:**
Quan trọng nhất: danh sách chính xác, có tình trạng cư trú, có lịch sử biến động và xuất nhanh được. Còn lại tùy Ban. Mình chưa có gì thêm.

**Analyst note:** Ưu tiên của CQ gắn với nhóm chức năng nhân khẩu.

**Requirement candidates discovered:**
- Ưu tiên sơ bộ: danh sách chính xác, tình trạng cư trú, lịch sử biến động, xuất nhanh

---

## 5. Bảng truy vết của biên bản này

| Câu hỏi | Wish | RAW |
|---|---|---|
| Q01 | — | — |
| Q02 | WISH-26 | RAW-009 |
| Q03 | — | RAW-007, 008 |
| Q04 | WISH-27 | RAW-006, 008 |
| Q05 | WISH-26 | RAW-009, 017 |
| Q06 | WISH-28 | RAW-007 |
| Q07 | WISH-30 | RAW-012, 019 |
| Q08 | — | (AS-16) |
| Q09 | — | RAW-024, 025 |
| Q10 | — | RAW-008 (Notes) |
| Q11 | WISH-29 | RAW-021 |
| Q12 | — | Ưu tiên sơ bộ |
