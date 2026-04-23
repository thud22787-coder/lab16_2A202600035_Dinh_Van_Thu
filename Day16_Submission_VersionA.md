# Day 16 Submission — Cá nhân (Phiên bản A)

## Members

- Đinh Văn Thư — 2A202600035

---

## 1. Idea Reframed

**Original idea:**

> Xây dựng chatbot AI hỗ trợ review hợp đồng cho người lao động.

**Reframed as a product opportunity:**

> Tại Việt Nam, phần lớn người lao động ký hợp đồng lao động mà không hiểu rõ các điều khoản đang bất lợi cho mình — về thời gian thử việc, điều khoản chấm dứt, phụ cấp, hay non-compete. Chi phí thuê luật sư quá cao và không thực tế trong bối cảnh ký offer; các công cụ tra cứu pháp luật hiện tại chỉ trả về điều luật thô, không đọc được hợp đồng cụ thể của từng người.
>
> **Observed gap:** Khoảng trống giữa "ký rồi mới biết bị thiệt" và "hiểu đủ để đặt câu hỏi đúng hoặc từ chối trước khi ký" — hiện chưa có sản phẩm nào lấp được khoảng trống này ở mức giá và tốc độ phù hợp với người lao động phổ thông.
>
> **Founding belief:** AI có thể giải thích hợp đồng bằng ngôn ngữ thường ngày, đánh dấu điều khoản rủi ro theo luật lao động Việt Nam, và gợi ý câu hỏi cần hỏi lại nhà tuyển dụng — không thay thế luật sư mà thay thế sự im lặng vì không biết hỏi ai.

---

## 2. Customer / Segment Card

| Trường                  | Nội dung                                                                                                                                                                                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Segment name**        | Lao động tri thức trẻ tại TP.HCM và Hà Nội, 22–32 tuổi, đang trong quá trình nhận và xem xét hợp đồng lao động mới (offer từ công ty)                                                                                                                  |
| **Operational context** | Nhận offer letter kèm file hợp đồng, có 1–5 ngày để quyết định ký hay không; không có người tư vấn pháp lý trong mạng lưới cá nhân                                                                                                                     |
| **Recurring workflow**  | Nhận file HĐ (PDF/Word) → đọc một mình → gặp điều khoản không hiểu → hỏi bạn bè không chuyên hoặc Google → không có câu trả lời rõ cho HĐ cụ thể của mình → ký vì không biết làm gì khác                                                               |
| **Pain moment**         | Khoảnh khắc đọc thấy một điều khoản "có vẻ lạ" (non-compete quá rộng, thử việc dài hơn luật cho phép, không ghi rõ phụ cấp) nhưng không biết nó có vi phạm luật không và có thể yêu cầu sửa không                                                      |
| **Why now**             | Thị trường lao động biến động mạnh sau 2023 — nhiều người chuyển việc thường xuyên hơn, gặp HĐ từ nhiều loại hình công ty (startup, FDI, nước ngoài) với điều khoản phức tạp hơn; đồng thời LLM tiếng Việt đã đủ khả năng xử lý văn bản pháp lý cơ bản |
| **Access path**         | Facebook groups (Góc chia sẻ dân văn phòng, Hội con sen, ITviec Community), LinkedIn Việt Nam, Telegram job channels, các nền tảng tuyển dụng như TopCV và ITviec                                                                                      |

**One-sentence description:**

> Người lao động trẻ 22–32 tuổi ở đô thị lớn, vừa nhận offer việc làm, đang cầm tờ hợp đồng trong tay và không biết điều khoản nào đang bất lợi cho mình hay có thể đàm phán được.

---

## 3. Need Map (3 needs)

### Need #1 _(priority)_

