---
tags:
  - office-hours
  - ogif
  - discord
title: "OGIF Office Hours #23 - Go weekly, Frontend report, Hybrid working support, and AI mixture agent"
date: 2024-09-16
description: In OGIF Office Hour 23 covered a variety of topics, including updates on Golang Weekly and its use in enterprise environments, comparing Go with Java and C++. The session explored the latest trends in React 19 AC, Next.js, and CSS Grid, alongside new form-building tools. Additionally, the team discussed productivity enhancements using AI-driven solutions like mixture agents, while introducing upcoming tests and hybrid work support.
authors:
  - innno_
---

85 minutes

### Highlights and Topics
1. **Financial Report & Golang Weekly**:
    - Financial performance for August.
    - Updates on Golang blog and survey responses.
2. **Go in Enterprises**:
    - Discussion on Go's readiness for large enterprises, comparison with Java and C++.
    - Challenges and benefits of transitioning to Go in enterprise environments.
3. **Technology Trends & Updates**:
    - React 19 AC, Next.js updates, and new optimizations.
    - Comparison between CSS Grid and Flexbox, updates on JavaScript and form-building tools like fity.
4. **Team Productivity Enhancements**:
    - Using mixture agents and EOM (large language models) to optimize learning and knowledge discovery.
    - Demoing mixture agent in real-world scenarios like learning Chinese and RP trading.
5. **AI-Driven Solutions**:
    - Automation using AI comments and system prompts to improve workflows.
    - Introduction of check-in features for team hybrid work environments.
6. **Upcoming Tests and Team Building**:
    - Design of AI and tool usage tests for the team to enhance efficiency
    - Plans for team outings and return to office support.

---

**Vietnamese Transcript**

**07:25** Anh Thành có nói được không nhỉ? Nghe được không? À, nghe được rồi. Ok, ok." "Có nhận feedback từ Discord rồi. Chờ tí nữa nhé.

**10:28** Hôm nay có review qua mấy số liệu không?

**11:39** Hay là bắt đầu luôn nhỉ? Ok, rồi. Chắc là mở đầu có hai bài báo cáo: một là báo cáo tài chính của tháng 8 vừa rồi, chắc là mình sẽ phát Go Lang Weekly luôn. Sau đó, chắc là mình có một bài liên quan đến ‘stay-ma’ của Go đúng không? Anh em tranh thủ nhé, để tí nữa tổng hợp lại. Bài này em có chỉnh lại, nó hơi dài dòng, hơi nhiều chữ, em đã chỉnh sửa và check lại một chút.

**12:46** Bài tuần vừa rồi thì bên core team đã gửi một khảo sát cho mọi người. Ai có feedback gì về cách sử dụng Go, cảm thấy có những thách thức gì khi xài Go, có thấy khó chịu hay có điều gì muốn đề xuất, thì có thể gửi vào link đã đính kèm ở đây nhé. Bài thứ hai cũng theo xu thế, nó ra một bài trên blog của Golang luôn. Bài này hướng dẫn cách build power app. Bên Google có hướng dẫn cách build app, sử dụng con Gin thôi, không có gì đặc biệt. Đây là phần code kiểu phần run server của họ. Mình có link đầy đủ cho mọi người xem code chi tiết. Mình nghĩ là sử dụng cũng ổn thôi. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/jcn5nn5GPS8?si=9aUk4HoTHhWTdFnv&amp;start=723" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**13:28** Bên cạnh đó, Go cũng ra mắt ZenKit, gần như y hệt Langchain, nhưng của Google. Cái này ra mắt giữa tháng 7, mọi người có thể xem qua. Ví dụ như có các interface vector store mà mình có thể sử dụng, như add document hoặc similarity search.

**14:22** Bài tiếp theo có lẽ sẽ dành cho những ai hứng thú với Erlang hay Langchain. Framework này mới ra bản mới và gần như đã có đầy đủ các tính năng. Bên Alan đang cố gắng map qua và gần như xong rồi, họ claim là đã sẵn sàng cho production. Cách chạy của nó kiểu như thế này. Mình có check qua issue list của nó, không có gì phức tạp, tính năng của nó gần như đã ready hết rồi. Dự đoán rằng framework này sẽ phát triển mạnh.

**15:22** Đó, chắc vậy thôi. À, anh có câu hỏi gì không? Ừ, hôm trước anh em có làm một bài về phần enterprise, chắc mình tranh thủ điểm qua luôn nhé. Bởi vì mình sẽ không có nhiều thời gian cho phần đó. Thắng có hỗ trợ em làm bài này, đúng không Thắng?

**16:23** Thắng có chia sẻ và giúp em viết phần này. Có một số bài trước em đã giới thiệu qua với mọi người về việc Go đã mature như thế nào. Nó đã sẵn sàng để các doanh nghiệp lớn lựa chọn. Nhưng để thay thế hẳn thì chưa được, bởi vì một số doanh nghiệp lớn vẫn đang dùng Java. Việc chuyển đổi có thể có chi phí quá lớn để hoàn toàn bỏ Java. Nhưng đối với các doanh nghiệp mới hoặc những enterprise muốn chuyển đổi, Go là lựa chọn thích hợp.

**17:26** Bài này sẽ trả lời các câu hỏi như thế nào là một enterprise standard language? Tại sao nên dùng Go trong enterprise? Và hiện tại, có những công ty lớn nào đang sử dụng Go. Đây là những bài viết sau, ví dụ như bài tại sao các doanh nghiệp lớn lại chọn Go.

**18:17** Ok, để em điểm qua nội dung nhé. Java được phát triển từ thời Sun Microsystems, với đặc điểm là viết một lần và chạy mọi nơi, vì vậy nó rất ổn định và có đầy đủ tính năng hỗ trợ. Các doanh nghiệp khi chọn ngôn ngữ lập trình thường xem xét tính năng và độ ổn định. Java Enterprise, trước đây gọi là Java EE, nay là Jakarta EE, hỗ trợ synchronous và asynchronous messaging, các định dạng như XML, JSON, và Protocol Buffers.

**19:11** Ngoài ra, doanh nghiệp thường so sánh Java với C++, vì C++ phức tạp hơn do phải quản lý bộ nhớ nhiều. Trong khi đó, Java có garbage collector giúp lo việc quản lý bộ nhớ, nên người dùng không cần quan tâm nhiều, chỉ tập trung vào việc triển khai (implementation) thôi. Hơn nữa, Java có một hệ sinh thái lớn, hỗ trợ gần như đầy đủ tất cả các thư viện và công cụ framework.

**20:15** Vậy, cái lợi của Java Enterprise là so sánh với C++? Đúng rồi, vào thời đó thì C++ còn phổ biến, nhưng C đã quá cũ, tầm 20-40 năm rồi. Những doanh nghiệp cũ dùng COBOL, sau đó chuyển qua C++, và cũng có một số doanh nghiệp chọn C# của Microsoft. Nhưng cộng đồng lập trình thấy rằng C++ có một giai đoạn ổn định hơn nhiều. 

**21:02** C# giống như là một hệ sinh thái riêng của Microsoft. Còn C++ thì được cộng đồng lập trình enterprise đón nhận rộng rãi hơn. Tuy không phải ai cũng sử dụng, nhưng khi nhắc đến ngôn ngữ lập trình enterprise, chỉ có Java và C++ là được đề cập nhiều nhất.

**22:14** Câu hỏi tiếp theo là tại sao Go lại là lựa chọn cho doanh nghiệp? Và những công ty nào đang sử dụng Go? Cái chính là khi làm bài này, anh nghĩ mấy anh em nên đặt mục tiêu là xác định rõ ràng tại sao Java nó thắng được, đúng không? Java nó thắng được với thằng C# và C++. Hiện tại, anh muốn tìm lý do để thuyết phục một người đang sử dụng Java chuyển sang Go. Phải có lý do cụ thể. Trong những bài mà mấy anh em đang làm, hãy tập trung vào điểm đó nhé, cần tìm ra lý do.

<iframe width="560" height="315" src="https://www.youtube.com/embed/jcn5nn5GPS8?si=mCE2JfLQlyLc_o1O&amp;start=1367" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**23:13** Lý do mà hiện tại có thể Go đã giải quyết hết tất cả những vấn đề của Java. Có thể Go mạnh hơn Java về mặt nào đó, hoặc vì những lý do mà bây giờ nên chuyển sang Go. Có thể thêm case study cho việc này. Dạ, chắc là mục tiêu là vậy. Nếu mấy em làm tiếp, nên cân nhắc mỗi bài như một câu hỏi thô, và trả lời mỗi câu hỏi đó với lý do thuyết phục. Đồng thời, có khả năng biến nó thành một slide để trình bày. Kiểu như bài đầu tiên, xem thử tuần sau post lên cộng đồng, nhóm Golang xem như thế nào.

