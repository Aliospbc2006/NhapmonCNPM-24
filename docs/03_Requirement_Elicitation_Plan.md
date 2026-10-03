# 03 — Requirement Elicitation Plan: BlueMoon v1.0

| Mục | Giá trị |
|---|---|
| Phiên bản tài liệu | 0.1 (Phase 2 — bản nháp, chờ nhóm xác nhận) |
| Loại | Simulated Interview / Role-play for Requirement Elicitation |
| Liên quan | [01_Project_Overview.md](01_Project_Overview.md), [02_Agile_Scrum_Plan.md](02_Agile_Scrum_Plan.md), [04_Interview_Report.md](04_Interview_Report.md) |

> **Về phương pháp.** Nhóm **không** liên hệ được với Ban quản trị hay cư dân BlueMoon. Vì vậy các buổi "phỏng vấn" trong project là **role-play stakeholder interview**. Một thành viên đóng vai Analyst và tự viết câu trả lời của các stakeholder *giả lập*, dựa trên đề bài BlueMoon, tài liệu hướng dẫn Elicitation và hiểu biết về nghiệp vụ.
> - Mọi biên bản là **Simulated stakeholder input** (*yêu cầu giả lập từ bối cảnh bài toán*). Đó không phải kết quả làm việc với người thật.
> - Không có tên thật, chữ ký, ghi âm, ảnh chụp, số điện thoại, địa chỉ, ngày hay giờ họp thật.
> - Nếu đem dự án ra ngoài môn học, nội dung giả lập phải được **xác thực** (validate) với khách hàng thật (xem mục 7).

---

## 1. Mục tiêu khai phá yêu cầu

Các mục tiêu dưới đây lấy từ OBJ-01…OBJ-08 trong tài liệu hướng dẫn BTL, cho Phase 2:

