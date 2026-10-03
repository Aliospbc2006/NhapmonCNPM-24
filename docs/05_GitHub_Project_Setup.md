# 05. Hướng dẫn thiết lập GitHub Project — BlueMoon (Nhóm 23)

**Phase 7.** Đây chỉ là tài liệu **hướng dẫn**. Nhóm chưa tạo GitHub Project, Issue, commit hay push nào. Khi cả nhóm đồng ý thì làm theo các bước bên dưới. Người phụ trách là Scrum Master (Châu Tuấn), theo `docs/02_Agile_Scrum_Plan.md`.

- Repository của nhóm: https://github.com/Aliospbc2006/NhapmonCNPM-24
- Dữ liệu để nhập lấy từ `deliverables/06_Product_Backlog_Sprint_Plan.xlsx` (sheet Product_Backlog, Sprint_1, Sprint_2, Sprint_3).
- Stakeholder, Wish, RAW và User Story đều là **Simulated stakeholder input** (*yêu cầu giả lập từ bối cảnh bài toán*). Khi tạo Issue, giữ dòng ghi chú này trong mô tả.

## Tóm tắt kế hoạch

| Hạng mục | Số lượng | Ghi chú |
|---|---|---|
| Product Backlog | 41 User Story | 21 Must, 18 Should, 2 Could; 143 Story Point |
| Sprint 1 | 11 story, 34 SP, 55 task, 202 giờ | Nền tảng, tài khoản, hộ, nhân khẩu |
| Sprint 2 | 10 story, 37 SP, 46 task, 174 giờ | Khoản thu và thu phí |
| Sprint 3 | 10 story, 35 SP, 49 task, 195 giờ | Tra cứu, thống kê, an toàn dữ liệu, ổn định hóa |
| Chưa xếp Sprint | 10 story, 37 SP | Should/Could, ở lại Product Backlog |
| Roadmap v2.0 | 0 story | RAW-029, RAW-030 không tạo Issue |

## 1. Tạo GitHub Project

1. Vào repository, mở tab **Projects**, chọn **New project** (hoặc vào trang cá nhân/tổ chức, tab Projects).
2. Chọn template **Team planning** hoặc **Table** (view nào cũng được; nhóm sẽ thêm view Board ở bước 2).
3. Đặt tên: `BlueMoon v1.0 — Nhóm 23`.
4. Mở **Settings** của Project, mục **Manage access**: thêm đủ 6 thành viên, mức *Write* trở lên. PO và SM nên có quyền *Admin*.
5. Liên kết Project với repository: trong Project, **Settings → Link a repository** (hoặc từ tab Projects của repo, **Link a project**).
6. Mở view **Board** và đặt cột nhóm theo trường Status (bước 2).

Không tạo Project thứ hai cho v2.0. Hạng mục roadmap chỉ nằm trong tài liệu (`docs/04_AsIs_ToBe.md`, mục 5).

## 2. Cột trạng thái (Status)

Trường **Status** có sẵn trong Project. Sửa danh sách lựa chọn thành 5 giá trị theo bảng mẫu của giảng viên (Bài 3.3), đúng thứ tự (`docs/02_Agile_Scrum_Plan.md`, mục 3):

```
Product Backlog → Sprint Backlog → Todo → Review → Done
```

| Status | Dùng cho | Ai chuyển vào |
|---|---|---|
| Product Backlog | Story chưa xếp sprint (10 story Unplanned) | PO |
| Sprint Backlog | Story đã chọn cho một sprint; task của sprint chưa bắt đầu | Cả nhóm khi Sprint Planning |
| Todo | Task của sprint đang chạy, đã có Assignee, sẵn sàng làm | Assignee |
| Review | Task xong, chờ reviewer xem | Assignee |
| Done | Reviewer đã approve; story được PO chấp nhận | Reviewer (task), PO (story) |

> **OPTIONAL / TEAM DECISION: "In Progress".** Bảng mẫu của giảng viên không có cột này. Nếu muốn, nhóm có thể thêm giá trị `In Progress` giữa Todo và Review (thành 6 giá trị), hoặc dùng làm nhãn phụ trong Todo. Đây là ý của nhóm, không phải yêu cầu của giảng viên. Tài liệu này mặc định dùng 5 cột.

