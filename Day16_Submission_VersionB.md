# Day 16 Submission — Cá nhân (Phiên bản B — BTVN)

## Members

- Đinh Văn Thư — 2A202600035

---

## Reflection: Từ A → B, tôi đã thay đổi gì và tại sao

Sau khi nộp Phiên bản A, tôi nhận ra 3 điểm yếu cốt lõi cần sửa:

**1. Segment quá rộng.** "Lao động tri thức 22–32 tuổi tại TP.HCM và Hà Nội" là một tập quá lớn và không có operational trigger rõ. Phiên bản B hẹp xuống còn: **fresher và mid-level trong ngành tech (developer, designer, data) nhận offer từ công ty nước ngoài hoặc startup có vốn ngoại**. Nhóm này nhận hợp đồng phức tạp hơn (điều khoản IP, ESOP, non-compete theo luật nước ngoài), có khả năng chi trả, và digital-native nên dễ tiếp cận và validate nhanh.

**2. Moat quá mỏng.** Phiên bản A mô tả flywheel đúng nhưng chưa nêu được điều kiện để flywheel thực sự spin. Phiên bản B thêm distribution moat cụ thể: partnership nhúng vào nền tảng tuyển dụng (ITviec, TopDev) — tiếp cận người dùng đúng lúc họ nhận offer, không phải sau khi đã ký.

**3. Story chưa nhất quán.** Phiên bản A có Customer nói về lao động phổ thông, nhưng Moat lại dựa vào tech worker với hợp đồng phức tạp — hai mảng không khớp nhau. Phiên bản B thống nhất toàn bộ câu chuyện quanh một segment duy nhất.

---

## 1. Idea Reframed

**Original idea:**

> Xây dựng chatbot AI hỗ trợ review hợp đồng cho người lao động.

**Reframed as a product opportunity:**

> Tech worker Việt Nam (developer, designer, data analyst) nhận offer từ công ty nước ngoài hoặc startup có vốn ngoại thường nhận hợp đồng bằng tiếng Anh hoặc song ngữ, kèm các điều khoản đặc thù mà hợp đồng lao động Việt Nam thông thường không có: điều khoản sở hữu trí tuệ (IP assignment), non-compete với phạm vi và thời hạn không rõ, ESOP vesting schedule, hoặc điều khoản chấm dứt hợp đồng theo law nước ngoài.
>
> **Observed gap:** Những người này đủ kỹ năng để hiểu tech stack phức tạp, nhưng không có nền tảng pháp lý để đánh giá điều khoản hợp đồng — và khoảng thời gian ra quyết định thường chỉ 2–5 ngày. Luật sư quá đắt và quá chậm cho tình huống này. Bạn bè trong ngành có thể chia sẻ kinh nghiệm nhưng không thể đọc hợp đồng cụ thể của bạn.
>
> **Founding belief:** Một chatbot AI được train trên khung pháp lý lao động Việt Nam kết hợp với các pattern hợp đồng phổ biến từ công ty nước ngoài có thể giải thích hợp đồng cụ thể của từng người, gắn flag vào điều khoản rủi ro, và đề xuất câu hỏi cần hỏi lại HR — đủ để người dùng ra quyết định có ý thức trong vài ngày mà không cần tốn tiền thuê luật sư.

---

## 2. Customer / Segment Card