**24:05** Xem coi mọi người đánh giá thế nào nhé. Ok rồi, phá dạ hết rồi. Tiếp theo, mình đi nhanh qua tình hình của Thắng. Tháng vừa rồi anh em tội lắm. Mọi người thấy Thắng đâu chưa? Chắc phải vào lại máy, chắc chơi máy Windows lâu quá.

**25:26** Máy bị treo luôn, đứng Discord ở trên Windows nó hay bị lag hơn Mac đúng không? Mac ngon hơn hẳn.Ok, ơi, không nghe tiếng rồi. Ok, nghe rõ rồi, ngon rồi. Vậy thì tiếp tục.

**26:31** Bài report tháng này cũng tương tự như tháng trước thôi, một số bài không hẳn là mới nhưng em đã tổng hợp lại những gì em thấy có liên quan. Để em điểm nhanh qua nhé. Em mở sẵn rồi, mình đi qua hết cái này rồi xong luôn. Đầu tiên là về React 19 AC. Nó đã ra mắt từ tháng 4, nhưng đến tháng trước mới có báo cáo đầy đủ. Cơ bản là vẫn là tập trung vào việc hỗ trợ server components và một số cải tiến trong việc quản lý script bất đồng bộ (asynchronous script). Đây là một lời nhắc nhở thân thiện cho những bạn nào chưa đọc thì có thể xem thử.

**27:17** Cá nhân em thấy React càng ngày càng rối, nên em sẽ tạm tránh xa phiên bản 19 này. Ý là, React có một số hooks mới, nhưng cảm giác như mình dùng những hooks có sẵn cũng được rồi. Nhưng họ lại đóng gói lại (wrap) và tạo ra thêm các utility hooks mới. Em nghĩ nó cũng ok, nhưng vấn đề là nền tảng như React đang ngày càng trở nên phức tạp, và em cảm thấy nó không còn ý nghĩa nhiều lắm nữa. Bởi vì ban đầu nó chỉ là một công cụ xây dựng đơn giản, nhưng giờ họ cứ cố thêm vào những thứ mà em thấy hơi dư thừa.

**27:55** Tiếp theo là về thằng Next 15. Cảm nhận của em với thằng này cũng tương tự. Next 15 phiên bản AC này cũng hỗ trợ React 19 AC với một số cải tiến. Cái em thấy hay là vụ React compiler. Cái này giống như một bước tối ưu, giúp React tối ưu code của mình. Mình có thể bỏ đi các hooks như `useMemo`, `useCallback`, các hooks mà gần như 90% người dùng React đều phải sử dụng. Bây giờ, với tính năng mới này thì không cần nữa.

**28:39** Cái này thì hay, nhưng vấn đề là những thứ khác, đặc biệt là `app router` của Next.js, em có nói chuyện với anh Thành rồi, hình như anh ấy cũng chán Next lắm. Em cảm giác, em đọc phần bình luận thì thấy cộng đồng cũng bối rối, tuần nào cũng có người hỏi là có cần sử dụng không. Stack hiện tại của họ thì vẫn ổn, nhưng React và Next.js ngày càng trở nên phức tạp. Điều này giống như việc OpenAI chuyển từ Next.js về Remix. Cảm giác thị trường đang dần dịch chuyển.

**29:17** Giống như chuyện OpenAI chuyển từ Next về Remix vậy. Cảm giác chung của cộng đồng là họ đang chuyển dần sang những giải pháp khác hiệu quả hơn. Nest với Next.js vẫn ok, nhưng cá nhân em thấy nó ngày càng phức tạp, đặc biệt là `app router`. Gần như từ khi ra mắt Next 10, 12, 13, em chưa xài nhiều. Dù nó là stack chính, nhưng có vẻ nó cũng không còn là `main stack` nữa

**29:56** Về `main stack` của Next.js, nó vẫn là `main stack`, kiểu vậy. Liên quan một chút với thằng Vercel (`v0`), video này khá ổn. Nó demo về sức mạnh của Vercel, kết hợp với thằng `shadcn`. `shadcn` này là một thư viện UI được build bằng Tailwind. Bên Vercel, nó có một component thiết kế cho phép import một giây vào `v0` để build, điều này khá thú vị. Em vẫn chưa có thời gian `playground` với nó, nhưng nhìn video demo thì thấy build game, build form, build 3D bằng Three.js khá thú vị.

<iframe width="560" height="315" src="https://www.youtube.com/embed/jcn5nn5GPS8?si=iHD3YYKBnkB7jlKb&amp;start=1707" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**30:48** Video đó khá ấn tượng, nên em quan tâm đến Vercel. Ok, tiếp theo là JavaScript. Đây là một vấn đề mà em thấy rất liên quan đến em, dù hiện tại nó chỉ đang ở giai đoạn đề xuất (`proposal`). Đó là việc xử lý ngày tháng (`date`) trong JavaScript. Chắc chắn ai làm front-end và phải xử lý ngày, đặc biệt là xử lý `time zone`, sẽ thấy vấn đề này rất phức tạp. Đề xuất này hứa hẹn sẽ giải quyết được vấn đề đó. Hi vọng không biết khi nào nó release, nhưng đây là một đề xuất đáng mong đợi.

**31:32** Một cái khác, em đang chia sẻ đúng màn hình không vậy? Anh có thấy màn hình không? Màn hình bên em vẫn hoạt động bình thường, nhưng màn hình bên anh có vẻ bị đứng nguyên một vị trí. Ok, em mới chia sẻ lại, có thấy chưa? Để em giảm độ phân giải xuống còn 700p. Ok, tiếp theo là về CSS. Cái này em nghĩ nó có từ lâu rồi, nhưng tháng trước em mới đọc được một bài viết về nó. Bài này em đã đưa vào báo cáo. Đó là một hướng dẫn tương tác (`interactive tutorial`) về cách sử dụng CSS Grid thay vì Flexbox. Khi đọc bài này, em nhớ tới một chuyện vui về CSS.

**32:35** Chuyện vui là về CSS3. Bây giờ, khi đi phỏng vấn tuyển dụng, họ vẫn đề cập đến HTML5 và CSS3, nhưng thật ra CSS3 đã ra mắt hơn chục năm rồi. Hiện tại, họ đang nói đến CSS4, có vẻ đã vài năm rồi. CSS5 hiện nay cũng đang trong quá trình phát triển với một số `proposal`. Nhưng không hiểu sao cộng đồng dev vẫn quen gọi là CSS3. Giống như với thằng `Grid`, nó cũng đã ra mắt từ lâu, nhưng không phải tất cả các trình duyệt (`browser`) đều hỗ trợ đầy đủ ngay từ đầu.

**33:17** CSS Grid đã ra mắt từ lâu và bây giờ gần như tất cả các trình duyệt đều hỗ trợ nó. Mọi người nên xem xét việc dừng sử dụng Flexbox và chuyển sang CSS Grid. Ok, tiếp theo là một chuyên mục khác – 'Mỗi Tuần Một Web'. Thằng `rb` vừa ra version 1.0, và như mọi khi, họ so sánh tốc độ nhanh hơn `WebP`. `WebP` vốn đã nhanh, nhưng giờ `rb` có vẻ còn nhanh hơn. Mọi người có thể xem xét thử `rb`.

**34:42** "Một cái khác là thằng `fity`, em tình cờ phát hiện ra. Nó cho phép build form bằng JSON, điều này thú vị vì nó khá khớp với suy nghĩ của em. Giống như dự án đầu tiên em làm với khách hàng Malaysia, kiểu như `chợ tốt` bên đó. `Muda` cũng sử dụng `buf` bằng JSON để đưa ra các `schema`, sau đó render ra form. Cảm giác rất thú vị.

**35:30** Còn một cái khác là thằng `i18n`, nó là một cộng đồng hướng đến việc `clean up`, `fit up`, và `level up`. Họ đi tìm những thư viện như `Lodash` để dọn dẹp và tối ưu chúng, tạo ra những phiên bản thay thế nhẹ hơn, sạch hơn. Cộng đồng này đã tạo ra khá nhiều thứ rồi. Em thấy mục tiêu của nhóm này rất hay. Nhưng thực ra, em chưa sử dụng các công cụ họ build ra."

**36:13** Ok, kết thúc với một bài ngắn về 'Top Programming Languages'. Đây có lẽ sẽ khiến mọi người hứng thú – top các ngôn ngữ lập trình trong năm 2024. Em sẽ xem qua. Ok, từ trên xuống dưới thì Python vẫn đứng đầu. Em không biết họ đánh giá kiểu gì, nhưng Python đứng đầu, rồi tới Java, rồi JavaScript. C++, TypeScript cũng nằm trong danh sách. Em không rõ họ thu thập dữ liệu kiểu gì, vì họ không nêu rõ, nhưng có vẻ như với các công việc lập trình, SQL, Python, Java, TypeScript vẫn ổn. Em nghĩ vậy.

