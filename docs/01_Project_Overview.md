# 01 — Project Overview: Phần mềm quản lý và thu phí chung cư BlueMoon

| Mục | Giá trị |
|---|---|
| Phiên bản tài liệu | 0.1 (Phase 1 — bản nháp, chờ nhóm xác nhận) |
| Cập nhật | 2026-10-03 |
| Nhóm thực hiện | Nhóm 24 — Châu Tuấn, Thanh Tuấn, Thành Nam, Đức Quang, Mạnh Trường, Tiến Thành |
| Đơn vị thực hiện | Nhóm 24, bài tập lớn môn Nhập môn Công nghệ phần mềm (IT4080) |
| Nhà tài trợ | Chưa xác định theo phần giới thiệu bài toán (đề bài chỉ nêu Ban quản trị có nhu cầu xây dựng phần mềm). Ví dụ Charter ở Chương 4 nêu Công ty ABC, chỉ để tham khảo. Với BTL: TEAM DECISION |
| Nguồn chính | `08. Bo Bai Tap.pdf` (phần "Giới thiệu bài toán", trang 6–8, đứng trước Chương 2; Chương 2–3 cho quy trình), `01_ Huong dan lap ke hoach phat hieu yeu cau BTL (Elicitation).pdf` |

> **Về nguồn dữ liệu.** Nhóm **chưa** phỏng vấn, khảo sát hay quan sát thực tế Ban quản trị, cư dân hoặc bên liên quan nào. Nội dung về stakeholder, nhu cầu và pain point trong tài liệu này có hai nguồn:
> - **[Đề bài]**: trích hoặc diễn giải lại từ đề bài BlueMoon.
> - **[Giả lập]**: *Simulated stakeholder input* (*yêu cầu giả lập từ bối cảnh bài toán*), nhóm suy ra từ nghiệp vụ. Đây không phải kết quả làm việc với người thật.
>
> Tên các nhân vật (ông Nguyễn Văn C, bà Phạm Thị A, ông Lê Văn B) lấy từ ví dụ Project Charter ở Bài 4.1 (Chương 4) của bộ bài tập. Nhóm chưa gặp ai trong số này. BTL chỉ đối chiếu phần giới thiệu bài toán, Chương 2 và Chương 3, nên các chi tiết lấy từ ví dụ Charter chỉ là bối cảnh tham khảo, nhóm tạm giả định (TEAM DECISION). Đó không phải yêu cầu của giảng viên.

---

## 1. Tên dự án

**Xây dựng phần mềm quản lý và thu phí ở chung cư BlueMoon** (gọi tắt: *BlueMoon*).

- Phiên bản đang thực hiện: **BlueMoon v1.0**.
- Phiên bản định hướng: **BlueMoon v2.0** (chỉ là roadmap, xem mục 8).

## 2. Bối cảnh

[Đề bài] Chung cư BlueMoon tọa lạc tại ngã tư Văn Phú, khởi công năm 2021 và hoàn thành năm 2023. Chung cư xây trên diện tích 450 m², gồm 30 tầng: tầng 1 làm kiot, 4 tầng đế, 24 tầng nhà ở và 1 tầng penthouse.

[Đề bài] Chủ sở hữu hoặc hộ gia đình phải đóng một khoản kinh phí định kỳ để vận hành và bảo dưỡng cơ sở vật chất. Việc quản lý và thu phí do **Ban quản trị chung cư** (do cư dân bầu ra) thực hiện. Hằng tháng Ban quản trị lập danh sách các khoản phí cần đóng của từng hộ và gửi thông báo thu tiền.

Các loại khoản thu thuộc phạm vi v1.0 [Đề bài]:

| Khoản thu | Tính chất | Cách tính / thu |
|---|---|---|
| Phí dịch vụ chung cư | Bắt buộc, theo tháng | Theo diện tích căn hộ, hiện dao động 2.500–16.500 đồng/m²/tháng |
| Phí quản lý chung cư | Bắt buộc, theo tháng | Từ 7.000 đồng/m² (theo tiêu chuẩn dự án) |
| Khoản đóng góp (quỹ vì người nghèo, quỹ biển đảo, quỹ từ thiện, …) | Không bắt buộc, tự nguyện | Thu theo từng đợt, phối hợp với chính quyền địa phương và tổ dân phố |