| ID | Mục tiêu | Chỉ số đạt | Artefact đầu ra |
|---|---|---|---|
| EL-01 | Thu thập yêu cầu thô (RAW) cho BlueMoon v1.0, bao phủ 7 nhóm chức năng | 20–30 RAW (hướng dẫn gốc nêu ≥30; Phase này chọn 30 gồm cả NFR và roadmap) | `deliverables/04_Raw_Requirements.xlsx` |
| EL-02 | Xác định yêu cầu phi chức năng (bảo mật, phân quyền, sao lưu, hiệu năng, audit log…) | ≥5 NFR | Sheet `NFR` |
| EL-03 | Ghi nhận hiện trạng (As-Is) và pain point từ góc nhìn từng stakeholder | Mỗi stakeholder có phần As-Is và Pain Points | 4 biên bản trong `docs/interviews/` |
| EL-04 | Ghi nhận mong muốn thô (Client's Wish List), chưa lọc, chưa ưu tiên chính thức | 20–30 wish | Sheet `Client_Wish_List`, `04_Interview_Report.md` |
| EL-05 | Phát hiện xung đột, giả định và câu hỏi cần xác thực | Danh sách Open Questions và Conflicts | `04_Interview_Report.md` |
| EL-06 | Làm đầu vào cho các phase sau: As-Is → To-Be → Epic → Feature → User Story → AC | Mỗi RAW có Source, Evidence Reference, Target Artefact | `deliverables/04_Raw_Requirements.xlsx` |

Phạm vi nội dung là **BlueMoon v1.0**: đăng nhập/đổi mật khẩu, hộ gia đình, nhân khẩu, khoản thu, thu phí, tra cứu/tìm kiếm, thống kê. Phí gửi xe và điện/nước/internet (v2.0) chỉ ghi ở mức roadmap, *Won't-have cho v1.0*.

## 2. Các nhóm stakeholder giả lập

Mỗi stakeholder là một **vai trò**, không gắn với người cụ thể.

| Mã | Stakeholder giả lập | Vai trò trong bài toán | Quan hệ với hệ thống v1.0 | Biên bản |
|---|---|---|---|---|
| BQT | Đại diện Ban quản trị (cấp quyết định) | Khách hàng; quyết định phạm vi, ưu tiên | Người dùng (quản trị) | `01_Ban_Quan_Tri_Interview.md` |
| TQ | Thủ quỹ / người thu phí | Người dùng cuối thao tác thu phí hằng ngày | Người dùng trực tiếp | `02_Thu_Quy_Interview.md` |
| CD | Chủ hộ / cư dân | Bên đóng phí, đối tượng được quản lý thông tin | Không dùng phần mềm ở v1.0 (AS-02) | `03_Cu_Dan_Interview.md` |
| CQ | Đại diện cơ quan chức năng (chính quyền địa phương / tổ dân phố, vai trò chung) | Bên yêu cầu thông tin hộ, nhân khẩu; phối hợp thu quỹ đóng góp | Gián tiếp: nhận thông tin do Ban quản trị cung cấp | `04_Co_Quan_Chuc_Nang_Interview.md` |

## 3. Nguồn phi con người

| Mã | Nguồn | Mô tả | Cách dùng |
|---|---|---|---|
| PS-01 | Đề bài BlueMoon — "Giới thiệu bài toán" (`08. Bo Bai Tap.pdf`) | Bối cảnh, các khoản phí, phạm vi v1.0 và v2.0, luồng nghiệp vụ | Nguồn gốc (ground truth) của phạm vi |
| PS-02 | Bộ bài tập — ví dụ Project Charter ở Bài 4.1 (Chương 4, **ngoài phạm vi đối chiếu BTL**) | Mục đích, mục tiêu đo được, phạm vi sản phẩm, loại trừ nhập liệu | Chỉ tham khảo bối cảnh; các giả định rút ra từ đây là TEAM DECISION, không phải yêu cầu của giảng viên |
| GD-01 | `01_ Huong dan … (Elicitation).pdf` | Quy trình Elicitation, artefact, chỉ tiêu | Khung phương pháp |
| DA-01 | Mẫu sổ quản lý thu các khoản đóng góp (Hình 1-1 trong đề) | Minh họa thu chi thủ công | Tham chiếu để suy luận cột dữ liệu; nhóm chưa dùng nội dung chi tiết của hình để tạo yêu cầu |
| DA-02 | **Biểu mẫu Excel giả định** (do nhóm đặt ra, xem bên dưới) | Mô hình hóa file Excel hiện hành của Ban quản trị | Phân tích tài liệu giả lập, ghi rõ là giả định |
| WA-01 | **Quy trình As-Is thu phí hằng tháng** (giả định) | Luồng thủ công hiện hành | Workflow analysis |
| WA-02 | **Quy trình As-Is quản lý hộ/nhân khẩu và cung cấp thông tin** (giả định) | Luồng thủ công hiện hành | Workflow analysis |

### 3.1 Biểu mẫu Excel giả định (DA-02) — *Assumption*

Đề bài chỉ nói Ban quản trị "có sử dụng một số công cụ hỗ trợ như Excel". Nhóm giả định hiện trạng có các bảng sau để làm cơ sở phân tích. Đây không phải file thật của Ban quản trị:

| Bảng giả định | Cột chính (giả định) |
|---|---|
| Danh sách hộ | Số căn hộ, tên chủ hộ, diện tích (m²), số điện thoại liên hệ, ghi chú |
| Danh sách nhân khẩu | Họ tên, ngày sinh, giới tính, quan hệ với chủ hộ, số căn hộ, tình trạng (thường trú/tạm trú/tạm vắng) |
| Sổ thu phí theo tháng | Số căn hộ, khoản phí, số tiền phải nộp, số tiền đã nộp, ngày nộp, người thu, ghi chú |
| Sổ thu quỹ đóng góp | Đợt, số căn hộ, số tiền tự nguyện, ngày nộp |

### 3.2 Quy trình As-Is giả định

**WA-01 — Thu phí hằng tháng:**
1. Ban quản trị lập danh sách các khoản phí mỗi hộ phải đóng trong tháng (tính tay theo diện tích × đơn giá).
2. Gửi thông báo thu tiền (giấy hoặc tin nhắn) cho hộ.
3. Hộ đến nộp tại văn phòng Ban quản trị; thủ quỹ nhận tiền, ghi vào sổ/Excel và viết biên lai tay.
4. Cuối tháng đối chiếu sổ và Excel, tổng hợp số liệu báo cáo trưởng ban.

**WA-02 — Hộ khẩu, nhân khẩu:**
1. Cư dân báo thay đổi (người mới chuyển đến, tạm vắng, tạm trú, sinh, chuyển đi) cho Ban quản trị.
2. Ban quản trị cập nhật vào sổ hoặc Excel.
3. Khi cơ quan chức năng yêu cầu, Ban quản trị tập hợp thông tin bằng tay và gửi lại.

## 4. Kỹ thuật khai phá

| Kỹ thuật | Áp dụng | Stakeholder / nguồn | Đầu ra |
|---|---|---|---|
| **Semi-structured interview (role-play)** | 4 biên bản, mỗi biên bản 10–12 câu hỏi theo Interview Script (mục 6) | BQT, TQ, CD, CQ | Biên bản trong `docs/interviews/`, Wish List, RAW |
| **Document analysis** | Đọc đề bài, hướng dẫn Elicitation; phân tích biểu mẫu Excel giả định | PS-01, PS-02, GD-01, DA-01, DA-02 | Ràng buộc phạm vi, trường dữ liệu, loại khoản phí |
| **Workflow analysis** | Mô hình hóa quy trình As-Is và pain point | WA-01, WA-02 | Cơ sở cho As-Is và To-Be ở phase sau |

Hướng dẫn gốc còn có quan sát công việc, khảo sát cư dân và workshop với Ban quản trị. Nhóm **không làm** các kỹ thuật này vì không gặp được stakeholder. Phần thiếu này được ghi vào Open Questions và danh sách mục cần xác thực.

## 5. Mục tiêu thông tin cần thu từ từng stakeholder

| Stakeholder | Thông tin cần thu được |
|---|---|
| **BQT** | Mục tiêu tổng thể; các khoản thu và cách tính; ai được dùng hệ thống, phân quyền; báo cáo, thống kê cần xem; yêu cầu sao lưu, truy vết; ranh giới phạm vi và việc để dành cho phiên bản sau; ưu tiên |
| **TQ** | Quy trình thu hằng ngày; các tình huống ngoại lệ (nộp thiếu, nộp gộp, nhập sai); thao tác tìm hộ; nhu cầu biên lai; pain point khi tra công nợ; số người dùng đồng thời; ưu tiên |
| **CD** | Cách cư dân biết khoản phải đóng; khó khăn khi đóng và đối chiếu; nhu cầu chứng từ, minh bạch; cách khai báo thay đổi nhân khẩu; mối lo về dữ liệu cá nhân; mong muốn ngoài phạm vi v1.0 |
| **CQ** | Khi nào và vì sao cần thông tin hộ, nhân khẩu; trường dữ liệu và dạng báo cáo cần; vai trò trong thu quỹ đóng góp; yêu cầu về độ chính xác, thời điểm, bảo mật khi cung cấp |

## 6. Interview Script

Mỗi biên bản dùng cùng khung 8 phần. Câu hỏi cụ thể được điều chỉnh theo vai trò.

| # | Phần | Mục đích | Câu hỏi mẫu | Câu hỏi thăm dò (probe) |
|---|---|---|---|---|
| 1 | **Introduction** | Làm rõ phạm vi, tạo ngữ cảnh | "Anh/chị giữ vai trò gì trong việc quản lý hoặc đóng phí ở chung cư?" | "Việc nào chiếm nhiều thời gian nhất?" |
| 2 | **Current process / As-Is** | Nắm quy trình hiện tại | "Hiện nay việc thu phí/cập nhật nhân khẩu được thực hiện thế nào, từ đầu đến cuối?" | "Công cụ nào đang dùng? Ai làm bước nào?" |
| 3 | **Pain Points** | Xác định vấn đề | "Điều gì gây khó khăn hoặc dễ sai sót nhất?" | "Lần gần nhất gặp vấn đề đó là khi nào, xử lý ra sao?" |
| 4 | **Wishlist** | Thu mong muốn thô | "Nếu có phần mềm hỗ trợ, anh/chị muốn nó làm được gì?" | "Việc đó thường xảy ra bao nhiêu lần?" |
| 5 | **Vision / To-Be** | Hình dung tương lai | "Một buổi thu phí lý tưởng sẽ diễn ra thế nào?" | "Điều gì sẽ thay đổi so với hiện nay?" |
| 6 | **NFR / Constraints** | Bảo mật, phân quyền, hiệu năng, sao lưu | "Ai được xem và sửa dữ liệu? Anh/chị lo ngại điều gì về dữ liệu?" | "Nếu mất dữ liệu thì hậu quả thế nào?" |
| 7 | **Priority** | Xếp ưu tiên | "Trong những việc vừa nêu, việc nào bắt buộc phải có ngay từ đầu?" | "Việc nào có thể để sau?" |
| 8 | **Closing** | Bắt ẩn ý và kết thúc | "Có điều gì quan trọng mà chúng tôi chưa hỏi không?" | "Chúng tôi tóm tắt lại để xác nhận…" |

Quy tắc viết biên bản role-play:
- Câu trả lời viết tự nhiên. Không cần hoàn hảo, có thể lẫn mong muốn, pain point, ưu tiên và vài chỗ hơi lệch ý giữa các stakeholder.
- Bám sát đề bài. Chỗ nào vượt ngoài đề bài thì đánh dấu *Assumption* trong Analyst note.
- Không tự bịa số liệu, quy định pháp luật hay biểu mẫu mà đề bài không nói. Những điểm đó ghi thành Open Question để xác thực sau.
- Mỗi câu hỏi có mã `SIM-INT-<mã stakeholder>-Qnn`, dùng làm Evidence Reference.

## 7. Bao phủ phạm vi và giới hạn

| Nhóm chức năng v1.0 | Interview chính |
|---|---|
| Đăng nhập / đổi mật khẩu | BQT (Q08), CD (Q07) |
| Hộ gia đình | BQT (Q04), CD (Q06), CQ (Q02, Q05) |
| Nhân khẩu | BQT (Q04), CD (Q06), CQ (Q04, Q06) |
| Khoản thu | BQT (Q06), CD (Q05), TQ (Q10) |
| Thu phí | TQ (Q02, Q04–Q07), CD (Q04) |
| Tra cứu / tìm kiếm | TQ (Q08, Q09), CQ (Q05) |
| Thống kê | BQT (Q07), TQ (Q09), CQ (Q07, Q11) |
| Roadmap v2.0 (Won't-have v1.0) | BQT (Q11), CD (Q10) |

Giới hạn:
- Yêu cầu rút ra từ role-play phải được xác thực với khách hàng thật trước khi dùng ngoài môn học.
- Các biên bản chỉ là cơ sở phân tích cho BTL, không phải bằng chứng khảo sát.
