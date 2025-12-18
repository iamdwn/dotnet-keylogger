# .NET Keylogger

Dự án này minh họa cách cài đặt Low-Level Keyboard Hook trong Windows bằng C#,
sử dụng thư viện `user32.dll` để bắt sự kiện phím toàn hệ thống,
Xây dựng nhằm phục vụ mục đích học tập về:

- Windows API hook bàn phím
- Ghi log phím nhấn
- Tự động chụp màn hình Desktop
- Gửi email tự động
- Khởi động cùng Windows
- Kỹ thuật ẩn console
- Tương tác registry
- Tương tác Mail SMTP

> **Lưu ý đạo đức & pháp lý:**  
> Project chỉ để nghiên cứu kỹ thuật. Không được sử dụng để theo dõi trái phép người khác.  
> Hành vi này có thể dẫn đến hậu quả pháp lý nghiêm trọng.
> Phần mềm chỉ được sử dụng cho:
   > Nghiên cứu cá nhân,
   > Thử nghiệm kỹ thuật hook input,
   > Học cách xử lý event bàn phím trong .NET.

---

## Tính năng:

- Ghi lại phím nhấn vào file log cục bộ
- Chạy nền trong Windows với hook `WH_KEYBOARD_LL`
- Cho phép ẩn/hiện cửa sổ console bằng phím tắt `Ctrl + K`
- Tùy chọn:
  - Chụp ảnh màn hình định kỳ
  - Gửi email chứa log và hình ảnh (cần chỉnh sửa SMTP)
  - Khởi chạy cùng Windows qua Registry
    
---

## Công nghệ

- .NET Framework / C#
- WinAPI Interop
- GDI+ Screenshot
- SMTP Email

---

## Cách hoạt động
Ứng dụng sử dụng Windows API để:

1. Móc (hook) bàn phím ở mức hệ thống.
2. Lắng nghe mọi sự kiện phím nhấn.
3. Ghi chuỗi nhấn phím vào log file.
4. Chạy nền mà không hiển thị giao diện.

---

## Cài đặt & build

```bash
git clone https://github.com/iamdwn/keylogger.git
```
```bash
cd keylogger
```
```bash
dotnet build
```
```bash
dotnet run
```