| Trường                  | Nội dung                                                                                                                                                                                                                                                                                                     |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Segment name**        | Fresher và mid-level trong ngành tech tại Việt Nam (developer, designer, data analyst, product), 22–30 tuổi, đang nhận offer từ công ty nước ngoài hoặc startup có vốn ngoại lần đầu hoặc lần thứ hai                                                                                                        |
| **Operational context** | Nhận offer letter + file hợp đồng (thường PDF tiếng Anh hoặc song ngữ), có 2–5 ngày để quyết định. Không có luật sư trong mạng lưới cá nhân. Thường hỏi anh/chị senior trong ngành — nhưng senior cũng không chắc về điều khoản pháp lý                                                                      |
| **Recurring workflow**  | Nhận email offer → mở file HĐ → đọc một lượt → không hiểu phần IP/non-compete/ESOP → hỏi bạn bè hoặc post lên group → nhận ý kiến không đủ cụ thể → ký vì deadline approaching và không muốn mất offer                                                                                                       |
| **Pain moment**         | Khoảnh khắc đọc điều khoản "All IP created during employment, including on personal time, belongs to the Company" hoặc "Non-compete for 12 months in Southeast Asia" và không biết: (1) điều này có hợp lệ theo luật Việt Nam không, (2) có thể yêu cầu sửa không, (3) nếu vi phạm thì hậu quả thực tế là gì |
| **Why now**             | Sau 2022–2023, số lượng công ty nước ngoài và startup vốn ngoại tuyển dụng trực tiếp tại Việt Nam tăng mạnh (theo dữ liệu tuyển dụng ITviec). Đồng thời LLM đã đủ khả năng xử lý văn bản pháp lý tiếng Anh và Việt với độ chính xác đủ dùng cho phân tích sơ bộ                                              |
| **Access path**         | ITviec community, TopDev blog và newsletter, Facebook group "Cộng đồng Developer Việt Nam" (~300k members), Viblo, LinkedIn Tech Vietnam; và đặc biệt: có thể nhúng trực tiếp vào ITviec/TopDev ngay tại trang job offer                                                                                     |

**One-sentence description:**

> Developer hoặc designer Việt Nam 22–30 tuổi vừa nhận offer từ công ty nước ngoài, đang cầm tờ hợp đồng tiếng Anh trong tay và không biết điều khoản IP hay non-compete kia có bất lợi gì hay có thể negotiate không.

---

## 3. Need Map (3 needs)

### Need #1 _(priority)_

- **Statement (JTBD):** When tôi nhận offer từ công ty nước ngoài và phải quyết định trong 2–5 ngày, I want hiểu ngay các điều khoản IP, non-compete, và chấm dứt HĐ trong file hợp đồng này có bất lợi gì cho tôi và có vi phạm luật lao động Việt Nam không, so I can ký với hiểu biết rõ ràng hoặc negotiate điều khoản cụ thể trước khi deadline qua đi.
- **Current workaround:** Post ảnh chụp điều khoản lên group Facebook hoặc hỏi anh/chị senior trong ngành — nhận được ý kiến chung chung như "điều khoản IP kiểu này bình thường ở công ty nước ngoài" nhưng không ai nói rõ nó có hợp lệ theo luật Việt Nam không hay mình có thể yêu cầu sửa như thế nào.
- **Pain signal:** Ký xong rồi mới biết điều khoản non-compete ràng buộc mình không được nhận freelance job trong 12 tháng sau khi nghỉ, hoặc mọi side project cá nhân đều thuộc sở hữu công ty — mất cơ hội thu nhập thực tế và tự do nghề nghiệp.
- **Evidence / proxy evidence:** Thread "Hợp đồng IP assignment — điều khoản này có bình thường không?" trên ITviec forum có 40+ replies, nhiều người chia sẻ tình huống tương tự; Group Facebook "Cộng đồng Developer Việt Nam" có post định kỳ về chủ đề hợp đồng với công ty nước ngoài được engage cao. _(Đây là proxy evidence quan sát từ bên ngoài — chưa có phỏng vấn trực tiếp.)_
- **Why underserved:** Luật sư tư giá 200k–500k/giờ và thường mất 2–3 ngày để có cuộc hẹn — quá chậm và đắt cho một quyết định phải đưa ra trong 2–5 ngày; senior trong ngành biết kinh nghiệm thực tế nhưng không có nền tảng pháp lý; LawNet và Thư Viện Pháp Luật chỉ tra cứu điều luật, không đọc được hợp đồng cụ thể.

---

### Need #2

