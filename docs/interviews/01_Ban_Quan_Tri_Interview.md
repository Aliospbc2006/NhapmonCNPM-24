# SIM-INT-BQT — Phỏng vấn role-play: Đại diện Ban quản trị

**Loại:** Phỏng vấn theo kịch bản (role-play) phục vụ Requirement Elicitation (bài tập môn học, không phải phỏng vấn thật).

| Mục | Giá trị |
|---|---|
| Mã biên bản | SIM-INT-BQT |
| Người được phỏng vấn | Đại diện Ban quản trị (cấp quyết định). Không có danh tính thật. |
| Người phỏng vấn | Analyst (thành viên nhóm đóng vai) |
| Hình thức | Role-play bằng văn bản. **Không phải buổi gặp thực tế.** Không có ngày, giờ, ghi âm, chữ ký hay ảnh. |
| Cơ sở | Đề bài BlueMoon (PS-01, PS-02), hướng dẫn Elicitation (GD-01), suy luận nghiệp vụ hợp lý |

> Toàn bộ câu trả lời dưới đây là thông tin stakeholder theo kịch bản, do nhóm viết để phục vụ phân tích yêu cầu.

---

## 1. Mục tiêu phỏng vấn

- Hiểu quy trình quản lý thu phí và quản lý hộ, nhân khẩu hiện tại ở góc nhìn người quyết định.
- Làm rõ các khoản thu, cách tính, nhu cầu thống kê, phân quyền, sao lưu, truy vết.
- Xác định ranh giới phạm vi v1.0 và hạng mục để dành cho phiên bản sau.
- Thu ưu tiên sơ bộ của Ban quản trị.

## 2. Vai trò người được phỏng vấn

Đại diện Ban quản trị chung cư BlueMoon (do cư dân bầu). Người này quyết định phạm vi, ưu tiên và nghiệm thu, và dùng hệ thống với quyền quản trị. Các thành viên Ban đều kiêm nhiệm, không chuyên công nghệ thông tin.

## 3. Bối cảnh

Theo đề bài, Ban quản trị đang thu phí thủ công, có dùng Excel. Chung cư có 24 tầng nhà ở. Mỗi tháng Ban lập danh sách phí của từng hộ và gửi thông báo thu tiền. Ban còn phải quản lý thông tin hộ, nhân khẩu để cung cấp cho cơ quan chức năng khi được yêu cầu. Phần mềm dự kiến là ứng dụng desktop. Phí gửi xe và điện/nước/internet để sang v2.0.

---

## 4. Nội dung phỏng vấn

### SIM-INT-BQT-Q01 — Giới thiệu

**Câu hỏi:** Anh/chị giới thiệu ngắn về vai trò của mình trong Ban quản trị và việc quản lý chung cư hiện nay?

**Trả lời:**
Mình đại diện Ban quản trị, phụ trách chung việc quản lý và thu phí ở BlueMoon. Ban do cư dân bầu ra nên ai cũng kiêm nhiệm, không có ai chuyên về máy tính. Việc chính là thu đủ phí để lo vệ sinh, bảo dưỡng khu chung, và nắm được mỗi căn hộ đang có ai sống. Thu phí thì mỗi tháng một lần, còn quản lý cư dân thì phát sinh lúc nào làm lúc đó.

**Ghi chú của Analyst:** Người dùng không chuyên IT, dùng thường xuyên theo chu kỳ tháng. Ảnh hưởng đến độ dễ dùng.

**Yêu cầu phát hiện được:**
- Hệ thống phải dễ dùng với người không chuyên IT → RAW-028 (WISH-19)

---

### SIM-INT-BQT-Q02 — Quy trình hiện tại: thu phí

**Câu hỏi:** Hiện nay việc thu phí hằng tháng được thực hiện thế nào, từ đầu đến cuối?

**Trả lời:**
Đầu tháng bên mình lập danh sách các khoản mỗi hộ phải đóng rồi gửi thông báo. Phí dịch vụ với phí quản lý tính theo diện tích nhân đơn giá. Còn quỹ đóng góp thì theo từng đợt, ai tự nguyện thì đóng. Hộ nộp thì lên văn phòng, bạn thủ quỹ ghi sổ, tối nhập vào Excel. Cuối tháng đối chiếu rồi báo cáo lại cho mình. Thật ra có hai nơi ghi là sổ giấy và Excel, đôi khi hai bên không khớp nhau.

