BẢN GHI CHÚ HỌC TẬP CHI TIẾT: BUỔI 02 - HỆ THỐNG QUẢN TRỊ QUY TRÌNH NGHIỆP VỤ (BPM)

1. Tổng quan và Chữa bài tập về nhà

Việc xác định đúng Actor và loại hình quy trình không chỉ giúp mô hình hóa chính xác mà còn là cơ sở để phát hiện các "điểm nghẽn" (bottlenecks) và sự dư thừa (redundancies) trong hệ thống.

1.1. Phân tích Bài tập 1: Quy trình mua hàng (Procurement Process)

Quy trình này điều phối dòng chảy vật tư để đảm bảo tính liên tục của sản xuất/kinh doanh.

* Hệ thống Actor và Đối tượng:
  1. Phòng mua hàng (Purchasing Dept): Điều phối giao dịch và tìm kiếm nguồn cung.
  2. Bộ phận kho (Warehouse): Lưu trữ và kích hoạt nhu cầu khi tồn kho đạt điểm đặt hàng.
  3. Kế toán thanh toán (Accounts Payable): Xử lý hóa đơn và dòng tiền.
  4. Người bán hàng (Supplier): Cung cấp hàng hóa/dịch vụ.
  5. Cơ sở dữ liệu mua hàng: Đây là Đối tượng thông tin (Information Object) lưu trữ hồ sơ số hóa, phân biệt với các Đối tượng vật lý (Physical Objects) như hàng hóa hay thiết bị.
* Giá trị chiến lược và Business Intelligence (BI): Hệ thống BI đóng vai trò trọng yếu trong việc dự báo (forecasting) thời điểm hết hàng và biến động giá cả để tối ưu hóa quy trình mua hàng.
* Xác định Customer: Trong quy trình nội bộ này, Bộ phận mua hàng (hoặc đơn vị yêu cầu) là khách hàng vì họ nhận giá trị trực tiếp và kích hoạt quy trình để đáp ứng nhu cầu sản xuất.
* Các yếu tố giá trị (Value Dimensions):
  * Thời gian (Time): Tránh chậm trễ (Delay), đảm bảo tính chính xác về thời điểm giao hàng.
  * Chất lượng (Quality): Đúng chủng loại, thông số kỹ thuật (ví dụ: loại sợi, mật độ vải).
  * Chi phí (Cost): Tối ưu hóa giá mua, chi phí vận chuyển và chi phí lưu kho.
* Phân loại Output:

Loại kết quả	Trạng thái cụ thể	Lý do/Điều kiện
Positive Outcome	Nhập kho thành công, thanh toán hoàn tất.	Đúng hạn, đúng số lượng, đúng chủng loại và giá cả.
Negative Outcome	Đơn hàng bị hủy hoặc hàng bị trả về.	Giao hàng trễ, sai mã sản phẩm (model), hoặc sai lệch dữ liệu thanh toán.

1.2. Phân tích Bài tập 2: Tình huống công ty xây dựng POT (Mượn thiết bị)

* Phân loại quy trình: Thuộc nhóm Procure-to-Pay (Mua/Mượn để chi trả). Quy trình bắt đầu từ khi phát sinh nhu cầu và kết thúc khi hoàn tất nghĩa vụ thanh toán và trả thiết bị.
* Phân nhiệm Actor và Task cụ thể:
  * Kỹ sư công trình (Site Engineer): Yêu cầu [Thiết bị] (Requesting equipment).
  * Thư ký (Clerk): Lựa chọn [Thiết bị phù hợp] (Selecting equipment) và Kiểm tra [Tính sẵn có] (Checking availability).
  * Kỹ sư văn phòng (Office Engineer): Xem xét [Yêu cầu] (Reviewing request) và Phê duyệt [Đơn mượn] (Approving request).
  * Nhà cung cấp (Supplier): Giao [Thiết bị] (Delivering equipment).
* Đánh giá hiệu suất: Khách hàng (Kỹ sư công trình) đo lường dựa trên tiêu chí: Đúng thiết bị và Đúng thời điểm (tránh lãng phí thời gian chờ đợi tại công trường).

2. Phân loại lớp quy trình nghiệp vụ (Process Classification)

Kiến trúc quy trình 3 lớp giúp doanh nghiệp phân bổ nguồn lực dựa trên mức độ đóng góp giá trị.

