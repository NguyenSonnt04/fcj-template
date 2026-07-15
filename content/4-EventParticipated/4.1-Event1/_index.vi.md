---
title: "Event 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Bài thu hoạch Event 1 – AI, AWS Cloud và hệ thống Multi-Agent

### Mục Đích Của Sự Kiện

- Chia sẻ cách cung cấp context phù hợp để AI tạo ra kết quả chính xác và hữu ích hơn.
- Giới thiệu các công cụ AI hỗ trợ khám phá dữ liệu, xây dựng workflow và trực quan hóa thông tin bằng ngôn ngữ tự nhiên.
- Trình bày vai trò của Amazon CloudFront trong tối ưu chi phí, bảo mật, độ tin cậy và hiệu năng của ứng dụng.
- Chia sẻ kinh nghiệm biến ý tưởng thành sản phẩm trong cuộc thi hackathon có thời gian giới hạn.
- Làm rõ tính không xác định của LLM và các biện pháp giảm thiểu rủi ro khi triển khai thực tế.
- Giới thiệu kiến trúc Multi-Agent cấp doanh nghiệp thông qua bài toán chấm điểm tín dụng startup.
- Cung cấp định hướng nghề nghiệp và tạo cơ hội hỏi đáp, trao đổi với các diễn giả.

### Danh Sách Diễn Giả

- **Tinh Truong** – *Context Is Everything: Making AI Actually Work for You*
- **Anh Pham** – *Friendly AI Assistant with Amazon Quick*
- **Thinh Nguyen** – *From Edge To Origin: CloudFront as Your Foundation*
- **Team VIB** – *36 hrs with LotusHacks – Building UTMorpho from Idea to Reality*
- **Duc Dao** – *Non-Determinism of “Deterministic” LLM Settings*
- **Vy Lam** – *Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring*

### Nội dung chương trình

#### 09:00 – 09:30 | Context Is Everything: Making AI Actually Work for You

**Diễn giả: Tinh Truong**

- Phân tích lý do hệ thống AI thường cho kết quả không tốt khi thiếu context và làm rõ ý nghĩa thực tế của context.
- Trình bày sự phát triển từ prompt đơn lẻ đến khả năng ghi nhớ, gắn với khái niệm **Second AI Brain**.
- Chia sẻ tư duy và các phương pháp cung cấp context tốt hơn để nâng cao chất lượng phản hồi của AI.
- Đưa ra định hướng nghề nghiệp và gợi ý cách sinh viên có thể bắt đầu xây dựng sản phẩm với AI.
- Giải đáp câu hỏi và trao đổi với người tham dự.

#### 09:30 – 09:45 | Friendly AI Assistant with Amazon Quick

**Diễn giả: Anh Pham**

- Giới thiệu **Quick Chat Agent**, trợ lý AI hỗ trợ khám phá dữ liệu và phân tích insight.
- Trình bày **Quick Flows**, công cụ tạo workflow thông minh bằng ngôn ngữ tự nhiên mà không cần viết code.
- Giới thiệu **Quick Spaces**, không gian cộng tác giúp chuyển insight cá nhân thành tri thức dùng chung của nhóm.
- Minh họa cách sử dụng **Quick Sight** để tạo dashboard và báo cáo từ dữ liệu thô bằng ngôn ngữ tự nhiên.

#### 09:45 – 10:25 | From Edge To Origin: CloudFront as Your Foundation

**Diễn giả: Thinh Nguyen**

- Trình bày cách Amazon CloudFront hỗ trợ nhiều loại workload, từ edge đến origin.
- Phân tích các phương án tối ưu chi phí khi phân phối nội dung qua CloudFront.
- Giới thiệu những khả năng bảo mật giúp bảo vệ ứng dụng và origin.
- Làm rõ cách CloudFront nâng cao độ tin cậy và khả năng sẵn sàng của hệ thống.
- Chia sẻ các kỹ thuật cải thiện hiệu năng và trải nghiệm người dùng.

#### 10:25 – 10:55 | 36 hrs with LotusHacks – Building UTMorpho from Idea to Reality

**Diễn giả: Team VIB**

- Chia sẻ lý do nhóm tham gia LotusHacks và quá trình brainstorming từ con số không.
- Trình bày cách xác định vấn đề và định hình giải pháp UTMorpho.
- Kể lại quá trình phát triển sản phẩm trong 36 giờ dưới áp lực về thời gian.
- Phân tích những khó khăn, thất bại và các bước ngoặt quan trọng của nhóm.
- Giới thiệu tổng quan sản phẩm UTMorpho và trình diễn giải pháp.
- Tổng kết bài học kinh nghiệm và định hướng phát triển tiếp theo.

#### 10:55 – 11:00 | Nghỉ giải lao

Người tham dự nghỉ ngắn trước khi tiếp tục hai phiên chuyên sâu về LLM và hệ thống Multi-Agent.

#### 11:00 – 11:30 | Non-Determinism of “Deterministic” LLM Settings

**Diễn giả: Duc Dao**