**37:07** Đó là những gì em thu thập được từ tháng trước. Ok, bây giờ nói về `a scraper`. Ừ, `a scraper` thì khoảng 2-3 ngày nữa sẽ có một bài giữa tháng. Em sẽ cố gắng mỗi hai tuần ra một bài. Còn `a scraper` thì chắc là mỗi hai tuần một bài. Nếu kéo dài đến một tháng, cảm giác bị miss mất khá nhiều thông tin vì nhiều quá, nên có thể mỗi ngày sẽ phải làm một ít. Cả frontend và backend đều như vậy mà, đúng không? Ok rồi.

**38:11** Ủa, LP, cái bài kia em làm xong chưa? Cái gì dính tới Thới á, em làm xong cái đó chưa? Ừ, chưa hả? Anh cũng chưa wrap up nữa. Con bot thì đã crawl được rồi, nhưng cần chuyển thêm một cái server backend để làm Discord bot. Cái đó em chưa làm, nhưng con bot thì chạy được rồi."

**38:55** Trước khi Tôm tiếp quản, anh có một vài thông báo. Đầu tiên, tuần vừa rồi mình có triển khai một vài thông tin. Liên quan đến việc `adopt` EOM để tăng năng suất cho team, anh đã post lên một `initiative`. Nếu anh em có thể phát triển hoặc sử dụng `cilus` ở một mức độ nhất định, thì sẽ có reward ICY cho mọi người. Danh sách việc cần làm sẽ nằm trên `workland` của mình, nhìn sơ qua cũng dễ hiểu.

**39:44** Ví dụ như bài của TnT, đó là một bài liên quan đến `concept` này. Anh ấy đã làm một bài về việc học tiếng Tây Ban Nha. Mặc dù nó không liên quan lắm, nhưng anh ấy đã demo con bot đó cho mọi người xem. Anh kỳ vọng rằng mọi người sẽ làm quen với việc đặt câu hỏi cho AI theo dạng `system prompt`, sau đó thực hiện triển khai (`deployment`). Những bài của 4C đã làm xong hết rồi. Cách triển khai (`prompt`) như thế nào, anh em có thể coi và `run` chính xác như vậy.

**40:31** Còn những phần khác thì sẽ xem xét thêm. Phần của Pish tuần trước nằm ở đây, show nhanh qua nhé. Điều mà mọi người thấy là kết quả của quá trình làm cái `script` mà T đã làm. Toàn bộ quá trình `prompt` để tạo ra kết quả này kéo dài khoảng vài giây, bao gồm các thông tin cần thiết và sau đó `spore` ra một `system prompt`, đưa lên trên cái `defile` này để mọi người sử dụng. Bên đây là nơi để xài, con `defile` này có thể `trip` ra thành `API`, và nếu anh em muốn sử dụng, có thể gọi trực tiếp `API` như một `serverless function`. Gọi API và nó sẽ trả về kết quả, sau đó mình chỉ cần đưa vào trong Discord hoặc các giao diện khác.

**41:13** Ví dụ như bài này, nó sẽ ghép với cái ngữ cảnh (`context`) trong môi trường làm việc. Khi đưa ra một `topic`, nó sẽ sinh ra một dạng `syntax` để `insert`. Một bên là so sánh hai loại câu hoặc hai ngôn ngữ, và nó đưa ra hai hoặc ba phản hồi (`response`) có thể đến từ đồng nghiệp. Sau đó, mình có thể trả lời tiếp theo như thế nào. Đồng thời, nó cũng sẽ gợi ý một số kiến thức (`knowledge`) mà mình có thể `pick up` từ cuộc hội thoại.

**42:17** Rồi đây, mọi người đang thấy trên màn hình đó là phần `system prompt` và `output`. Trong cái bảng mà anh yêu cầu thì cần nhiều hơn một chút. Để theo dõi quá trình học hỏi của mọi người, sẽ cần `problock` thêm nữa. Nếu anh em không có `cilus`, không có `ChatGPT`, có thể request để dùng chung với team mình. Trên đây team đã load sẵn các key rồi, cứ lấy và xài thôi, không vấn đề gì."

**43:04** Ví dụ nhé, gần như toàn bộ góc nhìn của tụi anh ở giai đoạn hiện tại là ở mức cơ bản nhất, team mình cần hiểu cách sử dụng mấy công cụ AI này như một phần của công việc hằng ngày. Trước đây, khoảng hai năm, team mình đã sử dụng rồi nhưng cách đặt câu hỏi, cách khai thác thông tin từ các mô hình dữ liệu lớn (`large data models`) không hiệu quả lắm. Anh đã chia sẻ tài khoản `ChatGPT` với vài anh em trong team, và qua quan sát hiện tại, cách sử dụng vẫn chưa tối ưu.

**43:41** Đây chính là lý do để mình làm thêm bài tập này. Giai đoạn này cần mọi người làm thử, học cách build các `cot`, sau này mình sẽ có công cụ cần thiết giúp ích cho công việc. Mỗi `to-do` trên đây tương đương với góc nhìn của mình là nó sẽ trở thành một công cụ `cilus` cho cá nhân hoặc team để giúp tăng tốc độ làm việc. Từ việc viết `doc`, `breakdown` công việc, hỗ trợ viết `requirement ticket`, biết cách chọn ngay `chai` (`API`) ra sao từ các `context` đưa vào.

**44:32** Đó là điều đầu tiên mà anh em cần để ý. Nhắc lại cho tuần vừa rồi, team mình đã bàn tiếp về chuyện đi chơi. Hiện tại, Huy Nguyễn đang chuẩn bị được bao nhiêu phần trăm rồi? Huy Nguyễn, theo ước lượng của em, chuẩn bị tới đâu rồi?

**45:35** Tuyệt vời. Ok, phần đó hoàn thành. Chính sách hỗ trợ cho mọi người sẽ có thay đổi một chút. Vì hiện tại ngân sách có vẻ hơi lớn, đang tăng lên khoảng 500-600 trên đầu người, hơi nhiều so với tình hình hiện tại. Nên sẽ có một số điều kiện kèm theo. Có hai điều chính: một là những gì đã nói trong việc sử dụng mô hình ngôn ngữ lớn, mấy anh em sẽ cần phải vượt qua một bài test do team soạn ra.

**46:14** Thật ra, bây giờ mình thấy có sự chênh lệch lớn giữa các bạn đã biết sử dụng `tools` và những bạn chưa biết. Rõ ràng là có một sự khác biệt rất lớn. Nó không hoàn toàn là 100%, nhưng khoảng 60-70% thôi. Những bài toán lớn, phức tạp hơn thì khó, nhưng kỹ năng cần thiết thì mình vẫn thấy được. Vì thế, nếu bây giờ không học thì sau này sẽ rất khó để có thể cạnh tranh với những người khác trong team, những bạn đã thành thạo `tools` rồi.

**47:01** Vậy nên, đây là yêu cầu cần thiết. Có gì Tôm với Huy Nguyễn sẽ cùng đứng ra thiết kế bài test này nhé. Bắt đầu nghĩ về việc đó giúp anh. Vì với các vai trò khác nhau trong team, sẽ có những bài tập phù hợp, nhưng điều kiện chung là phải hiểu được cách mô hình ngôn ngữ lớn hoạt động như thế nào, không nhất thiết phải hiểu chi tiết về `dataset`, nhưng cần biết cách sử dụng các công cụ như thế nào, tự `setup` được và dùng nó để tăng tốc công việc.

**47:51** Việc này là việc số hai. Huy Nguyễn với Tom sẽ giúp đỡ để hoàn thành bài test này nhé. Mấy bạn vượt qua được bài test này thì sẽ thoải mái hơn, không bị áp lực khi làm việc nữa. Theo kế hoạch, mình dự tính tới tháng 12 phải xong đúng không? Còn khoảng 2-3 tháng để anh em ôn tập và bắt đầu làm. Đây sẽ là tiêu chuẩn mới cho team mình. 

**48:37** Chuyện thứ ba liên quan tới việc planning cho Team Building. Team mình cũng đã thảo luận tuần trước về việc quay lại văn phòng làm việc hybrid. Mình sẽ bắt đầu hỗ trợ mọi người lên văn phòng để tạo sự kết nối tốt hơn. Một số bạn đã lên văn phòng rồi. Tôm cũng đang hỗ trợ lên văn phòng để xem anh em nào muốn 'make up' công việc thì tới văn phòng nhé. Cái `AIClub` mà Tom đang lead, bây giờ đã được chuyển thành một channel trong team rồi, nhưng chỉ invite các bạn vào với một số điều kiện nhất định.