2.1. Kiến trúc quy trình 3 lớp

Lớp quy trình	Định nghĩa & Mục đích	Ví dụ (Trường Đại học)
Quản lý (Management)	Thiết lập định hướng, chiến lược và các luật lệ vận hành.	Quản lý tầm nhìn, Quản lý chiến lược phát triển.
Cốt lõi (Core)	Giá trị gia tăng trực tiếp (Value-added): Là lý do khách hàng trả tiền cho tổ chức.	Giảng dạy, Nghiên cứu khoa học, Tư vấn tuyển sinh.
Hỗ trợ (Support)	Chi phí vận hành nội bộ (Internal overhead): Cung cấp tài nguyên cho các lớp khác.	Quản trị IT, Quản trị nhân sự, Quản lý tài sản.

Tư duy hệ thống: Lớp Quản lý định hướng hướng đi; lớp Cốt lõi tạo ra lợi nhuận/giá trị; lớp Hỗ trợ đảm bảo sự ổn định của nền tảng vận hành.

3. Khái niệm và Vai trò của Mô hình hóa quy trình

Mô hình hóa là sự trừu tượng hóa hiện thực, giúp chuyển đổi những diễn giải bằng lời mơ hồ thành các cấu trúc trực quan chuẩn hóa.

1. Hoạt động (Activity/Task): Đơn vị công việc thực thi, tiêu tốn thời gian và tài nguyên, làm thay đổi trạng thái của quy trình.
  * Cú pháp: [Động từ] + [Danh từ] (Ví dụ: Kiểm tra [Hóa đơn]).
2. Sự kiện (Event): Trạng thái xảy ra tức thời, không tiêu tốn thời gian, dùng để kích hoạt hoặc kết thúc một luồng công việc.
  * Cú pháp: [Danh từ] + [Quá khứ phân từ] (Ví dụ: Thiết bị [Đã nhận]).
3. Đối tượng (Objects):
  * Vật lý: Hàng hóa, thiết bị máy móc.
  * Thông tin (Data Object): Dữ liệu số, hồ sơ điện tử, tài liệu ERP.
4. Tài nguyên (Resource): Con người (nhân viên, vị trí) hoặc hệ thống (phần mềm CRM, SAP).

4. Vòng đời quản lý quy trình nghiệp vụ (BPM Lifecycle)

BPM là một chu trình cải tiến liên tục nhằm đạt tới trạng thái vận hành tối ưu.

Giai đoạn	Nội dung thực hiện	Bên liên quan chính
Xác định (Identification)	Lập bản đồ kiến trúc quy trình toàn tổ chức.	Process Owner
Mô hình hóa (Discovery)	Thu thập thông tin và vẽ lại quy trình thực tế.	Chuyên gia quy trình
Phân tích (Analysis)	Tìm ra lỗi, điểm nghẽn bằng Pareto, Xương cá.	Đội ngũ phân tích
Thiết kế lại (Redesign)	Xây dựng mô hình TO-BE (cải tiến).	Chuyên gia & Quản lý
Hiện thực hóa (Implementation)	Triển khai trên phần mềm hoặc thay đổi vận hành.	Đội ngũ IT & Vận hành
Giám sát (Monitoring)	Đo lường hiệu quả dựa trên KPI thực tế.	Quản trị viên hệ thống

Lưu ý về Simulation: Trước khi triển khai TO-BE, doanh nghiệp thường thực hiện mô phỏng (Simulation) trên phần mềm để dự báo hiệu suất và rủi ro, tránh gây gián đoạn vận hành thực tế.

5. Kỹ thuật và Góc nhìn trong Mô hình hóa

5.1. Các góc nhìn quy trình (Perspectives)

* Luồng điều khiển (Control Flow): Trình tự thực hiện (Tuần tự, Song song).
* Dữ liệu (Data): Nguồn đầu vào và đầu ra của dữ liệu.
* Nguồn lực (Resource): Phân nhiệm "Ai làm việc gì".

5.2. So sánh các kỹ thuật mô hình hóa

