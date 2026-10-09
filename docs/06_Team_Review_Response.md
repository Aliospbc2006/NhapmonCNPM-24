# 06. Phản hồi review của thành viên nhóm (Phase 9)

Review do Thanh Tuấn (Product Owner) thực hiện, gồm ba phần: Requirement Elicitation, As-Is/To-Be, Epic/User Story và Product Backlog/Sprint Plan. Tài liệu này ghi lại từng ý đã được **xác thực với file và đề bài của giảng viên**, việc đã sửa, việc để lại cho PO quyết định và các đề xuất không áp dụng (kèm lý do).

Nguyên tắc xử lý: không đổi phạm vi v1.0, không thêm requirement mới, không bịa dữ liệu khảo sát/quan sát. Stakeholder statement, Wish, RAW và User Story vẫn là **Simulated stakeholder input**.

Kết quả: phần lớn lỗi review nêu là đúng và đã sửa (mục 1 và 3); hai đề xuất đổi phạm vi không áp dụng (mục 2); câu hỏi MoSCoW để PO quyết định (mục 4). Phần Product Backlog, Sprint và Task được review xác nhận không có lỗi kỹ thuật.

## 1. Xác thực từng ý

### 1.1. Requirement Elicitation

| # | Ý kiến trong review | Xác thực | Xử lý |
|---|---|---|---|
| E1 | `03_Requirement_Elicitation_Plan.md` mục 4 bỏ qua hẳn Observation và Survey | **Đúng.** Hướng dẫn của giảng viên liệt kê các kỹ thuật này; tài liệu chỉ nói là không áp dụng. | Mục 4 nay giải thích hai kỹ thuật là mô phỏng, chưa thực hiện. Thêm 4.1 `SIM-OBS-01` (kịch bản quan sát thu phí) và 4.2 `SIM-SURVEY-01` (6 câu khảo sát cư dân S1–S6), trạng thái "chưa thực hiện". Hai mục chỉ dùng để đối chiếu WISH/RAW/PP đã có, không sinh requirement hay dữ liệu mới. |
| E2 | Q08, Q09 của cư dân (app di động, SMS) nên loại khỏi v1.0 và chuyển sang v2.0 | **Đã đáp ứng một nửa.** Bảng trong `03_Cu_Dan_Interview.md` đã ghi Q08/Q09 (WISH-24, WISH-25) là *Out of v1.0*. | Giữ nguyên. **Không chuyển sang v2.0**, vì đề bài định nghĩa v2.0 chỉ gồm phí gửi xe và điện, nước, internet. |
| E3 | Đưa việc nhập liệu Excel vào Out of Scope và thêm tính năng Import/Export Excel | **Đúng một phần.** Việc nhập dữ liệu cũ do Ban quản trị làm đã có ở AS-08, C-08, OQ-12. | **Không thêm tính năng Import Excel** (đổi phạm vi, cần PO và giảng viên đồng ý). OQ-12 giữ mở. |
| E4 | Mâu thuẫn tính phí (BQT: đơn giá cố định, Thủ quỹ: miễn/giảm) cần chốt công thức, đưa miễn/giảm sang v2.0 | **Đúng một phần.** C-02, OQ-02, AS-14 đã ghi: v1.0 tính theo diện tích × đơn giá, miễn/giảm không thuộc v1.0 trừ khi BQT xác nhận. | Giữ nguyên. **Không đưa miễn/giảm vào v2.0** (không thuộc danh sách v2.0 của đề bài); vẫn là Open Question OQ-02. |
| E5 | `04_Co_Quan_Chuc_Nang_Interview.md` Q04: các trường nhân khẩu bị ghi nguồn "giả định" | **Đúng.** Danh sách trường (CCCD, ngày cấp...) trùng với Bài 6.1, Chương 6. | Ghi chú CQ-Q04 nay viện dẫn Bài 6.1 làm tham khảo về trường dữ liệu và nói rõ đó là bài toán khác. AS-18 và OQ-07 giữ nguyên. |
| E6 | 17 RAW viết quá chi tiết, giống SRS (RAW-003, 006, 007, 008, 010, 011, 013, 015, 016, 018, 022–028) | **Đúng.** Đã đối chiếu từng RAW; các câu liệt kê field, công thức, ngưỡng, giải pháp kỹ thuật. | Viết lại ở mức nhu cầu stakeholder, xem mục 3. |
| E7 | Testability của NFR-001…007 | **Đúng.** Mọi nhận xét khớp với trạng thái *proposed / TBD* sẵn có. | Thêm tiêu chí `NFR-005.4` (số bản sao lưu, TBD) và `NFR-005.5` (quyền sao lưu/khôi phục). Các số khác vẫn là giả định chờ xác nhận. |
| E8 | ID không trùng, RAW-029/030 xử lý đúng v2.0 | Đúng. | Không đổi. |