Trong file 06, mọi task đang có Status = **Todo** (trạng thái ban đầu của kế hoạch). Trên GitHub, task của Sprint 2 và Sprint 3 nên để ở **Sprint Backlog** cho tới khi sprint đó bắt đầu, rồi chuyển sang Todo lúc Sprint Planning.

## 3. Các trường (Fields)

Tạo thêm các trường sau bằng **+ New field** ở cuối bảng. Cột "Lấy từ" cho biết lấy dữ liệu ở đâu.

| Trường | Kiểu | Giá trị | Lấy từ (file 06) |
|---|---|---|---|
| Title | Có sẵn | `[US-03] Đổi mật khẩu cá nhân` hoặc `[S1-T05] Xây form đổi mật khẩu` | Product_Backlog / Sprint_n |
| Type | Single select | `User Story`, `Technical Story`, `Task` | Cột User Story ("Technical Story" ghi ở US ID) |
| US ID | Text | `US-03`. Với task chung (không gắn story) để trống hoặc ghi `—` | US ID |
| Sprint | **Iteration** | Sprint 1, Sprint 2, Sprint 3 (bước 4). Story Unplanned để trống | Planned Sprint |
| Priority | Single select | High, Medium, Low | Priority |
| MoSCoW | Single select | Must, Should, Could | MoSCoW |
| Story Points | Number | Chỉ điền cho story (2, 3, 5, ...) | Story Points |
| Estimate (h) | Number | Chỉ điền cho task (2, 3, 4, 6, 8) | Estimate (h) |
| Assignee | Có sẵn | Người làm | Assignee |
| Reviewer | Single select | 6 tên thành viên (khác Assignee) | Reviewer |
| Status | Có sẵn | 5 giá trị ở bước 2 | Status |

Trường **Estimate (h)** là thêm ngoài danh sách tối thiểu, vì file 06 ước lượng task theo giờ còn story theo Story Point. Nhóm có thể bỏ nếu thấy không cần.

Cần trường **Reviewer** riêng vì trường Reviewers có sẵn của GitHub chỉ dùng cho Pull Request, không dùng cho Issue.

Nhãn (Labels) trên Issue: `user-story`, `technical-story`, `task`, `epic-01` … `epic-07`, `cross-cutting`, `blocked`. Không tạo nhãn `roadmap-v2.0` vì v2.0 không có Issue. Chỉ dùng nhãn này nếu sau này nhóm muốn theo dõi riêng (`docs/02` mục 3).

## 4. Iteration Sprint 1/2/3

1. **+ New field** → tên `Sprint` → kiểu **Iteration**.
2. Chọn độ dài iteration. Nhóm **chưa chốt** độ dài và ngày sprint (SQ-02, đề xuất 1 tuần). Nếu chưa chốt thì đặt tạm 1 tuần, sửa sau.
3. Đặt tiêu đề lần lượt `Sprint 1`, `Sprint 2`, `Sprint 3`, ba iteration liền nhau. Xóa các iteration thừa GitHub tạo sẵn.
4. Nếu bản GitHub của nhóm chưa có Iteration, dùng trường Single select tên `Sprint` với giá trị `Sprint 1`, `Sprint 2`, `Sprint 3`, `Unplanned`.
5. Tạo view **Sprint board**: Board, lọc `Sprint:@current`, nhóm theo Status.
6. Mục tiêu từng sprint (copy từ sheet Sprint_n) ghi vào phần mô tả của view hoặc vào Issue/Discussion đầu sprint. Mục tiêu đầy đủ nằm ở ô *Sprint Goal* trong sheet.

## 5. Nhập Product Backlog

GitHub Projects không nhập trực tiếp file Excel/CSV. Có hai cách, nhóm nên chọn cách A:

