---
tags:
  - office-hours
  - ogif
  - discord
title: "OGIF Office Hours #27 - Go Weekly, Frontend Report Sep, UX Guide to Prompt with AI, Computing the Union of Two Finite Automata"
date: 2024-10-14
description: In OGIF office hour 27, covering presentations on UX Guide to Prompt with AI, computing the union of finite automata, and other topics including Go Weekly and Frontend Report for September.
authors:
  - innno_
---

### Topic highlights
1. Nam's presentation on "UX Guide to Prompt with AI"
   - Overview of current AI-human interaction trends
   - Introduction to the "Race" (Role, Action, Context, Expectation) concept in AI prompting
   - Discussion of new methods to improve AI UX:
     - Context Through Rephrasing
     - Implicit Referencing
     - Continue Conversation
     - Racing and AI Scoring
     - System Prompting
   - Focus on designing AI tools for better user experience beyond speed and accuracy

2. Minh's presentation on computing the union of two finite automata
   - Applications of finite state machines in programming
   - Use of automata in input validation (e.g., regex for email, phone number checks)
   - Application in event-driven systems and event buttons
   - Demonstration using Go source code

3. Phat's presentation on Go Weekly commentary
   - Overview of recent developments in the Go programming language
   - Discussion of notable changes and updates
   - Insights into the Go community and ecosystem

4. Lap's presentation on Frontend Report for September
   - Overview of recent trends and developments in frontend technologies
   - Discussion of notable frameworks, libraries, and tools
   - Insights into the frontend community and ecosystem

---

**Vietnamese Transcript**

**08:02** Có thông tin gì cần phổ biến không? Không thì chắc để phát lên trước, nay thấy nhiều bài quá, để ưu tiên cho mấy bạn mới. Ok, nay có tới năm bài.

**09:13**  Xin mời anh em.  Anh em nào có topic thì lên sớm nhờ. Dạ, pha start trước rồi, chưa đến phần Thành, mời Nam.  Dạ, bài của em là "User Experience AI." Cái bài này chị team làm đi, rồi Thành bạn đã chuẩn bị chưa? Hôm nay, Nam sẽ chia sẻ về đề tài có tên là "UX Guide to  Prompt with AI."

<iframe width="560" height="315" src="https://www.youtube.com/embed/hq_u9GQdNMg?si=FdFGv418n1MC5Apq&amp;start=608" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**10:20** 
Thì em nói overview trước về tình hình hiện tại. Giao tiếp giữa con người và AI là chủ đề rất phổ biến hiện nay, và sự xuất hiện của LLM (Large Language Models) là công cụ hữu ích mà team mình đang muốn tìm hiểu. Bài hôm nay em sẽ dành cho ai quan tâm đến User Experience (UX) của AI, cụ thể hơn là cách các tool hiện đang thiết kế cho sự tương tác giữa người dùng và AI tốt hơn. Hiện nay có khá nhiều tool và platform ra đời, nhưng họ thường tập trung vào việc cải thiện tốc độ prompt và độ chính xác, thay vì chú trọng đến trải nghiệm người dùng.

**11:08** Cái khái niệm "Race" (Role, Action, Context, Expectation) rất phổ biến trong việc prompt AI. Người dùng cần prompt theo cấu trúc này để AI có thể tạo ra output chính xác nhất. Tuy nhiên, không phải trường hợp nào cũng áp dụng được "Race." Có nhiều công ty đã phát triển những phương pháp mới để cải thiện UX của AI, giúp tương tác giữa người dùng và AI mượt mà hơn.

**12:04** Phương pháp đầu tiên là "Context Through Rephrasing." Phương pháp này giúp AI truy vấn lại ngữ cảnh của câu hỏi trước, để trả lời câu hỏi tiếp theo một cách liên mạch, không cần từ đầu phải có cấu trúc prom chuẩn chỉnh. Ví dụ: Câu hỏi đầu tiên là “Who is the wife of Superman?” Tiếp theo, câu hỏi “When did they get married?” AI sẽ hiểu ngữ cảnh và liên kết đúng. Nhưng nếu không có ngữ cảnh phù hợp, như câu “What day did Titanic sink?”, AI sẽ không thể đưa ra kết quả đúng.

**12:50** Tiếp theo là "Implicit Referencing," ví dụ khi hỏi về số tầng của một building, AI sẽ tự động assume đó là một tòa nhà nổi tiếng như "Willis Tower in Chicago." Nếu hỏi “What day?” mà không có ngữ cảnh liên quan, AI không thể trả lời chính xác. Các câu hỏi cần có sự liên kết chặt chẽ với nhau để AI có thể trả lời tốt hơn, và điều này cũng áp dụng cho "Context Through Rephrasing."

**14:19** Một khái niệm tương tự là "Continue Conversation," như trong Google Assistant. Các câu hỏi được nối tiếp một cách tự nhiên, và mỗi câu hỏi mới sẽ liên quan đến những câu hỏi trước đó để tạo ra một chuỗi hội thoại liên tục.

**15:03** Phương pháp tiếp theo là "Racing and AI Scoring." Google Assistant cũng áp dụng phương pháp này. Nó cung cấp nhiều tùy chọn dựa trên các ngữ cảnh khác nhau, giúp người dùng có kết quả tốt hơn. AI cũng có thể tự động học từ những lựa chọn của người dùng để cải thiện khả năng tương tác. Ví dụ, khi AI không rõ ngữ cảnh, nó sẽ đưa ra các tùy chọn cho người dùng chọn.

**16:03** Cuối cùng là "System Prompting." Lý thuyết này định hướng cho AI hoạt động theo ngữ cảnh và mục tiêu người dùng đặt ra. Nó giúp AI tạo ra output chính xác mà không cần tuân theo một chuẩn prompt cố định. Ví dụ, cùng một câu hỏi “Plan for releasing a software product,” Chat GPT có thể đưa ra các khái niệm chung chung, trong khi GPT mini sẽ đưa ra các câu hỏi chi tiết hơn để giúp người dùng prompt tiếp và đạt kết quả chính xác hơn.

**17:45** Bài hôm nay sẽ tập trung vào việc thiết kế tool AI sao cho user experience tốt hơn, không chỉ dựa vào tốc độ hay độ chính xác, mà còn chú trọng đến sự tương tác và trải nghiệm tổng thể của người dùng.

**18:50** Tóm tắt lại bài này cho các bạn, đặc biệt là các bạn designer, bài của Nam có hai khía cạnh chính. Thứ nhất, nó giải thích cấu trúc của "Race" và cách áp dụng nó. Thứ hai, nó đưa ra một framework thiết kế tool AI tập trung vào việc prompt sao cho tương tác giữa AI và người dùng tốt hơn. Cấu trúc "Race" này gồm Role, Action, Context, và Expectation, và nó giúp cải thiện UX của AI.

**19:20** Giải thích cái cấu trúc sơ qua của chuyện là cái Race nó như thế nào, có những thể loại Race như thế nào là những phần nãy giờ Nam nói. Cái thứ hai đó là cái layer về chuyện xây dựng (build) một ứng dụng tập trung vào chuyện prompting, thì cấu trúc đó gắn vào ra làm sao. Khi viết một cái Race, bạn sẽ phải nói rõ Role, Action, Context, và Expectation.

**20:03** Race được mô tả rất rõ ràng: Role là gì, Action là gì, mọi thứ được mô tả theo cái Expect là gì, Task là gì. Tóm lại, chữ R thì cơ bản nhất là các designer sẽ nhìn và hiểu cấu trúc của một câu Race. Nó sẽ có cấu trúc nhất định, dựa trên đó mà đưa ra kết quả tiêu chuẩn. Input là như vậy, và output sẽ nhận được kết quả tương ứng.

**20:47** Phần thứ hai, phần cuối của bài này, sẽ nói về chuyện khi mình đã hiểu cấu trúc của một cái prompt rồi, và hiểu luôn cách để prompt sao cho chuẩn xác. Khi thiết kế, cần phải chú ý những gì? Phần này sẽ là phần mở vì bài này giống như là bài 101 cho các bạn designer để nhìn qua và hiểu cơ bản.

**21:30** Nam đã nói khá nhiều về cái chữ R, nên đôi lúc có thể mọi người sẽ hiểu lầm là bài này đang giải thích chi tiết lại cái đó. Nhưng thực ra bài này là giới thiệu về prompting cho UX designer. Ok, câu hỏi sẽ là, có ai có thắc mắc gì không? Bài này khá cơ bản, team mình xài nhiều rồi, demo cũng nhiều rồi. Có một phần cần lưu ý, bài này đặc biệt hơn ở chỗ giới thiệu về system prompting, mà các bài khác không có.

**22:31** Bài này giới thiệu cái system prompting mà các bài hướng dẫn khác thường không nhắc tới. Các bài viết cho người dùng cuối (end user) thường không đề cập đến điều này nhiều. Bài này nhắc tới system prompting vì nó viết dưới góc nhìn của designer – một người trong đội build. System prompting sẽ khác so với prompting thông thường, vì nó điều khiển cách AI hoạt động theo mục tiêu cụ thể của hệ thống.

**23:06** Cấu trúc của system prompting khác so với các loại R thông thường mà mọi người thường thấy khi đọc research. Thường thì các bạn chỉ thấy nói về 200 kiểu R khác nhau, nhưng không có góc độ là viết cho người build app. Bài này dành cho designer, không phải là end user, mà là người đứng giữa, để kết nối các phần lại với nhau.

**23:48** Bài này khác với những bài viết dành cho engineer vì nó không chỉ giới thiệu về tooling để xây dựng prompts, mà còn nói về việc kết hợp các kiểu R lại với nhau. Đây là bài ở mức độ trung gian, phù hợp cho các bạn làm designer, có vai trò đứng giữa, không trực tiếp build nhưng cũng không phải người dùng cuối. Nó giúp kết nối hai phần này với nhau.