- **Statement (JTBD):** When tôi nhận được hợp đồng lao động và phải quyết định trong vài ngày, I want biết ngay điều khoản nào bất thường, vi phạm quyền lợi của tôi, hoặc trái Bộ Luật Lao Động 2019, so I can ký có ý thức hoặc đề nghị sửa trước khi quá muộn.
- **Current workaround:** Hỏi bạn bè hoặc đăng lên group Facebook mô tả lại điều khoản — nhận được ý kiến không chuyên, không áp dụng được vào HĐ cụ thể; hoặc Google tìm điều luật nhưng không biết điều luật đó có áp dụng cho mình không.
- **Pain signal:** Mất quyền lợi tài chính và pháp lý thực tế sau khi ký (bị trừ lương sai, bị ràng buộc non-compete không hợp lý, không được hưởng phụ cấp đúng quy định) → phát sinh tranh chấp tốn kém hơn nhiều so với chi phí review trước.
- **Evidence / proxy evidence:** _(Quan sát bên ngoài — không phải phỏng vấn trực tiếp)_ Các thread dài trên ITviec forum và group Facebook về chủ đề "điều khoản HĐ kỳ lạ" có tương tác cao; báo Lao Động, VnExpress thường xuyên có bài "những điều khoản hợp đồng cần chú ý khi ký"; số lượng khiếu nại tranh chấp lao động tại Sở LĐTBXH TP.HCM tăng hằng năm (nguồn: báo cáo Sở LĐTBXH — _cần xác minh con số cụ thể_).
- **Why underserved:** Luật sư tư giá 200k–500k/giờ, không thực tế với người lao động bình thường cho một việc xảy ra định kỳ; các app pháp lý hiện có (LawNet, Thư Viện Pháp Luật) chỉ tra cứu điều luật thô, không đọc và phân tích HĐ cụ thể của người dùng.

---

### Need #2

- **Statement (JTBD):** When tôi thấy một điều khoản trong HĐ có vẻ bất thường, I want biết điều khoản đó có hợp lệ theo pháp luật không và mình có quyền yêu cầu sửa không, so I can đề nghị thay đổi với nhà tuyển dụng một cách tự tin và có căn cứ.
- **Current workaround:** Google điều luật liên quan → đọc văn bản pháp lý khô khan và dài → không chắc điều luật đó có áp dụng cho trường hợp cụ thể của mình không → bỏ cuộc và ký.
- **Pain signal:** Stress tâm lý khi không chắc mình đang đúng; đa số chọn im lặng và ký vì "thôi cứ ký đã, đi làm rồi tính" — mất cơ hội đàm phán điều khoản tốt hơn ngay từ đầu.
- **Evidence / proxy evidence:** _(Proxy)_ Lượng tìm kiếm cao cho các từ khóa như "hợp đồng lao động thử việc bao lâu", "điều khoản non-compete có hiệu lực không" trên Google VN — phản ánh nhu cầu thông tin cụ thể, không chỉ chung chung.
- **Why underserved:** Không có công cụ nào hiện tại nối được từ "câu hỏi cụ thể về HĐ của tôi" → "điều luật áp dụng" → "tôi có thể làm gì tiếp theo" trong một luồng liền mạch, bằng tiếng Việt thường ngày.

---

### Need #3

- **Statement (JTBD):** When tôi đã ký HĐ nhưng phát hiện công ty đang thực hiện sai một số điều khoản (ví dụ: tính lương OT sai, không đóng BHXH đúng hạn), I want hiểu mình có quyền gì và bước tiếp theo cụ thể là gì, so I can hành động bảo vệ quyền lợi mà không phải tốn tiền thuê luật sư ngay lập tức.
- **Current workaround:** Hỏi bạn bè, gọi đường dây tư vấn pháp luật miễn phí (thường bận hoặc chờ lâu), hoặc chịu đựng vì không biết bắt đầu từ đâu.
- **Pain signal:** Mất tiền lương, phúc lợi thực tế; cảm giác bất lực khi không có thông tin; nhiều người chọn im lặng hoặc nghỉ việc thay vì khiếu nại.
- **Evidence / proxy evidence:** _(Proxy)_ Đường dây tư vấn pháp luật miễn phí 1800 6179 của Bộ Tư pháp thường xuyên quá tải — signal rõ về cầu chưa được đáp ứng ở phân khúc không có khả năng trả tiền cho luật sư.
- **Why underserved:** Kênh hỗ trợ nhà nước quá tải và chậm; luật sư tư quá đắt; chưa có sản phẩm nào hướng dẫn người lao động tự xử lý tình huống đơn giản trước khi cần đến luật sư thật.