**Cách A: tạo Issue từ bảng (thủ công nhưng dễ kiểm soát).**
1. Mở sheet **Product_Backlog** trong file 06. Làm việc theo thứ tự cột *Order* (1 → 41).
2. Tạo Issue cho từng story theo mục 6, rồi thêm Issue vào Project (**Add item** → chọn Issue).
3. Điền các trường Type, US ID, Sprint, Priority, MoSCoW, Story Points, Status theo từng dòng.
4. Dùng view dạng bảng, điền hàng loạt bằng cách chọn một ô rồi kéo (fill) hoặc copy-paste giữa các ô cùng cột.

**Cách B: tạo item nháp bằng cách dán nhiều dòng.** Trong view bảng, ở dòng **+ Add item**, dán nhiều dòng một lần (mỗi dòng một tiêu đề) để GitHub tạo nhiều *draft item*. Sau đó điền các trường và chuyển draft thành Issue (**Convert to issue**). Cách này nhanh hơn nhưng phải đếm lại số lượng.

**Tùy chọn: script GitHub CLI.** Nhóm có thể tự viết script `gh issue create` và `gh project item-add` đọc từ file 06, cần chạy `gh auth refresh -s project`. Phase 7 không tạo hay chạy script nào. Chỉ chạy khi người quản lý repo đồng ý.

Kiểm tra sau khi nhập:

| Kiểm tra | Kết quả đúng |
|---|---|
| Số story trong Project | 41 (Product Backlog có 10 Unplanned, Sprint Backlog có 31) |
| Tổng Story Points | 143; trong đó đã xếp sprint: 106 |
| Số story Must | 21, tất cả có Sprint |
| Sprint 1 / 2 / 3 | 11 / 10 / 10 story |
| Story có US ID lặp | 0 |

## 6. Tạo Issue từ User Story

**Ánh xạ:** 1 User Story = 1 Issue (`Type = User Story` hoặc `Technical Story`). 41 story = 41 Issue.

Quy ước tiêu đề: `[US-03] Đổi mật khẩu cá nhân`. Gắn nhãn `user-story` (hoặc `technical-story`) và nhãn Epic (`epic-01` …).

Mẫu nội dung Issue (điền từ sheet **Product_Backlog** và sheet **Epic-Focused User Story Map** của file 05):

```markdown
**User Story:** Là một [vai trò], tôi muốn [mục tiêu], để [giá trị nghiệp vụ].

**Epic / Feature:** EPIC-01 Quản lý tài khoản và truy cập / FEAT-01-02 Tự phục vụ tài khoản
**Nguồn RAW:** RAW-002
**MoSCoW / Priority / SP:** Must / High / 2
**Phụ thuộc:** US-01

## Acceptance Criteria
(Dán nguyên văn các AC từ file 05, dạng Given / When / Then)
- [ ] AC-US03-01 …
- [ ] AC-US03-02 …

## Task
(xem mục dưới)

> Simulated stakeholder input (yêu cầu giả lập từ bối cảnh bài toán).
```

Không viết lại hay rút gọn Acceptance Criteria. File 05 là nguồn chuẩn. Nếu AC đổi thì sửa file 05 trước, rồi mới cập nhật Issue.

**Ánh xạ Task:** 150 task trong Sprint_1/2/3 (55 + 46 + 49). Tổng 117 + 24 + 9 = 150.

| Loại task | Cách tạo |
|---|---|
| Task gắn đúng một story (117 task) | **Sub-issue** của Issue story (hoặc Issue riêng có link `Part of #…` nếu repo chưa có sub-issue). Tiêu đề `[S1-T05] …`, `Type = Task`, `US ID` = story cha |
| Task chung, không gắn story (24 task: kiểm thử hồi quy, tài liệu, hướng dẫn, demo) | Issue độc lập, nhãn `cross-cutting` |
| Task PO nghiệm thu nhiều story (9 task, 3 task mỗi sprint) | Issue độc lập, liệt kê các US liên quan trong mô tả, `Blocked by` các task kiểm thử của các story đó |
| Task nhỏ cần theo dõi nhẹ | Có thể dùng checklist `- [ ] S1-T05 …` trong Issue story thay cho sub-issue. Khi đó không gán Assignee/Reviewer riêng cho từng task được |