**24:33** Ok, cảm ơn Nam. Tuần sau chắc sẽ scope lại bài theo content cho mọi người dễ hiểu hơn. Còn đi sâu vào chi tiết thì sẽ hơi khó để mọi người nắm bắt hết nội dung. Cảm ơn em nhé. Mời bạn tiếp theo. Để xem thử, không xem màn hình được, à vào lại rồi.

**25:41** Bài của em hôm nay là về một vấn đề nhỏ trong kỹ thuật lập trình, đó là cách compute một tổ hợp (Union) của hai cái finite automata hay còn gọi là finite state machine. Em sẽ demo nó trên một cái source code Go. Chủ đề này hôm nay sẽ có một số mục chính. Trước tiên sẽ giải thích các ứng dụng của automata để mọi người dễ hình dung trước, rồi sẽ đi vào chi tiết.

<iframe width="560" height="315" src="https://www.youtube.com/embed/hq_u9GQdNMg?si=nEFRO7pOhdBxjouy&amp;start=1617" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**26:41** Ứng dụng mà của finite state machine mà mọi người thường thấy nhất là nó sẽ dùng trong việc có một cái button và một cái input, thì mình sẽ muốn kiểm tra xem input này đưa vào cái button đó nó sẽ match hay là nó fail. Nó đơn giản chỉ là như vậy thôi. Cái dễ thấy nhất thường sẽ là dùng regex để kiểm tra xem một đoạn text có phải là một email hoặc là số điện thoại, hoặc là số nhà hay không. Mình sẽ có một cái button giống như vậy, và mình sẽ đưa một đoạn text vào cho nó kiểm tra xem nó có match với điều kiện đó không.

Ngoài regex, dễ thấy nhất, thì ở trong những cái hệ thống event-driven nó sẽ có cái gọi là event button. Mọi người sẽ define một cái button dưới dạng một cái state machine, sau đó, mỗi event sẽ là một state, nó sẽ đi qua event button này và sẽ được filter qua xem nó có match với cái event đó hay không. Nếu match thì nó sẽ đi qua và tới cái state tiếp theo để nó làm tiếp, còn nếu không thì nó sẽ fail và không đi qua được.

**27:27** Đây là một ví dụ của nó: Ví dụ, mình có một cái event bus, tất cả các event sẽ đi qua cái event bus này và sẽ được filter qua các rule. Nếu một event thỏa mãn điều kiện của rule thì nó sẽ đi qua để tiếp tục xử lý. Điều này thường thấy nhất trong các hệ thống cloud hiện tại, họ dùng rất nhiều cái hệ thống này để quản lý các event và filter chúng qua những cái rule như vậy. Mọi người có thể thấy trong những cái hệ thống lớn như của Amazon chẳng hạn, event của họ sẽ đi qua một chuỗi các rule như thế.

**28:05** Ví dụ là mình có một cái button, và tất cả những cái item nào có cái field image, trong cái field image đó có một cái object là width với giá trị là 800, thì nó sẽ được pass qua hết. Và ở dưới thì nó cũng sẽ thêm một vài cái rule nữa, chẳng hạn như những cái field khác nhau mà mình thêm vào cho cái button đó. Đó là một ví dụ về việc finite state machine và event button hoạt động như thế nào. Khi một event được đưa vào hệ thống, nó sẽ đi qua các rule, và nếu thỏa mãn các điều kiện thì nó sẽ được pass qua để tiếp tục các bước xử lý tiếp theo.

**28:56** Đây là một ví dụ cụ thể về hệ thống event của Amazon, nơi mà các event của họ sẽ đi qua một chuỗi các rule để được filter và xử lý. Hầu hết các hệ thống cloud hiện nay đều sử dụng những mẫu button tương tự để quản lý và xử lý các event một cách có tổ chức và hiệu quả.

**29:37** Trong thực tế, bây giờ mình sẽ đi ngược lại một chút về finite automata (f automata) dưới góc độ toán học, nó là cái gì. Thực chất, nó đơn giản là một cái machine trong đó có một tập hợp những states. Để đi từ một state này tới một state tiếp theo, nó cần phải đi qua một transition. Ví dụ, để từ start state tới một end state, nó sẽ luôn cần phải có một điểm bắt đầu gọi là start state và một điểm kết thúc gọi là end state. Vì vậy, nó được gọi là finite state machine bởi vì nó luôn có điểm bắt đầu và điểm kết thúc.

**30:21** Ở giữa, sẽ có một tập hợp các transitions và states để di chuyển từ điểm bắt đầu tới điểm kết thúc. Một input symbol là cái để đưa vào một state để nó di chuyển tới một state khác, và trong thực tế, input symbol thường sẽ là một ký tự. Tí nữa mình sẽ bàn chi tiết về vấn đề này. Accepting state là trạng thái mà khi input của nó được chấp nhận, thì nó sẽ được di chuyển tới một state khác thông qua một transition. Nếu như không chấp nhận thì nó sẽ không di chuyển tới đâu cả, coi như transition đó không dẫn tới một state nào.

**31:04** Có hai loại finite automata, đó là deterministic finite automata (DFA) và nondeterministic finite automata (NFA). Điểm khác biệt duy nhất ở đây là với DFA, mỗi state sẽ có một input symbol duy nhất dẫn tới một transition tới một state khác. Còn với NFA, nó có thể có nhiều transitions cho cùng một state, thậm chí có thể không có transition nào hết. Điều này chỉ khác nhau về cách thể hiện con đường từ điểm bắt đầu tới điểm kết thúc, chứ thật ra một cái finite state machine đều có thể được biểu diễn dưới dạng DFA hoặc NFA, chỉ khác nhau cách biểu diễn thôi.

**31:51** Về phần Union của hai cái finite automata, thì nó sẽ là tổ hợp của tất cả các states và transitions của hai cái finite automata cộng lại. Đặc điểm của nó là nếu ví dụ cái event A pass qua được cái finite automaton FA1 và event B pass qua cái finite automaton FA2, thì tổ hợp của hai cái này, Union của hai cái này, nó phải đảm bảo là cả event A và event B đều pass qua được.

**32:45** Tại sao chúng ta cần phải tính toán Union của hai cái finite automata? Trong thực tế, ví dụ như khi dùng một cái event button, ta sẽ không dùng một cái button mà sẽ dùng nhiều button kết hợp lại với nhau. Ví dụ ở trong hình, chúng ta có thể define rất nhiều button, và trong event của mình có thể chứa nhiều đoạn thông tin match với những button này. Khi muốn kết hợp những button đó lại với nhau, chúng ta sẽ cần tính toán tổ hợp của tất cả chúng lại.

**33:24** Nhưng mình sẽ không tính tất cả một lần, mà sẽ tính từng cái một, từng cặp một, ví dụ như cặp A và cặp B trước, sau đó lấy tổ hợp của A và B, rồi lại tính với cặp C. Chỉ cần tính toán hai button một lúc thôi, đây là mức cơ bản nhất để tính ra được tổ hợp của tất cả các button này.

Để tính toán Union của hai cái finite automata, theo lý thuyết thì chúng ta sẽ phải tính hết tất cả các states và transitions của hai automata đó. Ví dụ mình có hai cái button A và B, trong mỗi button sẽ có rất nhiều states, ví dụ như từ A1 đến Ax và từ B1 đến Bx. Khi tính toán theo kiểu lý thuyết, mình sẽ phải tính toán tất cả các trường hợp kết hợp giữa hai button này, ví dụ A1-B1, A2-B2, A1-B2, A2-B1, có rất nhiều trường hợp.

**34:07** Trong thực tế mình chỉ quan tâm đến việc khi đưa event vào button thì mình muốn biết nó có match hay không thôi. Mình chỉ cần quan tâm xem event đó sau khi đưa vào button, nó có thể đi đến state cuối hay không. Việc tính toán tất cả các states trong Union sẽ rất lãng phí và không cần thiết. Do đó, cách tiếp cận thực tế là mình sẽ có hai finite automata với các states từ A1 tới Ax và từ B1 tới Bx. Khi tính tổ hợp của chúng, mình sẽ kiểm tra xem state đó có dẫn tới một transition nào trong A hoặc B hay không. Nếu không, mình sẽ bỏ qua.

**35:40** Ví dụ như nếu state chỉ dẫn tới A1 và không có transition nào dẫn tới B, thì mình sẽ chỉ tính toán cho nhánh của A, bỏ qua nhánh của B. Ngược lại, cũng tương tự với B. Trường hợp cuối cùng là nếu A1 di chuyển tới Ax và B1 cũng di chuyển tới Bx, thì chúng ta sẽ tạo ra một state mới là Ax-Bx. Lúc này, mình sẽ bắt đầu đệ quy lại và tiếp tục tính toán từ bước đầu tiên này. Ví dụ, mình có A1-B1, và sau đó có A2-B2, thì mình sẽ lặp lại bốn bước này để tính toán tiếp.

**36:15** Khi đó, số lượng states mà mình có thể bỏ qua và không cần tính hoặc không cần lưu trữ sẽ giảm đi rất nhiều so với phương pháp lý thuyết ở trên.

Về input symbol, như trong ví dụ về event button hoặc regex, trong thực tế, các button và input mà chúng ta truyền vào chương trình đều sẽ ở dạng ký tự. Ký tự ở đây thường sẽ là những cái.

**37:04** Ký tự dưới dạng UTF-8, tức là những ký tự đơn giản ví dụ như từ a tới z hoặc từ 0 đến 9. Nó sẽ nằm gọn trong UTF-8, bao gồm 244 ký tự. Mặc dù UTF-8 xài 8 bits (2^8 - 1 = 256), nhưng những bits từ 245 đến 255 thì dư ra, nên mình không xài, chỉ có 244 bits đầu tiên thôi. Rồi, đây là phần detail implementation trong code. Đây là cái workflow cơ bản mà mình sẽ thực hiện. Không biết có zoom được không? Zoom hình hồi nãy thử xem, không thấy chữ gì hết. Từ từ, để xem lại.