**49:22** Anh cảm giác rằng ai đã sẵn sàng học và đặt câu hỏi hợp lý liên quan thì sẽ được mời vào nhóm này thôi. Hiện tại, có một số bạn đang xem qua rồi. Chiều nay vừa tạo, bắt đầu chuyển dần dần. Việc này cũng liên quan tới chuyện thay đổi mật khẩu, lỡ có show trên stream rồi. Trong vòng tuần tới, kỳ vọng là mọi người sẽ dành thời gian lên văn phòng một đến hai ngày. Nếu thấy ở nhà không tập trung hoặc phải tương tác nhiều với gia đình, không sát được công việc, thì cứ lên văn phòng làm việc một đến hai ngày.

**50:08** Khi anh em `check-in`, Tôm và Vi nhỏ đã làm tính năng `check-in` ở văn phòng. Nếu các bạn kết nối với Wi-Fi ở văn phòng, hệ thống sẽ nhận diện và gửi thông báo `bot` vào `channel` lobby. Cái này hơi spam một xíu nhưng sẽ được tinh chỉnh lại. Sau đó, team sẽ hỗ trợ tiền gửi xe và có thêm phần thưởng `IC`, khoảng 5 IC, kèm theo chuyện ăn trưa này nọ, team sẽ `subsidize` luôn. Đó là ba thông báo lớn nhất trong tuần qua, liên quan đến `benefit` của mọi người. Anh em để ý nhé.

**51:10** Rồi, giờ chắc nhường lại sân khấu cho Thành để tiếp tục với chủ đề nhé. Chủ đề của bạn Hiếu tuần trước chắc để tuần sau hẹn Hiếu vậy. Tuần trước Hiếu có chủ đề về `database reference` và vấn đề `circular reference`. Ok, để em làm luôn nhé, quất luôn. Hôm nay sẽ hơi chia sẻ về AI Comment mà mình đã làm cho team. Thực tế, AI Comment mình cũng dùng phương pháp giống như làm cho `Prompt` hoặc `Completion`, chỉ khác là mình sẽ làm thế nào để có `input` và `output` cụ thể.

**51:58** Nó sẽ trở thành một `chatbot` đơn giản thôi. Trong con bot này, nó sẽ copy lại những thứ từ trước, như `output` từ `sunbot`. Nó sẽ lấy `base case` từ `sunbot` luôn. Các `switch case` liên quan đến câu hỏi về `Memo`, ví dụ như mình hỏi 'What are the latest notes?', thì nó sẽ dựa trên các câu lệnh đã được `instruct` sẵn để tìm kiếm và trả lời. Hoặc nó có thể `query` phía dưới cho team mình. Không có gì phức tạp, cứ xem như ba cái `output` cơ bản, mỗi cái sẽ cung cấp các kết quả cần thiết.

**52:44** Giới thiệu là vậy, giải pháp cho những ai sợ đặt câu hỏi ngu và bị trừ lương thì đây là câu trả lời – một `auto-solution`. Cái này sẽ tự động hết cho mọi người. Mình làm một `agent` để tự động hóa quá trình này. Đây cũng là phương pháp mà OpenAI đã sử dụng, gọi là `mixture of agents`. Mỗi `agent` sẽ tự nói chuyện với chính nó để hiểu rõ hơn nhu cầu của mình, sau đó đưa ra các kết quả mà mình mong muốn. Đối với mỗi câu hỏi, nếu không có `input`, cứ để AI suy luận hết. Không cần phải `prompt` phức tạp.

**53:27** Nếu không có `output`, để AI tự suy luận. Mục tiêu của `output` là gì? Để AI tự suy nghĩ, xem cần những thông tin gì liên quan, có thể về công nghệ, y tế, hoặc bất kỳ lĩnh vực nào khác. AI sẽ tự hiểu, không cần phải đặt `prompt` quá phức tạp. Có một số mẫu mình sẽ thử cho mọi người dễ hình dung. Ví dụ: 'How to learn Chinese'. Dù mình nhập câu này vào ChatGPT hoặc Club, đôi khi nó sẽ đưa ra câu trả lời đúng, đôi khi thì không, vì nó không hiểu hết ý của mình.

**54:04** Nếu mình nói là mình muốn học tiếng Trung để liên quan đến thi đấu hoặc những thứ đặc biệt như HSK, thì `OpenAI` có thể đưa ra câu trả lời chính xác hơn, chuyên sâu hơn. Đúng là mình có thể copy dễ dàng, nhưng quá trình này có thể gồm một đến ba bước để AI tự suy luận (`reason`). Nó sẽ suy đoán từ những gì người dùng dự định (`intent`). Cái này có thể copy qua `mixture of agents` để sử dụng hiệu quả hơn.

**54:45** Mixture agent này sẽ hoạt động luôn. Mình có một cái LCK sẵn rồi nhé. Ok, một cái mới là `how to learn Chinese`. Đợi chút, để giải thích lại một chút cho mấy anh em đang chưa hiểu rõ. Đây là bài toán trong tuần vừa rồi mà tụi mình gặp. Việc đặt câu hỏi cho AI sẽ quyết định đến việc mình nhận được phản hồi (`response`) gì và tốc độ tiếp thu kiến thức mới của mình sẽ như thế nào. Đó là bài toán tụi mình gặp phải. Đề bài là như thế này: khi có một chủ đề mới, mình sẽ phải tiếp cận và tìm hiểu nó.

**55:30** Trước đây, mọi người thường sẽ lên Google để tìm kiếm thông tin, rồi tổng hợp lại, sau đó ghi nhận vào tài liệu của mình. Nhưng trong khoảng hai năm trở lại đây, cách làm đó đã thay đổi. Mọi người không còn tìm kiếm kiến thức qua Google nữa mà chuyển qua hỏi các mô hình ngôn ngữ lớn (`EOM`). Tuy nhiên, việc tìm kiếm thông tin đơn giản qua EOM có thể không đưa ra câu trả lời chất lượng cao, và sẽ rất lâu để mình có thể hiểu được các kiến thức cốt lõi của một chủ đề mới.

**55:59** Ví dụ như việc tập Dream thì sẽ có những thứ như các chỉ số (`metrics`) đo sự thay đổi của cơ thể. Hay ví dụ như học Chà ni (Chinese), sẽ có một số kiến thức chính mà mình cần biết. Vậy làm sao để từ không biết gì (`zero knowledge`) mình có thể học hết những thứ đó? Đây chính là quá trình mà con O1 của ChatGPT đã giới thiệu ngày hôm qua. Tom đã trải qua quá trình suy nghĩ và thực hiện phần này, và hôm nay Tom sẽ demo lại cách mà quá trình này hoạt động, cùng với việc Tom đã triển khai nó cho team mình luôn. Team có thể sử dụng hiệu quả hơn.

**56:36** Dạ, đúng rồi. Ok, để chia sẻ luôn phần `How to learn Chinese`. Đối với mình, khi tìm kiếm, mình đang muốn tìm các `keyword` liên quan đến thi đấu hoặc các `keyword` đặc biệt, như cách viết ký tự (`radical`) hoặc thứ tự sắp xếp (`stroke order`). Mixture agent này sẽ suy ra tất cả những điều đó. Nó hiểu rằng mình muốn tìm hiểu về điều gì và cần gì. Nó sẽ trả lời đầy đủ, có thể hơi thừa, nhưng thừa còn hơn là thiếu. Có cả code luôn, dễ hiểu mà.

**57:18** Ưu điểm của phương pháp này là mình có thể đi sâu hơn nữa, ví dụ như HSK6 chẳng hạn. Không biết HSK6 là gì và muốn đạt điểm bao nhiêu? Nó sẽ suy ra tất cả từ lịch sử cuộc hội thoại của mình. Nếu mình muốn học tiếng Trung để thi HSK6, nó sẽ giải thích và đưa ra cả một kế hoạch (`regimen`) học cho mình luôn. Đây là một phương pháp rất tốt nếu như mình không rành về việc viết prompt và không muốn bị trừ lương vì viết prompt sai.

**58:11** Mixture agent này sâu và có thể hơi thừa, nhưng nó cho phép mình chính xác hơn. Khi Together AI thiết kế `inference engine`, họ nhận thấy rằng `response` của các mô hình ngôn ngữ lớn (`LLM`) rất nhanh. Nên họ đã nghĩ tại sao không cho nhiều mô hình ngôn ngữ chạy cùng một lúc và sau đó đồng bộ thông tin lại cho AI đưa ra câu trả lời chính xác hơn?