## 3. Vấn đề hiện tại

**[Đề bài]** Ban quản trị quản lý thu phí theo phương thức thủ công, có dùng Excel và sổ thu chi giấy, nhưng "hiệu quả quản lý chưa cao". Thông tin hộ khẩu, nhân khẩu cũng cần được quản lý để cung cấp cho cơ quan chức năng khi được yêu cầu.

**[Giả lập]** Các pain point sau là suy luận hợp lý để phục vụ bước Requirement Elicitation. Chúng chưa được kiểm chứng với người dùng thật:

| # | Vấn đề (giả lập) | Hệ quả |
|---|---|---|
| 1 | Dữ liệu thu phí nằm rải rác trong Excel và sổ giấy | Khó biết hộ nào đã nộp, hộ nào còn nợ |
| 2 | Phí tính tay theo diện tích × đơn giá | Dễ sai sót, khó đối chiếu |
| 3 | Khó tra cứu, tìm kiếm theo hộ, căn hộ, khoản thu | Mất thời gian khi cư dân hỏi hoặc khi cần đối soát |
| 4 | Thống kê tình hình thu phí làm thủ công | Chậm, thiếu cái nhìn tổng thể về các khoản thu |
| 5 | Thông tin hộ gia đình và nhân khẩu không tập trung, thiếu lịch sử biến động (tạm vắng, tạm trú, …) | Khó cung cấp thông tin chính xác cho cơ quan chức năng |
| 6 | Không có kiểm soát truy cập đối với dữ liệu | Rủi ro lộ hoặc sửa nhầm dữ liệu cá nhân và dữ liệu tài chính |

## 4. Mục tiêu hệ thống

Mục tiêu chính, lấy theo ví dụ Charter ở Bài 4.1 (Chương 4) [Ví dụ tham khảo]:
- Quản lý được **100% các loại phí cần thu** trong phạm vi v1.0.
- Quản lý được **100% thông tin hộ gia đình** sống tại chung cư, cùng các **biến động nhân khẩu** của từng căn hộ.

Mục tiêu cụ thể cho v1.0 [Giả lập, suy ra từ đề bài]:
- Thay ghi chép thủ công bằng một ứng dụng có dữ liệu tập trung.
- Làm đúng luồng nghiệp vụ: **Tạo khoản thu → Thu phí → Thống kê các khoản đóng góp**.
- Tìm nhanh thông tin hộ, nhân khẩu, khoản thu và tình trạng nộp.
- Chỉ người đã đăng nhập mới xem được dữ liệu.

## 5. Đối tượng sử dụng

| Nhóm | Vai trò trong hệ thống v1.0 |
|---|---|
| **Ban quản trị chung cư** (gồm trưởng ban, kế toán, người thu phí) | **Người dùng duy nhất** của hệ thống v1.0. Đăng nhập bằng tài khoản được cấp, quản lý hộ, nhân khẩu, khoản thu, ghi nhận thu phí, tra cứu và xem thống kê. |

Lưu ý:
- Cư dân/hộ gia đình **không** dùng phần mềm ở v1.0. Đề bài mô tả ứng dụng desktop dành cho Ban quản trị. Cư dân chỉ là stakeholder (xem AS-02).
- Việc chia nhỏ quyền trong Ban quản trị (trưởng ban, kế toán, thu ngân) chưa được đề bài quy định. Xem AS-04 và Câu hỏi mở Q3.

## 6. Stakeholder

