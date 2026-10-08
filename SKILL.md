---
name: python-project
description: Hướng dẫn cơ bản để phát triển, chạy và kiểm tra dự án Python trong repository này.
---

# Dự án Python

## Phạm vi sử dụng

Sử dụng hướng dẫn này khi thêm hoặc chỉnh sửa mã Python trong repository.
File khởi chạy hiện tại là `app.py`; chương trình in ra `Hello World` và chỉ sử dụng thư viện chuẩn.

## Thiết lập môi trường

Sử dụng Python 3. Tạo môi trường ảo từ thư mục gốc repository:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Trên Windows, kích hoạt bằng `.venv\Scripts\activate`.
Nếu dự án có file `requirements.txt`, cài các thư viện bằng:

```bash
python -m pip install -r requirements.txt
```

Dự án hiện chưa có thư viện bên ngoài cần cài đặt.

## Chạy chương trình

```bash
python app.py
```

Kết quả hiện tại:

```text
Hello World
```

## Quy ước phát triển

- Tuân theo PEP 8, thụt lề bằng 4 dấu cách và lưu file dưới dạng UTF-8.
- Đặt tên biến và hàm theo `snake_case`, tên lớp theo `PascalCase`.
- Ưu tiên thư viện chuẩn; khai báo thư viện bên ngoài trong `requirements.txt` khi cần.
- Không đưa mật khẩu, khóa API, môi trường `.venv` hoặc file cache vào Git.
- Cập nhật hướng dẫn chạy khi thay đổi cách sử dụng chương trình.

## Kiểm tra thay đổi

Với chương trình hiện tại, chạy `python app.py` và xác nhận kết quả là `Hello World`.
Khi có thư mục `tests`, chạy các bài kiểm tra dùng thư viện chuẩn bằng:

```bash
python -m unittest discover -s tests
```

Trước khi commit, kiểm tra nội dung thay đổi bằng `git diff` và `git status`.
