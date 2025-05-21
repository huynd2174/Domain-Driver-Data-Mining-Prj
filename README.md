# Domain-Driver-Data-Mining-Prj

## Giới thiệu

Domain-Driver-Data-Mining-Prj là một dự án phân loại đa nhãn cho các bài báo tiếng Việt sử dụng các phương pháp khai phá dữ liệu hướng lĩnh vực. Dự án này tập trung vào việc phân tích và phân loại nội dung các bài báo tiếng Việt vào các danh mục khác nhau dựa trên nội dung của chúng, sử dụng kết hợp các kỹ thuật xử lý ngôn ngữ tự nhiên (NLP) và học máy.

Dự án được phát triển như một phần của môn học Khai phá dữ liệu hướng lĩnh vực, với mục tiêu xây dựng một hệ thống có khả năng tự động phân loại các bài báo tiếng Việt một cách chính xác, giúp tổ chức và quản lý thông tin hiệu quả hơn.

## Cấu trúc dự án

Dự án được tổ chức thành các thành phần chính sau:

```
Domain-Driver-Data-Mining-Prj/
├── model/                          # Thư mục chứa các notebook phân tích và mô hình
│   ├── dataset_analysis.ipynb      # Phân tích dữ liệu
│   ├── sol-with-cnn-ver2.ipynb     # Giải pháp sử dụng CNN phiên bản 2
│   ├── sol_with_cnn_ver1.ipynb     # Giải pháp sử dụng CNN phiên bản 1
│   ├── sol_with_ml.ipynb           # Giải pháp sử dụng các thuật toán học máy truyền thống
│   ├── solution_compare.ipynb      # So sánh các giải pháp
│   ├── test_data_preprocessed.ipynb # Tiền xử lý dữ liệu kiểm tra
│   └── train_data_preprocessed.ipynb # Tiền xử lý dữ liệu huấn luyện
├── notebook_html_view/             # Phiên bản HTML của các notebook để dễ dàng xem trực tuyến
├── vietnamese-stopwords/           # Thư mục chứa các tệp stopwords tiếng Việt
│   ├── vietnamese-stopwords.txt
│   ├── vietnamese-stopwords-dash.txt
│   └── vietnamese-stopwords-dash-custom.txt
├── requirements.txt                # Các thư viện và phụ thuộc cần thiết
└── README.md                       # Tài liệu hướng dẫn (file này)
```

## Tính năng chính

### 1. Phân tích dữ liệu

Dự án cung cấp các công cụ phân tích chi tiết về bộ dữ liệu bài báo tiếng Việt, bao gồm:
- Phân tích phân bố các nhãn và danh mục
- Thống kê độ dài văn bản
- Phân tích từ khóa và tần suất xuất hiện
- Trực quan hóa dữ liệu để hiểu rõ hơn về đặc điểm của bộ dữ liệu

### 2. Tiền xử lý dữ liệu

Hệ thống tiền xử lý dữ liệu tiếng Việt toàn diện với các bước:
- Chuẩn hóa văn bản (loại bỏ dấu câu, chuyển đổi chữ thường)
- Loại bỏ stopwords sử dụng danh sách tùy chỉnh cho tiếng Việt
- Tokenization và phân đoạn văn bản
- Tạo các đặc trưng cho mô hình học máy

### 3. Mô hình phân loại đa nhãn

Dự án triển khai và so sánh nhiều phương pháp phân loại đa nhãn:
- Mô hình CNN (Convolutional Neural Network) với hai phiên bản khác nhau
- Các thuật toán học máy truyền thống (Random Forest, SVM, Logistic Regression)
- Phân tích và đánh giá hiệu suất của từng phương pháp

### 4. So sánh giải pháp

Công cụ so sánh toàn diện giữa các phương pháp phân loại:
- Đánh giá các chỉ số như độ chính xác, độ thu hồi, F1-score
- So sánh thời gian huấn luyện và dự đoán
- Phân tích ưu nhược điểm của từng phương pháp

### 5. Hỗ trợ tiếng Việt

Dự án được tối ưu hóa đặc biệt cho ngôn ngữ tiếng Việt:
- Sử dụng các danh sách stopwords tiếng Việt tùy chỉnh
- Xử lý các đặc thù của ngôn ngữ tiếng Việt
- Tích hợp với thư viện VnCoreNLP để xử lý ngôn ngữ tự nhiên tiếng Việt

## Cài đặt và sử dụng

### Yêu cầu hệ thống

- Python 3.6+
- Các thư viện được liệt kê trong `requirements.txt`

### Cài đặt