| Stakeholder | Vai trò | Mối quan tâm chính | Mức tương tác với hệ thống | Nguồn |
|---|---|---|---|---|
| Ban quản trị chung cư | Khách hàng, người dùng chính | Thu đủ, đúng phí; nắm rõ tình hình thu; quản lý hộ và nhân khẩu | Trực tiếp (người dùng) | [Đề bài] |
| Trưởng ban quản trị (ông Nguyễn Văn C, theo ví dụ Charter Bài 4.1, Chương 4) | Đại diện khách hàng | Phạm vi, ưu tiên, nghiệm thu | Gián tiếp / ra quyết định | [Ví dụ tham khảo] |
| Kế toán ban quản trị (bà Phạm Thị A, theo ví dụ Charter Bài 4.1, Chương 4) | Đại diện người dùng cuối | Ghi nhận thu phí, đối chiếu, thống kê | Trực tiếp | [Ví dụ tham khảo] |
| Hộ gia đình / cư dân / chủ sở hữu | Bên đóng phí; đối tượng được quản lý thông tin | Minh bạch khoản phải nộp; thông tin cá nhân được bảo vệ | Không dùng phần mềm ở v1.0 | [Đề bài] |
| Cơ quan chức năng, tổ dân phố, chính quyền địa phương | Bên yêu cầu thông tin; phối hợp thu các khoản đóng góp | Nhận thông tin hộ và nhân khẩu chính xác khi yêu cầu | Gián tiếp (nhận thông tin từ Ban quản trị) | [Đề bài] |
| Công ty ABC (nhà tài trợ; ông Lê Văn B, nhân viên kinh doanh — theo ví dụ Charter Bài 4.1, Chương 4) | Nhà tài trợ / bộ phận kinh doanh | Phạm vi, ngân sách, tiến độ | Gián tiếp | [Ví dụ tham khảo] |
| Nhà cung cấp dịch vụ điện, nước, internet | Nguồn thông báo phí thu hộ | — | **Chỉ liên quan v2.0** | [Đề bài] |
| Nhóm phát triển (Nhóm 24) | Thực hiện dự án | Giao đúng phạm vi, đúng chất lượng | Xây dựng hệ thống | — |
| Giảng viên | Hướng dẫn và đánh giá BTL | Tuân thủ quy trình Elicitation và Agile/Scrum | Gián tiếp | — |

> Mọi "mong muốn" gán cho các stakeholder trong các tài liệu sau là **Simulated stakeholder input**.

## 7. Phạm vi v1.0

v1.0 có 7 nhóm chức năng, ở đây chỉ mô tả ở mức nhóm. Epic, Feature và User Story nằm trong `deliverables/05_Epic_UserStory.xlsx`. Product Backlog và Sprint Plan nằm trong `deliverables/06_Product_Backlog_Sprint_Plan.xlsx`. (Đăng nhập và đổi mật khẩu gộp chung một nhóm nên 8 hạng mục thành 7 nhóm.)

| # | Nhóm chức năng | Mô tả phạm vi | Module theo đề bài |
|---|---|---|---|
| 1 | Đăng nhập / đổi mật khẩu | Đăng nhập bằng tài khoản được cấp; đổi mật khẩu; chỉ truy cập các chức năng sau khi đăng nhập thành công; quản lý thông tin cá nhân cơ bản của người dùng | Quản lý người dùng |
| 2 | Quản lý hộ gia đình | Quản lý thông tin hộ gia đình (hộ khẩu), thông tin căn hộ (gồm diện tích dùng để tính phí), chủ hộ | Quản lý hộ gia đình |
| 3 | Quản lý nhân khẩu | Quản lý nhân khẩu trong từng hộ và các biến động: thay đổi nhân khẩu, tạm vắng, tạm trú | Quản lý hộ gia đình |
| 4 | Quản lý khoản thu | Tạo và quản lý các khoản thu v1.0: phí dịch vụ, phí quản lý, khoản đóng góp tự nguyện | Quản lý thu phí |
| 5 | Thu phí (ghi nhận thu phí) | Lập danh sách phải thu theo hộ và ghi nhận việc nộp phí của từng hộ | Quản lý thu phí |
| 6 | Tra cứu / tìm kiếm | Tìm kiếm thông tin hộ, nhân khẩu, khoản thu và tình trạng nộp | Xuyên suốt các module |
| 7 | Thống kê cơ bản | Thống kê tình hình các khoản thu và các khoản đóng góp (đã thu, chưa thu, theo khoản, theo hộ) | Quản lý thu phí |