**58:55** Thực ra, bên Together AI và một đội ngũ khác chỉ dùng mô hình Lama thôi mà họ cũng đánh bại được GPT-4. Điều kiện là mình phải cung cấp đủ thông tin cho AI để nó suy luận. Nó cần biết `input`, `output`, toán học, hóa học, hoặc bất kỳ lĩnh vực nào. Mình sẽ nhập tất cả những điều đó vào đây. Thiết kế của mixture agent khá đơn giản. Nó sẽ có một `system prompt` liên quan đến `reasoning` để AI suy luận những thứ liên quan đến toán, hóa học, và nó sẽ kéo những từ khóa (`keyword`) quan trọng ra để trả lời.

**59:37** Ví dụ, nếu muốn học tiếng Trung, `input` của mình là tiếng Anh vì mình trả lời bằng tiếng Anh. `Output` là phương pháp học tiếng Trung, sau đó có một `aggregator` sẽ sắp xếp lại toàn bộ thông tin này. Nó sẽ đưa ra một câu trả lời rất thông minh. Phần nặng nhất là ở đoạn này, nhưng mình có thể thêm một `layer` nữa, một tầng khác cho `conclusion`, hoặc cho `adapt`, hoặc thêm một tầng cho các thông tin kỹ thuật (`technical context`). Nó sẽ lấy `context` từ ba tầng đó. Nếu muốn biết từ đầu đến cuối nó hoạt động như thế nào, thì mình có thể vận hành theo ví dụ như học tiếng Tây Ban Nha chẳng hạn.

<iframe width="560" height="315" src="https://www.youtube.com/embed/jcn5nn5GPS8?si=Z93MIuCm63-wq-jm&amp;start=3215" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**1:00:10** Em lấy chủ đề là về RP trading đi. What is to learn? Ok, trong team mình có người có hiểu biết để kiểm tra xem câu trả lời có đúng không. Hoặc mình có thể chọn chủ đề liên quan đến RP trading, ví dụ What is to learn?. Trong team mình sẽ có người có hiểu biết để xem thử câu trả lời có đúng không. Ok, ai thử xem nào.

Mixture agent này sẽ hoạt động luôn. Mình có một cái LCK đấy luôn. Ok, một cái mới đó là how to learn Chinese. Đợi một chút, cái bài này để giải thích lại cho mấy anh em đang hiểu một xíu nhé. Đây là bài toán trong tuần vừa rồi khi anh em ngồi với nhau. Việc đặt câu hỏi cho AI sẽ quyết định đến việc mình nhận được phản hồi như thế nào và sau đó là tốc độ hấp thụ kiến thức mới của mình sẽ ra sao. Đó là bài toán mà trong tuần vừa rồi tụi mình gặp.

**1:00:45** Khi gặp một chủ đề mới, trước đây mọi người thường dùng Google Search để tìm kiếm thông tin. Sau đó, mình sẽ tổng hợp lại và ghi chép vào tài liệu. Nhưng trong hai năm gần đây, mình không làm vậy nữa. Thay vì dùng Google để tìm kiếm kiến thức, bây giờ mọi người đặt câu hỏi trực tiếp cho các mô hình ngôn ngữ lớn. Tuy nhiên, khi chỉ đơn giản hỏi AI thì kết quả trả về không luôn đúng chất lượng, và đôi khi rất lâu mình mới hiểu được những điểm quan trọng nhất của một chủ đề mới.

**1:01:18** Dụ như về tập Dream, nó sẽ có những chỉ số để đo lường sự thay đổi của cơ thể. Hay như học Tiếng Trung, sẽ có một số khái niệm quan trọng mà mình phải biết. Vậy làm thế nào để mình từ con số 0 có thể nắm bắt được hết những khái niệm đó? Toàn bộ quá trình này là thứ mà tối qua con o1 của ChatGPT đã giới thiệu cho mình.

**1:01:48** Tom đã trải qua cả quá trình đó và sẽ demo lại cho các anh em về cách thực hiện nó. Tôm cũng đã triển khai để team mình có thể sử dụng hiệu quả hơn.

**1:02:43** Có vẻ là có nhiều từ khóa hơn khi đi hỏi từ từ. Với một người không biết gì hết thì nó sẽ không đưa ra nhiều từ khóa như vậy, không nhắc đến mấy cái de, C, hay những thứ tương tự. Chắc phải thử xem CL nó sẽ như thế nào chứ không phải là o1. Em có review không? Để em tạo cái thử. Chắc phải đợi API, nó không có stream. Có lẽ do họ dùng mix agent nên hơi khó để chạy, chỉ có thể tạm chạy trên KP thôi. Hiểu bên kia, nó có diễn giải ở giữa.

**1:03:48** Đúng rồi, thử mở rộng xem mấy cái clip sáng nay, thấy review rồi. Nhìn cũng hợp lý nhỉ, y chang vậy. o1 ở nhà cũng rẻ hơn đấy, o1 ở nhà rồi. Đây là một cái demo về việc có một cái coin giúp quá trình khám phá kiến thức nhanh hơn. Thử hỏi về chuyện tập tay, "tập taichi?", xem nó trả lời như thế nào.

**1:04:51** Em gợi ý đủ các kỹ thuật cần thiết không? Có gì không nghe rõ à? Tập CIC trên Discord à? CIC là gì? How to CIC? Ok, thông minh phết nhỉ, nó đưa ra hết mấy cái động tác luôn. Ok, để thử CGR nữa. Wow, nó biết đấy, nó biết đấy. Ừ, ok. Piano thì sao? Đúng rồi, hồi chiều mới hỏi về piano. Thử thử đi.

**1:05:56** Ok, chơi học piano, học viên? Đúng rồi, học viên. Đội mình có ai học nhạc không để kiểm chứng xem. Em thấy số lượng từ khóa về piano nhiều hơn bình thường, dễ để khám phá thêm. Ok, chắc cũng được. Nếu xem history về piano thì sao? Chắc họ cũng bao gồm reg, jazz và những thứ tương tự thôi.

**1:07:01** Ok, nhìn có vẻ ổn. Đúng là có Suzuki Method và những thứ tương tự. Dễ quá! Ông o1 ở nhà xịn đấy. Học piano thì không chỉ có kiến thức mà còn cần thực hành nữa. Phải có thực hành. Thực hành thì tự đi luyện, không thể chỉ ngồi tập trên giấy được. Đang tự luyện, đang học cái gì rồi.

**1:08:05** Ok, chắc là xong một bài. Còn bài nào nữa đáng để VPF không? Cái HC thì đừng bàn nữa, cái prompt em làm cho mixture of agent này đều dùng AI để tạo, không cần viết tay. Đây là quy trình của em: lấy bài đã viết và chuyển thành mixture agent với bốn system prompts: một cái cho reasoning, một cái cho phân biệt input, một cái cho phân biệt output, và cuối cùng là tổng kết.

**1:09:10** Quá trình build là như vậy. Sau đó mình chỉnh sửa từng cái note. Nếu muốn thêm note, chỉ cần thêm system prompt. Nếu muốn chỉnh sửa system prompt, chỉ cần thêm vào. Thực ra, có một system prompt riêng để xử lý câu hỏi logic và tư duy phản biện, nên cũng có một cái riêng cho cái này luôn.

**1:09:55** Cái này chắc để sau, o1 thông minh quá đôi khi người ta không tin. Nếu vậy, bài tiếp theo có thể là làm thế nào để demo một workflow mà mọi người không cần phải code nữa. Mới làm xong cái Office Checking cho team, thực sự không có gì khó cả. Cái này dễ, chỉ cần setup khoảng 10 phút.

**1:10:45** Giờ thì mình cần làm một cái feature, và ngồi trong cái team đó để thực hiện. Cả hai đều là backend, không phải driver, chỉ để AI nó chạy thôi. Có thể dễ dàng setup trong 10 phút không? Ok, thử xem, nhưng cần hơn 10 phút để hoàn thành.

**1:11:49** Để xem, em sẽ lên kế hoạch. Buổi sau, chọn một dự án thật, ví dụ submit một bài báo cáo cho bên for. Lần trước không đủ thời gian để làm, lần này sẽ muốn hands-on hơn. Hãy chọn một dự án khác, coding hiện tại vẫn phải làm bằng tay nhiều, cần tự chỉnh sửa convention.

**1:13:36** Ý là, tự hiểu feature của repo, rồi viết một đoạn code để thực hiện luôn. Giống như làm open source vậy. Sau đó, đi sâu hơn về chiến thuật. Sẽ setup thêm một bản check-in, và cho phép mọi người demo luôn.

**1:14:57** Chọn Go, lấy một cái thư viện, sau đó copy context, để AI tự hiểu cách sử dụng. Khi AI đã hiểu hết, nó sẽ tạo context và giúp tự động document. Sau đó, AI sẽ hiểu function và message, chỉ cần đưa vào input/output.

