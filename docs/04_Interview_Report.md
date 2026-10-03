# 04 — Interview Report: Role-play Requirement Elicitation (BlueMoon v1.0)

| Mục | Giá trị |
|---|---|
| Phiên bản tài liệu | 0.1 (Phase 2 — bản nháp, chờ nhóm xác nhận) |
| Loại | Simulated Interview / Role-play for Requirement Elicitation |
| Đầu vào | [03_Requirement_Elicitation_Plan.md](03_Requirement_Elicitation_Plan.md), 4 biên bản trong `docs/interviews/` |
| Đầu ra liên quan | `deliverables/04_Raw_Requirements.xlsx` (sheet Client_Wish_List, Raw_Requirements, NFR, Interview_Summary) |

---

## 1. Phương pháp thực hiện

Nhóm làm **role-play stakeholder interview** dựa trên đề bài BlueMoon và tài liệu hướng dẫn Elicitation. Một thành viên đóng vai Analyst, tự viết câu trả lời của bốn nhóm stakeholder giả lập theo Interview Script gồm 8 phần: Introduction, Current process / As-Is, Pain Points, Wishlist, Vision / To-Be, NFR / Constraints, Priority, Closing.

Nhóm dùng ba kỹ thuật: semi-structured interview (role-play), document analysis (đề bài, biểu mẫu Excel giả định) và workflow analysis (quy trình As-Is giả định).

| Biên bản | Stakeholder giả lập | Số câu hỏi |
|---|---|---|
| [SIM-INT-BQT](interviews/01_Ban_Quan_Tri_Interview.md) | Đại diện Ban quản trị (cấp quyết định) | 12 |
| [SIM-INT-TQ](interviews/02_Thu_Quy_Interview.md) | Thủ quỹ / người thu phí | 12 |
| [SIM-INT-CD](interviews/03_Cu_Dan_Interview.md) | Chủ hộ / cư dân | 12 |
| [SIM-INT-CQ](interviews/04_Co_Quan_Chuc_Nang_Interview.md) | Đại diện cơ quan chức năng (vai trò chung) | 12 |
| **Tổng** | 4 biên bản | **48** |

## 2. Ghi chú: đây chỉ là role-play cho môn học

- Nhóm **không** phỏng vấn, khảo sát hay quan sát thực tế Ban quản trị, thủ quỹ, cư dân hoặc cơ quan chức năng.
- Mọi phát hiện, mong muốn và yêu cầu trong báo cáo này là **Simulated stakeholder input** (*yêu cầu giả lập từ bối cảnh bài toán*).
- Không có tên thật, chữ ký, ghi âm, ảnh chụp, số điện thoại, địa chỉ, ngày hay giờ họp.
- **Evidence Reference** chỉ trỏ tới mã câu hỏi giả lập (`SIM-INT-…`), đề bài (PS-01, PS-02) hoặc document analysis (DA-02, biểu mẫu giả định). Đó không phải bằng chứng từ người thật.
- Nếu dùng ngoài môn học, yêu cầu phải được xác thực với khách hàng thật (xem mục 9 và 11).

## 3. Stakeholder groups

| Mã | Stakeholder giả lập | Quan hệ với hệ thống v1.0 | Biên bản |
|---|---|---|---|
| BQT | Đại diện Ban quản trị (cấp quyết định) | Người dùng (quản trị) | [SIM-INT-BQT](interviews/01_Ban_Quan_Tri_Interview.md) |
| TQ | Thủ quỹ / người thu phí | Người dùng trực tiếp | [SIM-INT-TQ](interviews/02_Thu_Quy_Interview.md) |
| CD | Chủ hộ / cư dân | Không dùng phần mềm ở v1.0 (AS-02) | [SIM-INT-CD](interviews/03_Cu_Dan_Interview.md) |
| CQ | Đại diện cơ quan chức năng (vai trò chung) | Gián tiếp: nhận thông tin từ Ban quản trị | [SIM-INT-CQ](interviews/04_Co_Quan_Chuc_Nang_Interview.md) |

## 4. Tổng hợp phát hiện

**Hiện trạng (As-Is).**
- Ban quản trị lập danh sách phí hằng tháng, hộ nộp tại văn phòng, thủ quỹ ghi sổ giấy rồi gõ lại Excel và viết biên lai tay (WA-01). Dữ liệu nằm ở hai nơi, thường không khớp.
- Thông tin hộ và nhân khẩu nằm trong Excel cũ và sổ tay, cập nhật không đều; khi cơ quan chức năng hỏi thì Ban phải gom bằng tay (WA-02).

**Nhu cầu chung của các stakeholder.**
1. **Một nguồn dữ liệu duy nhất** cho thu phí và hộ/nhân khẩu (BQT, TQ).
2. **Tự tính và tra cứu nhanh**: tính phí theo diện tích × đơn giá, tìm hộ theo số căn hộ/tên chủ hộ, xem công nợ từng hộ (TQ, BQT).
3. **Chứng từ và minh bạch**: biên lai rõ ràng, thấy cách tính, biết tổng thu quỹ (CD, TQ).
4. **Truy vết và kiểm soát**: sửa/hủy có lý do, ghi ai làm gì khi nào, không xóa cứng (BQT, TQ, CQ).
5. **Lịch sử biến động nhân khẩu có ngày** và tình trạng cư trú rõ ràng (CQ, CD, BQT).
6. **Bảo vệ dữ liệu cá nhân và phân quyền** (CD, CQ, BQT).
7. **Sao lưu, dễ dùng, nhanh** cho người dùng không chuyên IT (BQT, TQ).

