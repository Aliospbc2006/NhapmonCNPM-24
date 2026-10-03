# BlueMoon — Phần mềm quản lý và thu phí chung cư

Bài tập lớn môn Nhập môn Công nghệ phần mềm (IT4080), **Nhóm 24**: Châu Tuấn (Scrum Master), Thanh Tuấn (Product Owner), Thành Nam, Đức Quang, Mạnh Trường, Tiến Thành (Developer).

Repository: https://github.com/Aliospbc2006/NhapmonCNPM-24

## Bài toán

Hiện nay Ban quản trị chung cư BlueMoon quản lý thu phí và thông tin cư dân bằng Excel và sổ giấy. Project này là phần **tài liệu** cho một phần mềm desktop (Java, MySQL) giúp Ban quản trị quản lý hộ gia đình, nhân khẩu, khoản thu và việc ghi nhận thu phí. Nhóm làm hai phần: **Requirement Elicitation** và **Agile/Scrum**. Chưa viết code ứng dụng.

> **Lưu ý về dữ liệu.** Nhóm chưa phỏng vấn, khảo sát hay quan sát thực tế. Stakeholder statement, Client Wish List, RAW requirement và User Story đều là **Simulated stakeholder input** (*yêu cầu giả lập từ bối cảnh bài toán*), dựa trên đề bài BlueMoon.

## Phạm vi

**v1.0 (triển khai):** đăng nhập và đổi mật khẩu; quản lý hộ gia đình; quản lý nhân khẩu; quản lý khoản thu; thu phí (ghi nhận thu); tra cứu / tìm kiếm; thống kê cơ bản.