- Giải thích cách LLM lựa chọn token tiếp theo trong quá trình inference.
- Phân tích giả định phổ biến rằng `temperature = 0` luôn đảm bảo kết quả xác định.
- Làm rõ ảnh hưởng của các kỹ thuật tối ưu inference khiến kết quả vẫn có thể thay đổi.
- Trình bày tác động thực tế đến kiểm thử, đánh giá và vận hành ứng dụng dùng LLM.
- Đề xuất các biện pháp giảm thiểu để hệ thống ổn định và có khả năng kiểm soát tốt hơn.

#### 11:30 – 12:00 | Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring

**Diễn giả: Vy Lam**

- Phân tích sự không tương thích về cấu trúc giữa hệ thống ngân hàng truyền thống và dữ liệu của startup.
- Làm rõ trường hợp nên và không nên sử dụng một AI agent duy nhất.
- Giới thiệu mô hình Multi-Agent và cách phân chia trách nhiệm giữa các agent chuyên biệt.
- Trình bày kiến trúc **Virtual Credit Committee** cho bài toán chấm điểm tín dụng startup.
- Phân tích guardrail, yêu cầu tuân thủ và kiểm soát rủi ro trong hệ thống cấp doanh nghiệp.
- Đánh giá ROI vận hành, lộ trình triển khai và hướng phát triển tiếp theo.
- Kết thúc bằng phần hỏi đáp với người tham dự.

### Kiến thức và kinh nghiệm đạt được

#### Xây dựng ứng dụng AI dựa trên context

- Hiểu rằng chất lượng của context ảnh hưởng trực tiếp đến tính chính xác và mức độ hữu ích của phản hồi AI.
- Nhận thức được sự phát triển từ prompt engineering sang memory, knowledge và context management.
- Biết cần thiết kế dữ liệu đầu vào, lịch sử hội thoại và tri thức liên quan một cách có chủ đích.

#### Khai thác AI để làm việc với dữ liệu

- Hiểu cách trợ lý hội thoại hỗ trợ khám phá dữ liệu và phân tích insight.
- Biết khả năng tạo workflow, không gian cộng tác, dashboard và báo cáo bằng ngôn ngữ tự nhiên.
- Nhận thấy tiềm năng giảm rào cản kỹ thuật cho người dùng không chuyên lập trình.

#### Nâng cao kiến thức về Amazon CloudFront

- Hiểu CloudFront không chỉ là CDN mà còn là lớp nền tảng hỗ trợ bảo mật, hiệu năng và độ tin cậy.
- Biết các khía cạnh cần xem xét khi tối ưu chi phí và bảo vệ origin.
- Có thêm góc nhìn về thiết kế workload từ edge đến hạ tầng phía sau.

#### Kinh nghiệm phát triển sản phẩm dưới áp lực

- Học được cách đi từ brainstorming, xác định vấn đề đến xây dựng và demo sản phẩm trong thời gian giới hạn.
- Nhận thức rõ vai trò của việc xác định phạm vi, ưu tiên tính năng và phối hợp nhóm trong hackathon.
- Hiểu rằng thất bại và thay đổi hướng đi là một phần quan trọng của quá trình phát triển sản phẩm.

#### Thiết kế hệ thống LLM đáng tin cậy

- Hiểu rằng `temperature = 0` không đồng nghĩa với kết quả luôn giống nhau tuyệt đối.
- Nhận thức được rủi ro khi viết test hoặc quy trình nghiệp vụ dựa trên giả định LLM hoàn toàn xác định.
- Biết cần kết hợp đánh giá theo tiêu chí, guardrail, logging và cơ chế xử lý sai khác.

#### Kiến trúc Multi-Agent cấp doanh nghiệp

- Phân biệt được tình huống phù hợp với Single Agent và Multi-Agent.
- Hiểu cách tổ chức các agent theo vai trò để mô phỏng một hội đồng ra quyết định.
- Nhận thức được tầm quan trọng của guardrail, compliance, khả năng giải thích và ROI khi đưa AI vào nghiệp vụ tài chính.

### Khả năng áp dụng vào công việc

- Cải thiện prompt và luồng AI của dự án bằng cách cung cấp context có cấu trúc thay vì chỉ sử dụng câu lệnh ngắn.
- Áp dụng CloudFront khi cần phân phối nội dung với hiệu năng cao, bảo vệ origin và tối ưu trải nghiệm người dùng.
- Thiết kế kiểm thử LLM theo mức độ chấp nhận được thay vì so sánh tuyệt đối từng câu trả lời.
- Chỉ lựa chọn Multi-Agent khi bài toán thực sự cần nhiều vai trò chuyên biệt, cơ chế phối hợp và kiểm soát quyết định.
- Áp dụng tư duy hackathon: xác định vấn đề cốt lõi, giới hạn phạm vi MVP và ưu tiên khả năng trình diễn giá trị thực tế.

### Tổng kết

Event 1 cung cấp góc nhìn đa chiều từ kỹ thuật AI, dữ liệu và hạ tầng AWS đến kinh nghiệm phát triển sản phẩm. Nội dung giúp tôi hiểu rõ hơn cách xây dựng ứng dụng AI có context, sử dụng CloudFront như một lớp nền tảng, kiểm soát tính không xác định của LLM và đánh giá đúng thời điểm áp dụng kiến trúc Multi-Agent. Phần chia sẻ của Team VIB cũng mang lại kinh nghiệm thực tế về làm việc nhóm, quản lý thời gian và biến ý tưởng thành sản phẩm trong điều kiện áp lực cao.
