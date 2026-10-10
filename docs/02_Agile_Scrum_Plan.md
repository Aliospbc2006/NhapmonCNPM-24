# 02 — Agile / Scrum Plan: BlueMoon v1.0

| Mục | Giá trị |
|---|---|
| Phiên bản tài liệu | 0.1 (bản nháp, chờ nhóm xác nhận) |
| Cập nhật | 2026-10-03 |
| Nhóm | Nhóm 24 — 6 thành viên |
| Liên quan | [01_Project_Overview.md](01_Project_Overview.md) |

> **Ghi chú.**
> - Đề bài và hướng dẫn BTL không nói ai giữ vai trò nào. **Cách phân vai ở mục 1 là đề xuất**, cả nhóm cần xác nhận.
> - "Product Owner" trong nhóm chỉ đại diện cho Ban quản trị trong phạm vi BTL, không phải khách hàng thật. Các ý kiến "của Ban quản trị" trong tài liệu vẫn là thông tin stakeholder theo kịch bản.
> - Product Backlog và Sprint Plan ở `deliverables/06_Product_Backlog_Sprint_Plan.xlsx`. Cách dựng bảng GitHub Project ở `docs/05_GitHub_Project_Setup.md`.

---

## 1. Vai trò Scrum

| Vai trò Scrum | Thành viên (đề xuất) | Số người |
|---|---|---|
| **Product Owner (PO)** | Thanh Tuấn | 1 |
| **Scrum Master (SM)** | Châu Tuấn | 1 |
| **Development Team (Dev)** | Thành Nam, Đức Quang, Mạnh Trường, Tiến Thành | 4 |

Một số điểm cần nhớ:
- Mỗi người giữ một vai trò chính. PO và SM vẫn có thể nhận task tài liệu hoặc kiểm tra chéo, nhưng **không tự review và không tự duyệt sản phẩm của mình**.
- Khi bắt đầu viết code, PO và SM nên nhận ít task hơn Dev.
- Có thể đổi vai trò giữa các sprint nếu cả nhóm đồng ý. Khi đó sửa lại bảng này.

## 2. Trách nhiệm từng vai trò

### Product Owner
- Giữ và sắp xếp **Product Backlog** theo giá trị và ưu tiên (MoSCoW).
- Giữ đúng phạm vi: v1.0 có 7 nhóm chức năng. Yêu cầu về phí gửi xe, điện, nước, internet ghi vào danh sách *Roadmap v2.0*, không đưa vào Sprint Backlog v1.0.
- Làm rõ yêu cầu, trả lời câu hỏi của Dev, viết hoặc duyệt Acceptance Criteria.
- Họp Sprint Planning và Sprint Review. Chấp nhận hoặc từ chối kết quả dựa trên Acceptance Criteria.
- Quyết định *làm gì và làm trước cái nào*. Cách làm là việc của Dev.

### Scrum Master
- Giúp nhóm làm đúng quy trình đã thống nhất. Tổ chức Sprint Planning, Daily, Review, Retrospective.
- Gỡ blocker cho nhóm và nhắc mọi người cập nhật bảng công việc.
- Tạo và quản lý repository, bảng GitHub Project, quyền truy cập (xem mục 7).
- Theo dõi tiến độ sprint và viết báo cáo ngắn cuối mỗi sprint.
- SM không ra lệnh cho nhóm, chỉ hỗ trợ nhóm tự quản lý.

### Development Team (Dev)
- Cùng chọn lượng việc nhận trong Sprint Planning, chia User Story thành task nhỏ và ước tính.
- Làm task (tài liệu, thiết kế, code, kiểm thử) cho đến khi đạt Definition of Done.
- Review sản phẩm của nhau (mục 4) và cập nhật bảng công việc hằng ngày.
- Báo blocker và rủi ro sớm cho SM/PO.
- Tự chia việc trong sprint. Mỗi task có đúng một người phụ trách (assignee).

## 3. Quy trình xử lý task

Luồng trạng thái trên bảng (GitHub Project theo mẫu Scrum, Bài 3.3 của đề: 5 cột):

```
Product Backlog → Sprint Backlog → Todo → Review → Done
```