---

## 4. Strategy Statement

```
For lao động tri thức trẻ tại TP.HCM và Hà Nội đang nhận offer và xem xét ký hợp đồng lao động mới

who struggle with việc không thể đọc hiểu và đánh giá rủi ro pháp lý trong hợp đồng một mình,
trong thời gian ngắn, với chi phí hợp lý,

our product helps them hiểu rõ từng điều khoản quan trọng bằng ngôn ngữ thường ngày,
nhận diện điều khoản bất lợi hoặc vi phạm Bộ Luật Lao Động 2019,
và biết cụ thể mình nên hỏi lại / đề nghị sửa / hay từ chối điều gì — trước khi ký,

through một chatbot AI có thể đọc file hợp đồng do người dùng upload,
phân tích theo khung pháp lý lao động Việt Nam được cấu trúc hóa,
và trả lời câu hỏi cụ thể của từng người bằng tiếng Việt thường ngày,

unlike các app tra cứu pháp luật hiện tại (chỉ trả về điều luật thô, không đọc HĐ cụ thể)
và tư vấn luật sư truyền thống (giá 200k–500k/giờ, không tiện lợi cho quyết định trong vài ngày),

because we can leverage khả năng xử lý văn bản pháp lý của LLM,
kết hợp với cơ sở pháp luật lao động Việt Nam được cấu trúc hóa và cập nhật,
và kênh tiếp cận người lao động qua digital community chi phí thấp (Facebook groups, LinkedIn, ITviec).
```

---

## 5. Moat Hypothesis

**Moat mechanism:** Domain-learning flywheel + Workflow embedding

Nếu triển khai **10.000+ lượt review hợp đồng** trong vertical hợp đồng lao động Việt Nam, những yếu tố sau sẽ cải thiện có hệ thống:

1. **Độ chính xác nhận diện điều khoản rủi ro tăng lên** — mô hình học được các pattern bất thường thực tế phổ biến tại thị trường Việt Nam (thử việc quá 60 ngày, non-compete không có thời hạn, phụ cấp ẩn không ghi trong HĐ...) mà không có trong văn bản luật.
2. **Thư viện tình huống thực tế (anonymized) trở thành tài sản dữ liệu độc quyền** — đối thủ mới vào không có lịch sử case; một LLM chung không có context này.
3. **Brand recall và trust trong cộng đồng người lao động tăng dần** — khi ai đó nhận offer, đây là công cụ đầu tiên họ nghĩ đến và recommend trong network của mình.

**Why competitors cannot easily replicate:**

> ChatGPT hay các LLM chung có thể làm điều tương tự ở mức cơ bản, nhưng thiếu context pháp lý lao động Việt Nam được cấu trúc hóa, thiếu lịch sử case thực tế từ thị trường, và không được embed vào đúng khoảnh khắc ra quyết định (nhận offer → cần review ngay). Các công ty luật truyền thống không có động cơ tự phá giá bằng AI. Các app pháp lý hiện tại (LawNet) đang phục vụ phân khúc tra cứu, không phải phân khúc ra quyết định.

---

## 6. Initial TAM / SAM / SOM