**38:21** Rồi, cái FA là gì? Finite automata hả? Đúng rồi, automata. Cái hàm này sẽ merge hai cái automata lại với nhau. Đầu tiên nó sẽ tạo ra một cái key để mình đánh dấu lại, để không phải đi lại những cái state mà mình đã xử lý rồi. Sau đó, nó sẽ check thử cái key này, nếu không trùng, thì nó bắt đầu làm việc. Nó sẽ tạo một cái combined state rỗng, bao gồm tất cả các transitions của hai cái finite automata đó. Rồi nó sẽ tiếp tục merge từng cái finite automata lại với nhau, từng cái một. Kéo lên, mình đọc chưa kịp cái đó.

**39:33** Trong quá trình implementation, sẽ có một số điểm cần chỉnh sửa trong cấu trúc dữ liệu để lưu lại những states đó. Đề tài này của em là em đang chạy cho cái example nào vậy? Hình này đang chạy sample nào? Đây chắc để em show code thì dễ nhìn hơn, phải nhìn vào đề bài mới biết đang code cho bài nào. Rồi, sau cái ví dụ này, sẽ có nhiều câu hỏi cho mình. Nhưng bài này chỉ cần Phúc và Tuấn hiểu là được, mọi người hiểu code rõ không?

Ví dụ hồi nãy về bài toán event button, ở đây mình sẽ define một cái button chẳng hạn. Cái button em define ra dưới dạng T, và đây là cái event. Khi mình chạy đoạn code này, nó chỉ là một phần logic thôi, ngoài ra còn nhiều đoạn code khác nữa. Nhưng khi chạy cái đó, kết quả mình mong đợi là nó sẽ kiểm tra xem event này có match với button này không. Nó sẽ trả về kết quả là đúng hay không đúng, event có match với button không.

**41:13** Đúng rồi, đó là bài toán mà vấn đề này đang giải quyết. Đây là đoạn code đơn giản, em sẽ chạy ra kết quả, chỉ kiểm tra xem nó có match với button này hay không thôi. Ví dụ ở đây, button này có transition với từ "user_register," chẳng hạn. Nếu em sửa lại điều gì đó khác, thì nó sẽ không match. Còn nếu event thỏa mãn điều kiện thì nó sẽ match, kiểu như vậy.

**42:09** Em sẽ đi thẳng tới phần logic chính. Nó sẽ là cái hàm để merge hai cái finite state machine lại với nhau. Mỗi cái finite automata này đại diện cho một cái button. Cứ tưởng tượng mình có nhiều cái button. Ở đây mới chỉ có một cái button thôi, ví dụ em tách cái này thành hai button. Hàm của mình có nhiệm vụ merge hai cái button đó lại để tạo ra một cái button tổng.

**43:31** Như đã nói, để tránh tính toán quá nhiều, trước tiên mình sẽ giải thích các tham số truyền vào hàm. Hai cái FAState là hai cái structure đại diện cho hai cái button hồi nãy của mình. Mỗi cái structure này bao gồm một small table để đại diện cho một dãy những input symbols và những transitions tương ứng. Epsilon là state mà tự đưa lại chính vị trí của nó, mình sẽ bỏ qua nó tạm thời. Ở đây mình chỉ quan tâm tới hai cái states này thôi. Đơn vị nhỏ nhất ở đây mà mình muốn làm input là file, bởi vì một ký tự sẽ được thể hiện dưới dạng UTF-8 và bao gồm 244 bits. Bây giờ mình sẽ loop qua từng bit trong từng ký tự này để so sánh.

**44:20** Ví dụ như trong ví dụ này, mình đưa một cái event vào, sau khi mình compute xong hai cái button này, nó sẽ bắt đầu từ từng ký tự. Ví dụ nó sẽ đi từ ký tự dấu ngoặc, rồi sẽ kiểm tra xem có transition nào tới cái "user" không. Nếu không có, nó sẽ skip phần ID, vì nó không match. Bạn này đang đi vào chi tiết cách so sánh từng ký tự.

**45:02** Skip đoạn này đi. Chỉ cần xem lợi ích và ý tưởng của việc cài đặt thôi, còn so sánh chi tiết thì không cần thiết ở đây. Lợi ích của phương pháp này đơn giản là nó giúp thuật toán không phải tính toán lại nhiều lần. Thuật toán khá đơn giản, chỉ là compare, như mình đã phân tích. Nếu một ký tự không có dẫn tới một transition nào, mình sẽ bỏ qua. Hoặc nếu nó chỉ dẫn tới một nhánh, mà nhánh đó không có transition nào, thì mình cũng bỏ qua luôn.

**46:34** Ví dụ nếu state A1 của mình đi đến state B, mà state B không tồn tại, thì mình sẽ bỏ qua nhánh đó. Ngược lại, nếu state này đã tồn tại trong map rồi, mình cũng sẽ bỏ qua. Chỉ khi nào thỏa hết các điều kiện thì mình mới bắt đầu tính toán và loop qua từng state trong finite automata. Sau khi loop qua từng bước với mỗi state tương ứng trong B, mình sẽ ra được cái state tổng và gán nó vào, sau đó return ra kết quả.

**47:17** Mọi người có hiểu không? Hỏi Minh xem. Minh đi coi cái này, anh kêu Minh quăng cái link lên. Bữa anh em nghe có hiểu không? Quan trọng là coi lại cái diagram đầu tiên, vì mình sợ mọi người không hiểu. Diagram này lâu lắm rồi, hơn cả tháng rồi đúng không? Đúng rồi, diagram này, mọi người có hiểu không?

**49:11** Hệ thống như event bus của Amazon cần phải merge có khi lên đến hàng triệu cái button, nên sẽ có một số chi tiết trong phần implementation để làm những việc này nhanh hơn. Rồi qua một hình khác nữa đi, hình kế tiếp, hình mà nó rẽ hai nhánh, dùng hình đó để nói dễ hơn. Hình rẽ hai nhánh, đúng rồi. Cái hình rẽ hai nhánh, cái nào mà nên? Ừ chắc dùng giữ hình này đi, mấy anh kia có hiểu không?

**50:11** Nói luôn cho rõ, lỡ nói bài này, mọi người nắm thì nó sẽ ok hơn. Hoàng có hiểu không? Em có hiểu cái này làm gì không? À, Phúc hỏi là có dùng bit operator không? Này thì chưa, chưa đến mức đó, chỉ là chi tiết so sánh rồi, không liên quan tới phần đó đâu. Tuấn, Minh ơi, Vincent đâu rồi, mọi người có hiểu bài này không? Không hiểu hả? Bài này nó ẩn tới ba lớp trong đó của phần Minh nói nha. Để mình clear vài thứ cho anh em đỡ lẫn lộn.

**51:03** Đầu tiên là finite automata, tức là cái machine trạng thái, giống như cái state transition diagram mà mấy anh em hay vẽ. Nhớ không? Nó có những trạng thái (states) và các nút (nodes) đại diện cho trạng thái đó. Cái thứ hai là các điều kiện (input symbols) để di chuyển từ trạng thái này qua trạng thái khác, gọi là transition. Đọc cho dễ hiểu, dễ nhớ nhé. Nó giống như cái state transition diagram, đó là cái đầu tiên.

**51:47** Cái thứ hai, cái mà Minh vừa show ra, là hai loại finite automata này. Tại sao lại show ra hai loại này? Vì có những trạng thái rất đơn giản, nó chỉ đi một chiều và không quay ngược lại được. Ví dụ, giờ ăn trưa chẳng hạn. Khi mình đi ra Hà Đô để ăn trưa, mình có thể đi ăn phở, đi bộ ra quán phở, ăn xong rồi đi về. Đó là hoàn thành một cái finite state trạng thái hũ hạn. Nó không có quay đầu lại được, đó là finite automata.

**53:10** Một ví dụ khác, có một trạng thái finite automata mới là đi ăn trưa, nhưng lần này đi xuống siêu thị mua cơm, trả tiền rồi đi về. Vẫn là một cái finite automata, nhưng nó có các states khác với cái trước.

**53:57** Câu chuyện là làm sao tính toán tổ hợp (union) của hai cái finite automata này. Giả sử có hai trạng thái tổ hợp, một là đi ăn phở, hai là đi mua cơm siêu thị. Ta cần build một cái union cho hai trạng thái đó, giống như Minh đã nói về việc merge hai cái state machines lại. Ở đây, chúng ta sẽ có hai lựa chọn: một là đi ăn phở, hai là đi siêu thị mua cơm. Ý tưởng là làm sao tổ hợp tất cả các lựa chọn có thể có giữa hai hệ thống states khác nhau.   

**54:30** Mình tính tổ hợp của nó thì mình gộp lại thôi. Trong cái trường hợp hồi nãy, ví dụ đó, mình sẽ có bao nhiêu options? Một người đi ăn phở, người kia đi siêu thị, đúng không? Ví dụ cũng là tính tổ hợp, nhưng đây là tổ hợp khác nha. Bài toán là có hai cái hệ thống finite automata (FA), và mình yêu cầu là tính union của chúng lại. Sau đó, mình kiểm tra như thế nào? Sẽ có hai phần: phần thứ nhất là đi theo luồng ban đầu – đi ăn phở, và phần thứ hai là đi theo luồng siêu thị. Một trường hợp khác là khi chập hai hệ điều kiện lại với nhau, nó sẽ sinh ra một hệ phụ nữa. Khi đó, mình lại phải tiếp tục tính toán và compute thêm.

**55:17** Rồi, idea cơ bản của việc làm union của nhiều finite automata là vậy. Nó giống như phần mà Minh đã show lúc nãy, Minh có show cái source code. Rồi, coi lại cái hàm lúc nãy đi. Được rồi, ở đây, hàm của Minh có cái hàm để merge tất cả các states lại. Tức là, như đây, mình giả lập là có hai cái hệ states thôi đúng không, của hai cái finite automata khác nhau. Sau đó mình gộp lại thành một hệ chung, rồi ra được cái bảng lớn. Trên cái bảng lớn đó, mình mới tiếp tục tính toán với từng điều kiện.