### 1.2. As-Is và To-Be

| # | Ý kiến | Xác thực | Xử lý |
|---|---|---|---|
| T1 | Mô hình actor mâu thuẫn: `01_Project_Overview` nói chỉ có Ban quản trị, còn `03` và `04` tách BQT, Thủ quỹ, Quản trị | **Đúng.** | AS-02 và AS-04 trong `01_Project_Overview.md` nay định nghĩa người dùng hệ thống chỉ thuộc Ban quản trị, gồm 3 vai trò: Quản trị hệ thống, Thành viên Ban quản trị, Thủ quỹ. Cập nhật câu liên quan và Q3. `04_AsIs_ToBe.md` đổi actor ở TB-01, TB-05b, TB-07. |
| T2 | Review nhắc "NFR-023" | **Không tồn tại.** NFR chỉ có NFR-001…007. Ý đúng là NFR-002 (RAW-023, phân quyền). | Không có gì để sửa; ghi lại để tránh nhầm. |
| T3 | Correct/Cancel nên là nhánh ngoại lệ | **Đúng.** | TB-05a (in biên lai) ghi là nhánh tùy chọn; TB-05b là nhánh ngoại lệ (Thủ quỹ đề nghị, Quản trị hệ thống hoặc Thành viên BQT duyệt). |
| T4 | TB-06 gom nhiều nghiệp vụ | **Đúng.** | Ghi chú: gồm 4 chức năng, có thể tách TB-06a–06d khi cần. Chưa tách để không đổi số bước. |
| T5 | PP-08 chỉ giải quyết một phần; PP-10 giải quyết ở lớp NFR | **Đúng.** | PP-08 ghi "chỉ giải quyết một phần" (cư dân không dùng hệ thống v1.0); PP-10 ghi xử lý qua NFR. |
| T6 | As-Is chỉ phản ánh đúng ở mức đề bài, chi tiết còn là suy luận/giả lập | **Đúng**, không phải lỗi. | Giữ cách ghi hiện có (suy luận/giả lập). Chưa có khảo sát thật. |

### 1.3. Epic, User Story, Product Backlog, Sprint, Task

| # | Ý kiến | Xác thực | Xử lý |
|---|---|---|---|
| B1 | Font không phù hợp tiếng Việt | **Đúng.** `05` và `06` dùng Century Gothic. | Đổi sang Arial trong `styles.xml` của hai file (định dạng khác giữ nguyên). File mẫu giảng viên trong `templates/` không đụng tới. |
| B2 | 21 Must (51%) hơi cao; xem lại US-03, US-17, US-31, US-33 | **Đúng là câu hỏi hợp lệ.** Không có lỗi "tất cả đều Must", Priority khớp MoSCoW. | **Không đổi.** MoSCoW là quyết định của PO, xem mục 4. |
| B3 | Story Point, Dependency, Sprint 1/2/3, 150 task, Workload | Review xác nhận không có lỗi (không story >5 SP, không dependency ngược sprint, 0 task tự review, task lớn nhất S1-T39 8 giờ). | Giữ nguyên. Ước lượng lại bằng Planning Poker ở Sprint Planning; theo dõi S1-T39. |
| B4 | Epic, Feature, User Story, AC, truy vết RAW | Review xác nhận hợp lý. | Giữ nguyên. |

## 2. Đề xuất không áp dụng

| Đề xuất | Lý do |
|---|---|
| Thêm Import/Export Excel | Thêm chức năng mới, ngoài phạm vi đã chốt; chưa có xác nhận của PO/giảng viên. |
| Chuyển app/SMS và miễn/giảm phí sang v2.0 | Đề bài chỉ định v2.0 là phí gửi xe và điện, nước, internet. Các mục kia đã ở trạng thái Out of v1.0 hoặc Open Question. |

## 3. Nhật ký viết lại 17 RAW

Giữ nguyên ID và số lượng RAW. Với mỗi RAW:

- `Raw_Requirements` (file 04): cột *Raw Requirement* dùng câu mới; câu chi tiết cũ chuyển vào cột *Notes*, sau cụm "Chi tiết ban đầu (trước Phase 9)".
- `NFR` (file 04): các dòng NFR-001…007 giữ nguyên câu chi tiết, vì NFR là mức đặc tả và cần chỉ tiêu cụ thể.
- `RAW_Review` (file 05) và `Traceability` (file 06): dùng câu RAW mới. Câu Legend "Nội dung RAW không bao giờ bị sửa" được thay bằng ghi chú Phase 9.
- `04_Interview_Report.md` (bảng RAW) và `04_AsIs_ToBe.md` (mục 7.1): đồng bộ câu mới. Mục 6 và ghi chú N-3 của `04_AsIs_ToBe.md` nêu rõ RAW-022…028 nay ở mức nhu cầu, còn con số nằm ở NFR.
- User Story, Acceptance Criteria, Sprint Plan và GitHub Issue không đổi (chỉ trích dẫn RAW ID).

