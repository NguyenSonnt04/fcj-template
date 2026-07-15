---
title: "Các events đã tham gia"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 4. </b> "
---

Trong suốt quá trình thực tập tại doanh nghiệp, song song với công việc chuyên môn phát triển sản phẩm **TrustBite**, mình đã được tạo điều kiện tham gia các buổi hội thảo công nghệ lớn và chuyên sâu về Điện toán đám mây (AWS Cloud) và Trí tuệ nhân tạo (AI/LLM). 

Dưới đây là tóm tắt tổng quan về hai sự kiện công nghệ quan trọng mà mình đã tham gia, cùng những kiến thức tích lũy được để ứng dụng vào dự án thực tế:

---

### 1. [Event 1 — AI, AWS Cloud và hệ thống Multi-Agent](4.1-Event1/)

*   **Thời gian:** 09:00 – 12:00
*   **Vai trò:** Người tham dự
*   **Tóm tắt nội dung chính:**
    Hội thảo tập trung vào các kỹ thuật thiết kế context tối ưu cho LLM (Context Engineering), cách trực quan hóa dữ liệu bằng ngôn ngữ tự nhiên thông qua bộ công cụ **Amazon Quick** (Quick Chat Agent, Quick Flows, Quick Spaces), và tối ưu hóa hạ tầng phân phối nội dung an toàn hiệu năng cao bằng **Amazon CloudFront**. 
    Đồng thời, hội thảo cũng đi sâu vào tính phi xác định (Non-Determinism) của LLM kể cả khi đặt **temperature = 0**, và mô hình kiến trúc **Multi-Agent** cấp doanh nghiệp thông qua bài toán chấm điểm tín dụng doanh nghiệp startup (**Virtual Credit Committee**).
*   **Giá trị tích lũy:**
    *   Hiểu rõ vai trò cốt lõi của **Context Engineering** trong việc định hình kết quả phản hồi của AI.
    *   Nắm bắt kiến trúc phân phối nội dung từ Edge đến Origin bằng Amazon CloudFront để tối ưu chi phí và bảo vệ máy chủ gốc.
    *   Học hỏi kinh nghiệm phát triển sản phẩm MVP dưới áp lực thời gian cao từ cuộc thi LotusHacks.
    *   Tư duy thiết kế hệ thống Multi-Agent phân rã nhiệm vụ và thiết lập cơ chế kiểm định LLM đáng tin cậy.

---

### 2. [Event 2 — AI-Powered Cloud Operations và Enterprise Productivity](4.2-Event2/)

*   **Thời gian:** 09:00 – 11:30
*   **Vai trò:** Người tham dự
*   **Tóm tắt nội dung chính:**
    Sự kiện đi sâu vào các giải pháp ứng dụng trí tuệ nhân tạo để nâng cao hiệu suất doanh nghiệp và vận hành đám mây tự động. Các chủ đề cốt lõi bao gồm **Deep Response Engine** (tự động hóa phát hiện và khắc phục sự cố Cloud nhằm giảm tối đa thời gian downtime), phát triển trợ lý giọng nói thời gian thực độ trễ thấp thông qua mô hình nền tảng **Amazon Nova Sonic**, và ứng dụng **AWS DevOps Agent** hỗ trợ vận hành đa đám mây.
    Đặc biệt, sự kiện hướng dẫn giải pháp tích hợp và thiết lập kết nối riêng tư bảo mật qua VPC dựa trên giao thức **Model Context Protocol (MCP)** kết hợp cùng Amazon Quick để truy xuất dữ liệu doanh nghiệp an toàn.
*   **Giá trị tích lũy:**
    *   Tiếp cận tư duy vận hành đám mây tự động (Autonomous Cloud Operations) giúp giảm thiểu chỉ số MTTD và MTTR.
    *   Hiểu kiến trúc xử lý truyền tải âm thanh thời gian thực (Speech-to-Speech) độ trễ thấp của AI Voice Agent.
    *   Nắm vững cách thức hoạt động của giao thức **Model Context Protocol (MCP)** trong việc kết nối chuẩn hóa dữ liệu doanh nghiệp nội bộ với các mô hình ngôn ngữ lớn một cách an toàn.

---

### 3. Tổng kết và Khả năng áp dụng vào thực tế
Việc tham gia hai sự kiện công nghệ chuyên sâu này đã giúp mình tích lũy được nhiều tư duy thiết kế hệ thống hiện đại. Cụ thể, mình đã ứng dụng trực tiếp các kiến thức này vào quá trình phát triển sản phẩm thực tập **TrustBite**:
1.  **Thiết kế Prompt & Context có cấu trúc:** Áp dụng phương pháp Context Engineering để tối ưu cấu trúc prompt và context đầu vào cho AI Agent chạy OCR và chống gian lận.
2.  **Thiết kế bộ lọc chấm điểm rủi ro chống gian lận:** Hiểu rõ tính phi xác định của LLM giúp mình thiết lập thuật toán chấm điểm rủi ro (Risk Scoring) và sử dụng khoảng cách tương đối Levenshtein thay vì so khớp tuyệt đối để hệ thống ra quyết định thông minh hơn.
3.  **Tư duy phát triển MVP gọn nhẹ:** Áp dụng quy tắc rút gọn phạm vi tính năng từ bài học LotusHacks để tập trung phát triển và hoàn thiện luồng S3 Upload -> OCR Textract -> Chống gian lận cốt lõi của TrustBite đúng hạn.