**Ghi chú của Analyst:** Khớp với WA-01 và đề bài. Dữ liệu ghi ở hai nơi là gốc của sai lệch. *Assumption:* thông báo thu tiền hiện làm ngoài hệ thống (AS-07).

**Yêu cầu phát hiện được:**
- Tạo khoản thu và lập danh sách phải thu theo hộ → RAW-010, RAW-011
- Ghi nhận nộp phí vào một nguồn dữ liệu duy nhất → RAW-013

---

### SIM-INT-BQT-Q03 — Khó khăn hiện tại

**Câu hỏi:** Điều gì gây khó khăn hoặc dễ sai sót nhất trong cách làm hiện tại?

**Trả lời:**
Khó nhất là muốn biết ngay hộ nào đã đóng, hộ nào còn thiếu thì phải mở Excel lọc rồi so lại sổ. Cuối tháng cư dân hỏi "tháng trước nhà tôi đóng chưa" là phải lục. Có lần ghi nhầm diện tích một căn hộ, thu sai mấy tháng liền mới phát hiện. Rồi chuyện số liệu giữa sổ với Excel lệch nhau nữa, mình không biết tin bên nào.

**Ghi chú của Analyst:** Pain point: tra công nợ chậm, dữ liệu sai do nhập tay, thiếu đối soát. Cần khả năng sửa thông tin hộ (diện tích) và tính lại. Chính sách tính lại khi diện tích sai là *Open Question* (OQ-14).

**Yêu cầu phát hiện được:**
- Xem tình trạng nộp của từng hộ → RAW-018
- Danh sách hộ chưa nộp → RAW-020
- Sửa thông tin hộ (diện tích) → RAW-004

---

### SIM-INT-BQT-Q04 — Hộ gia đình và nhân khẩu hiện tại

**Câu hỏi:** Việc quản lý thông tin hộ gia đình và nhân khẩu hiện nay ra sao, và Ban cung cấp thông tin cho cơ quan chức năng thế nào?

**Trả lời:**
Thông tin hộ với nhân khẩu nằm trong một file Excel cũ và sổ ghi tay. Có người chuyển đến, tạm vắng hay đổi chủ căn hộ thì cập nhật không đều, có khi quên. Khi cơ quan chức năng hỏi danh sách thì phải ngồi gom lại, mất cả buổi. Mình muốn mọi thứ nằm một chỗ: từng hộ ai là chủ hộ, có mấy người, ai ở tạm, ai đang vắng. Đổi chủ căn hộ thì phải còn lịch sử, đừng xóa mất người cũ. À, dữ liệu cũ đang nằm trong Excel, mình mong có người nhập giúp vào phần mềm luôn.

**Ghi chú của Analyst:** Khớp WA-02. Yêu cầu nhập liệu ban đầu mâu thuẫn với ví dụ Charter (Bài 4.1, Chương 4, chỉ tham khảo: phạm vi dự án **không** gồm nhập liệu; giả định AS-08 của nhóm) → ghi *Open Question* (OQ-12); import Excel không đưa vào v1.0 nếu chưa xác nhận.

**Yêu cầu phát hiện được:**
- Thêm, xem, cập nhật hộ gia đình → RAW-003, RAW-004
- Đổi chủ hộ / hộ chuyển đi, giữ lịch sử → RAW-005
- Quản lý nhân khẩu và biến động → RAW-006, RAW-007, RAW-008
- Xuất danh sách cho cơ quan chức năng → RAW-009

---

### SIM-INT-BQT-Q05 — Mong muốn

**Câu hỏi:** Nếu có phần mềm, anh/chị muốn nó giúp được những việc gì đầu tiên?

**Trả lời:**
Mình chọn vài việc trước. Một là thu phí cho gọn: tạo khoản thu, ghi nhận ai nộp bao nhiêu. Hai là quản lý hộ và nhân khẩu. Ba là xem được thống kê tình hình thu. Với lại tìm một hộ phải nhanh, gõ số căn hộ hoặc tên chủ hộ là ra.

**Ghi chú của Analyst:** Khớp 7 nhóm chức năng v1.0. Câu trả lời chưa nhắc đăng nhập (xem Q08).

**Yêu cầu phát hiện được:**
- Quản lý hộ tập trung → RAW-003, RAW-004 (WISH-02)
- Tìm hộ nhanh → RAW-016
- Tạo khoản thu, ghi nhận nộp, thống kê → RAW-010, RAW-013, RAW-019

---

### SIM-INT-BQT-Q06 — Khoản thu và cách tính

**Câu hỏi:** Các khoản thu hiện có là gì và được tính như thế nào?

