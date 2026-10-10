# GitHub Project Setup — BlueMoon v1.0 (Nhóm 24)

**Giai đoạn 8.** GitHub Project, 41 Issue User Story và 150 Issue task đã được tạo từ dữ liệu đã chốt trong `deliverables/06_Product_Backlog_Sprint_Plan.xlsx` (sheet Product_Backlog, Traceability, Sprint_1/2/3) và `deliverables/05_Epic_UserStory.xlsx`. Không có requirement, User Story, Acceptance Criteria, MoSCoW, Story Point, Sprint hay phân công nào bị thay đổi.

- Repository: https://github.com/Aliospbc2006/NhapmonCNPM-24
- Project name: **BlueMoon v1.0 - Nhóm 24**
- Project URL: https://github.com/users/Aliospbc2006/projects/2
- Mô tả Project: Bảng quản lý Product Backlog, Sprint Backlog và tiến độ phát triển của dự án BlueMoon Nhóm 24.
- Stakeholder, Wish, RAW và User Story đều là thông tin stakeholder theo kịch bản.

## Tóm tắt kế hoạch

| Hạng mục | Số lượng | Ghi chú |
|---|---|---|
| Product Backlog | 41 User Story | 21 Must, 18 Should, 2 Could; 143 Story Point |
| Sprint 1 | 11 story, 34 SP, 55 task, 202 giờ | Nền tảng, tài khoản, hộ, nhân khẩu |
| Sprint 2 | 10 story, 37 SP, 46 task, 174 giờ | Khoản thu và thu phí |
| Sprint 3 | 10 story, 35 SP, 49 task, 195 giờ | Tra cứu, thống kê, an toàn dữ liệu, ổn định hóa |
| Chưa xếp Sprint | 10 story, 37 SP | Should/Could, ở lại Product Backlog, field Sprint để trống |
| Roadmap v2.0 | 0 story | RAW-029, RAW-030 không có User Story nên không tạo Issue |

## Workflow

```
Product Backlog → Sprint Backlog → Todo → Review → Done
```

Board dùng đúng 5 cột Status theo bảng mẫu của giảng viên, theo thứ tự trên. Không có cột In Progress, Testing, Blocked.

| Status | Ý nghĩa |
|---|---|
| Product Backlog | User Story chưa được đưa vào Sprint đang thực hiện |
| Sprint Backlog | User Story đã được chọn cho Sprint |
| Todo | Task cụ thể sẵn sàng thực hiện |
| Review | Công việc đã thực hiện và đang được kiểm tra |
| Done | Công việc đã đáp ứng Acceptance Criteria / Definition of Done |

### Trạng thái ban đầu trên board

| Loại | Status ban đầu |
|---|---|
| Story của Sprint 1 (11 story) | Sprint Backlog |
| Story của Sprint 2, Sprint 3 và chưa xếp Sprint (30 story) | Product Backlog (field Sprint vẫn ghi Sprint 2 / Sprint 3) cho tới khi sprint đó được kích hoạt |
| Mọi task (150 task) | Todo |
| Review, Done | Chưa có item nào |

Lưu ý: cột Status trong sheet Product_Backlog ghi "Sprint Backlog" cho cả 31 story đã xếp Sprint 1–3. Theo hướng dẫn Giai đoạn 8, chỉ story Sprint 1 được đặt ở Sprint Backlog; story Sprint 2 và 3 giữ ở Product Backlog tới khi sprint bắt đầu. Khi kích hoạt Sprint 2 hoặc 3, chuyển các story của sprint đó sang Sprint Backlog.

## Custom fields

| Field | Kiểu | Giá trị |
|---|---|---|
| Status | Single select (có sẵn, đã sửa) | Product Backlog, Sprint Backlog, Todo, Review, Done |
| Sprint | Single select | Sprint 1, Sprint 2, Sprint 3, Roadmap |
| Priority | Single select | High, Medium, Low (suy ra từ MoSCoW trong workbook; chỉ điền cho story) |
| MoSCoW | Single select | Must, Should, Could, Won't (chỉ điền cho story) |
| Story Points | Number | Chỉ điền cho story |
| Item Type | Single select | User Story, Task |
| Task Reviewer | Text | Tên reviewer của task, lấy từ cột Reviewer trong sheet Sprint_n |