**1:15:56** Ok, hẹn tuần sau nhé. Mình sẽ chọn một dự án, để team ngồi lại với nhau. Ai cũng sẽ cần làm một script hoặc docker để chạy lên được. Nghệ nhân chọn dự án mà mình chưa biết để thử nghiệm từ đầu. Workflows sẽ cho phép mọi người so sánh cách làm việc với AI.

**1:17:15** Ok, tạm thời là vậy. Hẹn gặp lại mọi người vào thứ tư tuần sau nhé. Mình sẽ hoàn thành các bước còn lại và chuẩn bị cho bài test.

**1:18:05** Hy vọng tháng sau, tất cả anh em sẽ thành thạo các kỹ thuật này. Chúng ta sẽ tăng hiệu suất công việc. Có ai có câu hỏi gì không?

**1:19:44** Ok, vậy nhé, test lại cái workflow. Nếu không còn gì thì hẹn gặp mọi người vào tuần sau nhé. Chúc cuối tuần vui vẻ!

**1:20:46** Đội Phúc hỏi về một bài báo cáo bên team, có thể sắp xếp buổi giao lưu giữa hai team để học hỏi kinh nghiệm về open source và data sản phẩm. Hy vọng buổi OGIF tiếp theo sẽ hiệu quả hơn.

**1:21:29** Hy vọng từ đây đến khi đó, mọi người sẽ nắm được toàn bộ quy trình và không còn phải làm mọi thứ thủ công nữa. Nếu không còn gì nữa thì happy weekend. Chào mừng thêm một thành viên mới lên chức nhé! Chúc mừng nhé.

---

**English Transcript**

**07:25** Can you hear me, Thành? Can you hear me? Ah, I can hear you now. Ok, ok. I received feedback from Discord. Please wait a bit longer.

**10:28** Did we review some figures today?

**11:39** Or should we start right away? Ok, sure. Let’s begin with two reports: first, the financial report for August, and then I’ll present Go Lang Weekly. After that, we have an article related to Go’s “stamina,” right? Let’s move quickly so we can summarize later. I’ve edited the article a bit—it was too lengthy and wordy, so I’ve revised and checked it again.

**12:46** Last week, the core team sent out a survey to everyone. If anyone has feedback about using Go, any challenges, frustrations, or suggestions, feel free to send them through the link attached here. The second article is on the same trend, published on Golang’s blog. This article provides guidance on building a power app. Google has a guide on building an app using Gin only, nothing too special. This is their code, like their server-side run code. We have the full link so everyone can check the detailed code. I think it's pretty usable.

**13:28** Additionally, Go has introduced ZenKit, which is almost identical to Langchain but from Google. It was launched in mid-July. You can take a look. For example, there are vector store interfaces that we can use, like adding documents or similarity search.

**14:22** The next article may interest those into Erlang or Langchain. This framework just released a new version and almost has all the features. Alan is working hard to map it over, and it's almost done. They claim it’s ready for production. Here’s how it runs. I checked the issue list, and there’s nothing complicated. Most of the features are ready. I predict this framework will grow strongly.

**15:22** That’s about it. Do you have any questions? Oh, last time, we worked on an enterprise article, right? Let’s quickly go over it since we won’t have much time for that. Thắng helped me with this article, didn’t you, Thắng?

**16:23** Thắng shared and helped me write this part. There were a few previous articles where I introduced how Go has matured. It's ready for large enterprises to adopt, but it hasn’t fully replaced other languages yet. Some large enterprises still use Java. Switching fully to Go might be too costly. But for new enterprises or those looking to transition, Go is a suitable choice.

**17:26** This article addresses questions like what defines an enterprise standard language, why Go should be used in the enterprise, and which big companies are using Go. These are the follow-up articles, for example, why large enterprises choose Go.

**18:17** Ok, let me summarize the content. Java was developed during the Sun Microsystems era, known for the “write once, run anywhere” philosophy. It’s stable and has full feature support. When enterprises choose a programming language, they typically consider stability and features. Java Enterprise, previously called Java EE, now Jakarta EE, supports synchronous and asynchronous messaging, and formats like XML, JSON, and Protocol Buffers.

**19:11** Moreover, enterprises usually compare Java to C++ because C++ is more complex, requiring manual memory management. Meanwhile, Java has a garbage collector that handles memory management, so users can focus solely on implementation. Furthermore, Java has a large ecosystem, with nearly complete support for all libraries and frameworks.

**20:15** So, what’s the advantage of Java Enterprise compared to C++? At that time, C++ was still popular, but C was getting old—about 20-40 years old. Many older enterprises used COBOL, then switched to C++, while some opted for Microsoft’s C#. But the programming community found that C++ reached a more stable phase.

**21:02** C# is like Microsoft’s own ecosystem. Meanwhile, C++ was more widely embraced by the enterprise programming community. Not everyone used it, but when it comes to enterprise programming languages, Java and C++ were mentioned the most.

**22:14** The next question is why Go is the choice for enterprises and which companies are using Go. The key thing is, when working on this article, I think we should aim to clearly define why Java won, right? Java won against C# and C++. Right now, we need to find a reason to convince someone using Java to switch to Go. There must be a specific reason. In the articles you’re working on, focus on that point—find a reason.

**23:13** The reason might be that Go has solved all of Java’s problems. Maybe Go is better than Java in some ways, or for some reason, now is the time to switch to Go. Maybe add a case study for that. Yes, that’s probably the goal. If you continue working on this, consider structuring each article as a rough question and answer each one with a convincing reason. Then, you can turn it into a slide presentation. Like the first article, try posting it to the Golang community next week and see how it goes.

**24:05** Let’s see what the feedback is. Ok, let’s move on. Quickly go over Thắng’s status. Last month, Thắng had it rough. Have you seen Thắng? Maybe he needs to restart his machine, probably been on Windows for too long.

**25:26** His computer froze. Discord on Windows tends to lag more than on Mac, right? Mac is much smoother. Ok, I can hear you now. Ok, clear now. Let’s continue.

**26:31** This month’s report is similar to last month. Some articles aren’t new, but I’ve collected what I found relevant. Let me quickly go over it. I have everything ready, so let’s finish this. First up, React 19 AC. It was released back in April, but last month was when the full report came out. Basically, it still focuses on supporting server components and improving asynchronous script management. This is just a friendly reminder for those who haven’t read it yet to take a look.

**27:17** Personally, I find React getting more complex, so I’m going to avoid version 19 for now. It’s like React has some new hooks, but it feels like we could have achieved the same with the existing hooks. But they’ve wrapped them up and created new utility hooks. I think it’s fine, but the problem is that a platform like React is becoming more and more complex, and I feel like it’s losing its original simplicity. Initially, it was just a simple building tool, but now they’re adding things that feel a bit unnecessary.

**27:55** Next up, Next 15. My thoughts on this are similar. Next 15 AC also supports React 19 AC with some improvements. What I found interesting is the React compiler. It optimizes React code. You can skip using hooks like useMemo and useCallback, which nearly 90% of React users need to use. Now, with this new feature, you don’t need those hooks anymore.

**28:39** This is cool, but the problem is other things, especially the app router of Next.js. I talked to Thành about it, and he seems fed up with Next.js too. I read through the comments, and the community seems confused. Every week, there’s someone asking whether it’s necessary. Their current stack is still fine, but both React and Next.js are getting more complicated. It’s like when OpenAI switched from Next.js to Remix. It feels like the market is shifting.

**29:17** It’s similar to how OpenAI switched from Next.js to Remix. The community’s sentiment is shifting toward more efficient solutions. Next and Nest are still okay, but personally, I find them getting more complex, especially the app router. Since Next.js 10, 12, 13, I haven’t used it much. Even though it’s the main stack, it doesn’t seem to be the main stack anymore.

**29:56** Speaking of the main stack of Next.js, it’s still the main stack, something like that. Related a bit to Vercel, the video is quite good. It demos the power of Vercel combined with shadcn. Shadcn is a UI library built with Tailwind. Vercel has a design component that allows you to import it into v0 to build, which is interesting. I haven’t had the chance to play around with it yet, but from the video demo, building games, forms, and 3D with Three.js looks interesting.

**30:48** That video is impressive, so I’m interested in Vercel. Ok, next up is JavaScript. This is an issue I find very relevant, even though it’s still just a proposal. It’s about handling dates in JavaScript. Anyone doing front-end work and dealing with dates, especially time zones, knows this is a complicated problem. This proposal promises to fix that. Hopefully, it will be released soon. It’s something to look forward to.

**31:32** Another thing—am I sharing the right screen? Can you see my screen? My screen is working fine, but on your side, it seems stuck in one position. Ok, I’ve re-shared it. Can you see now? Let me lower the resolution to 700p. Ok, next up is CSS. This has been around for a while, but I read an article about it last month. I included it in the report. It’s an interactive tutorial about using CSS Grid instead of Flexbox. When I read this, it reminded me of something funny about CSS.