| Cột | Ý nghĩa | Ai chuyển vào | Điều kiện vào cột |
|---|---|---|---|
| **Product Backlog** | Danh sách mọi hạng mục, đã xếp ưu tiên, chưa cam kết làm | PO | Hạng mục có mô tả rõ ràng và mức ưu tiên |
| **Sprint Backlog** | Hạng mục được chọn cho sprint hiện tại | Cả nhóm, trong Sprint Planning | Có Acceptance Criteria; có ước tính; vừa năng lực sprint |
| **Todo** | Đã chia thành task nhỏ (khoảng 1–2 ngày công trở xuống), có người nhận, sẵn sàng làm | Assignee | Có assignee; hiểu rõ Acceptance Criteria |
| **Review** | Đã làm xong, chờ người khác xem xét | Assignee | Đã tự kiểm tra theo DoD; có link PR hoặc tài liệu cần xem; đã chỉ định reviewer |
| **Done** | Đạt Definition of Done | Reviewer (sau khi duyệt); PO chấp nhận với User Story | Reviewer approve; PO chấp nhận kết quả theo Acceptance Criteria |

> **OPTIONAL / TEAM DECISION: nhãn "In Progress".** Bảng mẫu của giảng viên (Bài 3.3) chỉ có 5 cột ở trên, không có "In Progress". Nhóm có thể dùng "In Progress" làm nhãn phụ *trong cột Todo* để đánh dấu task đang làm, hoặc bỏ qua. Đây là ý của nhóm, **không phải yêu cầu của giảng viên**, và vẫn là câu hỏi mở. Sheet Legend của file 06 cũng ghi nhãn này là tùy chọn.

Quy tắc luồng:
1. **Không bỏ qua cột.** Task không đi thẳng từ Todo sang Done mà không qua Review.
2. **Review không đạt:** reviewer ghi nhận xét rõ ràng và chuyển task về **Todo**. Assignee sửa rồi đưa lại vào **Review**.
3. **Bị chặn:** gắn nhãn `blocked`, ghi lý do trong comment và báo SM trong ngày; task vẫn giữ nguyên cột.
4. **Giới hạn công việc dở dang (WIP):** mỗi người tối đa 2 task đang làm cùng lúc (đề xuất của nhóm); ưu tiên hoàn thành và review trước khi nhận task mới.
5. **Thay đổi giữa sprint:** không thêm hạng mục mới vào sprint đang chạy, trừ khi PO và Dev đồng ý đổi một hạng mục có cùng độ lớn. Yêu cầu mới đưa vào Product Backlog.
6. **Yêu cầu v2.0:** gắn nhãn `roadmap-v2.0` trong danh sách riêng, không vào Product Backlog v1.0 và không kéo vào Sprint Backlog.

Nhịp làm việc (đề xuất, xem SQ-02):
- **Sprint:** 1 tuần.
- **Sprint Planning:** đầu sprint.
- **Daily Scrum:** 15 phút mỗi ngày.
- **Sprint Review và Retrospective:** cuối sprint.

## 4. Review process

Áp dụng cho mọi sản phẩm: tài liệu, thiết kế, code.

1. **Tự kiểm tra:** assignee tự rà soát theo checklist DoD (mục 5) trước khi chuyển sang Review.
2. **Chỉ định reviewer:** reviewer là **một thành viên khác** với assignee. Với code, tối thiểu 1 reviewer là Dev.
3. **Thời hạn:** reviewer phản hồi trong 1 ngày làm việc. Quá hạn thì nhắc trong kênh nhóm; SM điều phối nếu bị kẹt.
4. **Nội dung review:**
   - Tài liệu: đúng phạm vi v1.0/v2.0, đúng ID, giữ truy vết (RAW → Epic → Feature → User Story → AC), nguồn dữ liệu stakeholder được ghi rõ.
   - Code (khi có): chạy được, đúng Acceptance Criteria, dễ đọc, không lộ thông tin nhạy cảm.
5. **Kết quả:** *Approve* → task sang Done. *Request changes* → task về Todo kèm nhận xét cụ thể.
6. **Chấp nhận User Story:** sau khi các task của User Story xong, PO kiểm tra theo Acceptance Criteria rồi mới đóng User Story.
7. **Sprint Review:** cuối sprint, nhóm trình bày kết quả đã Done cho PO. Hạng mục chưa đạt DoD không được tính là hoàn thành.

## 5. Definition of Done (sơ bộ)

Bản sơ bộ, sẽ tinh chỉnh khi có Product Backlog và bắt đầu code.