GitHub không cho đặt tên field là "Type" hoặc "Reviewer" (tên dành riêng), nên hai field này tên là **Item Type** và **Task Reviewer**. Estimate (giờ) của task ghi trong body Issue, không có field riêng.

## Quy ước Issue

**User Story:** 1 User Story = 1 Issue. Tiêu đề `[US-XX] <tiêu đề ngắn tiếng Việt>`, nhãn `user-story` và nhãn MoSCoW (`must` / `should` / `could`). Body gồm User Story nguyên văn, mục Thông tin (US ID, Epic, Feature, Business Value, MoSCoW, Story Points, Dependency, Planned Sprint, Source RAW ID) và toàn bộ Acceptance Criteria (123 AC) copy nguyên văn từ workbook. Tiêu đề ngắn là phần duy nhất do Giai đoạn 8 đặt, workbook không có cột này.

**Task:** đúng Task ID trong workbook. Tiêu đề `[S1-T01] <mô tả task>`, nhãn `task`. Body gồm Task ID, Related User Story, Sprint, Assignee, Estimate, Dependency, Deliverable, Reviewer và mô tả.

| Loại task | Số task | Cách liên kết |
|---|---|---|
| Gắn đúng một story | 117 | Sub-issue của Issue story |
| Task xuyên suốt, không có US ID trong workbook | 24 | Issue độc lập, ghi rõ trong body |
| Task PO nghiệm thu nhiều story | 9 | Issue độc lập, body liệt kê các Issue story liên quan (một sub-issue chỉ có một cha) |

## Assignee và Reviewer

- Workbook ghi người phụ trách bằng tên (Châu Tuấn, Thanh Tuấn, Thành Nam, Đức Quang, Mạnh Trường, Tiến Thành). Tên người phụ trách nằm trong body Issue (dòng `Assignee:`). GitHub Assignee đã gán cho cả 150 task theo dòng `Assignee:`: Châu Tuấn (`Aliospbc2006`, 24), Thanh Tuấn (`GreentunaNTT`, 30), Thành Nam (`vothanhnamnn`, 22), Đức Quang (`BlueKevin66-code`, 24), Mạnh Trường (`truonglm16375`, 25), Tiến Thành (`thenggne`, 25).
- Story (41 Issue) không có người phụ trách riêng trong workbook nên Assignee để trống. Khi đổi người làm task, sửa cả dòng `Assignee:` trong body và Assignee của Issue.
- Reviewer ghi trong body Issue và field **Task Reviewer**. Người review khác người thực hiện.

## Dùng board hằng ngày

1. Mở Project, view Board, nhóm theo Status.
2. **Sprint Planning:** PO xác nhận story của sprint; chuyển story của sprint đó sang **Sprint Backlog**. Task của sprint ở **Todo**.
3. **Làm task:** người thực hiện lấy task ở **Todo** (cột Assignee trong body), làm theo Acceptance Criteria của story cha. Mỗi người nên làm tối đa 2 task cùng lúc.
4. **Xong phần việc:** chuyển task sang **Review**, ghi link PR hoặc tài liệu trong Issue và báo Task Reviewer.
5. **Review:** reviewer duyệt thì chuyển **Done**; chưa đạt thì chuyển về **Todo** kèm nhận xét cụ thể. Không chuyển thẳng Todo sang Done.
6. **Story Done:** PO chuyển story sang **Done** khi mọi task con đã Done và mọi Acceptance Criteria đạt. Không đưa story vào Done khi chưa nghiệm thu.
7. Việc mới phát sinh vào Product Backlog, không thêm vào sprint đang chạy.
8. Không đóng Issue khi công việc chưa hoàn thành. Cuối sprint, story chưa xong quay về Sprint Backlog của sprint sau hoặc Product Backlog, ghi lý do.

Chi tiết quy trình Scrum, Definition of Done và vai trò: `docs/02_Agile_Scrum_Plan.md`.

## Trạng thái thiết lập

| Việc | Trạng thái |
|---|---|
| Tạo GitHub Project, liên kết repository | Xong |
| 5 cột Status đúng thứ tự | Xong |
| Custom fields | Xong (Item Type, Task Reviewer thay cho Type, Reviewer) |
| Issue từ 41 User Story, thêm vào Project | Xong |
| Issue từ 150 task (55 + 46 + 49), thêm vào Project, 117 sub-issue | Xong |
| Gán GitHub Assignee | Xong: 150/150 task |
| Thay đổi sau review của thành viên | Đã merge vào `main` |