| Layer   | Estimate                            | Key assumptions                                                                                                                                  | Confidence                                                     |
| ------- | ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------- |
| **TAM** | 700 tỷ – 1.200 tỷ VNĐ/năm           | ~4–5 triệu lượt ký/gia hạn HĐ lao động chính thức mỗi năm tại VN; sẵn sàng trả 150k–250k/lần review nếu có giá trị rõ ràng                       | **Low** — con số lượt ký là ước tính, chưa có nguồn chính thức |
| **SAM** | 100 tỷ – 180 tỷ VNĐ/năm             | Tập trung lao động tri thức tại TP.HCM + Hà Nội; tỷ lệ sẵn sàng trả tiền cao hơn mức bình quân; ước tính ~600k–800k lượt/năm trong phân khúc này | **Low** — chưa có data về willingness to pay thực tế           |
| **SOM** | 1,5 tỷ – 5 tỷ VNĐ (12–24 tháng đầu) | 10.000–25.000 lượt sử dụng trả phí; model freemium với tỷ lệ convert 15–25%; giá 99k–199k/lần hoặc gói subscription                              | **Low** — chưa validate giá và convert rate                    |

**Top 3 unknowns cần research thêm:**

1. **Willingness to pay thực sự là bao nhiêu?** — người lao động có sẵn sàng trả tiền cho dịch vụ này không, hay sẽ dùng ChatGPT miễn phí? Cần phỏng vấn ít nhất 10–15 người trong segment.
2. **Rủi ro pháp lý về hành nghề tư vấn luật không phép** — sản phẩm có thể bị coi là "hành nghề luật sư" trái phép theo Luật Luật sư 2006 không? Cần tham vấn luật sư để xác định cách định vị an toàn (ví dụ: "công cụ giáo dục pháp luật" vs "tư vấn pháp lý").
3. **Chất lượng output AI có đủ tin cậy để người dùng ra quyết định?** — nếu AI sai một điều khoản quan trọng, hậu quả với người dùng có thể nghiêm trọng. Cần xác định mức độ disclaimer cần thiết và cơ chế kiểm soát chất lượng.

**Judgment:**

- [x] **Worth pursuing — nhưng chưa phải ngay.** Cần validate willingness to pay và làm rõ rủi ro pháp lý trước khi build full product. MVP thử nghiệm (ví dụ: Telegram bot hoặc Google Form + phân tích thủ công) có thể chạy trong 2–4 tuần để thu thập signal thực.

---

## 7. Positioning Note

**What we are:**

> Công cụ giúp người lao động hiểu hợp đồng của chính mình bằng ngôn ngữ thường ngày — nhanh, rẻ, và đúng khoảnh khắc họ cần ra quyết định.

**What we are not / not yet:**

> Không phải dịch vụ tư vấn pháp lý có trách nhiệm pháp lý, và chưa phục vụ doanh nghiệp (bên soạn hợp đồng) hay các tranh chấp lao động phức tạp trong giai đoạn đầu.

---

## 8. Self-assessment trước Day 17

**Mắt xích yếu nhất hiện tại:** **Moat** — lợi thế domain-learning flywheel có logic, nhưng barrier thực sự trước một big tech player hoặc một công ty luật lớn muốn làm sản phẩm tương tự vẫn còn mỏng. Cần nghĩ thêm về distribution moat — cụ thể là partnership với nền tảng tuyển dụng (TopCV, ITviec, VietnamWorks) để tiếp cận người dùng đúng lúc nhận offer, thay vì chỉ dựa vào organic community.

**Open questions muốn khám phá ở Day 17:**

1. **MVP tối giản nhất là gì** — chatbot web upload PDF, hay Telegram bot, hay thậm chí một landing page + review thủ công để test willingness to pay trước khi build AI?
2. **Cách định vị pháp lý an toàn** — "công cụ tra cứu và giáo dục pháp luật" có đủ để tránh bị coi là hành nghề luật sư không phép không?
3. **Kênh phân phối nào tiếp cận người dùng đúng khoảnh khắc** — người lao động cần review HĐ ngay khi nhận offer, không phải sau khi đã ký xong 2 tuần. Làm thế nào để xuất hiện đúng lúc đó?

---

> **Ghi chú về evidence:** Toàn bộ bài này được viết từ góc quan sát bên ngoài (không có phỏng vấn khách hàng trực tiếp). Các proxy evidence được ghi rõ nguồn và mức độ chắc chắn. Các con số market sizing đều là ước tính với confidence thấp — cần research thực tế trước khi dùng để ra quyết định.