**56:04** Giờ mình đã build xong cái bảng lớn, một cái array lớn là danh sách tổng các điều kiện nằm ngay đó. Bây giờ mình sẽ bắt đầu tính toán. Khi có một điều kiện mới đưa vào, nó sẽ bắt đầu bằng cách kiểm tra tất cả các điều kiện của hệ đầu tiên. Nếu không được, thì nó kiểm tra các điều kiện của hệ thứ hai. Nếu vẫn không match, thì nó sẽ kiểm tra tiếp điều kiện của hệ tổ hợp giữa hai hệ trước đó. Logic tính toán cơ bản là như vậy.

**57:02** Cái khó của bài này, nếu anh em cảm thấy hơi lẫn lộn, là do quá trình mô hình hóa từ toán học sang lập trình. Cho xem lại cái hàm và cái hình lúc nãy. Hình này là để giải thích tại sao trong bài regular expressions, người ta lại mention điều đó. Khi mình check trong cái dấu ngoặc vuông trong regular expressions, mình phải đi qua bao nhiêu điều kiện trong đó. Vì có nhiều options như vậy, mỗi option lại được mô hình hóa thành toán để dễ xử lý. Mỗi điều kiện là một cái finite automata, và chúng ta tính union của các điều kiện này.

**58:38** Mô hình hóa toán logic thành lập trình là quá trình tính toán với nhiều hệ khác nhau. Mình phải tính toán xem điều kiện union của các hệ 1, 2, 3, 4... Nếu không có điều kiện nào, thì mình phải tính tiếp hệ giao của từng cặp điều kiện. Bài toán này là như vậy. Nếu anh em muốn tìm hiểu thêm, đây là một bài quan trọng vì nó giúp cho hiểu cách mà mình làm trong các hệ thống logic lớn.

**59:21** Chắc bữa trước đưa cho Minh coi rồi. Tại vì điều này quan trọng, bởi nó liên quan tới việc làm hàm cộng trong logic. So sánh phổ biến nhất là login authentication, như bài log in, nó sẽ dính tới bài này. Trong quá trình log in, sẽ có nhiều điều kiện, ví dụ như nó pass bằng 2FA, hoặc email, hoặc SMS, hoặc password. Mỗi thứ này có thể mô hình hóa thành một cái finite automata riêng, và khi mình compute, mình gom tất cả lại.

**01:00:00** Ví dụ như có yêu cầu là người dùng phải có vừa face scan vừa có QR code trên app để đăng nhập. Đó là một điều kiện tổ hợp (giao), chứ không đơn giản là một điều kiện if như bình thường. Trong mô hình toán học, ta sẽ dễ dàng xử lý hơn vì nó sẽ có tính chất đệ quy để tính toán các tổ hợp logic phức tạp. Cái quan trọng nhất là làm sao để tính được tổ hợp này mà không phải tính lại nhiều lần. Output sẽ là success hoặc failure. Nhưng đối với các bạn junior, khi thêm một case mới mà không có tư duy mô hình hóa, họ sẽ làm rất nhiều if statements lộn xộn, gây khó khăn khi bảo trì code.

**01:01:29** Khi thêm một feature mới mà không có tư duy về mô hình hóa, code sẽ trở nên rối rắm và không hiệu quả. Họ sẽ phải sửa lại nhiều lần, gây ra nhiều lỗi và mất nhiều thời gian hơn để kiểm thử và sửa lỗi. Đó là lý do tại sao bài toán này quan trọng, vì nó ảnh hưởng tới việc thiết kế hệ thống, đặc biệt là các hệ thống như login authentication, nơi mà việc tổ hợp nhiều điều kiện là rất phổ biến.

**01:02:23** Còn câu hỏi nào không? Không có hả? Minh, em có hiểu hết không? Ok, chắc hết giờ rồi. Thành ơi, còn bài nào nữa không? Chắc còn hai bài nữa, tranh thủ làm nốt thôi. Để em xem nào. Mọi người thấy màn hình không? Ok, tuần này em chỉ biết được hai bài, còn một bài nữa nhưng nó dài quá, chắc hẹn tuần sau. Bài đó cần chi tiết hơn về cách sử dụng.

**01:03:36** Bài tiếp theo là về Go và cách embed file. Go embed là gì? Nó cho phép mình embed một cái file trực tiếp vào trong binary. Điều này giúp mình giảm thiểu việc handle các external files. Cách sử dụng là khi mình embed một file vào binary, quá trình handle sẽ trở nên đơn giản hơn. Nhưng có một hạn chế, đó là nếu file quá lớn, thì binary của mình sẽ phình to ra. Nên cần phải cẩn thận khi sử dụng.

<iframe width="560" height="315" src="https://www.youtube.com/embed/hq_u9GQdNMg?si=Jiktpv6YYMbiOzp8&amp;start=3793" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**01:04:15** Cách sử dụng như thế này: mình chỉ việc import rồi sử dụng như bình thường. Ví dụ, mình có một cái file message, mình embed file đó vào, rồi có thể truy cập file đó trực tiếp trong binary. Đối với nhiều file, mình có thể thêm ký tự sau như thế này. Sau đó, mình dùng biến đã embed để read file hoặc access như một file bình thường. Hoặc mình có thể embed nguyên một thư mục Directory luôn.

**01:04:57** Thường thì chúng ta muốn embed cái static file như file ảnh, HTML, hoặc cái gì đó kiểu vậy. Về cái limitation mình nói trước đó, cái thứ hai là về reflect một cái package. Bài này thì nội dung cũng không mới. Thật ra cũng không mới nếu như mà em xài Go và có đọc trước bài của bác R rồi. Em sẽ nói qua luôn. Context của ông tác giả này cũng giống như mình thôi. Ví dụ như ổng đang xài một cái tool, một cái codebase nào đó, xong ổng gặp vấn đề về reflect và viết lại bài này. Thì nhìn chung, reflect có ba phần cần chú ý.

**01:05:49** Ba phần quan trọng là: từ interface value cho đến reflection object, và ngược lại. Phần cuối cùng là khi muốn modify thì những cái value đó phải settable – nghĩa là phải được export, tức là phải viết trên capitalized value. Interface value là gì? Reflection object là gì? Interface value là mỗi hàm mà mình xài trong package reflect, nó luôn được hiểu là một interface{} rộng, cho nên nó là giá trị interface. Còn cái giá trị này là reflection object, và ngược lại.

**01:06:36** Về chiều đi: ValueOf sẽ trả về một reflection object. Còn chiều ngược lại: từ đây, mình có thể dùng method là .Interface() để trả ngược lại giá trị ban đầu. Bên Go thì hiện tại nó đã mặc định sẵn rồi. Nếu muốn cập nhật (update) cái gì đó, mình cần tìm cái settable. Reflect có method này để mình có thể dùng và cập nhật được.

**01:07:12** Còn một ý nữa là bên bài viết đó cũng đã nói rồi – nên tránh dùng reflect trừ trường hợp bất khả kháng. Vì nếu mình dùng các hàm như FieldByName, nếu input không được kiểm soát tốt, nó có thể dẫn đến panic hoặc crash ngay lập tức. Nên chỉ dùng khi thực sự cần thiết thôi, trong những trường hợp bí bách.

**01:07:53** Còn một bài khác nữa mà em nói là dài, nói về map. Bài này so sánh giữa việc xài map bình thường với khi cần hỗ trợ concurrency, thì mình cần dùng locking strategy. Có thể xài mutex hay cái gì đó, hoặc lock khác. Bên package sync có hỗ trợ một cái sync.Map. Bài đó sẽ so sánh giữa hai cách tiếp cận này. Thực sự thì không có cái nào hơn cái nào, mà tuỳ vào use case mà xài.

**01:08:35** Rồi chắc tới phần sau. Phát dạ, đơn giản thôi. Minh Trần đang hỏi về logic của ba automata, rồi yêu cầu thêm hai automata nữa. Thì Minh Trần đang hiểu sai thứ tự rồi. Thứ tự sẽ là theo logic khác. Tại sao anh Huy lại nói về các automata của hệ thống Việt Nam? Là bởi vì trước đây họ tiếp cận từ góc độ máy công nghiệp, những hệ máy tự động hoá. Không thể build tụi nó để chúng tương tác với nhau, chạy với nhau tự động, vì chi phí thử và sai rất cao.

**01:09:31** Vì thế, để đảm bảo hiệu quả, họ phải tính toán về mặt logic trước, xem có bao phủ hết các trường hợp không. Ví dụ, khi có ba hệ thống, thêm hai hệ thống nữa là thành năm hệ thống. Trước tiên, phải xem thiết kế logic có chồng chéo gì không. Sau đó, mình mới list out các cây logic ra và tính toán. Đó là bước đầu tiên, sau đó mới tiến hành cài đặt.

**01:10:09** Còn phần lập trình thực hiện sau đó tuỳ vào cách bạn muốn làm: có thể là union các hệ thống hoặc làm hàm cộng. Quan trọng là trước khi làm gì, mình phải đảm bảo phần logic đã cover được hết các trường hợp. Logic ở đây không chỉ là chuyển từ A sang B, mà là hệ logic tổng quát, bao gồm việc tính toán trên cây logic.

**01:10:50** Union trong bài này nói về logic toán học một chút thôi. Còn khi implementation, nếu anh em đã làm thì chắc cũng dễ dàng làm được hàm cộng. Chỉ cần hiểu là trong union logic, chúng ta gom các điều kiện lại và tính toán. Sau khi gom các điều kiện đó, câu hỏi sẽ là trong hàm cộng, nó thực hiện như thế nào. Thường thì mọi người sẽ cố gắng explicitly từng bước một.

**01:11:53** Ok, chắc ổn rồi. Thành còn gì nữa không? Ok, được rồi, để bên DevOps xử lý tiếp. Vào thử lại xem có vấn đề gì không. Mọi người tranh thủ làm bài test sớm nhé. Đợt này có deal về tài chính và AI, nên hãy chú ý.

