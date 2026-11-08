# Task 3 – Băm và kiểm tra mật khẩu (2 điểm)
Module độc lập, chạy được riêng.

```bash
pip install -r requirements.txt
python -m pytest -q
```
Dùng thử:
```python
from app.security import hash_password, verify_password, validate_password_strength
validate_password_strength("Abcdef1@")      # [] = hợp lệ
h = hash_password("Abcdef1@")               # "$2b$12$..."
verify_password("Abcdef1@", h)              # True
```
File chính: `app/security.py`. Tài liệu: `docs/`. Task 2 và Task 1 sẽ import module này.