**32:35** The funny thing is about CSS3. Now, when you go for job interviews, they still mention HTML5 and CSS3, but CSS3 was released over a decade ago. They’re now talking about CSS4, which has been in development for a few years. CSS5 is currently in progress with some proposals. But for some reason, the dev community still refers to CSS3. It’s like with Grid, which was released long ago, but not all browsers supported it fully at first.

**33:17** CSS Grid has been out for a while, and now almost all browsers fully support it. People should consider moving away from Flexbox and switching to CSS Grid. Ok, next up is another section—'A Web a Week.' rb just released version 1.0, and as always, they compare its speed with WebP. WebP is already fast, but now rb seems even faster. Everyone can check out rb.

**34:42** Another one is fity, which I discovered by accident. It lets you build forms using JSON, which is interesting because it aligns with my thinking. It’s like the first project I did with a Malaysian client, something like their ‘chợ tốt’ there. Muda also uses buf with JSON to provide schema, which then renders the form. It’s a really interesting approach.

**35:30** Another one is i18n, which is a community focused on clean up, fit up, and level up. They go around finding libraries like Lodash to clean them up and optimize them, creating lighter, cleaner alternatives. This community has built quite a few things already. I think the group’s goal is really cool, but I haven’t actually used the tools they’ve built yet.

**36:13** Ok, let’s wrap up with a short article on 'Top Programming Languages.' This might interest people—the top programming languages of 2024. I’ll take a look. Ok, from top to bottom, Python is still number one. I don’t know how they rank it, but Python is at the top, followed by Java, and then JavaScript. C++, TypeScript are also on the list. I’m not sure how they’re collecting data since they didn’t explain, but for dev jobs, SQL, Python, Java, and TypeScript seem to be doing fine. That’s what I think.

**37:07** That’s everything I’ve gathered from last month. Ok, now talking about a scraper. Yes, a scraper will have a mid-month post in 2-3 days. I’ll try to do one post every two weeks. If I stretch it out to a month, I feel like I’ll miss out on a lot of information since there’s too much, so maybe I’ll just work on a little bit every day. Both frontend and backend are like that, right? Ok.

**38:11** Hey, LP, did you finish that article yet? The one related to Thới, have you finished that one? Oh, not yet? I haven’t wrapped up either. The bot has been able to crawl, but I still need to add a backend server for the Discord bot. I haven’t done that yet, but the bot is already running.

**38:55** Before Tom takes over, I have a few announcements. First, last week we rolled out some updates. Related to adopting EOM to improve team productivity, I posted an initiative. If team members can develop or use cilus to a certain level, there will be ICY rewards for everyone. The task list will be on our workland, and it’s fairly easy to understand.

**39:44** For example, TnT’s post, it’s an article related to this concept. He wrote an article on learning Spanish. It’s not directly related, but he demoed the bot for everyone last time. I expect that everyone will get used to asking AI using system prompts, then deploying. Most of 4C’s articles have been completed. How to prompt and execute is something everyone can review and run exactly like that.

**40:31** As for the other parts, we’ll see what else needs to be done. Pish’s work from last week is here, let me show you quickly. What you’re seeing is the result of the process of creating the script that T did. The whole prompt process to get this result took just a few seconds, including all the necessary information, and then spored into a system prompt, which was uploaded to the defile for everyone to use. Over here is where you can use it. This defile can be tripped into an API, and if you want to use it, you can call the API like a serverless function. Call the API, and it will return the result. Then, you just need to input it into Discord or other interfaces.

**41:13** For example, this post, it will link to the context in the working environment. When you input a topic, it will generate a syntax to insert. One side compares two types of sentences or languages and provides two or three possible responses from colleagues. After that, you can decide how to respond. It also suggests some knowledge that you can pick up from the conversation.

**42:17** Right now, you’re seeing on the screen the system prompt and the output. In the table I requested, I need a bit more detail. To track everyone's learning process, I’ll need a problock. If you don’t have cilus or ChatGPT, you can request to use them with our team. We’ve already loaded some keys, so just take and use them, no problem.

**43:04** For example, nearly the entire perspective we have right now is at the most basic level. Our team needs to understand how to use these AI tools as part of their daily work. About two years ago, our team already started using them, but the way of asking questions and extracting information from large data models wasn’t very effective. I shared my ChatGPT account with a few members of the team, and from my observation, the way it's being used isn’t optimized yet.

**43:41** This is the reason we’re doing this exercise. At this stage, everyone needs to try and learn to build cot so that later we will have the necessary tools to assist our work. Each to-do on here corresponds to our perspective—it will become a cilus tool for individuals or the team to increase work speed. From writing docs to breaking down tasks to supporting writing requirement tickets, to knowing how to choose chai (API) from the context provided.

**44:32** That’s the first thing everyone should pay attention to. A reminder from last week, we also talked about team outings. Right now, Huy Nguyễn is preparing. Huy Nguyễn, how far along are you, according to your estimate?

**45:35** Awesome. Ok, that part is done. The support policy for everyone will have some adjustments. Right now, the budget seems a bit big—it’s rising to around 500-600 per person, which is a lot compared to the current situation. So there will be some conditions attached. Two main things: first is what we mentioned about using large language models, and team members will need to pass a test created by the team.

**46:14** Actually, now I’m seeing a big difference between those who know how to use tools and those who don’t. It’s a very noticeable gap. It’s not completely 100%, but around 60-70%. For more complex problems, it’s hard, but we can still see the necessary skills. So, if we don’t learn now, it will be tough later to compete with others in the team, especially those who have already mastered the tools.

**47:01** So, this is a required step. Tom and Huy Nguyễn will design the test. Start thinking about that for me. Since there are different roles in the team, there will be appropriate tasks, but the common requirement is to understand how large language models work. It’s not necessary to know all the details of the dataset, but we need to know how to use the tools, set them up, and use them to speed up our work.

**47:51** That’s task number two. Huy Nguyễn and Tom will help design the test. Once you pass it, you’ll be more comfortable, not feeling stressed at work anymore. According to the plan, we’re aiming to finish by December, right? There are about 2-3 months left for everyone to study and get ready. This will be the new standard for our team.

**48:37** The third issue relates to planning for team building. Last week, we discussed getting back to the office and hybrid work. We will begin supporting people to come back to the office to build better connections. Some have already started going back. Tom is also supporting the return to the office, so those who want to ‘make up’ their work can come to the office. The AI Club that Tom is leading has now been turned into a channel in the team, but invites are only sent under certain conditions.

**49:22** I feel that whoever is ready to learn and ask reasonable questions will be invited to this group. A few people are already looking into it. It was just created this afternoon, so we’ll gradually transition people in. This is also related to the need to change passwords since they’ve been exposed on the stream. Over the next week, the expectation is that people will spend 1-2 days at the office. If staying at home feels too distracting or you need to interact with family too much and it’s hard to focus on work, just come to the office 1-2 days a week.

**50:08** When people check in, Tom and Vi have set up the check-in feature at the office. If you connect to the office Wi-Fi, the system will recognize it and send a bot notification to the lobby channel. It’s a bit spammy now, but it will be fine-tuned. After that, the team will support parking fees and provide a bonus of around 5 IC along with lunch subsidies. These are the three main announcements for the past week regarding everyone’s benefits. Pay attention to that.

**51:10** Now, I’ll hand the stage over to Thành to continue with the topic. Hiếu’s topic from last week can be postponed to next week. Hiếu had a topic on database references and circular references last week. Ok, I’ll do it now. Let’s go. Today, I’ll share about the AI Comment we created for the team. Actually, AI Comment uses the same method as building a prompt or completion—it’s just about how to get specific input and output.

**51:58** It will become a simple chatbot. In this bot, it will copy the things from before, like the output from sunbot. It will take the base case from sunbot. The switch cases related to Memo questions, for example, if you ask ‘What are the latest notes?’, it will switch to the instructed commands to find and reply. Or it can query below for our team. Nothing complicated, just think of three basic outputs, each providing the necessary results.

**52:44** That’s the introduction. For those worried about asking dumb questions and getting penalized, this is the solution—an auto-solution. This will automate everything for you. We create an agent to automate this process. This is also the method OpenAI uses, called mixture of agents. Each agent will talk to itself to better understand what you need, and then give you the desired results. For each question, if there’s no input, just let the AI infer everything. No need for complex prompts.