- **Statement (JTBD):** When tôi thấy một điều khoản trong HĐ có vẻ bất thường và muốn yêu cầu công ty sửa, I want biết mình đang đứng trên cơ sở pháp lý nào và nên diễn đạt yêu cầu đó như thế nào với HR, so I can negotiate hiệu quả mà không bị coi là "khó tính" hoặc mất offer.
- **Current workaround:** Google tìm "non-compete clause Vietnam law" → đọc bài viết tiếng Anh chung chung về luật Việt Nam → không chắc áp dụng được vào trường hợp cụ thể → im lặng và ký để không mất offer.
- **Pain signal:** Bỏ lỡ cơ hội negotiate điều khoản tốt hơn (ví dụ: carve-out side project cá nhân khỏi IP clause) vì không có căn cứ để yêu cầu và không biết cách diễn đạt.
- **Evidence / proxy evidence:** _(Proxy)_ Số lượt tìm kiếm cao cho "điều khoản không cạnh tranh có hiệu lực không Việt Nam" và "IP assignment clause Vietnam" trên Google — phản ánh nhu cầu thông tin cụ thể nhưng chưa có nguồn đáng tin cậy và tiện lợi.
- **Why underserved:** Thông tin pháp lý hiện có hoặc quá chuyên sâu (văn bản luật) hoặc quá chung chung (bài blog) — không ai giúp được bạn soạn câu trả lời cho HR của công ty cụ thể đang offer bạn.

---

### Need #3

- **Statement (JTBD):** When tôi đang làm việc và phát hiện công ty đang áp dụng điều khoản HĐ theo cách tôi không đồng ý (ví dụ: claim sở hữu một side project tôi làm ngoài giờ), I want hiểu ngay quyền của tôi và bước tiếp theo cụ thể là gì, so I can phản hồi có căn cứ thay vì chỉ im lặng hoặc nghỉ việc.
- **Current workaround:** Gọi đường dây tư vấn pháp luật miễn phí (chờ lâu, bận), hỏi bạn bè, hoặc chịu đựng.
- **Pain signal:** Mất tài sản trí tuệ thực tế (side project, open-source contribution) hoặc phải trả tiền phạt vi phạm điều khoản non-compete khi chuyển việc.
- **Evidence / proxy evidence:** _(Proxy)_ Đường dây 1800 6179 của Bộ Tư pháp thường xuyên quá tải — signal về cầu chưa được đáp ứng. Các bài báo VnExpress, Dân Trí về tranh chấp IP với lao động ngành tech xuất hiện định kỳ.
- **Why underserved:** Kênh nhà nước quá tải và chậm; luật sư quá đắt; không có sản phẩm nào hướng dẫn người lao động tự xử lý tình huống đơn giản trước khi cần đến luật sư thật.

---

## 4. Strategy Statement

```
For fresher và mid-level tech worker tại Việt Nam đang nhận offer từ công ty nước ngoài
hoặc startup có vốn ngoại lần đầu hoặc lần thứ hai,

who struggle with việc không hiểu được các điều khoản pháp lý phức tạp
(IP assignment, non-compete, ESOP) trong hợp đồng tiếng Anh hoặc song ngữ,
trong khoảng thời gian ra quyết định chỉ 2–5 ngày,

our product helps them hiểu rõ từng điều khoản rủi ro bằng ngôn ngữ thường ngày,
biết điều khoản nào hợp lệ / bất lợi / có thể negotiate theo luật lao động Việt Nam,
và có sẵn đề xuất cách diễn đạt yêu cầu sửa đổi với HR —
tất cả trong dưới 15 phút kể từ khi upload file hợp đồng,

through một chatbot AI đọc file hợp đồng do người dùng upload (PDF/Word, tiếng Anh hoặc tiếng Việt),
phân tích theo khung pháp lý lao động Việt Nam được cấu trúc hóa,
flag các điều khoản rủi ro và giải thích bằng tiếng Việt thường ngày,
và gợi ý câu hỏi / yêu cầu cụ thể người dùng có thể đặt cho HR,

unlike tra cứu pháp luật truyền thống (LawNet — chỉ trả điều luật thô, không đọc HĐ cụ thể),
senior trong ngành (biết kinh nghiệm nhưng không có nền tảng pháp lý),
và tư vấn luật sư (200k–500k/giờ, mất 2–3 ngày để có cuộc hẹn — quá chậm và đắt),

because we can leverage khả năng xử lý văn bản pháp lý tiếng Anh và Việt của LLM,
kết hợp với cơ sở pháp luật lao động Việt Nam được cấu trúc hóa,
và distribution channel trực tiếp vào đúng khoảnh khắc ra quyết định
thông qua partnership với ITviec và TopDev — nền tảng nơi người dùng nhận offer.
```

