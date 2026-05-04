#  Cryptography Toolkit - Project Lab

Dự án xây dựng bộ công cụ mã hóa cơ bản nhằm áp dụng các kiến thức lý thuyết về An toàn thông tin vào thực hành lập trình.Ứng dụng hỗ trợ các tính năng mã hóa đối xứng, bất đối xứng và hàm băm thông qua giao diện Web trực quan

##  Mục tiêu dự án
* Hiểu và thực thi luồng xử lý của mã hóa đối xứng (Symmetric), bất đối xứng (Asymmetric) và hàm băm (Hash).
* Làm quen với việc tích hợp các thư viện bảo mật tiêu chuẩn (`PyCryptodome`, `hashlib`).
* Quản lý dự án chuyên nghiệp thông qua Hệ thống quản lý phiên bản (VCS - GitHub)

##  Các tính năng chính 

 1. Mã hóa đối xứng (Symmetric Encryption) 
* Thuật toán hỗ trợ: DES, 3DES, AES (Chế độ ECB)
* Chức năng: * Cho phép nhập văn bản gốc (Plaintext) và khóa (Secret Key).
    * Mã hóa dữ liệu sang dạng Ciphertext (Base64)
    * Giải mã ngược lại từ Ciphertext về Plaintext ban đầu.

2. Mã hóa bất đối xứng (Asymmetric Encryption) 
* [Thuật toán hỗ trợ:** RSA
* **Chức năng:**
    * Tạo khóa: Phát sinh ngẫu nhiên cặp Public Key & Private Key 2048-bit
    * Mã hóa: Sử dụng Public Key để mã hóa văn bản
    * Giải mã: Sử dụng Private Key tương ứng để giải mã dữ liệu

3. Hàm băm (Hash Functions) 
* Thuật toán hỗ trợ: MD5, SHA-256
* Chức năng: Tính toán giá trị băm (Digest) từ một chuỗi văn bản đầu vào để kiểm tra tính toàn vẹn

## Công nghệ & Thư viện sử dụng 
* Ngôn ngữ: Python 3.x
* Framework: Flask (Giao diện Web App) 
* Thư viện mật mã: `pycryptodome`: Xử lý AES, DES, 3DES, RSA.
    * `hashlib`: Xử lý MD5, SHA-256.



HƯỚNG DẪN CHẠY 
pip install -r requirements.txt
python main.py