**01:13:04** Rồi, em sẽ nói qua luôn. Trong tháng 9 này thì không có nhiều tin nổi bật. Em sẽ nói nhanh thôi. Đầu tiên là về React, với những keywords như server actions, server functions, và React compiler. Có một bài viết trên freeCodeCamp về kiến trúc của React 19, nói rõ về cách tối ưu hoá hiệu suất. Nếu mọi người có thời gian thì nên đọc bài này.

<iframe width="560" height="315" src="https://www.youtube.com/embed/hq_u9GQdNMg?si=2kaVp-rYPWxf3Rup&amp;start=4446" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

**01:15:12** Về Next.js, không có gì mới. Chỉ có một cái lùm xùm hồi đầu tháng khi OpenAI chuyển từ Next.js sang Remix. Tóm lại, OpenAI muốn trang của họ nhẹ hơn vì Next.js hơi nặng đối với kiểu trang SPA của chatbox. Vì vậy, họ quyết định quay về dùng Remix. Điều này liên quan đến một xu hướng mà em cảm thấy đang xuất hiện trong cộng đồng engineer: các framework như Next.js dần không được ưa chuộng như trước nữa.

**01:15:51**
Còn về Next.js, không có gì nhiều, chỉ vậy thôi. Ngoài ra, có một cái OpenNext, nó đang hướng tới hỗ trợ việc host Next.js trên tất cả các runtime. Hiện tại, Next.js chỉ chính thức hỗ trợ hosting trên các môi trường cụ thể, còn nếu muốn host ở những môi trường khác thì rất khó khăn.

**01:16:28** Thằng OpenNext này thì mục tiêu của tụi nó là muốn hướng tới một cách mà mọi người có thể host Next.js trên tất cả các môi trường, kiểu không còn bị Versel độc quyền nữa. Vậy nên, có thằng này làm để giải quyết vấn đề đó. Qua cái mục này thì em thấy có hai cái thú vị đang được feature ở đây. Có một thanh niên đang implement một hệ thống real-time đơn giản dùng TypeScript và React. Nói chung, nó khá đơn giản, nhưng mà khi đọc thì thấy nó vui vui, kiểu như là JavaScript làm được mọi thứ vậy.

**01:17:14** Next là một bài về chủ đề này. Nó hơi giống như commentary, nhưng mà em để bên này vì thấy nó cũng khá liên quan. Bài này bàn về trạng thái của ES5 trên web. ES5 giống như đợt trước em có nói, kiểu như CSS3 vậy, mấy cái công nghệ này tồn tại quá lâu rồi. Bài này khảo sát xem các thư viện, trang web trên internet liệu còn bao nhiêu trang web đang còn dùng ES5 hay đã move qua ES6 hết rồi. Tóm lại, kết luận là 89% của top 10.000 trang web hiện tại đã shift sang ES6 rồi.

**01:17:55** Cho nên, kết luận ở đây là ES5 vẫn xài, nhưng mà khi làm một cái gì đó mới, nhất là khi làm thư viện mới, thì nói chung là không nên hướng tới ES5 nữa, vì nó cũng sắp lỗi thời rồi, nó đã quá lâu rồi. State of ES5 vẫn khá là liên quan.

**01:18:44** Về phía trending, không có gì nhiều, nhưng có một bài này em thấy khá vui. Người ta đang có một cái open letter để kêu gọi thằng Oracle bỏ cái trademark của JavaScript. Em mới biết là JavaScript thuộc về trademark của Oracle. Khi nhắc tới Oracle, mọi người chỉ biết về Java thôi, gần như không có sản phẩm nào liên quan tới JavaScript, nhưng mà trademark của JavaScript lại thuộc về Oracle. Nên cái open letter này là kiểu mấy ông lớn trong giới developer yêu cầu Oracle thả cái trademark của JavaScript ra đi, đừng giữ nữa, vì Oracle không có đóng góp gì cho cộng đồng JavaScript.

**01:19:22** Có rất nhiều người nổi tiếng đã ký vào bức thư này, những người creator của Node.js và JavaScript, kiểu rất nhiều người họ đã ký. Em cũng mới biết tới, nhưng mà thấy cũng hay hay.

**01:20:16** Rồi tiếp theo, quay lại mấy cái framework và library mới, nhưng chắc phần này em sẽ skip vì không có gì đặc biệt. Có một cái bài commentary mà anh Thành gửi cho em, nó liên quan về cái sentiment của cộng đồng về React và JavaScript, đặc biệt là Next.js. Bài này khá dài, nhưng tóm lại ý chính của họ là các framework như Next.js càng ngày càng nặng.

**01:20:55** Họ chỉ trích xu hướng hiện tại của cộng đồng engineer React là các front-end developers đang chạy theo các framework và library lạm dụng quá nhiều JavaScript. Điều này có lợi cho trải nghiệm của developer (DX), nhưng lại làm giảm trải nghiệm của người dùng (UX) vì phải ship quá nhiều JavaScript về phía client. Tóm lại là code thì sướng, nhưng sản phẩm cuối cùng thì người dùng lại không thích. Đặc biệt là họ chỉ đích danh thằng Next.js, nói rằng cần đẩy ngược các phần nặng về lại server để cải thiện trải nghiệm người dùng.

**01:21:28** Cái sentiment này khá rõ ràng, họ đang kêu gọi mọi người chuyển ngược về server-side nhiều hơn. Em thấy bên front-end cứ đi vòng quanh vậy thôi, từ server chuyển xuống client, rồi từ client nặng quá lại kêu chuyển về server.

**01:22:19** Nói chung là đó là mấy bài em thấy thú vị trong đợt tháng 9 vừa rồi. Drama thì cũng có chút thú vị, lôi kéo sự chú ý. Bên Go thì ổn định quá nên không có drama, thành ra không ai nói gì nhiều. Còn bên JavaScript thì cứ có drama suốt, từ server-side script, JavaScript modules, kiểu như drama quanh đi quẩn lại. Cộng đồng này lúc nào cũng vậy, không có biên chuẩn rõ ràng thì lúc nào cũng cãi nhau về chuyện đó.

Cảm ơn mọi người. Về phần reminder, các anh em tranh thủ làm bài test sớm nhé, để có thời gian xử lý kịp. Còn một số phần team lab cần xem lại, đặc biệt là báo cáo kết quả sau khi chuyển hết phần này, xem còn gì cần report không. Thành, chắc tụi mình sẽ wrap up ở đây và tập trung vào các case đã nói trước rồi, nhé.

**01:23:30** Rồi, cảm ơn mọi người! Về phần reminder, các anh em tranh thủ làm bài test sớm nhé, để có thời gian xử lý kịp. Còn một số phần team lab cần xem lại, đặc biệt là báo cáo kết quả sau khi chuyển hết phần này, xem còn gì cần report không. Thành, chắc tụi mình sẽ wrap up ở đây và tập trung vào các case đã nói trước rồi, nhé.

**01:24:04** Lập, xem lại giúp nhé. Cát có share một bài bên ngoài, bài đó mới post lên, dễ hiểu, mọi người thử xem nhé. Xu hướng hiện tại của mình sẽ kết thúc chu kỳ của mấy cái software không cần suy nghĩ nhiều, mà tập trung vào phần tooling nhiều hơn. Giờ mấy cái kỹ thuật cơ bản về toán và logic đang quay lại. Sắp tới, team lab sẽ report các chủ đề theo hướng logic nhiều hơn, để anh em nghe quen dần.

**01:24:50** Tom hồi giữa tuần có dựng lại một cái library mới tên là WebUI sau khi cái library cũ bị shut down. Mọi người thử xem. Thằng này khá là legit, khi mình hỏi về chủ đề compile union của hai cái finite automata, nó trả lời toàn bộ theo công thức toán hết, nhìn rất dễ hiểu. Nó giải thích rõ ràng từng bước làm thế nào để tính union của hai hệ thống finite automata.

**01:26:15** Đây, hai hệ rời, hệ chập lại điều kiện để tính toán điều kiện của hai cái dưới đây. Nó nói về chuyện state transitions, anh đang thử nghiệm một vài khái niệm về toán trên đây, và thấy khá là legit. Nếu được, khuyến khích anh em xài con này nhiều hơn. Con này, Tôm đã ngồi mod lại cái system của nó rồi. Ban đầu có thể sẽ nhìn hơi khó chịu một chút, vì mình đã quen nói chuyện bằng ngôn ngữ bình thường khi giải đề toán rất bình thường. Giờ mình phải step back lại một chút, để thấy rằng mấy kiến thức về khối A (toán học) giờ nó có giá trị. Full logic luôn. Rồi, advance như thế nào, practical implications là như thế nào, kỹ thuật làm như thế nào, đều có hết.

**01:26:57** Thành thử ra, với những gì đang diễn ra, với các inquiry và commentary, anh ngồi dò, chắc chắn là thị trường sẽ chuyển qua hướng tài chính. Từ năm ngoái đến giờ, sau đợt blockchain và crypto, team mình hiện tại, đội của Huy Nguyễn vẫn đang tiếp tục, và đội đó vẫn rất ổn. Một số kỹ thuật mới hơn bên blockchain, như Monas hay gì đó, thì mình chưa xem, nhưng chắc cũng tương tự thôi, không có kỹ thuật nào khác biệt quá.

**01:28:29** Về mảng tài chính, mình đang tích cực gần với các cycles về tài chính. Domain đó đang build up theo hướng này, và có vẻ như đây là một cửa rất sáng. Hướng này team mình cũng đang dần làm gần hết rồi, giờ chỉ còn lại là số lượng case study nhiều hay ít nữa thôi. Anh nghĩ vậy là hợp lý. Chất lượng đội ngũ cũng đang được cải thiện dần. Như bài lúc nãy đưa cho Minh, không nhớ là đã đưa cho Minh Lư chưa, nhưng Minh có xem được thì chắc cũng đã hiểu được tầm 6/10. Nhưng anh tin rằng nó vẫn hơn rất nhiều so với nhiều người khác. Mặc dù có sợ, nhưng không report lại được. Minh đã mở hai phần của finite state ra và giải thích rất legit.