**Chung cho mọi task:**
- [ ] Đáp ứng đầy đủ Acceptance Criteria liên quan.
- [ ] Đã được ít nhất một thành viên khác review và approve.
- [ ] Nằm trong phạm vi v1.0 (không có nội dung phí gửi xe, điện, nước, internet).
- [ ] Thẻ công việc được cập nhật đầy đủ (người phụ trách, ước tính thực tế, link kết quả).

**Với tài liệu:**
- [ ] ID thống nhất (RAW-001…, NFR-001…, EPIC-01…, FEAT-01…, US-01…, AC-US01-01…) và có truy vết.
- [ ] Nội dung stakeholder, wish list, yêu cầu ghi rõ nguồn là kịch bản role-play (docs/03).
- [ ] Không có biên bản, chữ ký, ngày phỏng vấn, ghi âm hay ảnh khảo sát giả.
- [ ] Không mâu thuẫn với [01_Project_Overview.md](01_Project_Overview.md); đã chính tả.

**Với tính năng (áp dụng từ giai đoạn code):**
- [ ] Code chạy được trên nhánh đã merge vào `main`, không làm hỏng chức năng đã có.
- [ ] Đã kiểm thử theo Acceptance Criteria (có ghi nhận kết quả kiểm thử).
- [ ] Không commit mật khẩu, thông tin kết nối thật hay dữ liệu cư dân thật.

## 6. Quy tắc cập nhật công việc

1. **Bảng công việc là nguồn sự thật duy nhất** về trạng thái. Việc gì chưa có thẻ thì chưa tính là việc của sprint.
2. **Mỗi task một thẻ**, gồm: ID hoặc tên liên kết (ví dụ `US-xx`), mô tả ngắn, Acceptance Criteria hoặc link tới AC, người phụ trách, ước tính, nhãn ưu tiên và nhãn nhóm chức năng.
3. **Cập nhật hằng ngày** trước Daily Scrum: kéo thẻ đúng cột, ghi comment ngắn nếu có thay đổi quan trọng.
4. **Đổi phạm vi hoặc Acceptance Criteria** phải qua PO và ghi lại trong thẻ.
5. **Bị chặn:** gắn nhãn `blocked` và báo ngay (xem mục 3).
6. **Không xóa thẻ** để che lỗi hay trễ hạn; chuyển cột hoặc ghi chú để giữ lịch sử.
7. **Cuối sprint**, SM rà soát bảng; hạng mục chưa Done quay lại Product Backlog hoặc chuyển sprint sau do PO quyết định.

## 7. Quy tắc Git/GitHub (mức đơn giản)

> Repository GitHub của nhóm: https://github.com/Aliospbc2006/NhapmonCNPM-24. Việc xử lý review của thành viên ghi ở `docs/06_Team_Review_Response.md`.

1. **Một repository chung**, nhánh chính là `main`. **Không push trực tiếp lên `main`.**
2. **Nhánh làm việc** đặt tên theo mẫu:
   - `docs/<mô-tả-ngắn>` — tài liệu.
   - `feature/US-xx-<mô-tả-ngắn>` — tính năng (khi có User Story).
   - `fix/<mô-tả-ngắn>` — sửa lỗi.
3. **Commit nhỏ, rõ ràng**, nội dung dạng: `loại: mô tả ngắn [US-xx hoặc task]`, ví dụ `docs: thêm Project Overview`. Mỗi commit một thay đổi có ý nghĩa.
4. **Pull Request (PR)** để đưa vào `main`:
   - Mô tả thay đổi, liên kết tới thẻ công việc.
   - Cần ít nhất **1 reviewer approve** (khác người tạo PR) mới được merge.
   - Người tạo PR không tự merge khi chưa có approve.