1. Clone repository về máy:
```bash
git clone https://github.com/huynd2174/Domain-Driver-Data-Mining-Prj.git
cd Domain-Driver-Data-Mining-Prj
```

2. Cài đặt các thư viện cần thiết:
```bash
pip install -r requirements.txt
```

3. Tải và cài đặt VnCoreNLP (nếu chưa có):
```bash
# Tải VnCoreNLP từ trang chủ hoặc GitHub
# Đặt đường dẫn đến VnCoreNLP trong các notebook
```

### Sử dụng

1. Phân tích dữ liệu:
   - Mở notebook `model/dataset_analysis.ipynb` để phân tích và hiểu về bộ dữ liệu

2. Tiền xử lý dữ liệu:
   - Sử dụng `model/train_data_preprocessed.ipynb` và `model/test_data_preprocessed.ipynb` để tiền xử lý dữ liệu

3. Huấn luyện và đánh giá mô hình:
   - Mô hình CNN: `model/sol_with_cnn_ver1.ipynb` hoặc `model/sol-with-cnn-ver2.ipynb`
   - Mô hình học máy truyền thống: `model/sol_with_ml.ipynb`

4. So sánh các giải pháp:
   - Sử dụng `model/solution_compare.ipynb` để so sánh hiệu suất của các phương pháp

## Phương pháp và quy trình

### Thu thập dữ liệu

Dự án sử dụng bộ dữ liệu bài báo tiếng Việt đã được thu thập và gán nhãn. Mỗi bài báo có thể thuộc một hoặc nhiều danh mục (phân loại đa nhãn).

### Tiền xử lý dữ liệu

1. **Chuẩn hóa văn bản**:
   - Loại bỏ HTML tags, dấu câu
   - Chuyển đổi về chữ thường
   - Loại bỏ số và ký tự đặc biệt

2. **Xử lý ngôn ngữ**:
   - Loại bỏ stopwords tiếng Việt
   - Tokenization sử dụng VnCoreNLP
   - Tạo các n-grams để nắm bắt ngữ cảnh

3. **Tạo đặc trưng**:
   - Chuyển đổi văn bản thành vector sử dụng TF-IDF hoặc CountVectorizer
   - Tạo embedding cho các mô hình deep learning

### Mô hình phân loại

1. **Mô hình CNN**:
   - Sử dụng các lớp Embedding, Conv1D, MaxPooling1D
   - Tối ưu hóa với Adam optimizer
   - Sử dụng binary cross-entropy loss cho bài toán đa nhãn

2. **Mô hình học máy truyền thống**:
   - Random Forest với tối ưu hóa siêu tham số
   - SVM với kernel khác nhau
   - Logistic Regression với regularization

3. **Đánh giá**:
   - Sử dụng các chỉ số: accuracy, precision, recall, F1-score
   - Phân tích confusion matrix
   - So sánh thời gian huấn luyện và dự đoán

## Kết quả và đánh giá

Dự án đã thực hiện so sánh các phương pháp khác nhau cho bài toán phân loại đa nhãn bài báo tiếng Việt. Kết quả cho thấy:

- Mô hình CNN phiên bản 2 đạt hiệu suất tốt nhất với F1-score cao nhất
- Các mô hình học máy truyền thống có thời gian huấn luyện nhanh hơn nhưng độ chính xác thấp hơn
- Việc sử dụng danh sách stopwords tùy chỉnh giúp cải thiện hiệu suất của các mô hình

Chi tiết về kết quả đánh giá có thể được tìm thấy trong notebook `solution_compare.ipynb`.

## Hướng phát triển tương lai

- Thử nghiệm với các kiến trúc mạng neural phức tạp hơn như LSTM, Transformer
- Tích hợp các kỹ thuật augmentation dữ liệu cho tiếng Việt
- Xây dựng API để triển khai mô hình trong thực tế
- Mở rộng hỗ trợ cho các ngôn ngữ khác trong khu vực

## Tác giả

- **Giảng viên hướng dẫn**: TS. Trần Mai Vũ
- **Nhóm thực hiện**:
  - Phùng Khôi Nguyên
  - Nguyễn Đức Mạnh
  - Nguyễn Đức Huy
  
Sinh viên ngành Hệ thống thông tin, khoa Công nghệ thông tin, trường Đại học Công nghệ, Đại học Quốc gia Hà Nội (UET - VNU)

## Giấy phép
## Tài liệu tham khảo

1. VnCoreNLP: A Vietnamese Natural Language Processing Toolkit
2. Convolutional Neural Networks for Sentence Classification
3. Multi-Label Text Classification: An Overview
4. Natural Language Processing for Vietnamese: Challenges and Perspectives
