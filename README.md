# Smart Food – Phân tích rủi ro và khôi phục dữ liệu

## Phần 1. Phân tích thảm họa dữ liệu truyền thống

1. **Mất code do ghi đè:** Nam xóa nhầm đoạn code rồi nhấn `Ctrl + S`, khiến bản đang làm việc bị thay đổi.
2. **Xung đột phiên bản:** Nhiều file như `main_v1.py`, `main_v2_final.py` làm cả nhóm khó biết đâu là bản mới nhất.
3. **Nguy cơ mất toàn bộ dữ liệu:** Nếu máy hỏng, mất hoặc ổ cứng lỗi, các file chỉ lưu trên máy có thể mất theo.
4. **Khó cộng tác:** Gửi file qua Zalo dễ gây trùng lặp, sửa nhầm bản và không theo dõi được ai đã thay đổi gì.

**Kết luận:** Lưu nhiều bản trên cùng một máy không thay thế được sao lưu và lịch sử phiên bản.

## Phần 2. Thiết lập Hybrid Workflow (Local + Cloud)

**Công cụ:** VS Code và OneDrive.

1. **Thiết lập:** Đăng nhập OneDrive trên máy và tạo thư mục `OneDrive/SmartFood/`.
2. **Làm việc cục bộ:** Đặt file `main.py` trong thư mục này và viết code bằng VS Code như bình thường, kể cả khi tạm mất mạng.
3. **Đồng bộ:** Sau khi nhấn `Ctrl + S`, OneDrive tự đồng bộ file lên Cloud khi có Internet. Kiểm tra trạng thái đồng bộ thành công.
4. **Khôi phục:** Vào **onedrive.com** → chọn `main.py` → **Version history (Lịch sử phiên bản)** → chọn bản trước khi xóa nhầm → **Restore (Khôi phục)**.
5. **Cộng tác:** Dùng Git/GitHub để quản lý thay đổi code của cả nhóm, thay vì gửi nhiều file `final` qua Zalo.

**Kết quả:** Nam vẫn code nhanh trên máy, có bản lưu trên Cloud và có thể khôi phục phiên bản cũ bằng thao tác **Restore**.

> **Lưu ý:** Version History chỉ khôi phục được các phiên bản đã được đồng bộ lên OneDrive. Nếu file trước đó chỉ nằm trên máy, không thể mặc định khôi phục bằng tính năng này.