5. **Cập nhật trước khi làm:** kéo `main` mới nhất về trước khi tạo nhánh hoặc trước khi tạo PR để giảm xung đột.
6. **Xử lý xung đột:** người tạo PR tự giải quyết; cần giúp thì nhờ SM.
7. **Không** `force push` lên `main`; **không** commit file nhạy cảm (mật khẩu, thông tin kết nối thật, dữ liệu cư dân thật). Dùng `.gitignore` cho file cấu hình riêng.
8. **File mẫu của giảng viên:** giữ nguyên bản gốc, chỉ làm việc trên bản copy.
9. **Quyền deploy / phát hành (đề xuất, chờ nhóm xác nhận):** chỉ Scrum Master (người quản lý dự án) hoặc một Dev do SM chỉ định mới được merge PR vào `main` và triển khai bản phát hành, sau khi PR đã có approve và PO đã chấp nhận các User Story liên quan. Các thành viên khác không tự triển khai. (Theo Bài 2.3, Bước 2-2: việc deploy do người có trách nhiệm và kinh nghiệm, thường là người quản lý dự án.)
10. **GitHub Project:** dùng bảng theo mẫu Scrum với 5 cột `Product Backlog | Sprint Backlog | Todo | Review | Done` (khớp mục 3 và Bài 3.3). Cột "In Progress" chỉ là tùy chọn của nhóm (OPTIONAL / TEAM DECISION).

## 8. Quy tắc communication của nhóm

1. **Kênh chính:** nhóm chọn **một** kênh nhắn tin chung để trao đổi hằng ngày (xem SQ-04). Quyết định quan trọng phải được ghi lại trong thẻ công việc hoặc PR, không chỉ nằm trong tin nhắn.
2. **Daily Scrum (15 phút)**, mỗi người trả lời ngắn:
   - Hôm qua đã làm gì?
   - Hôm nay sẽ làm gì?
   - Có blocker nào không?

   Nếu không họp được, gửi cập nhật bằng văn bản vào kênh chung trước giờ đã thống nhất.
3. **Sprint Planning (đầu sprint):** PO trình bày mục tiêu và các hạng mục ưu tiên; Dev chọn lượng việc cam kết và chia task.
4. **Sprint Review (cuối sprint):** trình bày kết quả đã Done cho PO.
5. **Retrospective (cuối sprint):** mỗi người nêu điều làm tốt, điều cần cải thiện, một hành động cho sprint sau.
6. **Phản hồi:** trả lời tin nhắn liên quan đến công việc trong vòng 1 ngày làm việc; việc gấp ghi rõ "gấp" và báo SM.
7. **Báo sớm:** nếu dự đoán trễ hoặc vắng, báo SM và PO càng sớm càng tốt, kèm đề xuất xử lý.
8. **Cách ra quyết định:**
   - Về phạm vi và ưu tiên: PO quyết định.
   - Về cách thực hiện: Dev quyết định.
   - Về quy trình và cách phối hợp: cả nhóm thống nhất, SM điều phối.
   - Bất đồng không giải quyết được trong nhóm: SM tổng hợp các phương án và hỏi ý kiến giảng viên.
9. **Biên bản họp nội bộ:** nếu có, chỉ ghi các cuộc họp **thật** của nhóm, ghi đúng người tham dự. Tuyệt đối không ghi biên bản họp hoặc phỏng vấn với stakeholder khi chưa diễn ra.
10. **Văn hóa:** góp ý vào sản phẩm, không công kích cá nhân; mọi thành viên đều được đặt câu hỏi.

## 9. Lựa chọn mô hình quy trình (Bài 2.3, Bước 1)

Nhóm trả lời các câu hỏi gợi ý của Bài 2.3 trước khi chọn mô hình. Nguồn: phần "Giới thiệu bài toán" [Đề bài] hoặc suy luận của nhóm.

| # | Câu hỏi | Trả lời |
|---|---|---|
| 1 | Phần mềm mới hay không? | Mới. Thay việc thu phí thủ công bằng Excel và sổ giấy bằng một ứng dụng [Đề bài]. |
| 2 | Phạm vi áp dụng? | Phần mềm nội bộ cho Ban quản trị chung cư BlueMoon, thay đổi cách quản lý thu phí và thông tin hộ dân cư [Đề bài]. |
| 3 | Vai trò của các bên liên quan? | Ban quản trị là khách hàng và người dùng chính; cư dân, cơ quan chức năng là stakeholder gián tiếp (`01_Project_Overview.md`, mục 6). |
| 4 | Quy trình nghiệp vụ đã rõ chưa? | Tương đối rõ (thu phí, hộ gia đình, nhân khẩu) nhưng còn nhiều câu hỏi mở cần làm rõ dần (OQ-xx trong `04_Interview_Report.md`). |
| 5 | Kích thước phần mềm? | Nhỏ: v1.0 có 7 nhóm chức năng, 41 User Story, 143 Story Point (file 06). |
| 6 | Đội ngũ cần bao nhiêu người? | 6 thành viên (1 PO, 1 SM, 4 Developer), xem mục 1. |

