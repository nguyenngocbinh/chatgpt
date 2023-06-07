# Basic Deep learning

## Một số thuật ngữ cơ bản trong deep learning

### Layer

### Neuron

### Weights and biases

### Activation function

### Feed Forward 

### Back Propagation

### Gradient Descent

## Ví dụ các bước update trọng số

Giả sử chúng ta có một mạng neural với một neuron duy nhất và muốn huấn luyện nó để thực hiện phân loại nhị phân. Neuron có hai đầu vào, được ký hiệu là x1 và x2, và các trọng số tương ứng là w1 và w2. Chúng ta có một ví dụ huấn luyện với các đầu vào (x1, x2) và đầu ra mục tiêu tương ứng là y.

1. Khởi tạo:
   - Khởi tạo các trọng số w1 và w2 với giá trị ngẫu nhiên hoặc số nhỏ gần với không.
   - Đặt tỷ lệ học (learning rate), điều khiển bước nhảy cho việc cập nhật trọng số.

2. Lan truyền tiến (Feed Forward):
   - Tính tổng có trọng số của đầu vào và trọng số: z = w1*x1 + w2*x2.
   - Áp dụng một hàm kích hoạt, như hàm sigmoid, để thu được đầu ra dự đoán: y_pred = sigmoid(z).

3. Tính toán hàm mất mát:
   - Tính toán mất mát giữa đầu ra dự đoán y_pred và đầu ra mục tiêu y bằng cách sử dụng một hàm mất mát phù hợp, chẳng hạn như hàm cross-entropy nhị phân: loss = -[y*log(y_pred) + (1-y)*log(1-y_pred)].

4. Lan truyền ngược (Backpropagation):
   - Tính gradient của hàm mất mát theo trọng số: dL/dw1 và dL/dw2. Điều này có thể được thực hiện bằng cách áp dụng quy tắc chuỗi của đạo hàm.

5. Cập nhật trọng số:
   - Cập nhật trọng số sử dụng thuật toán gradient descent: w1 = w1 - learning_rate * dL/dw1 và w2 = w2 - learning_rate * dL/dw2. Tỷ lệ học xác định bước nhảy của việc cập nhật.

6. Lặp lại:
   - Lặp lại các bước 2-5 cho tất cả các ví dụ huấn luyện hoặc một nhóm ví dụ nhỏ.
   - Tiếp tục lan truyền tiến, tính toán mất mát, lan truyền ngược và cập nhật trọng số lặp đi lặp lại trong nhiều epoch hoặc cho đến khi mất mát hội tụ.