**01:29:12** Định hướng của team là theo hướng đó. Nếu khéo, thì chắc là hết tháng này, mình có thể đẩy thêm được nội dung về toán logic nhiều hơn một chút, cố gắng so sánh giữa những khái niệm cũ và những khái niệm mới mà mình đang biết, tương đương với nhau thôi. Biên lại, chỉnh lại cho phù hợp. Ok, không yêu cầu tất cả mọi người phải đi theo hướng đó, nhưng theo quan sát cơ bản, anh thấy thị trường đang dịch chuyển theo hướng đó. Để giữ giá trị khác biệt, mình chơi game theo cách khác chút. Đó là message để anh em aware.

**01:29:58** Nếu không có gì khác thì còn một bài của anh Thành, chắc để sau. Còn lại, mọi thứ, thằng vừa rồi nếu mọi người chưa có access, thì xin chỗ Tom nhé. Hẹn gặp lại anh em tuần sau. Thứ Tư tuần sau sẽ không có buổi họp giữa tuần, mọi người ngồi và làm tiếp theo hướng mình vừa nói nhé. Content làm sao để anh em hiểu.

**01:30:57** Ok, chắc là vậy nhé. Bye bye anh em, hẹn gặp lại anh em vào Thứ Sáu tuần sau. Thứ Tư tuần sau sẽ không có buổi nào ở giữa nữa. Mọi người dành thời gian xem thêm nội dung liên quan tới những gì cần để hoàn thành bài test nhé. Cảm ơn tất cả anh em. Bye bye, hẹn gặp lại.

---

**English transcript**

**08:02** Is there any information that needs to be shared? If not, let's have Phát go first, I see a lot of topics today, so let's prioritize the new members. Ok, there are five topics today.

**09:13** Please come forward. Whoever has a topic, please go early. Yes, Phát will start first, and then Thành’s part will follow. Nam, are you ready? Today, Nam will share a topic called "UX Guide to Prompt with AI."

**10:20** I’ll give an overview of the current situation first. Interaction between humans and AI is a popular topic today, and the emergence of Large Language Models (LLM) is a useful tool that our team is looking into. Today’s topic is for anyone interested in the User Experience (UX) of AI, specifically how tools are currently designed to improve the interaction between users and AI. Many tools and platforms are being developed today, but they mostly focus on improving prompt speed and accuracy instead of focusing on the user experience.

**11:08** The concept of "RACE" (Role, Action, Context, Expectation) is quite common in prompting AI. Users need to prompt in this structure for AI to generate the most accurate output. However, not every case applies to "RACE." Many companies have developed new methods to improve AI UX, helping make the interaction between users and AI smoother.

**12:04** The first method is "Context Through Rephrasing." This method helps AI query the context of the previous question to answer the next question coherently, without needing a perfectly structured prompt from the start. For example, if the first question is "Who is the wife of Superman?" and then you ask, "When did they get married?" AI will understand the context and connect the dots. But if there is no relevant context, such as asking, "What day did the Titanic sink?" AI won’t be able to provide the right answer.

**12:50** Next is "Implicit Referencing," for example, when asking about the number of floors in a building, AI might assume it's a famous building like the "Willis Tower in Chicago." If you ask, "What day?" without proper context, AI cannot give an accurate answer. Questions must be tightly connected for AI to answer better, and this also applies to "Context Through Rephrasing."

**14:19** A similar concept is "Continue Conversation," like in Google Assistant. Questions are naturally linked, and each new question relates to the previous ones to create a continuous conversation.

**15:03** The next method is "Racing and AI Scoring." Google Assistant also applies this method. It provides multiple options based on different contexts, helping users get better results. AI can also learn from user choices to improve interaction. For example, when AI is unclear about the context, it will give users options to choose from.

**16:03** Lastly, there is "System Prompting." This theory directs AI to operate based on the context and user-defined goals. It helps AI generate accurate output without following a fixed prompt standard. For example, when asking, "Plan for releasing a software product". ChatGPT may provide general concepts, while GPT mini will ask more detailed questions to help users continue prompting for more precise results.

**17:45** Today’s discussion focuses on designing AI tools to improve user experience, not just in terms of speed or accuracy but also in terms of user interaction and overall experience.

**18:50** To summarize this for everyone, especially designers, Nam's topic has two main aspects. First, it explains the structure of "RACE" and how to apply it. Second, it presents a framework for designing AI tools, focusing on how to prompt effectively to improve the interaction between AI and users. The RACE structure includes Role, Action, Context, and Expectation, and it helps enhance AI UX.

**19:20** To explain briefly, R stands for Role, and there are different types of R’s that Nam mentioned earlier. For designers to understand the R structure, it's important to look at how to build an app focused on prompting and how this structure ties in. It involves introducing the R technique, a common technique Nam mentioned earlier, called RACE. When writing a RACE, you need to clearly state the Role, Action, Context, and Expectation.

**20:03** RACE is described very clearly: what is Role, what is Action, everything is explained, including what Expectation is and what Task is. In summary, the most basic thing for designers is to understand the structure of a RACE prompt. It follows a specific structure, which produces standard results. The input follows that structure, and the output will provide corresponding results.

**20:47** The second and final part of this presentation will discuss what to pay attention to when designing once you understand the structure of a prompt and how to prompt accurately. This part is open-ended because this is like a 101 guide for designers to look at and understand the basics.

**21:30** Nam has talked quite a bit about the letter R, so some people might misunderstand that this topic is just explaining that concept in detail. But in fact, this presentation is introducing prompting to UX designers. Ok, any questions? This topic is quite basic; our team has used it a lot, and we’ve demoed it many times. There’s one point to note: this topic is special because it introduces system prompting, which other guides don’t cover.

**22:31** This presentation introduces system prompting, which is usually not mentioned in other guides. Guides for end-users (end users) rarely mention this. This topic covers system prompting because it’s written from a designer’s perspective – someone who is part of the team building it. System prompting differs from regular prompting because it controls how AI operates based on the system's specific goals.

**23:06** The structure of system prompting differs from the usual R's that people often see when reading research. Typically, you see discussions about 200 different types of R’s, but there is no perspective from someone building the app. This topic is for designers, not for end-users, but for those in-between to connect the different parts.

**23:48** This is different from articles for engineers because it not only introduces the tools to build prompts but also discusses how to combine different R types. This is an intermediate-level topic, suitable for designers who play the intermediary role, not directly building but also not the end-users. It helps bridge these two parts together.

**24:33** Ok, thanks, Nam. Next week, we will scope this topic again to make the content easier to understand for everyone. Going into detail might be a bit difficult for everyone to grasp. Thank you, Nam. Now, on to the next speaker. Let’s see if we can view the screen. Ah, it’s back.

**25:41** My topic today is a small problem in programming techniques, which is how to compute the union of two finite automata, also known as finite state machines. I will demo it using Go source code. Today’s topic will have a few key points. First, I’ll explain the applications of automata for everyone to get an idea, then we’ll go into the details.

**26:41** The most common application of finite state machines is that when you have a button and an input, you want to check whether the input matches or fails. It’s as simple as that. The most common example is using regex to check whether a piece of text is an email, a phone number, or a street number. We have a button like that, and we feed in a piece of text to check if it matches the condition.

Aside from regex, another common case is in event-driven systems, where we have event buttons. You define a button in the form of a state machine, and each event is a state. The event will go through the event button and get filtered to see if it matches that event. If it matches, it moves on to the next state for further processing; otherwise, it fails and doesn’t go through.

**27:27** Here’s an example: Suppose we have an event bus, and all the events pass through this event bus and get filtered through the rules. If an event satisfies the rule, it proceeds for further processing. This is most commonly seen in modern cloud systems, where they use a lot of these systems to manage events and filter them through rules like this. You can see this in large systems like Amazon, where their events pass through a series of rules.

**28:05** For example, suppose we have a button, and all items with a field "image" that contains an object with a width of 800 will pass through. And we can also add a few more rules for different fields that we add to that button. This is an example of how finite state machines and event buttons work. When an event enters the system, it passes through rules, and if the conditions are met, it will pass through to the next processing steps.

**28:56** This is a specific example of Amazon’s event system, where their events pass through a series of rules to be filtered and processed. Most cloud systems today use similar button patterns to manage and process events in an organized and efficient way.

**29:37** In practice, let's go back a bit to finite automata (f automata) in mathematical terms, what it is. In essence, it's simply a machine with a set of states. To move from one state to the next, it needs to go through a transition. For example, to go from the start state to the end state, there will always need to be a start point called the start state and an endpoint called the end state. That’s why it’s called a finite state machine because it always has a start and an end.

**30:21** In between, there will be a set of transitions and states to move from the start point to the end point. An input symbol is what you feed into a state to move it to another state, and in practice, the input symbol is often a character. We’ll talk more about this in detail later. The accepting state is the state where if the input is accepted, it moves to another state through a transition. If it’s not accepted, it doesn’t go anywhere, as if the transition doesn’t lead to any state.

**31:04** There are two types of finite automata, deterministic finite automata (DFA) and nondeterministic finite automata (NFA). The only difference is that with DFA, each state has a single input symbol leading to a transition to another state. With NFA, there can be multiple transitions for the same state, and there may even be no transitions at all. This difference is just about how the path from the start to the end is represented, but both finite state machines can be expressed as either DFA or NFA. It’s just a matter of representation.

**31:51** Regarding the union of two finite automata, it’s the combination of all the states and transitions of the two finite automata. Its feature is that if event A passes through finite automaton FA1 and event B passes through finite automaton FA2, the union of these two must ensure that both event A and event B pass through.

**32:45** Why do we need to compute the union of two finite automata? In practice, for example, when using an event button, we don’t use just one button, we use multiple buttons combined. For example, in the diagram, we can define many buttons, and in our event, we may have multiple pieces of information that match these buttons. When we want to combine these buttons, we need to compute the union of all of them.

**33:24** But we don’t compute them all at once; we compute them one at a time, for example, first with pairs A and B, then take the union of A and B and compute it with pair C. We just need to compute two buttons at a time—this is the most basic level of calculating the union of all these buttons.