| RAW | Câu mới |
|---|---|
| RAW-003 | BQT muốn lưu thông tin hộ gia đình tập trung và tránh trường hợp nhập trùng căn hộ. |
| RAW-006 | BQT muốn quản lý thông tin những người thuộc từng hộ và vẫn tra cứu được người đã rời đi. |
| RAW-007 | BQT muốn theo dõi các thay đổi nhân khẩu của từng hộ theo thời gian. |
| RAW-008 | BQT muốn theo dõi tình trạng tạm trú/tạm vắng và thời hạn liên quan. |
| RAW-010 | BQT muốn tự quản lý các khoản thu và có thể thay đổi mức thu khi cần. |
| RAW-011 | BQT muốn hệ thống hỗ trợ tính phí theo diện tích căn hộ để giảm tính toán thủ công. |
| RAW-013 | Thủ quỹ muốn ghi nhận việc hộ nộp tiền, kể cả khi chỉ nộp một phần hoặc nhiều khoản cùng lúc. |
| RAW-015 | Thủ quỹ muốn xử lý được giao dịch thu ghi nhầm; phần truy vết thay đổi nằm ở RAW-025 và NFR-004. |
| RAW-016 | Thủ quỹ và BQT muốn tìm hộ gia đình theo số căn hộ và tên chủ hộ, kèm số tiền phải nộp; yêu cầu tốc độ nằm ở NFR-006. |
| RAW-018 | BQT và Thủ quỹ muốn tra cứu khoản thu và lịch sử đóng tiền của từng hộ theo nhiều tiêu chí. |
| RAW-022 | BQT muốn tài khoản được bảo vệ an toàn và hạn chế truy cập trái phép. |
| RAW-023 | Mỗi loại người dùng chỉ được thực hiện công việc phù hợp với trách nhiệm của mình. |
| RAW-024 | Thông tin cá nhân nhạy cảm chỉ được người có thẩm quyền xem. |
| RAW-025 | BQT muốn biết ai đã thay đổi dữ liệu quan trọng và thay đổi khi nào. |
| RAW-026 | BQT lo mất dữ liệu và muốn có cách sao lưu, khôi phục khi có sự cố. |
| RAW-027 | Thủ quỹ muốn việc tìm kiếm và mở danh sách không bị chậm khi dữ liệu tăng. |
| RAW-028 | Người dùng muốn giao diện tiếng Việt, dễ hiểu và thao tác thu phí đơn giản. |

Cột *Stakeholder*, *Source*, *Evidence Reference* của các RAW này không đổi.

## 4. Việc dành cho PO (chưa áp dụng)

Đây là đề xuất để PO cân nhắc, nhóm **chưa sửa** MoSCoW trong file nào. Nếu đổi MoSCoW thì phải đổi cùng lúc cột Priority (Must = High, Should = Medium, Could = Low), Backlog, Sprint Plan, nhãn và field trên GitHub Project.

| Story | Hiện tại | Gợi ý |
|---|---|---|
| US-03 Đổi mật khẩu | Must | Giữ Must: mật khẩu ban đầu được cấp sẵn nên người dùng cần đổi được. |
| US-33 Tổng đóng góp tự nguyện theo đợt | Must | Giữ Must: thống kê khoản đóng góp là nhu cầu có trong đề bài. |
| US-17 Đổi đơn giá, hạn nộp, ngừng áp dụng khoản thu | Must | PO cân nhắc hạ xuống Should nếu ở bản đầu có thể tạo khoản thu mới thay cho việc sửa. |
| US-31 Danh sách hộ chưa đóng hoặc còn nợ | Must | PO cân nhắc: tra cứu từng hộ (US-27) đã đủ cho luồng thu, còn danh sách tổng hợp là thống kê. Nếu hạ thì Priority hạ theo. |
| US-41 Tạo, vô hiệu hóa tài khoản | Should | PO cân nhắc nâng lên Must, vì cấp tài khoản là bước đầu của luồng sử dụng và hiện đang ở Sprint 2. |
| Có thêm trường dân cư của Bài 6.1 vào US-10 không | Chưa | Khuyến nghị **không thêm** (bài toán khác, AS-18/OQ-07 đang mở). |

Khi PO quyết định, nhóm sẽ cập nhật 05/06 và GitHub rồi ghi vào mục này.

## 5. Còn mở

- Số liệu trong NFR (3 giây, quy mô dữ liệu, số lần đăng nhập sai, tần suất và số bản sao lưu) vẫn là giả định, cần stakeholder xác nhận.
- Hai kịch bản SIM-OBS-01 và SIM-SURVEY-01 chưa thực hiện; nếu thực hiện thì mới có bằng chứng thật.
- GitHub Assignee chờ username của các thành viên (Thanh Tuấn: `GreentunaNTT`).