**Các ý ngoài phạm vi v1.0.** Stakeholder còn nhắc phí gửi xe và điện/nước/internet (roadmap v2.0), cư dân tự xem trên điện thoại, nhắc nộp phí tự động và nhập giúp dữ liệu cũ (WISH-09, 10, 24, 25; C-04, C-05, C-08).

**Xung đột chính cần xác thực.** Dùng chung tài khoản và audit (C-01), miễn/giảm phí (C-02), giấy tờ tùy thân đầy đủ và bảo mật (C-03).

## 5. Pain Points

| ID | Pain point (giả lập) | Nguồn (simulated interview) | RAW liên quan |
|---|---|---|---|
| PP-01 | Dữ liệu thu phí ghi ở hai nơi (sổ giấy và Excel), hai bên không khớp. | SIM-INT-BQT-Q02, Q03 | RAW-013, RAW-018 |
| PP-02 | Muốn biết hộ nào đã nộp hoặc còn thiếu phải lọc Excel và đối chiếu sổ; cuối tháng cư dân hỏi lại phải lục. | SIM-INT-BQT-Q03; SIM-INT-TQ-Q09 | RAW-018, RAW-020 |
| PP-03 | Tính phí tay (diện tích × đơn giá) cho từng hộ, đã có lần nhầm; ghi sai diện tích thu sai nhiều tháng. | SIM-INT-TQ-Q03; SIM-INT-BQT-Q03; SIM-INT-CD-Q11 | RAW-004, RAW-011 |
| PP-04 | Tìm một hộ trong Excel mấy trăm dòng chậm, nhất là lúc đông người; trùng họ tên dễ nhầm. | SIM-INT-TQ-Q03, Q08 | RAW-016, RAW-027 |
| PP-05 | Sửa đè hoặc gạch xóa số liệu nên không biết ai sửa, không còn dấu vết. | SIM-INT-TQ-Q06; SIM-INT-BQT-Q09 | RAW-015, RAW-025 |
| PP-06 | Biên lai viết tay chậm, chữ khó đọc, thiếu thông tin; cư dân khó đối chiếu. | SIM-INT-TQ-Q07; SIM-INT-CD-Q03, Q04 | RAW-014 |
| PP-07 | Thông tin hộ và nhân khẩu rời rạc (Excel cũ, sổ tay), cập nhật không đều; cung cấp cho cơ quan chức năng phải gom thủ công, mất nhiều thời gian. | SIM-INT-BQT-Q04; SIM-INT-CQ-Q02, Q03 | RAW-003, RAW-006, RAW-009 |
| PP-08 | Cư dân không hiểu số tiền được tính ra sao và quỹ đóng góp thu được bao nhiêu. | SIM-INT-CD-Q03, Q05 | RAW-011, RAW-019 |
| PP-09 | Tạm trú, tạm vắng và biến động nhân khẩu không được ghi nhận rõ thời gian; danh sách còn hộ đã chuyển đi. | SIM-INT-CD-Q06; SIM-INT-CQ-Q03 | RAW-005, RAW-007, RAW-008 |
| PP-10 | Cư dân lo ngại lộ thông tin cá nhân (số giấy tờ, số điện thoại). | SIM-INT-CD-Q07 | RAW-023, RAW-024 |

## 6. Client Wishes

Danh sách mong muốn thô, **30 wish** (26 thuộc v1.0, 2 roadmap v2.0, 2 ngoài v1.0). Chưa lọc, chưa ưu tiên chính thức. Đây là *Simulated stakeholder input*.