Luồng nghiệp vụ chính của v1.0 [Đề bài]: *Tạo khoản thu → Thu phí → Thống kê các khoản đóng góp*, thực hiện sau khi đăng nhập.

Nền tảng dự kiến [Đề bài]: ứng dụng desktop Java, dữ liệu lưu tập trung trên MySQL server. Việc chạy trên Windows là giả định của nhóm (tham khảo ví dụ Charter Bài 4.1).

## 8. Out-of-scope / Roadmap v2.0

### 8.1 Roadmap v2.0 — chỉ mô tả định hướng, **không triển khai ở v1.0**

| Hạng mục v2.0 | Mô tả theo đề bài |
|---|---|
| Phí gửi xe | Thu hằng tháng theo thông tin phương tiện đăng ký của hộ gia đình. Xe máy 70.000 đồng/xe/tháng; ô tô ghi trong đề là "1.200.000 nghìn đồng/xe/tháng" (có vẻ là lỗi đánh máy, cần xác nhận lại trước khi dùng) |
| Điện | Khoản thu hộ hằng tháng theo thông báo của công ty cung cấp dịch vụ |
| Nước | Khoản thu hộ hằng tháng theo thông báo của công ty cung cấp dịch vụ |
| Internet | Khoản thu hộ hằng tháng theo thông báo của công ty cung cấp dịch vụ |

Bốn hạng mục này không có màn hình, bảng dữ liệu, User Story hay task sprint nào trong v1.0. Chúng chỉ xuất hiện ở Visionary Scenario và roadmap trong các tài liệu sau.

### 8.2 Các hạng mục khác ngoài phạm vi v1.0 (đề xuất, chờ nhóm xác nhận)

- Cổng thông tin hoặc ứng dụng cho cư dân tự xem phí, lịch sử đóng phí (xem AS-02).
- Tự đăng ký tài khoản (xem AS-03).
- Thanh toán trực tuyến, tích hợp ngân hàng/ví điện tử.
- Ứng dụng di động hoặc web.
- Gửi thông báo tự động qua SMS, email (xem AS-07).
- Tích hợp trực tiếp với hệ thống của cơ quan chức năng.
- Nhập dữ liệu ban đầu (hộ khẩu, nhân khẩu, các loại phí): nhóm tạm giả định theo ví dụ Charter Bài 4.1 (Chương 4), vì ví dụ này loại việc nhập liệu khỏi phạm vi dự án.

## 9. Các giả định