**34:07** To compute the union of two finite automata, theoretically, we would have to calculate all the states and transitions of both automata. For example, if we have two buttons, A and B, and each button has many states, such as from A1 to Ax and from B1 to Bx. Theoretically, we would have to calculate all combinations of these two buttons, like A1-B1, A2-B2, A1-B2, A2-B1—there are many combinations.

34:07 In practice, we only care about whether, when feeding an event into the button, we want to know if it matches or not. We only care if, after feeding the event into the button, it can reach the final state or not. Calculating all the states in the union would be wasteful and unnecessary. Therefore, the practical approach is to have two finite automata with states from A1 to Ax and from B1 to Bx. When calculating their union, we check if the state leads to any transition in A or B. If not, we skip it.

**35:40** For example, if the state only leads to A1 and there’s no transition leading to B, then we only calculate the branch for A and skip B. Similarly, we do the same for B. The last case is if A1 moves to Ax and B1 also moves to Bx, then we create a new state, Ax-Bx. At this point, we recursively start again and continue calculating from this first step. For example, we have A1-B1, and then we have A2-B2, so we repeat these four steps to continue calculating.

**36:15** This way, the number of states we can skip and not calculate or store is significantly reduced compared to the theoretical method mentioned earlier.

Regarding input symbols, like in the event button or regex examples, in practice, the buttons and inputs we feed into the program are always in the form of characters. Characters here are often those.

**37:04** Characters in UTF-8, which are simple characters like from a to z or from 0 to 9. They fit into UTF-8, which includes 244 characters. Although UTF-8 uses 8 bits (2^8 - 1 = 256), the bits from 245 to 255 are left over, so we don’t use them, just the first 244 bits. Now, here’s the implementation detail in the code. This is the basic workflow we’ll follow. Not sure if it can be zoomed in? Try zooming in on the diagram from earlier, the text isn't visible. Wait a moment, let’s check again.

**38:21** Alright, what is FA? Finite automata? Yes, automata. This function will merge two automata together. First, it creates a key to mark the states that have already been processed so that we don’t have to revisit them. Then, it checks this key, and if it’s not a duplicate, it starts working. It creates an empty combined state that includes all the transitions of the two finite automata. Then it continues merging each finite automaton, one by one. Scroll up, I couldn’t read that part in time.

**39:33** During implementation, there will be some points where we need to modify the data structure to store those states. Which example is your topic based on? Which sample is this diagram running? Let me show the code; it’ll be easier to see. You have to look at the problem to know which code we're dealing with. After this example, we’ll have more questions. But this topic only needs Phúc and Tuấn to understand, does everyone understand the code clearly?

**40:13** The earlier example about the event button, here we define a button, for example. The button I defined is in the form of T, and here’s the event. When we run this code, it’s just part of the logic; there are more parts of the code. But when running that, the expected result is that it will check if this event matches this button. It will return whether the event matches the button or not.

**41:13** That’s right, that’s the problem this code is solving. This is simple code; it will run and return results, just checking if it matches this button or not. For example, here, this button has a transition with "user_register," for instance. If I change something else, it won’t match. But if the event meets the condition, it will match, something like that.

**42:09** I’ll go straight to the main logic. It’s the function to merge two finite state machines together. Each of these finite automata represents a button. Imagine we have multiple buttons. Here we only have one button, but imagine I split this into two buttons. My function is responsible for merging those two buttons into one total button.

**43:31** As mentioned earlier, to avoid too much calculation, I’ll first explain the parameters passed into the function. The two FAState are two structures representing the two buttons we had earlier. Each structure includes a small table to represent a series of input symbols and their corresponding transitions. Epsilon is the state that returns to its own position, we’ll skip that for now. Here, we only care about these two states. The smallest unit we want to use as input is the file because a character is represented in UTF-8 and includes 244 bits. Now, we’ll loop through each bit in these characters to compare.

**44:20** For example, in this case, when I input an event, after computing these two buttons, it starts from each character. For example, it starts with a bracket and checks if there’s any transition to "user." If there isn’t, it skips the ID part because it doesn’t match. This part goes into the details of comparing each character.

**45:02** Skip this part. Just look at the benefits and the idea behind the implementation; there’s no need to compare in detail here. The benefit of this method is simple: it helps the algorithm avoid recalculating too many times. The algorithm is quite simple, it’s just comparing, as we analyzed earlier. If a character doesn’t lead to a transition, we skip it. Or if it only leads to one branch, and that branch doesn’t have any transitions, we skip it as well.

**46:34** For example, if state A1 moves to state B, but state B doesn’t exist, we skip that branch. Conversely, if that state already exists in the map, we skip it. Only when all conditions are met do we start calculating and loop through each state in the finite automata. After looping through each step with the corresponding state in B, we get the final state and assign it, then return the result.

**47:17** Does everyone understand? Ask Minh. Minh, check this out. I told Minh to send the link. Did you all understand this? The important thing is to review the first diagram because I’m afraid people don’t understand it. This diagram was a long time ago, more than a month ago, right? Yes, this diagram, does everyone understand?

**49:11** Systems like Amazon’s event bus need to merge sometimes up to millions of buttons, so there will be some details in the implementation to speed up these tasks. Switch to another diagram, the next one, the one that branches into two; use that to explain better. The branching diagram, which one should we use? Let’s stick with this diagram, do the others understand?

**50:11** Let’s explain it clearly so that everyone gets it. Hoàng, do you understand? Do you get what this is doing? Ah, Phúc asked if it uses a bit operator. Not yet, it hasn’t reached that level, it’s just detailed comparisons, unrelated to that part. Tuấn, Minh, where’s Vincent? Does everyone understand this topic? No? This topic is nested in three layers from what Minh discussed earlier. Let’s clear a few things to make it less confusing for everyone.

**51:03** First, finite automata, or state machines, are like state transition diagrams that you often draw. Remember? They have states and nodes representing those states. Second, there are conditions (input symbols) that allow you to move from one state to another, called transitions. Read it carefully to understand and remember it better. It’s like a state transition diagram; that’s the first point.

**51:47** The second point is the two types of finite automata that Minh just showed. Why show these two types? Because some states are simple, they only move in one direction and can’t reverse. For example, lunchtime. When you walk out to Hà Đô to eat pho, you can walk to the pho restaurant, eat, and return. That completes a finite state; it doesn’t reverse, that’s a finite automaton.

**53:10** Another example is a new finite automaton where you go to the supermarket to buy lunch, pay, and return. It’s still a finite automaton, but it has different states than the previous one.

**53:57** The issue is how to calculate the union of these two finite automata. Let’s say there are two states: one where you eat pho, and the other where you go to the supermarket to buy lunch. We need to build a union of these two states, like how Minh talked about merging two state machines. Here, we have two choices: one is to eat pho, and the other is to go to the supermarket. The idea is to compute all possible combinations of these two state systems.

**54:30** We calculate their union by simply combining them. In the earlier example, how many options do we have? One person goes to eat pho, and the other goes to the supermarket, right? This example is also calculating the union, but it’s a different kind of union. The problem is that there are two finite automata (FA), and we need to compute their union. Then we check how to combine them. There are two parts: one part follows the original flow—eating pho, and the other part follows the supermarket flow. Another case is when you combine two sets of conditions, which will generate a new set. At that point, we have to continue calculating and computing more.

**55:17** The basic idea of creating a union of multiple finite automata is like that. It’s similar to what Minh showed earlier—Minh showed the source code. Now, let’s go back to that function. Alright, here, Minh’s function has a method to merge all the states. This means we simulate having two state systems only, right? From two different finite automata. Then we merge them into a unified system, which gives us a big table. From that big table, we continue to calculate based on each condition.

**56:04** Now, we’ve built the big table—a large array that contains the complete list of conditions. Now, we’ll start calculating. When a new condition is input, it begins by checking all the conditions of the first system. If it doesn’t match, it checks all the conditions of the second system. If it still doesn’t match, it checks the conditions of the union of the two systems. The basic calculation logic is just like that.

**57:02** The difficulty of this problem, if you feel a bit confused, lies in the process of modeling from mathematics into programming. Do you get it, Tư? Lucky, did you grasp it? Ok, follow the problem. Show the function and the diagram from earlier. This diagram explains why regular expressions mention this. When you check in square brackets in regular expressions, you need to go through all the conditions inside. Because there are so many options, each option is modeled mathematically to make it easier to handle. Each condition is a finite automaton, and we compute the union of these conditions.

**58:38** Modeling mathematical logic into programming is the process of calculating with different systems. We need to calculate the union condition of systems 1, 2, 3, 4... If none of the conditions are met, we have to calculate the intersection of each pair of conditions. This problem is like that. If you want to learn more, this is an important topic because it helps you understand how we operate in large logic systems.

**59:21** I think I gave this to Minh earlier. This is important because it relates to creating logic addition functions. A common comparison is login authentication, like in the login process, which relates to this problem. During the login process, there are many conditions, for example, passing 2FA, email, SMS, or password. Each of these can be modeled into its own finite automaton, and when we compute them, we combine them all.

**0 1:00:00** For example, there might be a requirement for the user to have both face scan and QR code to log in. That’s a combined condition (intersection), not just a simple if statement. In mathematical modeling, we can handle this easily because it has recursive properties to compute complex logic combinations. The most important thing is how to calculate this combination without recalculating many times. The output will either be success or failure. But for junior developers, when adding a new case without the modeling mindset, they’ll end up creating many messy if statements, making it hard to maintain the code.

**01:01:29** When adding a new feature without a modeling mindset, the code becomes messy and inefficient. They’ll have to rewrite it many times, causing many bugs and wasting time fixing and testing. That’s why this problem is important, as it impacts system design, especially in systems like login authentication, where combining multiple conditions is common.

**01:02:23** Any more questions? No? Minh, do you understand it all? Ok, looks like we’re out of time. Thành, are there any more topics? There are two more, but let’s try to wrap them up quickly. Let me check. Can everyone see the screen? Ok, this week, I only have two topics, there’s another one, but it’s too long, we’ll do it next week. That one requires more detail in terms of usage.