Mỗi task có sẵn Assignee, Reviewer, Estimate (h), Dependency và Deliverable trong sheet Sprint_n. Chép các cột này vào Issue task. Dependency `S1-T03` hoặc `US-01` ghi thành link Issue (`Blocked by #…`).

Lưu ý khi tạo Issue: **không** bỏ qua Reviewer (khác Assignee) và **không** chuyển task sang Done khi tạo.

## 7. Quản lý một Sprint

**Trước sprint (Sprint Planning):**
1. PO xác nhận thứ tự Product Backlog và mục tiêu sprint (sheet Sprint_n).
2. Cả nhóm đọc danh sách story của sprint, kiểm tra phụ thuộc và khối lượng (cột Total Story Points, Total Estimate).
3. Đặt `Sprint = Sprint n` cho story và task của sprint; story ở **Sprint Backlog**; task chuyển sang **Todo**.
4. Mỗi người nhận task theo cột Assignee. Điều chỉnh nếu có người vắng và ghi lại lý do trong Issue.

**Trong sprint:**
1. Họp Daily ngắn: làm gì hôm qua, làm gì hôm nay, đang bị chặn gì. Task bị chặn gắn nhãn `blocked` và báo SM trong ngày.
2. Mỗi người chỉ làm tối đa 2 task cùng lúc (đề xuất của nhóm).
3. Không thêm story mới vào sprint đang chạy, trừ khi PO và Developer đồng ý đổi lấy story cùng độ lớn. Yêu cầu mới vào Product Backlog.
4. SM cập nhật Workload (so với sheet Workload_Summary) nếu có thay đổi người nhận.

**Cuối sprint:**
1. Sprint Review: trình bày story đã Done cho PO. Hạng mục chưa đạt Definition of Done không tính là xong.
2. Story chưa xong quay về **Sprint Backlog** của sprint kế hoặc về **Product Backlog**, ghi lý do.
3. Retrospective: ghi vào Discussion hoặc Issue `Retro Sprint n`.
4. Cập nhật file 06 (Planned Sprint, Status) nếu kế hoạch đổi, giữ nhất quán với Project.

## 8. Chuyển task: Todo → Review → Done

| Bước | Ai làm | Điều kiện | Ghi chú |
|---|---|---|---|
| Bắt đầu làm (vẫn ở Todo) | Assignee | Task đã có Assignee và đã hiểu Acceptance Criteria; chưa vượt 2 task đang làm | Tạo nhánh `feature/US-03-change-password` nếu là task code (`docs/02` mục 7). Có thể gắn nhãn phụ `In Progress` nếu nhóm chọn (OPTIONAL / TEAM DECISION) |
| Todo → Review | Assignee | Đã tự kiểm tra theo Definition of Done; có link PR hoặc tài liệu; đã chỉ định Reviewer | Mở Pull Request, ghi `Closes #…` hoặc `Refs #…` |
| Review → Done | Reviewer | Reviewer (khác Assignee) approve; đủ điều kiện DoD | Task code: Developer review Developer. PO và SM không nhận task code |
| Review → Todo | Reviewer | Chưa đạt: ghi nhận xét cụ thể | Assignee sửa rồi đưa lại Review |
| Story → Done | PO | Mọi task của story đã Done và PO kiểm tra đạt từng Acceptance Criteria | PO chấp nhận story, chỉ khi mọi AC đạt |

Quy tắc: **không bỏ qua cột**, và không có task nào từ Todo sang Done trực tiếp mà không qua Review.

Trạng thái hiện tại của kế hoạch: **không có task nào Done.**

## 9. Trạng thái thiết lập

| Việc | Trạng thái |
|---|---|
| Tạo GitHub Project | Chưa làm (chờ nhóm) |
| Tạo Issue từ User Story / Task | Chưa làm |
| Commit, push, thay đổi remote | Chưa làm, theo yêu cầu của nhóm |
| Hướng dẫn thiết lập (tài liệu này) | Xong |