**Trả lời:**
Có ba loại chính. Phí dịch vụ và phí quản lý là bắt buộc, thu theo tháng, tính theo diện tích căn hộ. Còn các khoản đóng góp thì theo từng đợt, tự nguyện, ai muốn đóng bao nhiêu thì đóng. Đơn giá do Ban quyết định và thỉnh thoảng điều chỉnh, nên đừng cố định cứng trong phần mềm. Mình nghĩ mọi căn cùng một đơn giá... à mà tầng 1 là kiot, chưa biết có tính khác không, phải bàn lại trong Ban.

**Ghi chú của Analyst:** Khớp đề bài (PS-01). Đơn giá phải cấu hình được (AS-05). Có điểm chưa chắc về kiot/penthouse: *Open Question* OQ-03. Câu trả lời này có thể mâu thuẫn với TQ-Q10 (miễn giảm).

**Yêu cầu phát hiện được:**
- Tạo và quản lý khoản thu, cấu hình đơn giá → RAW-010
- Tự tính phí theo diện tích × đơn giá → RAW-011
- Khoản đóng góp tự nguyện theo đợt → RAW-012

---

### SIM-INT-BQT-Q07 — Thống kê

**Câu hỏi:** Anh/chị cần xem những số liệu thống kê nào?

**Trả lời:**
Mình cần xem tổng tiền đã thu và còn thiếu theo từng khoản, theo tháng hoặc theo đợt. Muốn thấy luôn danh sách hộ chưa nộp. Thêm số hộ, số nhân khẩu hiện tại, bao nhiêu người tạm trú, tạm vắng. Cũng không cần quá cầu kỳ, biểu đồ đẹp thì để sau. Nhưng mà họp cư dân thì mình hay cần số liệu theo từng hộ nữa.

**Ghi chú của Analyst:** Có chút không nhất quán ("không cầu kỳ" nhưng cần nhiều chiều). Giữ ở mức thống kê cơ bản và đưa ra xác thực với Ban. Biểu đồ: *Won't-have* cho v1.0 (chưa xác nhận).

**Yêu cầu phát hiện được:**
- Thống kê tiền đã thu, còn phải thu theo khoản và kỳ → RAW-019
- Danh sách hộ chưa nộp → RAW-020
- Thống kê số hộ, nhân khẩu, tạm trú, tạm vắng → RAW-021

---

### SIM-INT-BQT-Q08 — Truy cập, phân quyền, tài khoản

**Câu hỏi:** Ai sẽ dùng phần mềm, và anh/chị muốn kiểm soát việc truy cập thế nào?

**Trả lời:**
Chỉ Ban quản trị dùng, cư dân không vào. Tài khoản do Ban cấp, không cần ai tự đăng ký. Mình nghĩ đơn giản nhất là cả Ban dùng chung một tài khoản cho tiện... nhưng nếu vậy lỡ sai thì ai chịu nhỉ. Thôi mỗi người một tài khoản cũng được, miễn đừng rườm rà. Bạn thu phí thì chỉ nên làm phần thu, còn sửa hộ khẩu, đổi đơn giá là việc của mình. Ai cũng phải tự đổi được mật khẩu của mình và sửa thông tin cá nhân của tài khoản.

**Ghi chú của Analyst:** Củng cố AS-02 và AS-03 (tài khoản cấp sẵn, không tự đăng ký). Mâu thuẫn nhỏ: tài khoản dùng chung và tài khoản riêng → **Conflict C-01**; *Assumption AS-11*: mỗi người một tài khoản. Mức phân quyền chi tiết cần xác thực (OQ-04).

**Yêu cầu phát hiện được:**
- Đăng nhập bằng tài khoản được cấp → RAW-001
- Đổi mật khẩu, sửa thông tin cá nhân của tài khoản → RAW-002
- Bảo vệ mật khẩu, xác thực → RAW-022
- Phân quyền theo vai trò → RAW-023

---

### SIM-INT-BQT-Q09 — Truy vết và kiểm soát sửa đổi

**Câu hỏi:** Khi dữ liệu bị sửa hoặc hủy, anh/chị muốn biết điều gì?

**Trả lời:**
Mình muốn biết ai nhập, ai sửa, sửa lúc nào, nhất là phần tiền. Trước đây sửa trong sổ là gạch xóa, không ai biết người nào làm. Hủy một giao dịch thì phải ghi lý do. Chỉ cần xem lại được lịch sử chứ không cần phức tạp.