**01:03:36** The next topic is about Go and how to embed files. What is Go embed? It allows us to embed a file directly into the binary. This helps reduce the need to handle external files. The way it works is that when we embed a file into the binary, the handling process becomes simpler. But there’s a limitation: if the file is too large, the binary will expand. So, be careful when using this.

**01:04:15** The usage is like this: we just import it and use it as usual. For example, we have a message file, we embed that file into the binary, and then we can access that file directly. For multiple files, we can add additional characters like this. Then, we use the embedded variable to read or access it like a normal file. Or we can even embed an entire directory.

**01:04:57** Usually, we want to embed static files like images, HTML, or something like that. As for the limitation I mentioned earlier, the second topic is about reflecting a package. This topic is not new. It’s not really new if you’ve used Go and read the article by Dr. R. I’ll go over it quickly. The context is that the author encountered a problem with reflection while using a tool or codebase and wrote this article. In general, reflection has three key points to note.

**01:05:49** The three important points are: from interface value to reflection object, and vice versa. The final point is when you want to modify the values, they need to be settable, meaning they need to be exported, or written with a capitalized value. What is an interface value? What is a reflection object? The interface value is, in every function we use in the reflect package, it’s always understood as a wide interface{}, so it’s an interface value. And this value is a reflection object, and vice versa.

**01:06:36** As for the direction: ValueOf returns a reflection object. In the opposite direction, from here, we can use the method .Interface() to return the original value. In Go, this is now default. If you want to update something, you need to find something settable. Reflect has this method for you to use and update.

**01:07:12** Another point mentioned in that article is to avoid using reflect unless absolutely necessary. If you use functions like FieldByName, if the input is not well-controlled, it can lead to panic or crashes immediately. So, only use it when absolutely necessary, in cases where there’s no other option.

**01:07:53** There’s another article that I mentioned that’s quite long, about map. It compares using regular maps with the need to support concurrency, where you’ll need a locking strategy. You can use mutex or something else, or some other lock. The sync package provides a sync.Map. The article compares these two approaches. There’s no better option; it depends on the use case.

**01:08:35** Now, let’s move on to the next part. Phát, simple stuff. Minh Trần is asking about the logic of three automata and then adding two more automata. But Minh Trần is misunderstanding the order. The order will follow different logic. Why did Huy mention automata systems in Vietnam? Because previously, they approached it from the perspective of industrial machines, automated systems. They couldn’t build them to interact with each other or run automatically because the cost of trial and error was too high.

**01:09:31** So, to ensure effectiveness, they had to calculate the logic first to see if it covered all cases. For example, when there are three systems, and you add two more, making five systems. First, you have to see if the logic design overlaps. Then, we list out the logic trees and calculate. That’s the first step, then we proceed with implementation.

**01:10:09** As for implementation, it depends on how you want to do it: you can union the systems or create an addition function. The important thing is that before you do anything, you must ensure the logic covers all the cases. Logic here is not just about going from A to B; it’s a general logic system, including calculations on logic trees.

**01:10:50** Union in this article talks about mathematical logic a bit. When it comes to implementation, if you’ve done it before, you’ll find it easy to create an addition function. Just understand that in union logic, we combine conditions and calculate. After combining those conditions, the question is how the addition function performs. Usually, people try to explicitly go step by step.

**01:11:53** Ok, seems good now. Thành, is there anything else? Ok, got it, DevOps team will handle the rest. Try it again and see if there’s any issue. Everyone, please do your tests early. We’ve got a financial and AI deal this time, so pay attention.

**01:13:04** Now, I’ll move on. In September, there weren’t many notable updates. I’ll go over it quickly. First, about React, with keywords like server actions, server functions, and React compiler. There’s an article on freeCodeCamp about React 19’s architecture, detailing how to optimize performance. If you have time, you should read that article.

**01:15:12** Regarding Next.js, nothing much new. There was some noise at the beginning of the month when OpenAI switched from Next.js to Remix. In short, OpenAI wanted their page to be lighter because Next.js was a bit heavy for a chatbox SPA (Single Page Application). So, they decided to switch back to Remix. This relates to a trend I’m noticing in the engineer community: frameworks like Next.js are becoming less favored.

**01:16:28** The goal of OpenNext is to make it so that people can host Next.js on any environment, no longer being restricted by Vercel’s exclusivity. So, this project is here to solve that problem. Moving on, I see two interesting things being featured. There’s someone implementing a simple real-time system using TypeScript and React. It’s pretty simple, but reading it makes you smile, like JavaScript can do everything.

**01:17:14** Next is a piece about this topic, which is kind of like commentary, but I’m putting it here because it’s still relevant. This article discusses the state of ES5 on the web. ES5 is like what I mentioned before, like CSS3, technologies that have been around for too long. This article surveys how many websites on the internet are still using ES5 or if they’ve moved on to ES6. In short, the conclusion is that 89% of the top 10,000 websites have already shifted to ES6.

**01:17:55** So, the takeaway here is that ES5 is still in use, but when building something new, especially when building a new library, generally, you shouldn’t aim for ES5 anymore because it’s almost outdated; it’s been around for too long. The state of ES5 is still somewhat relevant.

**01:18:44** Regarding trending topics, there’s not much, but there is an amusing one. There’s an open letter asking Oracle to give up the JavaScript trademark. I just found out that JavaScript belongs to Oracle's trademark. When people think of Oracle, they only know Java, and almost no product relates to JavaScript. But the trademark for JavaScript is owned by Oracle. So this open letter is basically developers asking Oracle to release the JavaScript trademark, not hold onto it anymore, because Oracle hasn’t contributed anything to the JavaScript community.

**01:19:22** Many big names have signed the letter, including the creators of Node.js and JavaScript, many well-known people have signed it. I just found out, but it seems interesting.

**01:20:16** Moving on to new frameworks and libraries, but I’ll probably skip this part because there’s nothing special. There’s a commentary from Thành, relating to the sentiment in the React and JavaScript community, especially around Next.js. The article is quite long, but to sum it up, the main point is that frameworks like Next.js are getting heavier.

**01:20:55** They criticize the current trend in the React engineer community: front-end developers are chasing after frameworks and libraries that overuse JavaScript. This benefits the developer experience (DX), but it reduces the user experience (UX) because too much JavaScript is being shipped to the client. In short, writing code is fun, but the final product doesn’t make the user happy. They specifically mention Next.js, saying that the heavy parts need to be pushed back to the server to improve the user experience.

**01:21:28** This sentiment is quite clear; they’re calling for a shift back to more server-side solutions. I feel like the front-end community keeps going in circles: moving from the server to the client, and now the client is too heavy, so they’re calling to move back to the server.

**01:22:19** In general, those are the interesting topics I found in September. Drama is always interesting; it grabs attention. In Go, everything is stable, so there’s no drama, which is why no one talks much. But in JavaScript, there’s always drama, from server-side scripts to JavaScript modules, the drama just keeps coming back around. The community is always like this; without clear standards, people are always arguing.

**01:23:30** Thanks, everyone. Regarding the reminder, please do your tests early so there’s time to handle everything. The team lab still has some work to review, especially the reports after everything is transferred over. Thành, I think we’ll wrap up here and focus on the cases we mentioned earlier.

**01:24:04** Lập, please review. Cát shared an article outside, it’s new, easy to understand, everyone take a look. The current trend seems to be ending the cycle of software that doesn’t require much thought, focusing more on tooling. Now, basic techniques in math and logic are making a return. In the future, the lab team will report more on topics in logic, so everyone gets used to it.

**01:24:50** Tom rebuilt a new library called WebUI after the old one was shut down. Everyone take a look. This one is quite legit. When you ask it about the union of two finite automata, it responds with everything in mathematical formulas, very easy to understand. It explains clearly how to compute the union of two finite automata systems.

**01:26:15** Here, the two systems combine conditions to calculate. It talks about state transitions, I’m testing a few mathematical concepts on it, and it seems quite legit. If possible, I encourage everyone to use this more. Tom has already modified its system. Initially, it might seem a bit uncomfortable because we’ve been used to using normal language to talk about these problems for so long. Now, we have to step back a little, and see that knowledge in math is valuable now. Full logic. Then, how to advance, practical implications, how to implement it—everything is there.

**01:26:57** Given what’s happening with the inquiries and commentary, I’ve been checking, and I’m certain the market is shifting toward finance. Since last year, after the blockchain and crypto wave, our team, Huy Nguyễn’s team, is still moving forward, and that team is still doing well. Some newer techniques in blockchain, like Monas or something, we haven’t looked at yet, but it’s probably similar, no major technical differences.

**01:28:29** In finance, we’re actively working with the financial cycles. That domain is building up this way, and it seems like a bright opportunity. Our team is also almost done with this, now it’s just a matter of how many case studies there are. I think this direction is reasonable. The team’s quality is gradually improving. Like the material I gave to Minh earlier, I can’t remember if I gave it to Minh Lư yet, but if Minh has seen it, he should understand about 6/10. But I believe it’s still much better than many others. Even though there might be fear, he didn’t report back. Minh opened two parts of the finite state machine and explained them very well.

**01:29:12** The team’s direction is to follow this path. If done skillfully, by the end of this month, we could push more content about math and logic. We’ll try to compare old concepts with new ones we already know. Let’s refine and adjust. Ok, it’s not required that everyone follow this path, but based on basic observation, I see the market is shifting in that direction. To keep our value distinct, we have to play a different game. Consider this as a message for everyone to be aware.

**01:29:58** If there’s nothing else, there’s one more article from Thành, but we’ll leave it for later. As for the rest, if anyone doesn’t have access to the thing from earlier, ask Tom. See you next week. Next Wednesday, there won’t be a mid-week meeting, everyone sit and continue along the direction we just discussed. Let’s work on the content so that everyone can understand.

**01:30:57** Ok, I think that’s it. Bye-bye, everyone, see you next Friday. Next Wednesday, there won’t be a mid-week meeting. Everyone take time to review the content related to what needs to be done for the test. Thanks, everyone. Bye-bye, see you.