---

## 5. Moat Hypothesis

**Moat mechanism:** Distribution embedding + Domain-learning flywheel

**Tầng 1 — Distribution moat (ngắn hạn, khó replicate nhanh):**
Nếu được nhúng vào luồng tuyển dụng của ITviec hoặc TopDev — ví dụ: nút "Review HĐ này" xuất hiện ngay khi candidate nhận offer letter trên platform — sản phẩm tiếp cận người dùng đúng khoảnh khắc ra quyết định, không cần người dùng chủ động tìm kiếm. Đối thủ muốn replicate phải đàm phán lại partnership tương tự từ đầu.

**Tầng 2 — Domain-learning flywheel (trung hạn, compound theo thời gian):**
Nếu chạy được **5.000+ lượt review hợp đồng** trong vertical hợp đồng lao động tech tại Việt Nam, những yếu tố sau sẽ cải thiện có hệ thống:

1. **Độ chính xác nhận diện điều khoản rủi ro tăng lên** — mô hình học được các pattern bất thường thực tế phổ biến trong hợp đồng công ty nước ngoài tại thị trường Việt Nam (IP clause quá rộng, non-compete không giới hạn địa lý, vesting schedule bất lợi) mà không có trong văn bản luật chính thức.
2. **Thư viện tình huống thực tế (anonymized) trở thành tài sản dữ liệu độc quyền** — đối thủ mới vào không có lịch sử case; một LLM chung (ChatGPT) không có context này và không được nhúng vào đúng kênh phân phối.
3. **Brand recall trong cộng đồng tech Việt Nam** — khi developer nhận offer từ công ty nước ngoài, đây là công cụ đầu tiên họ nghĩ đến và recommend cho đồng nghiệp. Word-of-mouth trong cộng đồng tech Việt Nam đặc biệt mạnh vì network tập trung.

**Why competitors cannot easily replicate:**

> ChatGPT có thể review hợp đồng ở mức cơ bản — nhưng người dùng phải biết hỏi đúng câu và tự copy-paste nội dung, không có luồng UX tối ưu. Quan trọng hơn, ChatGPT không được nhúng vào khoảnh khắc người dùng nhận offer. Các app pháp lý hiện tại (LawNet) không có khả năng đọc HĐ cụ thể và phục vụ phân khúc tra cứu, không phải ra quyết định. Công ty luật truyền thống không có động cơ tự phá giá bằng AI. Để replicate được cả hai tầng moat — distribution partnership + domain-learning data — một đối thủ mới cần ít nhất 12–18 tháng và không có lợi thế first-mover.

---

## 6. Initial TAM / SAM / SOM

| Layer   | Estimate                          | Key assumptions                                                                                                                                                       | Confidence                                                                                                                |
| ------- | --------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **TAM** | 500 tỷ – 900 tỷ VNĐ/năm           | ~3–4 triệu lao động chuyển việc/ký HĐ mới mỗi năm tại Việt Nam (nguồn: GSO ước tính — _cần xác minh_); giả định sẵn sàng trả 150k–250k/lần review nếu thấy giá trị rõ | **Low**                                                                                                                   |
| **SAM** | 40 tỷ – 80 tỷ VNĐ/năm             | ~200k–300k lao động tech nhận offer mỗi năm tại TP.HCM và Hà Nội; trong đó ~30–40% từ công ty nước ngoài/startup vốn ngoại; conversion rate 20–30% sang trả phí       | **Low–Med** — con số lao động tech có proxy từ báo cáo tuyển dụng ITviec, nhưng conversion rate là giả định chưa validate |
| **SOM** | 1 tỷ – 4 tỷ VNĐ (12–18 tháng đầu) | 5.000–20.000 lượt sử dụng trả phí; model freemium (3 lần review miễn phí, sau đó 99k–149k/lần hoặc 199k/tháng subscription)                                           | **Low** — chưa có data thực về willingness to pay                                                                         |