| Wish ID | Stakeholder | Statement | Source interview | Related RAW | Scope | Notes |
|---|---|---|---|---|---|---|
| WISH-01 | BQT | Ban quản trị muốn mỗi người dùng đăng nhập bằng tài khoản được cấp và tự đổi được mật khẩu của mình; chỉ người được cấp tài khoản mới vào được hệ thống. | SIM-INT-BQT-Q08 | RAW-001, RAW-002, RAW-022 | v1.0 | Không cần tự đăng ký (AS-03). Có lúc nghĩ dùng chung một tài khoản (C-01). |
| WISH-02 | BQT | Ban quản trị muốn quản lý thông tin các hộ gia đình ở một chỗ duy nhất, kể cả khi đổi chủ căn hộ vẫn còn lịch sử. | SIM-INT-BQT-Q04, SIM-INT-BQT-Q05 | RAW-003, RAW-004, RAW-005 | v1.0 | Muốn có người nhập dữ liệu cũ giúp: ngoài phạm vi (C-08, OQ-12). |
| WISH-03 | BQT | Ban quản trị muốn quản lý nhân khẩu trong từng hộ và các biến động (ai chuyển đến, tạm vắng, ở tạm). | SIM-INT-BQT-Q04 | RAW-006, RAW-007, RAW-008 | v1.0 | — |
| WISH-04 | BQT | Ban quản trị muốn tạo các khoản thu và tự đặt, thay đổi đơn giá khi cần, không bị cố định trong phần mềm. | SIM-INT-BQT-Q06 | RAW-010, RAW-011 | v1.0 | Chưa chắc kiot tầng 1 có tính khác không (OQ-03). |
| WISH-05 | BQT | Ban quản trị muốn xem tổng số tiền đã thu và còn thiếu theo từng khoản, theo tháng hoặc đợt. | SIM-INT-BQT-Q07 | RAW-019, RAW-021 | v1.0 | Thống kê cơ bản, chưa cần biểu đồ (C-06). |
| WISH-06 | BQT | Ban quản trị muốn biết ai đã nhập, sửa hoặc hủy số liệu tiền, vào lúc nào. | SIM-INT-BQT-Q09 | RAW-015, RAW-025 | v1.0 | — |
| WISH-07 | BQT | Ban quản trị muốn dữ liệu được sao lưu tự động hoặc bằng một thao tác, không để mất. | SIM-INT-BQT-Q10 | RAW-026 | v1.0 | Coi là bắt buộc. |
| WISH-08 | BQT | Ban quản trị muốn người thu phí chỉ làm phần thu; việc sửa hộ, đổi đơn giá do trưởng ban. | SIM-INT-BQT-Q08 | RAW-023 | v1.0 | Mức phân quyền chi tiết chưa chốt (OQ-04). |
| WISH-09 | BQT | Về sau Ban quản trị muốn quản lý phí gửi xe trong cùng phần mềm. | SIM-INT-BQT-Q11 | RAW-029 | Roadmap v2.0 | Won't-have v1.0. Đợt đầu chưa làm. |
| WISH-10 | BQT | Về sau Ban quản trị muốn quản lý các khoản thu hộ điện, nước, internet trong cùng phần mềm. | SIM-INT-BQT-Q11 | RAW-030 | Roadmap v2.0 | Won't-have v1.0. |
| WISH-11 | TQ | Thủ quỹ muốn hệ thống tự tính số tiền phí dịch vụ, phí quản lý của từng hộ theo diện tích, khỏi bấm máy tính tay. | SIM-INT-TQ-Q03, SIM-INT-TQ-Q10 | RAW-011 | v1.0 | Miễn/giảm chưa thuộc v1.0 (C-02, OQ-02). |
| WISH-12 | TQ | Thủ quỹ muốn ghi nhận nộp tiền chỉ một lần: chọn hộ, khoản, nhập số tiền và ngày, không ghi sổ rồi gõ lại Excel. | SIM-INT-TQ-Q02 | RAW-013 | v1.0 | — |
| WISH-13 | TQ | Thủ quỹ muốn ghi nhận được trường hợp hộ nộp thiếu hoặc nộp gộp nhiều tháng và biết còn thiếu bao nhiêu. | SIM-INT-TQ-Q05 | RAW-013, RAW-018 | v1.0 | Chính sách phạt chậm nộp/nộp trước chưa rõ (OQ-05). |
| WISH-14 | TQ | Thủ quỹ muốn in biên lai thay cho viết tay. | SIM-INT-TQ-Q07 | RAW-014 | v1.0 | Ưu tiên Should. Mẫu biên lai chưa chốt (OQ-06). |
| WISH-15 | TQ | Thủ quỹ muốn sửa hoặc hủy giao dịch nhập nhầm kèm lý do, và không bị mất dấu vết. | SIM-INT-TQ-Q06 | RAW-015, RAW-025 | v1.0 | — |
| WISH-16 | TQ | Thủ quỹ muốn tìm hộ nhanh theo số căn hộ hoặc tên chủ hộ và thấy ngay số tiền phải nộp. | SIM-INT-TQ-Q08 | RAW-016, RAW-017 | v1.0 | — |
| WISH-17 | TQ | Thủ quỹ muốn mở từng hộ để xem các tháng đã đóng, còn thiếu tháng nào, thiếu bao nhiêu. | SIM-INT-TQ-Q09 | RAW-018 | v1.0 | — |
| WISH-18 | TQ | Thủ quỹ muốn lọc danh sách hộ chưa nộp theo tháng để nhắc. | SIM-INT-TQ-Q09 | RAW-020 | v1.0 | — |
| WISH-19 | TQ | Thủ quỹ muốn phần mềm nhanh và ít bước để không làm khách xếp hàng chờ. | SIM-INT-TQ-Q03, SIM-INT-TQ-Q11 | RAW-027, RAW-028 | v1.0 | Quy mô vài trăm hộ (AS-13). |
| WISH-20 | CD | Chủ hộ muốn nhận chứng từ nộp tiền ghi rõ khoản, tháng, số tiền, ngày và cách tính (diện tích, đơn giá). | SIM-INT-CD-Q03, SIM-INT-CD-Q04 | RAW-011, RAW-014 | v1.0 | Cư dân không dùng phần mềm; yêu cầu thực hiện qua Ban quản trị. |
| WISH-21 | CD | Chủ hộ muốn biết tổng thu và số hộ góp của từng đợt đóng góp, nhưng đây là tự nguyện, không bị ghi tên nhắc khi chưa đóng. | SIM-INT-CD-Q05 | RAW-012, RAW-019 | v1.0 | Liên quan C-07, AS-19. |
| WISH-22 | CD | Chủ hộ muốn Ban quản trị ghi nhận đúng khi gia đình thêm người, có người ở tạm hoặc đi vắng, kèm thời gian rõ ràng. | SIM-INT-CD-Q06 | RAW-006, RAW-007, RAW-008 | v1.0 | — |
| WISH-23 | CD | Chủ hộ muốn thông tin cá nhân của gia đình chỉ người có quyền trong Ban quản trị xem được. | SIM-INT-CD-Q07 | RAW-024, RAW-023 | v1.0 | Liên quan C-03. |
| WISH-24 | CD | Chủ hộ muốn tự xem số tiền phải đóng và lịch sử đóng phí trên điện thoại. | SIM-INT-CD-Q08 | — | Ngoài v1.0 (Won't-have) | Mâu thuẫn AS-02 (C-04). Không tạo RAW; ghi vào roadmap. |
| WISH-25 | CD | Chủ hộ muốn được nhắn nhắc trước hạn nộp phí. | SIM-INT-CD-Q09 | — | Ngoài v1.0 (Won't-have) | Thông báo/nhắc ngoài hệ thống (AS-07, C-05). Ban dùng RAW-020 để nhắc thủ công. |
| WISH-26 | CQ | Đại diện cơ quan chức năng muốn Ban quản trị cung cấp nhanh danh sách hộ, nhân khẩu khi có yêu cầu và tra nhanh được một người. | SIM-INT-CQ-Q02, SIM-INT-CQ-Q05 | RAW-009, RAW-017 | v1.0 | Đóng dấu xác nhận nằm ngoài hệ thống (AS-16). |
| WISH-27 | CQ | Đại diện cơ quan chức năng muốn thông tin nhân khẩu có tình trạng cư trú (thường xuyên, tạm trú, tạm vắng) kèm thời hạn. | SIM-INT-CQ-Q04 | RAW-006, RAW-008 | v1.0 | Trường dữ liệu chính xác cần xác thực (OQ-07). |
| WISH-28 | CQ | Đại diện cơ quan chức năng muốn có lịch sử biến động nhân khẩu (chuyển đến, đi, sinh, mất) kèm ngày và không bị xóa. | SIM-INT-CQ-Q06 | RAW-007 | v1.0 | Danh sách loại biến động chưa chốt (OQ-13). |
| WISH-29 | CQ | Đại diện cơ quan chức năng muốn báo cáo số hộ, nhân khẩu, tạm trú, tạm vắng tại một thời điểm, ghi rõ tính đến ngày nào. | SIM-INT-CQ-Q11 | RAW-021 | v1.0 | — |
| WISH-30 | CQ | Đại diện cơ quan chức năng muốn biết tổng thu từng đợt đóng góp và danh sách hộ đã đóng để báo cáo. | SIM-INT-CQ-Q07 | RAW-012, RAW-019 | v1.0 | Không coi hộ chưa đóng là nợ (AS-19, C-07). |

## 7. Functional Requirements

21 FR cho v1.0, thêm 2 FR roadmap (Won't-have cho v1.0). Nội dung đầy đủ nằm ở sheet `Raw_Requirements`.

| RAW ID | Stakeholder | Raw Requirement | Evidence Reference | Target Artefact (dự kiến) |
|---|---|---|---|---|
| RAW-001 | BQT; CD | Hệ thống cho phép Ban quản trị đăng nhập bằng tài khoản được cấp sẵn (tên đăng nhập, mật khẩu); các chức năng quản lý chỉ truy cập được sau khi đăng nhập thành công. | SIM-INT-BQT-Q08; SIM-INT-CD-Q07; PS-01 | Epic (dự kiến): Tài khoản & truy cập |
| RAW-002 | BQT | Người dùng tự đổi mật khẩu của mình và xem, cập nhật thông tin cá nhân của tài khoản. | SIM-INT-BQT-Q08; PS-01 | Epic (dự kiến): Tài khoản & truy cập |
| RAW-003 | BQT | Cho phép thêm hộ gia đình mới gồm số căn hộ, chủ hộ, diện tích căn hộ (m²), thông tin liên hệ; không cho trùng số căn hộ. | SIM-INT-BQT-Q04; SIM-INT-BQT-Q05; PS-01; DA-02 | Epic (dự kiến): Quản lý hộ gia đình |
| RAW-004 | BQT; CD | Cho phép xem chi tiết và sửa thông tin hộ gia đình (diện tích, chủ hộ, liên hệ), kèm danh sách nhân khẩu của hộ. | SIM-INT-BQT-Q03; SIM-INT-BQT-Q04; SIM-INT-BQT-Q05; SIM-INT-CD-Q11 | Epic (dự kiến): Quản lý hộ gia đình |
| RAW-005 | BQT | Cho phép ghi nhận đổi chủ hộ hoặc hộ chuyển đi / ngừng cư trú mà vẫn lưu lịch sử, không xóa dữ liệu cũ. | SIM-INT-BQT-Q04 | Epic (dự kiến): Quản lý hộ gia đình |
| RAW-006 | BQT; CD; CQ | Cho phép thêm, sửa nhân khẩu trong hộ: họ tên, ngày sinh, giới tính, quan hệ với chủ hộ, giấy tờ tùy thân (nếu có); không xóa cứng nhân khẩu đã rời đi. | SIM-INT-BQT-Q04; SIM-INT-CD-Q06; SIM-INT-CQ-Q04; PS-01 | Epic (dự kiến): Quản lý nhân khẩu |
| RAW-007 | BQT; CD; CQ | Ghi nhận biến động nhân khẩu (chuyển đến, chuyển đi, sinh, mất…) kèm ngày và lý do; xem lịch sử biến động của từng hộ và từng nhân khẩu. | SIM-INT-BQT-Q04; SIM-INT-CD-Q06; SIM-INT-CQ-Q03; SIM-INT-CQ-Q06; PS-01 | Epic (dự kiến): Quản lý nhân khẩu |
| RAW-008 | BQT; CD; CQ | Ghi nhận tạm trú và tạm vắng của nhân khẩu với thời gian bắt đầu, kết thúc và lý do; đánh dấu khi hết thời hạn. | SIM-INT-BQT-Q04; SIM-INT-CD-Q06; SIM-INT-CQ-Q03; SIM-INT-CQ-Q04; SIM-INT-CQ-Q10; PS-01 | Epic (dự kiến): Quản lý nhân khẩu |
| RAW-009 | BQT; CQ | Cho phép xuất hoặc in danh sách hộ gia đình, nhân khẩu và biến động để Ban cung cấp cho cơ quan chức năng khi có yêu cầu. | SIM-INT-BQT-Q04; SIM-INT-CQ-Q02; SIM-INT-CQ-Q05; PS-01 | Epic (dự kiến): Quản lý nhân khẩu |
| RAW-010 | BQT | Cho phép tạo, xem, sửa, ngừng áp dụng khoản thu (phí dịch vụ, phí quản lý, khoản đóng góp) gồm tên, loại (bắt buộc / tự nguyện), kỳ thu hoặc đợt, đơn giá hoặc mức thu, hạn nộp; đơn giá cấu hình được. | SIM-INT-BQT-Q02; SIM-INT-BQT-Q05; SIM-INT-BQT-Q06; PS-01 | Epic (dự kiến): Quản lý khoản thu |
| RAW-011 | BQT; TQ; CD | Hệ thống lập danh sách khoản phải thu của từng hộ theo kỳ và tự tính phí dịch vụ, phí quản lý theo diện tích × đơn giá; hiển thị rõ cách tính. | SIM-INT-BQT-Q02; SIM-INT-BQT-Q06; SIM-INT-TQ-Q03; SIM-INT-TQ-Q10; SIM-INT-CD-Q03; SIM-INT-CD-Q04; PS-01 | Epic (dự kiến): Quản lý khoản thu |
| RAW-012 | BQT; CD; CQ | Hỗ trợ khoản đóng góp tự nguyện theo đợt: hộ tự nguyện số tiền, không bắt buộc; hộ chưa đóng không bị coi là nợ. | SIM-INT-BQT-Q06; SIM-INT-CD-Q05; SIM-INT-CQ-Q07; PS-01 | Epic (dự kiến): Quản lý khoản thu |
| RAW-013 | BQT; TQ | Cho phép ghi nhận hộ nộp tiền: chọn hộ, khoản thu, số tiền, ngày nộp, hình thức nộp, người thu; hỗ trợ nộp một phần và nộp gộp nhiều khoản hoặc nhiều kỳ trong một lần. | SIM-INT-BQT-Q02; SIM-INT-BQT-Q05; SIM-INT-TQ-Q02; SIM-INT-TQ-Q04; SIM-INT-TQ-Q05; PS-01 | Epic (dự kiến): Thu phí |
| RAW-014 | TQ; CD | Cho phép in hoặc xuất biên lai (phiếu thu) cho từng lần nộp gồm số căn hộ, khoản, kỳ, số tiền, ngày, người thu và cách tính. | SIM-INT-TQ-Q07; SIM-INT-CD-Q03; SIM-INT-CD-Q04 | Epic (dự kiến): Thu phí |
| RAW-015 | TQ; BQT; CD | Cho phép sửa hoặc hủy giao dịch thu nhầm kèm lý do; không xóa cứng, lưu người thực hiện và thời điểm. | SIM-INT-TQ-Q06; SIM-INT-BQT-Q09; SIM-INT-CD-Q11 | Epic (dự kiến): Thu phí |
| RAW-016 | TQ; BQT | Tìm hộ gia đình theo số căn hộ và tên chủ hộ; kết quả hiển thị nhanh kèm số tiền phải nộp. | SIM-INT-TQ-Q03; SIM-INT-TQ-Q08; SIM-INT-BQT-Q05; PS-01 | Epic (dự kiến): Tra cứu & thống kê |
| RAW-017 | TQ; CQ | Tìm nhân khẩu theo họ tên (và thông tin cơ bản) trên toàn bộ các hộ. | SIM-INT-TQ-Q08; SIM-INT-CQ-Q05; PS-01 | Epic (dự kiến): Tra cứu & thống kê |
| RAW-018 | BQT; TQ; CD | Tra cứu, lọc khoản thu và giao dịch theo hộ, khoản thu, kỳ, trạng thái nộp (đã nộp, còn thiếu, chưa nộp) và khoảng thời gian; xem công nợ và lịch sử nộp của một hộ. | SIM-INT-BQT-Q03; SIM-INT-BQT-Q12; SIM-INT-TQ-Q05; SIM-INT-TQ-Q09; SIM-INT-CD-Q03; SIM-INT-CD-Q11 | Epic (dự kiến): Tra cứu & thống kê |
| RAW-019 | BQT; CD; CQ | Thống kê tổng số tiền đã thu và còn phải thu theo khoản thu, theo tháng hoặc đợt; thống kê tổng thu và danh sách hộ đã đóng theo từng đợt đóng góp. | SIM-INT-BQT-Q05; SIM-INT-BQT-Q07; SIM-INT-CD-Q05; SIM-INT-CQ-Q07; PS-01 | Epic (dự kiến): Tra cứu & thống kê |
| RAW-020 | TQ; BQT | Lập danh sách hộ chưa nộp hoặc còn nợ theo kỳ (đối với khoản bắt buộc) để Ban nhắc nộp. | SIM-INT-TQ-Q09; SIM-INT-BQT-Q07; SIM-INT-BQT-Q03 | Epic (dự kiến): Tra cứu & thống kê |
| RAW-021 | CQ; BQT | Thống kê số hộ, số nhân khẩu, số người tạm trú, tạm vắng tại một thời điểm, ghi rõ ngày tính. | SIM-INT-CQ-Q11; SIM-INT-BQT-Q07 | Epic (dự kiến): Tra cứu & thống kê |
| RAW-029 | BQT; CD | [Roadmap v2.0] Quản lý phí gửi xe: thu theo tháng theo thông tin phương tiện đăng ký của hộ gia đình. | SIM-INT-BQT-Q11; SIM-INT-CD-Q10; PS-01 | Product Backlog: Won't-have v1.0 / Roadmap v2.0 |
| RAW-030 | BQT; CD | [Roadmap v2.0] Quản lý các khoản thu hộ điện, nước, internet theo thông báo của nhà cung cấp dịch vụ. | SIM-INT-BQT-Q11; SIM-INT-CD-Q10; PS-01 | Product Backlog: Won't-have v1.0 / Roadmap v2.0 |

Bao phủ phạm vi v1.0:

> Nhóm chức năng ở đây là bản dự kiến lúc role-play (6 nhóm). Thiết kế cuối cùng gồm 7 Epic, xem `deliverables/05_Epic_UserStory.xlsx`.

| Nhóm chức năng | RAW |
|---|---|
| Đăng nhập / đổi mật khẩu | RAW-001, RAW-002 (+ NFR: RAW-022, RAW-023) |
| Quản lý hộ gia đình | RAW-003, RAW-004, RAW-005 |
| Quản lý nhân khẩu | RAW-006, RAW-007, RAW-008, RAW-009 |
| Quản lý khoản thu | RAW-010, RAW-011, RAW-012 |
| Thu phí (ghi nhận thu phí) | RAW-013, RAW-014, RAW-015 |
| Tra cứu / tìm kiếm | RAW-016, RAW-017, RAW-018 |
| Thống kê cơ bản | RAW-019, RAW-020, RAW-021 |
| NFR (bảo mật, phân quyền, riêng tư, truy vết, sao lưu, hiệu năng, dễ dùng) | RAW-022 … RAW-028 |
| Roadmap v2.0 — Won't-have v1.0 (phí gửi xe; điện, nước, internet) | RAW-029, RAW-030 |

## 8. Non-Functional Requirements

7 NFR (đồng bộ với sheet `NFR`). Các con số cụ thể (ngưỡng, thời gian, quy mô) là **giả định** cần xác thực.

| NFR ID | Related RAW | Loại | Mô tả | Evidence Reference |
|---|---|---|---|---|
| NFR-001 | RAW-022 | Bảo mật | Xác thực an toàn: mật khẩu không lưu ở dạng rõ (băm), giới hạn số lần đăng nhập sai liên tiếp. | SIM-INT-BQT-Q08; SIM-INT-CD-Q07; PS-01 |
| NFR-002 | RAW-023 | Phân quyền | Phân quyền theo vai trò: tối thiểu phân biệt quản trị và người thu phí; chỉ quản trị được sửa hộ, nhân khẩu, khoản thu, đơn giá và tài khoản. | SIM-INT-BQT-Q08; SIM-INT-CD-Q07 |
| NFR-003 | RAW-024 | Quyền riêng tư | Bảo vệ dữ liệu cá nhân: che bớt số giấy tờ khi hiển thị thường ngày; chỉ tài khoản có quyền mới xem đầy đủ và xuất dữ liệu. | SIM-INT-CD-Q07; SIM-INT-CQ-Q09 |
| NFR-004 | RAW-025 | Truy vết (audit) | Audit log: ghi người thực hiện, thời điểm, loại thao tác, giá trị trước và sau cho việc thêm, sửa, hủy dữ liệu thu phí và nhân khẩu, và mỗi lần xuất dữ liệu; log không sửa hoặc xóa được qua giao diện. | SIM-INT-BQT-Q09; SIM-INT-TQ-Q06; SIM-INT-CQ-Q09 |
| NFR-005 | RAW-026 | Độ tin cậy (sao lưu) | Sao lưu và khôi phục dữ liệu: sao lưu tự động hoặc bằng một thao tác, có thể khôi phục khi cần. | SIM-INT-BQT-Q10 |
| NFR-006 | RAW-027 | Hiệu năng | Hiệu năng: tìm kiếm và hiển thị danh sách trong tối đa 3 giây với quy mô vài trăm hộ, vài nghìn nhân khẩu và 2–3 người dùng đồng thời. | SIM-INT-TQ-Q08; SIM-INT-TQ-Q11 |
| NFR-007 | RAW-028 | Khả năng sử dụng | Dễ dùng: giao diện tiếng Việt, tiền tệ VND hiển thị dễ đọc, thông báo lỗi rõ ràng; ghi nhận một lần nộp tiền không quá khoảng 5 thao tác chính; người không chuyên IT dùng được sau hướng dẫn ngắn. | SIM-INT-BQT-Q01; SIM-INT-BQT-Q10; SIM-INT-TQ-Q03; SIM-INT-TQ-Q11 |

## 9. Open Questions

| ID | Câu hỏi | Liên quan | Phát sinh từ |
|---|---|---|---|
| OQ-01 | v1.0 có cần chức năng tự đăng ký tài khoản không? (Ban nói tài khoản do Ban cấp.) | RAW-001 | BQT-Q08; Q1 Phase 1 |
| OQ-02 | Có chính sách miễn/giảm phí cho hộ đặc biệt không, và có thuộc v1.0 không? | RAW-011 | TQ-Q10; BQT-Q06 |
| OQ-03 | Kiot tầng 1 và penthouse có đơn giá hoặc cách tính khác không? | RAW-010, RAW-011 | BQT-Q06 |
| OQ-04 | Phân quyền: có những vai trò nào, mỗi vai trò làm được gì? | RAW-023 | BQT-Q08; Q3 Phase 1 |
| OQ-05 | Có tính phạt chậm nộp hoặc cho phép nộp trước nhiều kỳ không? | RAW-013 | TQ-Q05 |
| OQ-06 | Mẫu biên lai và mẫu thông báo thu tiền chính thức là gì? Thông báo có in từ hệ thống không? | RAW-011, RAW-014 | TQ-Q07; Q2 Phase 1 |
| OQ-07 | Cơ quan chức năng yêu cầu chính xác những trường thông tin và biểu mẫu nào theo quy định hiện hành? | RAW-006, RAW-008, RAW-009 | CQ-Q04 |
| OQ-08 | Có lưu số giấy tờ tùy thân không, nếu có thì mức che và ai được xem? | RAW-006, RAW-024 | CQ-Q04; CD-Q07 |
| OQ-09 | Cần ghi nhận những hình thức nộp nào (tiền mặt, chuyển khoản, khác)? | RAW-013 | TQ-Q04 |
| OQ-10 | Quy mô thực tế: số hộ, số nhân khẩu, số người dùng đồng thời? | RAW-027 | TQ-Q11 |
| OQ-11 | Lịch sử giao dịch, biến động và log cần lưu trong bao lâu? | RAW-025 | BQT-Q09 |
| OQ-12 | Dữ liệu hộ, nhân khẩu hiện có trong Excel do ai nhập vào phần mềm, có cần chức năng nhập từ Excel không? | RAW-003, RAW-006 | BQT-Q04; PS-02 |
| OQ-13 | Danh sách các loại biến động nhân khẩu và thời hạn cập nhật do Ban quy định là gì? | RAW-007, RAW-008 | CQ-Q06, Q10 |
| OQ-14 | Khi sửa diện tích hoặc hủy giao dịch, các kỳ đã tính trước đó được tính lại như thế nào? | RAW-004, RAW-011, RAW-015 | BQT-Q03; CD-Q11 |

## 10. Assumptions

Tiếp nối AS-01…AS-10 trong [01_Project_Overview.md](01_Project_Overview.md).

| ID | Giả định | Căn cứ |
|---|---|---|
| AS-11 | Mỗi người dùng trong Ban quản trị có một tài khoản riêng (để có audit log và phân quyền). | C-01 |
| AS-12 | v1.0 chỉ ghi nhận hình thức nộp (tiền mặt, chuyển khoản) như thông tin phụ, không tích hợp thanh toán online. | TQ-Q04 |
| AS-13 | Quy mô khoảng vài trăm hộ và vài nghìn nhân khẩu; 2–3 người dùng đồng thời (dùng cho NFR hiệu năng). | TQ-Q11 |
| AS-14 | Miễn hoặc giảm phí không thuộc v1.0 trừ khi Ban quản trị xác nhận. | TQ-Q10, C-02 |
| AS-15 | Người nộp phí thường là chủ hộ nhưng có thể nhờ người khác nộp hộ; v1.0 chỉ ghi nhận người nộp hộ như thông tin phụ của giao dịch. | TQ-Q02 |
| AS-16 | Cơ quan chức năng không truy cập hệ thống; Ban quản trị là đầu mối xuất hoặc in danh sách. Việc đóng dấu xác nhận nằm ngoài hệ thống. | CQ-Q05, Q08 |
| AS-17 | Dữ liệu thu phí, hộ và nhân khẩu được xử lý bằng sửa hoặc hủy kèm lý do và lưu vết, không xóa cứng. | BQT-Q09, TQ-Q06, CQ-Q06 |
| AS-18 | v1.0 lưu các trường cư trú cơ bản (họ tên, ngày sinh, giới tính, quan hệ chủ hộ, tình trạng cư trú, thời hạn); biểu mẫu chính xác sẽ xác thực sau. | CQ-Q04 |
| AS-19 | Hộ chưa đóng khoản đóng góp tự nguyện không bị coi là nợ và không xuất hiện trong danh sách nhắc nộp. | CD-Q05, CQ-Q07 |
| AS-20 | Mức ưu tiên MoSCoW trong tập RAW chỉ là gợi ý sơ bộ; Product Owner chốt khi lập Product Backlog. | Phase 3+ |

## 11. Conflicts / items requiring validation

| ID | Nguồn | Nội dung | Vấn đề | Hướng xử lý tạm thời |
|---|---|---|---|---|
| C-01 | BQT-Q08 | Ban nghĩ dùng chung một tài khoản cho tiện, nhưng cũng muốn biết ai sửa (BQT-Q09). | Tài khoản dùng chung mâu thuẫn với audit log và phân quyền. | Giả định mỗi người một tài khoản riêng (AS-11). Cần Ban xác nhận (OQ-04). |
| C-02 | BQT-Q06 / TQ-Q10 | Ban nghĩ mọi căn cùng đơn giá; thủ quỹ nói đôi khi có hộ được miễn, giảm. | Chưa rõ có quy tắc miễn/giảm hay không. | Miễn/giảm không thuộc v1.0 nếu chưa xác nhận (AS-14, OQ-02). |
| C-03 | CQ-Q04, Q09 / CD-Q07 | Cơ quan cần số giấy tờ đầy đủ; cư dân lo bị lộ. | Đầy đủ dữ liệu và bảo mật cùng được yêu cầu. | Lưu đủ, che bớt khi hiển thị, giới hạn quyền xem và xuất, ghi log xuất (RAW-024, RAW-025). OQ-08. |
| C-04 | CD-Q08 / PS-01 | Cư dân muốn tự xem phí trên điện thoại; đề bài mô tả ứng dụng desktop cho Ban quản trị. | Ngoài phạm vi v1.0. | Won't-have v1.0, ghi vào roadmap; không tạo RAW (WISH-24, AS-02). |
| C-05 | CD-Q09 / AS-07 | Cư dân muốn nhận nhắc nộp phí tự động; thông báo hiện nằm ngoài hệ thống. | Ngoài phạm vi v1.0. | Won't-have v1.0; Ban dùng danh sách hộ chưa nộp (RAW-020) để nhắc thủ công (WISH-25). |
| C-06 | BQT-Q07 | Ban nói thống kê không cần cầu kỳ nhưng lại cần nhiều chiều (khoản, kỳ, hộ, nhân khẩu). | Phạm vi thống kê cơ bản chưa rõ ranh giới. | Thống kê cơ bản theo khoản, kỳ, hộ; không biểu đồ ở v1.0; cần PO xác thực. |
| C-07 | CQ-Q07 / CD-Q05 | Cơ quan muốn danh sách hộ đã đóng quỹ; cư dân không muốn bị ghi tên nhắc khi chưa đóng. | Minh bạch và tính tự nguyện. | Chỉ báo cáo tổng thu và hộ đã đóng; không có khái niệm nợ với khoản tự nguyện (AS-19). |
| C-08 | BQT-Q04 / PS-02 | Ban mong có người nhập dữ liệu cũ từ Excel; ví dụ Charter (Bài 4.1, Chương 4, chỉ tham khảo) loại trừ nhập liệu khỏi phạm vi dự án; AS-08 là giả định của nhóm. | Phạm vi nhóm. | Ngoài phạm vi (AS-08); import Excel chưa đưa vào v1.0 (OQ-12). |

Các mục trên cần xác thực với khách hàng thật (nếu có). Trong BTL, **Product Owner** của nhóm tạm quyết định khi lập Product Backlog và ghi rõ đó là giả định.

## 12. Truy vết và sẵn sàng cho phase sau

- Mỗi RAW có Source, Stakeholder, Evidence Reference và Target Artefact (Epic dự kiến). Sáu Epic dự kiến: *Tài khoản & truy cập*, *Quản lý hộ gia đình*, *Quản lý nhân khẩu*, *Quản lý khoản thu*, *Thu phí*, *Tra cứu & thống kê*. NFR sẽ chuyển thành Technical Story hoặc Definition of Done.
- Chuỗi truy vết hiện có: Simulated interview (Q) → Wish → RAW. Các phase sau nối tiếp: RAW → Epic → Feature → User Story → Acceptance Criteria.
- Phần As-Is dựa vào WA-01, WA-02 và các câu trả lời về *Current process / Pain Points*. Phần To-Be dựa vào các câu *Wishlist / Vision*. Epic, Feature và US dựa vào cột Target Artefact và danh sách RAW.
- Ưu tiên MoSCoW trong sheet RAW chỉ là gợi ý ban đầu (AS-20).

## 13. Số liệu tổng hợp

| Chỉ số | Giá trị |
|---|---|
| Simulated interview | 4 (48 câu hỏi) |
| Client Wish | 30 |
| Pain Point | 10 (tại thời điểm role-play; Phase 3 bổ sung PP-11 và PP-12, tổng 12 trong `04_AsIs_ToBe.md`) |
| RAW requirement | 30 (FR 23: 21 v1.0 + 2 roadmap; NFR 7) |
| Open Question | 14 |
| Assumption mới (Phase 2) | 10 |
| Conflict | 8 |
