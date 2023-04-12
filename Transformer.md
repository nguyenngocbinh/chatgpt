
### Transformer là gì?

Năm 2017, bài báo tiêu đề [Attention Is All You Need](https://arxiv.org/abs/1706.03762). **Transformer** nhận đồng thời toàn bộ chuỗi đầu vào. Nó phụ thuộc vào việc biến đổi một trình tự thành một trình tự khác, giống như các mô hình trình tự theo trình tự thông thường khác, cộng với việc sử dụng cơ chế **Attention**. 

Trong các mô hình NLP, cơ chế **Attention** xem xét mối quan hệ giữa các từ, bất kể chúng được đặt ở đâu trong câu. **Transformer** thực hiện một số lượng nhỏ nhưng không đổi các bước được chọn theo kinh nghiệm. Ở mỗi bước, nó áp dụng mối quan hệ giữa tất cả các từ trong câu bằng cơ chế *self-attention*. Để tính toán biểu diễn cho một từ nhất định, Transformer so sánh nó với mọi từ khác trong câu.

### So sánh với phương pháp khác

Trước khi giới thiệu Transformer, hầu hết các mô hình NLP tiên tiến nhất đều dựa trên RNN. RNN xử lý dữ liệu tuần tự — từng từ một để truy cập vào ô của từ cuối cùng. RNN không hiệu quả lắm trong việc xử lý các chuỗi dài. Mô hình có xu hướng quên nội dung của vị trí ở xa hoặc, trong một số trường hợp, trộn lẫn nội dung của các vị trí liền kề: càng nhiều bước, mạng hồi quy càng khó đưa ra quyết định. Bản chất tuần tự của RNN khiến việc tận dụng tối đa các thiết bị điện toán nhanh hiện đại như TPU và GPU trở nên khó khăn hơn.

Bộ nhớ dài hạn ngắn hạn (LSTM) mang lại một cải tiến nhỏ so với RNN thông thường. LSTM tận dụng cơ chế Cổng để xác định thông tin nào ô cần nhớ và thông tin nào cần quên. Nó cũng có thể loại bỏ vấn đề biến mất độ dốc (vanishing gradient) mà RNN mắc phải. LSTM tốt nhưng không đủ tốt. Giống như RNN, LSTM không thể được đào tạo song song.

Multilayer Perceptrons (MLP) là một mạng thần kinh cơ bản, rất phổ biến vào những năm 1980. Tuy nhiên, nó đã lỗi thời đối với bất kỳ công việc nặng nhọc nào so với các mạng như CNN hoặc RNN.

Mạng thần kinh chuyển đổi (Convolutional Neural Network - CNN) có lợi thế hơn RNN (và LSTM) vì chúng dễ dàng song song hóa. CNN tìm thấy ứng dụng rộng rãi trong NLP vì chúng được đào tạo nhanh và hiệu quả với các câu ngắn hơn. Nó nắm bắt sự phụ thuộc giữa tất cả các kết hợp có thể có của các từ. Tuy nhiên, trong các câu dài, việc nắm bắt sự phụ thuộc giữa các tổ hợp từ khác nhau có thể rườm rà và không thực tế.

Transformer tránh đệ quy bằng cách xử lý toàn bộ câu bằng cách sử dụng cơ chế *Attention* và nhúng vị trí. Các mẫu mới hơn như [Transformer-XL](https://analyticsindiamag.com/what-is-transformer-xl/) cũng có thể khắc phục các vấn đề về kích thước đầu vào cố định.

### Các trường hợp sử dụng Transformer

*GPT-3: Generative Pretraining Transformer-3 (GPT-3)* là một trong những bước đột phá quan trọng nhất vào năm 2020. GPT-3 là mô hình dự đoán ngôn ngữ thế hệ thứ ba trong chuỗi GPT-n của OpenAI. Với 75 tỷ tham số máy học, GPT-3 đã phá kỷ lục của Turing NLG của Microsoft, là mô hình ngôn ngữ lớn nhất (với 17 tỷ tham số) cho đến thời điểm đó.

*GPT-2*: được phát hành vào năm 2019, là một mô hình ngôn ngữ dựa trên large-transformer với 1,5 tỷ tham số, nhiều hơn ít nhất mười lần so với mô hình GPT trước đó. GPT-2 được đào tạo trên tập dữ liệu gồm 8 triệu trang web để 'dự đoán từ tiếp theo, dựa trên tất cả các từ trước đó trong một số văn bản'.

BERT: Vào năm 2018, Google đã mã nguồn mở một kỹ thuật đào tạo trước NLP có tên là Biểu diễn bộ mã hóa hai chiều từ Transformers (Bidirectional Encoder Representations from Transformers - BERT). Nó được xây dựng dựa trên các công trình trước đó như học trình tự bán giám sát (semi-supervised sequence learning), ELMo, ULMFit và Generative Pre-Training. BERT đã đạt được kết quả tiên tiến trên một loạt các nhiệm vụ NLP.

Một startup NLP Hugging Face có một thư viện tên là Transformers. Nó cung cấp các kiến trúc có mục đích chung tiên tiến nhất để Hiểu ngôn ngữ tự nhiên và Tạo ngôn ngữ tự nhiên với khả năng tương tác sâu giữa TensorFlow 2.0 và PyTorch.

### References

- [Why Transformers Are Increasingly Becoming As Important As RNN And CNN?](https://analyticsindiamag.com/why-transformers-are-increasingly-becoming-as-important-as-rnn-and-cnn/)
- [Why does the transformer do better than RNN and LSTM in long-range context dependencies?](https://ai.stackexchange.com/questions/20075/why-does-the-transformer-do-better-than-rnn-and-lstm-in-long-range-context-depen)