**Kết luận: nhóm dùng Agile/Scrum.** Lý do:
1. Nhiều yêu cầu vẫn cần làm rõ, nên chia thành sprint nhỏ để PO góp ý sớm.
2. Sản phẩm nhỏ, nhóm nhỏ, vừa với Scrum (Product Backlog, Sprint Backlog, 3 sprint).
3. Chương 3 của bộ bài tập hướng dẫn quản lý công việc theo Agile-Scrum trên GitHub.
4. Xếp ưu tiên theo MoSCoW giúp đưa Must vào sprint đầu và để Should/Could lại sau.

Thành viên và vai trò: xem mục 1 (đề xuất, chờ nhóm xác nhận, SQ-01).

## 10. Công cụ và môi trường (Bài 2.3, Bước 2-2)

| Hạng mục | Quy định |
|---|---|
| Quản lý mã nguồn, phiên bản | Git và GitHub; quy tắc nhánh, commit, Pull Request ở mục 7. |
| Quản lý công việc | GitHub Project theo mẫu Scrum, 5 cột (mục 3, mục 7). |
| Công nghệ, môi trường phát triển | Ứng dụng desktop Java, dữ liệu trên MySQL server [Đề bài]. IDE, phiên bản JDK và MySQL: chưa chốt (TEAM DECISION). |
| Quyền deploy | Mục 7, điều 9. |
| Giao tiếp | Mục 8. |

## 11. Kế hoạch tổng thể ban đầu (Bài 2.3, Bước 2-1)

Kế hoạch theo thứ tự công đoạn, **chưa có ngày cụ thể** vì nhóm chưa chốt độ dài sprint và hạn nộp (SQ-02, TEAM DECISION). Khi có hạn nộp, SM thêm cột thời gian.

| Công đoạn | Nội dung | Sản phẩm |
|---|---|---|
| Giai đoạn 1 | Project Overview, kế hoạch Agile/Scrum | `01_Project_Overview.md`, `02_Agile_Scrum_Plan.md` |
| Giai đoạn 2 | Kế hoạch khai phá yêu cầu, Client's Wish List, Raw Requirement | `03_Requirement_Elicitation_Plan.md`, `04_Interview_Report.md`, `04_Raw_Requirements.xlsx` |
| Giai đoạn 3 | As-Is, Pain Point, To-Be (Visionary), NFR | `04_AsIs_ToBe.md` |
| Giai đoạn 4 | Epic, Feature, User Story, Acceptance Criteria | `05_Epic_UserStory.xlsx` |
| Giai đoạn 5 | Product Backlog (thứ tự, MoSCoW, Story Point) | `06_Product_Backlog_Sprint_Plan.xlsx` |
| Giai đoạn 6 | Sprint Planning: Sprint 1, 2, 3 và Sprint Backlog | `06_Product_Backlog_Sprint_Plan.xlsx` |
| Giai đoạn 7 | Rà soát cuối, chuẩn bị GitHub Project | `05_GitHub_Project_Setup.md`, `FINAL_DELIVERABLES.md` |
| Giai đoạn 8 | Tạo GitHub Project, Issue User Story và task | `05_GitHub_Project_Setup.md` |
| Giai đoạn 9 | Xác thực và xử lý review của thành viên | `06_Team_Review_Response.md` |
| Sprint 1 → 3 | Thực hiện theo Sprint Backlog (khi bắt đầu giai đoạn code) | Xem sheet Sprint_1, Sprint_2, Sprint_3 |

## Câu hỏi mở (liên quan Scrum)

| ID | Câu hỏi | Mặc định tạm dùng |
|---|---|---|
| SQ-01 | Nhóm có đồng ý phân vai: PO — Thanh Tuấn, SM — Châu Tuấn, Dev — Thành Nam, Đức Quang, Mạnh Trường, Tiến Thành không? | Phân vai ở mục 1 |
| SQ-02 | Độ dài sprint và thời hạn (deadline) các mốc của BTL là gì? | Sprint 1 tuần; chưa có ngày cụ thể |
| SQ-03 | Ai tạo và quản lý repository GitHub, khi nào tạo? | Scrum Master, sau khi nhóm đồng ý |
| SQ-04 | Nhóm dùng kênh liên lạc chính nào, giờ Daily cố định lúc nào? | Chưa chốt |