**Ghi chú của Analyst:** Yêu cầu phi chức năng về truy vết (audit log) và quy tắc "hủy chứ không xóa" (AS-17).

**Yêu cầu phát hiện được:**
- Hủy/điều chỉnh giao dịch có lý do và lưu vết → RAW-015
- Audit log → RAW-025

---

### SIM-INT-BQT-Q10 — Sao lưu và môi trường sử dụng

**Câu hỏi:** Anh/chị lo ngại điều gì về dữ liệu và máy móc sử dụng?

**Trả lời:**
Máy ở văn phòng Ban, dùng Windows. Mất dữ liệu là nguy lắm, nên phải có sao lưu, mà đừng bắt người dùng làm phức tạp, tự động hoặc bấm một nút là được. Giao diện tiếng Việt, đơn giản, các cô chú trong Ban không rành máy tính.

**Ghi chú của Analyst:** Khớp ràng buộc desktop và Windows (đề bài). Mức đơn giản của giao diện có thể kiểm chứng ở bước kiểm thử người dùng (sau này).

**Yêu cầu phát hiện được:**
- Sao lưu và khôi phục dữ liệu → RAW-026
- Giao diện tiếng Việt, dễ dùng → RAW-028

---

### SIM-INT-BQT-Q11 — Tầm nhìn và hạng mục để sau (roadmap)

**Câu hỏi:** Có khoản thu hoặc chức năng nào Ban muốn bổ sung về sau không?

**Trả lời:**
Phí gửi xe với tiền điện nước internet thì sau này cũng muốn đưa vào vì bên mình thu hộ hằng tháng. Nhưng đợt đầu cứ lo phí chung cư và hộ khẩu cho xong đã. Đừng làm gộp nặng nề.

**Ghi chú của Analyst:** Đúng với đề bài (v2.0). Ghi nhận ở mức roadmap, **Won't-have cho v1.0**.

**Yêu cầu phát hiện được:**
- Phí gửi xe → RAW-029 (Roadmap v2.0)
- Điện, nước, internet thu hộ → RAW-030 (Roadmap v2.0)

---

### SIM-INT-BQT-Q12 — Ưu tiên và kết thúc

**Câu hỏi:** Trong những việc vừa nêu, việc nào bắt buộc có ngay từ đầu, việc nào có thể để sau? Còn điều gì chúng tôi chưa hỏi?

**Trả lời:**
Bắt buộc có: đăng nhập, quản lý hộ và nhân khẩu, tạo khoản thu và ghi nhận thu, tìm kiếm, thống kê tổng thu. Sao lưu mình coi là bắt buộc luôn. Nên có: in biên lai, xuất danh sách cho cơ quan chức năng. Để sau: biểu đồ, phí xe, điện nước. Còn điều gì chưa hỏi thì... à, mình cần xem được lịch sử đóng phí của từng hộ qua các tháng.

**Ghi chú của Analyst:** Ưu tiên sơ bộ để PO xác nhận khi lập Product Backlog. Ý "lịch sử đóng phí từng hộ" đã có trong RAW-018.

**Yêu cầu phát hiện được:**
- Ưu tiên sơ bộ (Must): đăng nhập, quản lý hộ và nhân khẩu, tạo khoản thu, ghi nhận thu, tìm kiếm, thống kê tổng thu, sao lưu
- Ưu tiên sơ bộ (Should): in biên lai, xuất danh sách cho cơ quan chức năng
- Won't-have v1.0: biểu đồ, phí gửi xe, điện/nước/internet (roadmap v2.0)
- (Ưu tiên chi tiết từng RAW nằm ở cột Notes của `Raw_Requirements`.)

---

## 5. Bảng truy vết của biên bản này

| Câu hỏi | Wish | RAW |
|---|---|---|
| Q01 | WISH-19 | RAW-028 |
| Q02 | — | RAW-010, 011, 013 |
| Q03 | — | RAW-004, 018, 020 |
| Q04 | WISH-02, WISH-03 | RAW-003–009 |
| Q05 | WISH-02 | RAW-003, 004, 010, 013, 016, 019 |
| Q06 | WISH-04 | RAW-010, 011, 012 |
| Q07 | WISH-05 | RAW-019, 020, 021 |
| Q08 | WISH-01, WISH-08 | RAW-001, 002, 022, 023 |
| Q09 | WISH-06 | RAW-015, 025 |
| Q10 | WISH-07 | RAW-026, 028 |
| Q11 | WISH-09, WISH-10 | RAW-029, 030 |
| Q12 | — | Ưu tiên sơ bộ |
