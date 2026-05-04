#  Cryptography Toolkit - Project Lab

Dự án xây dựng bộ công cụ mã hóa cơ bản nhằm áp dụng các kiến thức lý thuyết về An toàn thông tin vào thực hành lập trình[cite: 3, 4].Ứng dụng hỗ trợ các tính năng mã hóa đối xứng, bất đối xứng và hàm băm thông qua giao diện Web trực quan[cite: 8, 11].

##  Mục tiêu dự án
* Hiểu và thực thi luồng xử lý của mã hóa đối xứng (Symmetric), bất đối xứng (Asymmetric) và hàm băm (Hash)[cite: 5].
* Làm quen với việc tích hợp các thư viện bảo mật tiêu chuẩn (`PyCryptodome`, `hashlib`)[cite: 6, 9].
* Quản lý dự án chuyên nghiệp thông qua Hệ thống quản lý phiên bản (VCS - GitHub)[cite: 45].

##  Các tính năng chính [cite: 11]

 1. Mã hóa đối xứng (Symmetric Encryption) [cite: 12]
* Thuật toán hỗ trợ: DES, 3DES, AES (Chế độ ECB)[cite: 13].
* Chức năng: * Cho phép nhập văn bản gốc (Plaintext) và khóa (Secret Key)[cite: 15].
    * Mã hóa dữ liệu sang dạng Ciphertext (Base64)[cite: 16].
    * Giải mã ngược lại từ Ciphertext về Plaintext ban đầu[cite: 19].

2. Mã hóa bất đối xứng (Asymmetric Encryption) [cite: 20]
* [Thuật toán hỗ trợ:** RSA[cite: 21].
* **Chức năng:**
    * Tạo khóa: Phát sinh ngẫu nhiên cặp Public Key & Private Key 2048-bit[cite: 24].
    * Mã hóa: Sử dụng Public Key để mã hóa văn bản[cite: 25].
    * Giải mã: Sử dụng Private Key tương ứng để giải mã dữ liệu[cite: 26].

3. Hàm băm (Hash Functions) [cite: 27]
* [Thuật toán hỗ trợ: MD5, SHA-256[cite: 28].
* Chức năng: Tính toán giá trị băm (Digest) từ một chuỗi văn bản đầu vào để kiểm tra tính toàn vẹn[cite: 31, 53].

## Công nghệ & Thư viện sử dụng [cite: 9, 51]
* Ngôn ngữ: Python 3.x
* Framework: Flask (Giao diện Web App) [cite: 8]
* Thư viện mật mã: `pycryptodome`: Xử lý AES, DES, 3DES, RSA.
    * `hashlib`: Xử lý MD5, SHA-256.

## Cấu trúc thư mục (Code Organization) 

1_Toolkit/
├── main.py              # File chạy chính, điều hướng API Flask
├── templates/
│   └── index.html       # Giao diện người dùng (Frontend)
├── utils/               # Thư mục chứa logic thuật toán (Backend)
│   ├── symmetric.py     # Xử lý AES, DES, 3DES
│   ├── asymmetric.py    # Xử lý RSA & Tạo khóa
│   └── hashing.py       # Xử lý MD5, SHA-256
├── requirements.txt     # Danh sách thư viện cần cài đặt


HƯỚNG DẪN CHẠY 
pip install -r requirements.txt
python main.py