**v2.0 (chỉ roadmap, Won't-have v1.0):** phí gửi xe; điện, nước, internet. Không có Epic, User Story hay task cho v2.0.

## Cách làm: Agile/Scrum

- Nhóm có 1 PO, 1 SM và 4 Developer. Task đi qua 5 cột: `Product Backlog → Sprint Backlog → Todo → Review → Done` (theo mẫu của giảng viên). Cột "In Progress" là tùy chọn, nhóm chưa quyết định. Người review phải khác người làm. Chi tiết ở `docs/02_Agile_Scrum_Plan.md`.
- Backlog đi theo thứ tự Epic → Feature → User Story (INVEST) → Acceptance Criteria (Given/When/Then). Ưu tiên theo MoSCoW, ước lượng User Story bằng Story Point (Fibonacci), ước lượng task bằng giờ.
- Độ dài và ngày của sprint **chưa chốt** (SQ-02). 3 sprint bên dưới chỉ là kế hoạch đề xuất.

## Quy trình yêu cầu

1. Kế hoạch Elicitation và Interview Script (`docs/03`).
2. Role-play 4 stakeholder (Ban quản trị, Thủ quỹ, Cư dân, Cơ quan chức năng) → 30 Wish, 30 RAW, 7 NFR (`docs/interviews/`, `docs/04_Interview_Report.md`).
3. Phân tích As-Is, pain point, To-Be (`docs/04_AsIs_ToBe.md`).
4. Chuẩn hóa thành Epic, Feature, User Story, AC (`deliverables/05`).
5. Product Backlog, Traceability, Sprint Plan (`deliverables/06`).

Quy ước ID: `RAW-001`, `NFR-001`, `EPIC-01`, `FEAT-01-01`, `US-01`, `AC-US01-01`, `S1-T01`. Truy vết: RAW → Epic → Feature → User Story → AC → Backlog → Sprint → Task.

## Cấu trúc thư mục

```
Bluemoon_Nhom24/
├── README.md
├── docs/
│   ├── 01_Project_Overview.md
│   ├── 02_Agile_Scrum_Plan.md
│   ├── 03_Requirement_Elicitation_Plan.md
│   ├── 04_Interview_Report.md
│   ├── 04_AsIs_ToBe.md
│   ├── 05_GitHub_Project_Setup.md
│   ├── FINAL_DELIVERABLES.md
│   ├── TEACHER_REQUIREMENTS_AUDIT.md   đối chiếu với yêu cầu trong 2 PDF của giảng viên
│   ├── WRITING_STYLE_REVIEW.md         ghi chú lần rà văn phong
│   └── interviews/                 4 biên bản role-play
├── deliverables/
│   ├── 04_Raw_Requirements.xlsx
│   ├── 05_Epic_UserStory.xlsx
│   └── 06_Product_Backlog_Sprint_Plan.xlsx
├── templates/
│   └── Mẫu Epic - User story.xlsx  mẫu giảng viên, giữ nguyên bản gốc
├── references/                     tài liệu nguồn (xem ghi chú)
├── 01_ Huong dan lap ke hoach phat hieu yeu cau BTL (Elicitation).pdf
└── 08. Bo Bai Tap.pdf
```

Ghi chú: hai file PDF vẫn nằm ở thư mục gốc vì lúc chuyển, Windows báo file đang mở. Đóng trình xem PDF rồi chuyển chúng vào `references/` (lệnh ở `docs/FINAL_DELIVERABLES.md`, mục 4).

## Deliverable chính

Danh sách đầy đủ, owner và trạng thái: `docs/FINAL_DELIVERABLES.md`.

| Deliverable | Nội dung |
|---|---|
| `deliverables/04_Raw_Requirements.xlsx` | Client Wish List, 30 RAW, NFR, Interview Summary |
| `deliverables/05_Epic_UserStory.xlsx` | 7 Epic, 24 Feature, 41 User Story, 123 AC |
| `deliverables/06_Product_Backlog_Sprint_Plan.xlsx` | Product Backlog, Traceability, Sprint 1/2/3, Workload, Legend |

## Tổng quan Sprint

| Sprint | Mục tiêu | Story | SP | Task | Giờ |
|---|---|---|---|---|---|
| 1 | Nền tảng, tài khoản, hộ gia đình, nhân khẩu | 11 | 34 | 55 | 202 |
| 2 | Khoản thu và ghi nhận thu phí | 10 | 37 | 46 | 174 |
| 3 | Tra cứu, thống kê, an toàn dữ liệu, ổn định hóa | 10 | 35 | 49 | 195 |
| Chưa xếp | Should/Could ở lại Product Backlog | 10 | 37 | — | — |

Tổng: 41 story (21 Must, 18 Should, 2 Could), 143 SP; đã xếp 31 story, 106 SP, 150 task, 571 giờ. Truy vết 28/28 RAW v1.0.

## Dùng GitHub Project

GitHub Project: [BlueMoon v1.0 - Nhóm 24](https://github.com/users/Aliospbc2006/projects/2). Nhóm quản lý Scrum trên board 5 cột `Product Backlog → Sprint Backlog → Todo → Review → Done`. Mỗi User Story là một Issue `[US-XX]`, mỗi task là một Issue `[Sn-Txx]` (sub-issue của story khi task gắn đúng một story). Các field, quy ước Issue và cách dùng board hằng ngày nằm trong `docs/05_GitHub_Project_Setup.md`.

## Trạng thái hiện tại

- Phase 0–7 đã xong (kế hoạch và tài liệu), đang chờ nhóm và giảng viên xem.
- Nội dung mô tả đã viết bằng tiếng Việt. Tiêu đề, tên cột và thuật ngữ chuẩn vẫn giữ tiếng Anh. Nhóm cũng đã đối chiếu với 2 PDF của giảng viên, kết quả ở `docs/TEACHER_REQUIREMENTS_AUDIT.md`.
- Văn phong đã được rà lại một lượt, xem `docs/WRITING_STYLE_REVIEW.md`.
- Phase 8: đã tạo GitHub Project, 41 Issue User Story và 150 Issue task từ dữ liệu planning. GitHub Assignee còn để trống, chờ GitHub username của thành viên.
- Chưa có code ứng dụng; các file local của thư mục này chưa được commit hay push lên repository.
- Chưa có task nào Done. Giờ làm và người nhận task mới chỉ là đề xuất.
- Các việc còn tồn đọng nằm ở `docs/FINAL_DELIVERABLES.md`, mục 4.