**53:27** If there’s no output, let the AI infer that too. What’s the purpose of the output? Let the AI figure it out. See if it needs technical, medical, or any other related information. AI will know on its own, no need for a complex prompt. There are some templates I’ll try out for everyone to visualize. For example: ‘How to learn Chinese.’ Even if I input this into ChatGPT or Club, sometimes it gives the right answer, sometimes not, because it doesn’t fully understand what I mean.

**54:04** If I say I want to learn Chinese for competition or something specific like HSK, OpenAI can give a more accurate and detailed response. Yes, I can easily copy that, but the process might take 1-3 steps for AI to reason it out. It will infer from what the user is trying to do. This can be copied to a mixture of agents for more effective use.

**54:45** Mixture agent will run immediately. We’ve already set up an LCK for that. Ok, something new—‘how to learn Chinese.’ Wait a minute, let me explain a bit for those who are still confused. This is the problem we faced last week when we were sitting together. Asking questions to AI will determine what kind of response we get and how quickly we absorb new knowledge. That’s the problem we faced. The task is this: when there’s a new topic, we have to approach and learn it.

**55:30** Before, people used to Google search for information, then compile it and record it into their documents. But in the last two years, that method has changed. People no longer search for knowledge through Google but instead ask large language models (EOM). However, simply asking an EOM might not yield high-quality answers, and it can take a long time to understand the core knowledge of a new topic.

**55:59** For example, Dream training has metrics to measure body changes. Or, for example, learning Chinese, there are key pieces of knowledge you need to know. How do you go from zero knowledge to learning all that? This is the process that ChatGPT’s O1 introduced yesterday. Tom has gone through this process of thinking and implementation, and today, Tom will demo how it works and show how Tom has deployed it for our team. The team can use it more effectively.

**56:36** Yes, that’s right. Ok, let’s move on to ‘How to learn Chinese.’ For me, when searching, I want to find keywords related to competition or specific keywords like radical or stroke order. Mixture agent will infer all of that. It knows what I want to learn and what I need. It will provide a full response—it might give too much information, but better too much than too little. There’s even code. It’s easy to understand.

**57:18** The advantage of this method is that I can go even deeper, like with HSK6. Don’t know what HSK6 is or how to get a certain score? It will infer everything from the conversation history. If I want to learn Chinese to take HSK6, it will explain it all and even give me a study regimen. This is a great method if you’re not familiar with writing prompts and don’t want to be penalized for writing poor prompts.

**58:11** Mixture agent is deep and may provide extra information, but it helps you be more precise. When Together AI designed the inference engine, they noticed that responses from large language models (LLMs) are really fast. So, they thought, why not run multiple LLMs simultaneously and then synchronize the information for AI to give a more accurate answer?

**58:55** Actually, Together AI and another team only used the Lama model, and they beat GPT-4. The condition is that you need to provide enough information for AI to infer. It needs to know the input, the output, the math, chemistry, or whatever field. You’ll enter all of that here. The design of mixture agents is quite simple. It has a system prompt related to reasoning to help AI infer things related to math and chemistry. It will pull out important keywords to answer.

**59:37** For example, if you want to learn Chinese, your input is in English because you responded in English. The output is the method to learn Chinese. Then, an aggregator will organize all this information and provide a very intelligent response. The heaviest part is here, but you can add another layer for conclusion, or for adaptation, or a technical layer. It will take context from those three layers. If you want to know how it operates from start to finish, you can run it as an example, like learning Spanish.

**1:00:10** Let’s take a topic about RP trading. What is to learn? Ok, we have someone in the team who knows this. Or, we can choose a topic related to RP trading. For example, what is to learn? We have someone in the team who has insight into this to verify the answer. Ok, let’s see what it says.

This mixture agent will run immediately. We’ve already set up an LCK for that. Ok, something new—‘how to learn Chinese.’ Hold on, let me explain a bit for those who are still confused. This is the problem we faced last week when we were sitting together. Asking questions to AI will determine what kind of response we get and how quickly we absorb new knowledge. That’s the problem we faced.

**1:00:45** When faced with a new topic, in the past, people used Google search to find information. Then, they would compile it and write it down in their documents. But in the last two years, we don’t do that anymore. Instead of using Google to search for knowledge, people now ask large language models. However, just simply asking AI doesn’t always give high-quality results, and sometimes it takes a long time to understand the key points of a new topic.

**1:01:18** For example, in Dream training, there are metrics to measure body changes. Or in learning Chinese, there are some key concepts you need to know. So how do you go from zero knowledge to grasping all these concepts? The entire process is something that ChatGPT’s O1 introduced to me last night.

**1:01:48** Tom has gone through this whole process and will demo it for everyone. Tom has also implemented it so our team can use it more effectively.

**1:02:43** It seems there are more keywords when you ask step by step. For someone who knows nothing, it won’t give that many keywords, and it won’t mention de, C, or anything like that. Let’s try seeing what CL will do, not O1. Did you review it? Let me create a test. Probably have to wait for the API, it’s not streaming. Maybe because they’re using a mixture of agents, it’s hard to run, so it’s just running on KP for now. I understand, the other side has explanations in between.

**1:03:48** That’s right, try expanding and see the clips this morning. I saw a review, looks legit, right? Looks just like that. O1 at home is cheaper too, O1 at home already. This is a demo of having a coin that helps the knowledge discovery process go faster. Let’s try asking about hand exercises, "taichi exercises?" and see how it responds.

**1:04:51** Did you suggest all the necessary techniques? Is there anything unclear? Hand exercises on Discord? What’s CIC? How to CIC? Ok, pretty smart, huh? It even gives all the steps. Ok, let’s try CGR too. Wow, it knows, it knows. Ok, how about piano? Yes, we just asked about piano this afternoon. Let’s try that.

**1:05:56** Ok, playing piano, a student? Yes, a student. Does anyone in our team play music to verify this? I see there are more keywords about piano than usual, easier to explore further. Ok, looks fine. If we look at piano history, what will it say? It probably includes reg, jazz, and things like that.

**1:07:01** Ok, looks good. It even mentions Suzuki Method and similar things. Too easy! O1 at home is great. Learning piano doesn’t just require knowledge, you need practice too. You need practice. You can’t just learn on paper, you have to practice yourself. Currently practicing, studying something.

**1:08:05** Ok, I think we’re done with this one. Any other lessons worth doing for VPF? The HC one, let’s not discuss that. The prompts I created for this mixture of agents were generated by AI, no need to write manually. Here’s my process: take the written piece and convert it into a mixture agent with four system prompts—one for reasoning, one for input identification, one for output identification, and finally a summary.

**1:09:10** That’s the build process. After that, we’ll adjust each note. If we want to add a note, just add a system prompt. If we want to adjust the system prompt, just ask to add it in. In fact, there’s a separate system prompt for handling logical questions and critical thinking, so there’s one specifically for that too.

**1:09:55** This one might be left for later, o1 is so smart that sometimes people don’t believe it. If that’s the case, the next task might be to demo a workflow where people don’t need to code anymore. I just finished the Office Checking for the team, honestly, there’s nothing hard about it. It’s easy, just need about 10 minutes to set it up.

**1:10:45** Now we need to make a feature, and sit in the team to implement it. Both are backend, not drivers, just let AI run it. Can we set it up in 10 minutes? Ok, let’s try, but it might take more than 10 minutes to complete.

**1:11:49** Let’s see, I’ll plan it out. Next session, pick a real project, for example, submitting a report for the for team. Last time, we didn’t have enough time to finish, this time we want to be more hands-on. Let’s pick a different project. Currently, coding still requires manual work and adjusting conventions.

**1:13:36** Meaning, we need to understand the feature of the repo and then write a piece of code to execute it. It’s like doing open source. After that, go deeper into strategy. We’ll set up another check-in and let everyone demo it.

**1:14:57** Pick Go, take a library, copy the context, and let AI understand how to use it. Once AI understands it fully, it will generate the context and help auto-document it. Then, AI will understand the function and message, just input/output it.

**1:15:56** Ok, see you next week. We’ll pick a project so the team can sit together. Everyone will need to create a script or Docker to run it. The master artisan will pick a project that we don’t know yet to test it from scratch. The workflows will allow everyone to compare how to work with AI.

**1:17:15** Ok, that’s about it. See you next Wednesday. We’ll finish the remaining steps and prepare for the test.

**1:18:05** Hopefully next month, all team members will be proficient in these techniques. We’ll increase work efficiency. Any questions?

**1:19:44** Ok, that’s it. Let’s test the workflow again. If there’s nothing else, see you all next week. Have a great weekend!

**1:20:46** Phúc’s team asked about a report from their team, maybe we can arrange a meeting between the two teams to share experience on open source and product data. Hopefully, the next OGIF session will be more productive.

**1:21:29** Hopefully, by then, everyone will fully understand the process and no longer have to do everything manually. If there’s nothing else, happy weekend. Welcome a new team member to their new role! Congratulations!