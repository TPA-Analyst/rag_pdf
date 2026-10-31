# 📚 RAG PDF - Retrieval-Augmented Generation with PDF Documents

Hệ thống Hỏi - Đáp thông minh (Question & Answering) dựa trên tài liệu PDF sử dụng kiến trúc **Retrieval-Augmented Generation (RAG)**. Dự án cho phép trích xuất nội dung từ tệp PDF, lập chỉ mục ngữ nghĩa (indexing/vector embeddings) và truy xuất thông tin chính xác theo ngữ cảnh câu hỏi.

---

## 🌟 Tính năng chính

- **Xử lý & Phân tích PDF:** Trích xuất văn bản từ tài liệu PDF đầu vào (`cybersoft.pdf`).
- **Semantic Indexing:** Lưu trữ và quản lý chỉ mục ngữ nghĩa qua `rag_index.json`.
- **Truy xuất thông tin chính xác:** Tối ưu hóa việc tìm kiếm các phân đoạn liên quan nhất tới truy vấn.
- **Tạo câu trả lời tự nhiên:** Kết hợp ngữ cảnh từ tài liệu với mô hình ngôn ngữ lớn để trả lời câu hỏi trực tiếp, chính xác và không bị bịa đặt thông tin (hallucination).

---

## 📂 Cấu trúc dự án

```text
rag_pdf/
├── cybersoft.pdf      # Tài liệu PDF mẫu dùng để trích xuất & truy vấn
├── demo.py            # Script chạy thử nghiệm nhanh pipeline RAG
├── main.py            # Mã nguồn chính thực thi toàn bộ luồng hỏi đáp
├── rag_index.json     # Dữ liệu chỉ mục / vector embeddings được lập sẵn
├── requirements.txt   # Danh sách các thư viện Python phụ thuộc
├── .gitignore         # Cấu hình bỏ qua môi trường ảo (.venv) và file bí mật (.env)
└── README.md          # Tài liệu hướng dẫn sử dụng dự án

```

---

## 🚀 Hướng dẫn cài đặt & Khởi chạy

### 1. Yêu cầu hệ thống

* **Python**: Phiên bản `3.9+` khuyến nghị.
* Đã cài đặt **Git**.

### 2. Thiết lập môi trường ảo

Mở terminal tại thư mục dự án và chạy:

```bash
# Tạo môi trường ảo
python -m venv .venv

# Kích hoạt môi trường ảo:
# Trên Windows:
.venv\Scripts\activate

# Trên macOS / Linux:
source .venv/bin/activate

```

### 3. Cài đặt các thư viện phụ thuộc

```bash
pip install --upgrade pip
pip install -r requirements.txt

```

### 4. Cấu hình biến môi trường (`.env`)

Tạo một file `.env` ở thư mục gốc và cung cấp các khóa API cần thiết (ví dụ API key của OpenAI, Cohere hoặc Google Gemini tùy mô hình bạn dùng):

```env
# Ví dụ cấu hình API Key
OPENAI_API_KEY=your_api_key_here

```

> **Lưu ý:** Tuyệt đối không commit file `.env` lên GitHub để bảo vệ thông tin bí mật cá nhân.

---

## 💻 Cách chạy chương trình

### Chạy bản Demo nhanh:

```bash
python demo.py

```

### Khởi chạy chương trình chính:

```bash
python main.py

```

---

## 🛠️ Công nghệ sử dụng

* **Ngôn ngữ:** Python
* **Mô hình / Framework:** LLM, Embeddings, Vector Search / JSON Storage
* **Xử lý tài liệu:** Trích xuất PDF và phân đoạn dữ liệu văn bản (Text Chunking)

```
```

### Cách đưa file `README.md` này lên GitHub từ VS Code:

1. Trong VS Code, tạo một file mới đặt tên là `README.md` tại thư mục gốc của `rag_pdf`.
2. Dán nội dung trên vào, chỉnh sửa thêm API Key tương ứng mà bạn đang dùng (nếu có), sau đó nhấn `Ctrl + S` để lưu.
3. Mở tab **Source Control** (`Ctrl + Shift + G`):
   - Nhập thông điệp commit: `docs: add README.md`
   - Nhấn **Commit** rồi chọn **Sync Changes** (hoặc mở Terminal chạy lệnh `git add README.md && git commit -m "docs: add README.md" && git push`).
4. Tải lại trang repository GitHub để xem giao diện tài liệu hoàn thiện.

<ElicitationsGroup message="Bạn có cần tùy chỉnh thêm nội dung nào không?">
  <Elicitation label="Cụ thể hóa framework sử dụng" query="Dự án của tôi dùng LangChain và OpenAI, hãy cập nhật lại README.md theo đúng thư viện này"/>
  <Elicitation label="Tạo file .env.example" query="Hướng dẫn tôi cách tạo file .env.example để chia sẻ cấu hình mẫu an toàn"/>
</ElicitationsGroup>

```