**Top 3 unknowns cần research / validate trước khi build:**

1. **Willingness to pay thực sự là bao nhiêu — và so với dùng ChatGPT miễn phí?** Người dùng sẵn sàng trả tiền cho một sản phẩm chuyên biệt không, hay sẽ tự dùng ChatGPT? Cần phỏng vấn 10–15 người trong segment và thử landing page test trước khi build.
2. **Rủi ro pháp lý: có bị coi là "hành nghề tư vấn pháp luật không phép" không?** Luật Luật sư 2006 và Luật Trợ giúp pháp lý 2017 có thể ảnh hưởng đến cách định vị sản phẩm. Cần tham vấn luật sư để xác định ranh giới an toàn ("công cụ giáo dục pháp luật" vs "tư vấn pháp lý").
3. **ITviec / TopDev có sẵn sàng partnership distribution không, và với điều kiện gì?** Toàn bộ distribution moat phụ thuộc vào câu trả lời này. Nếu không có partnership, cần tính lại cả strategy và moat.

**Judgment:**

- [ ] Worth pursuing now
- [x] **Worth pursuing but not now** — cần validate 3 unknowns trên trước khi commit build. Đặc biệt: rủi ro pháp lý và khả năng partnership là 2 unknown có thể thay đổi hoàn toàn cấu trúc sản phẩm. MVP thử nghiệm (landing page + review thủ công hoặc Telegram bot) có thể chạy trong 3–4 tuần để có signal thực mà không cần build full product.
- [ ] Not worth pursuing as currently framed

---

## 7. Positioning Note

**What we are:**

> Công cụ giúp tech worker Việt Nam hiểu hợp đồng lao động từ công ty nước ngoài bằng ngôn ngữ thường ngày — nhanh hơn, rẻ hơn, và đúng khoảnh khắc cần ra quyết định.

**What we are not / not yet:**

> Không phải dịch vụ tư vấn pháp lý có trách nhiệm pháp lý; không giải quyết tranh chấp lao động phức tạp; và chưa phục vụ doanh nghiệp (bên soạn hợp đồng) hay người lao động ngoài ngành tech trong giai đoạn đầu.

---

## 8. Self-assessment trước Day 17

**Mắt xích nào vẫn yếu nhất sau Phiên bản B:**

**Market sizing** — con số SAM và SOM vẫn dựa trên nhiều assumption chưa validate. Tôi chưa có phỏng vấn thực tế nào với người trong segment. Toàn bộ phần market dựa vào proxy evidence và ước tính từ bên ngoài. Đây là điều cần làm đầu tiên trước Day 17.

**Open questions muốn khám phá ở Day 17:**

1. **MVP nào chạy được trong 2 tuần** mà không cần build AI — ví dụ: nhận file HĐ qua Telegram bot, phân tích thủ công, trả kết quả trong 24h với giá 99k — để test willingness to pay thực sự trước khi đầu tư thêm.
2. **Cách định vị pháp lý an toàn** — "công cụ tra cứu và giáo dục pháp luật lao động" thay vì "tư vấn pháp lý" có đủ để hoạt động không? Cần câu trả lời rõ trước khi ra mắt công khai.
3. **Nếu ITviec / TopDev không muốn partnership**, distribution moat sụp đổ — kế hoạch B cho distribution là gì? Có thể build organic community trust trên ITviec forum hoặc Viblo trước khi có partnership chính thức không?

---

> **Ghi chú về evidence (giữ nguyên từ Phiên bản A, không thêm fact bịa):** Toàn bộ bài này được viết từ góc quan sát bên ngoài. Các proxy evidence đều được ghi rõ nguồn và giới hạn. Con số market sizing là ước tính với confidence thấp và được ghi nhận rõ như vậy. Phiên bản B cải thiện về sắc bén tư duy sản phẩm và tính nhất quán của câu chuyện — không phải bằng cách thêm vào facts mà không có.