| ID | Giả định | Căn cứ |
|---|---|---|
| AS-01 | Mọi stakeholder input, Client Wish List, RAW requirement và User Story là **giả lập** dựa trên đề bài. Nhóm không có biên bản phỏng vấn hay khảo sát thật. | Quy định của nhóm |
| AS-02 | Ở v1.0, người dùng hệ thống chỉ là Ban quản trị. Cư dân/hộ gia đình là stakeholder, không đăng nhập. Các nhu cầu dành cho cư dân tự phục vụ thuộc ngoài v1.0. | Đề bài mô tả ứng dụng desktop cho Ban quản trị; chức năng "chỉ truy cập được sau khi Ban quản trị đăng nhập" |
| AS-03 | Tài khoản Ban quản trị được cấp sẵn. v1.0 chỉ gồm đăng nhập và đổi mật khẩu, không có chức năng tự đăng ký. Tài khoản được Quản trị hệ thống tạo trong phần mềm (US-41); tài khoản quản trị đầu tiên được nạp sẵn khi cài đặt (giả định). | Đề bài nêu "tài khoản đã cung cấp"; luồng nghiệp vụ có bước "Đăng kí tài khoản" nên cần nhóm xác nhận (Q1) |
| AS-04 | Ban đầu coi Ban quản trị là một nhóm người dùng. Việc phân quyền chi tiết (trưởng ban, kế toán, thu ngân) xác định ở bước yêu cầu phi chức năng. | Đề bài chưa quy định |
| AS-05 | Phí dịch vụ và phí quản lý được tính theo diện tích căn hộ × đơn giá do Ban quản trị thiết lập. Hệ thống không cố định mức giá. | Đề bài chỉ nêu khoảng giá |
| AS-06 | Khoản đóng góp tự nguyện thu theo đợt và số tiền do hộ tự nguyện; hệ thống chỉ ghi nhận, không ép buộc. | Đề bài |
| AS-07 | v1.0 hỗ trợ lập danh sách khoản phải thu theo hộ; việc gửi thông báo thu tiền (in, giao tận nơi, …) Ban quản trị thực hiện ngoài hệ thống. | Giả lập, cần xác nhận (Q2) |
| AS-08 | Dữ liệu đầu vào (hộ, nhân khẩu, loại phí) do Ban quản trị nhập; nhóm không nhập liệu hộ. | Giả định của nhóm; tham khảo ví dụ Charter Bài 4.1 (Chương 4) |
| AS-09 | Hệ thống phục vụ một chung cư (BlueMoon), một đơn vị tiền tệ (VND). | Đề bài |
| AS-10 | Dữ liệu nhân khẩu là dữ liệu cá nhân nhạy cảm. Khi demo, kiểm thử hay đưa lên GitHub chỉ dùng dữ liệu mẫu giả, không dùng dữ liệu thật. | Suy luận hợp lý |

## 10. Các ràng buộc

| Loại | Ràng buộc | Nguồn |
|---|---|---|
| Phạm vi | v1.0 gồm đúng 7 nhóm chức năng ở mục 7; không đưa phí gửi xe, điện, nước, internet vào v1.0 | Đề bài, quy định của nhóm |
| Công nghệ | Ứng dụng desktop Java, dữ liệu tập trung trên MySQL server | Đề bài ("dự kiến") |
| Môi trường | Bộ cài chạy trên máy tính cá nhân dùng Windows | Giả định của nhóm; tham khảo ví dụ Charter Bài 4.1 (Chương 4) |
| Truy cập | Chức năng quản lý chỉ truy cập được sau khi đăng nhập thành công | Đề bài |
| Quy trình | Áp dụng Agile/Scrum; truy vết RAW → Epic → Feature → User Story → Acceptance Criteria | Hướng dẫn BTL |
| Tài liệu | Các nội dung stakeholder phải ghi rõ là giả lập; không tạo bằng chứng giả (biên bản, chữ ký, ngày phỏng vấn, ghi âm, ảnh khảo sát) | Quy định của nhóm |
| Giai đoạn hiện tại | Chỉ làm tài liệu BTL (Elicitation, Agile/Scrum theo Chương 2–3); chưa viết code ứng dụng | Quy định của nhóm |
| Ngân sách, lịch tham khảo | Ví dụ Charter của đề: ngân sách 100.000.000 đồng, thực hiện trong Q4/2023, không quá 4 tháng. Đây là ví dụ minh họa, **chưa** phải ràng buộc chính thức của nhóm | Ví dụ Charter Bài 4.1 (Chương 4), chỉ tham khảo |

## Câu hỏi mở (liên quan Phase 1)

| ID | Câu hỏi | Ảnh hưởng |
|---|---|---|
| Q1 | v1.0 có cần "Đăng kí tài khoản" không, hay chỉ tài khoản cấp sẵn (AS-03)? | Phạm vi nhóm chức năng 1 |
| Q2 | v1.0 chỉ lập danh sách phải thu hay có in/xuất thông báo thu tiền (AS-07)? | Phạm vi nhóm chức năng 5 |
| Q3 | Ban quản trị có phân quyền nhiều vai trò khác nhau không (AS-04)? | NFR phân quyền |

Các câu hỏi về phân vai Scrum, độ dài sprint, kênh liên lạc nằm trong `02_Agile_Scrum_Plan.md`.
