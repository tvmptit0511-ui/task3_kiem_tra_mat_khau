# TASK3 Bam va kiem tra mat khau
Người thực hiện: Trần Văn Mỹ  |  Dự án: Gia sư AI  |  Công nghệ: Python, FastAPI, MySQL

## Task 3 – Băm và kiểm tra mật khẩu (2 điểm)
File: `app/security.py`

- **Thuật toán:** bcrypt, cost 12, tự sinh salt → cùng mật khẩu nhưng hash khác nhau mỗi lần.
- `hash_password(plain)` → chuỗi hash bắt đầu bằng `$2`.
- `verify_password(plain, hashed)` → `True/False`, không ném lỗi khi đầu vào sai kiểu hoặc hash hỏng.
- `validate_password_strength(plain)` → danh sách lỗi (rỗng = hợp lệ).

**Quy tắc mật khẩu:** 8–64 ký tự, có chữ hoa, chữ thường, số, ký tự đặc biệt, không có khoảng trắng (và ≤ 72 byte vì bcrypt chỉ xử lý tối đa 72 byte).

`verify_password` sẽ được dùng lại ở task Đăng nhập.