Kỹ thuật	Ưu điểm	Nhược điểm & Lý do (Suy luận)
BPMN 2.0	Tiêu chuẩn quốc tế, hỗ trợ tốt cho cả nghiệp vụ và kỹ thuật.	Đòi hỏi thời gian đào tạo cao do hệ thống ký hiệu phức tạp.
Flowchart	Đơn giản, dễ tiếp cận cho mọi đối tượng.	Suy luận: Không thể hiện được các tác vụ song song và phân vùng trách nhiệm phức tạp.
UML	Rất mạnh trong thiết kế hệ thống phần mềm.	Suy luận: Quá thiên về kỹ thuật (IT-centric), khó hiểu với nhân sự nghiệp vụ thuần túy.
DFD	Làm rõ luồng di chuyển của dữ liệu số.	Suy luận: Thiếu sự hiện diện của con người và yếu tố thời gian/trình tự sự kiện.
Sơ đồ Vai trò	Minh bạch trách nhiệm của từng Actor.	Suy luận: Dễ gây rối mắt (matrix overload) khi số lượng Actor và Task tăng lên.

6. Tổng kết thông tin hành chính và Nhắc nhở

* Tương tác: Tiếp tục đánh số trên chat Teams để ghi nhận sự hiện diện tích cực.
* Bài tập về nhà: Mô tả quy trình doanh nghiệp đã chọn (Xác định Actors, Customers, Outcomes và danh sách Tasks).
* Dự án cuối kỳ: Còn 05 tuần. Sinh viên cần chuẩn bị nội dung để sẵn sàng báo cáo sau khi kết thúc deadline nộp bài.
* Đọc trước: Tìm hiểu các ký hiệu BPMN 2.0 cơ bản (Pool, Lane, Gateway, Event) cho buổi thực hành vẽ sơ đồ.

7. Phụ lục học tập chuyên sâu

7.1. Thuật ngữ mới (Glossary)

1. Positive Outcome: Kết quả thành công (đạt được mục tiêu quy trình).
2. Negative Outcome: Kết quả thất bại (lỗi, hủy đơn, không đạt giá trị).
3. AS-IS: Mô hình trạng thái hiện tại (để phân tích vấn đề).
4. TO-BE: Mô hình trạng thái tương lai (sau khi đã cải tiến).
5. BPMN: Business Process Model and Notation.
6. Information Object: Đối tượng dữ liệu (hồ sơ, bản ghi số).
7. Bottleneck: Điểm nghẽn (nơi quy trình bị chậm lại).
8. Redundancy: Sự dư thừa (các bước không tạo giá trị).
9. Simulation: Mô phỏng quy trình trên máy tính.
10. Procurement: Quy trình mua sắm/mua hàng.

7.2. Gaps - Kiến thức bổ trợ

* Biểu đồ Pareto: Nguyên lý 80/20 dùng để xác định 20% nguyên nhân gây ra 80% lỗi trong quy trình.
* Mô hình Xương cá (Ishikawa): Công cụ phân tích nguyên nhân - kết quả để tìm ra gốc rễ của vấn đề vận hành.

7.3. Checklist sau buổi học

* [ ] Phân loại được các phòng ban trong dự án nhóm vào 3 lớp: Quản lý, Cốt lõi, Hỗ trợ.
* [ ] Viết danh sách ít nhất 5 Task theo đúng cú pháp [Động từ] + [Danh từ].
* [ ] Xác định được quy trình của nhóm là Order-to-Cash hay Procure-to-Pay.

7.4. Câu hỏi tự ôn tập

1. Tại sao trong quy trình mua hàng nội bộ, Phòng mua hàng lại được coi là Khách hàng?
2. Phân biệt sự khác nhau về tính chất thời gian giữa Activity và Event.
3. Business Intelligence (BI) hỗ trợ gì cho giai đoạn lập kế hoạch mua hàng?
4. Tại sao Flowchart truyền thống thường không đủ để mô tả quy trình doanh nghiệp hiện đại?
5. Vai trò của mô hình AS-IS trong vòng đời BPM là gì?
6. Khi nào một quy trình được coi là rơi vào trạng thái Negative Outcome?
7. Giải thích nguyên lý 80/20 của biểu đồ Pareto trong phân tích lỗi quy trình.
8. Mô hình Xương cá giúp ích gì cho chuyên gia quy trình trong giai đoạn "Analysis"?
9. Tại sao cần thực hiện Simulation trước khi triển khai mô hình TO-BE?
10. Phân biệt Đối tượng vật lý và Đối tượng thông tin bằng ví dụ thực tế tại một kho hàng.
