# HCM-KS26_NhapMonCNTT_Session16_Ex2# Bản thiết kế phân quyền: Bảng phân loại đối tượng tương ứng với các mức quyền truy cập an toàn nhất.
| vai trò | mức quyền tối ưu | quyền | mục đích bảo mật |
| :--- | :---: | :---: | ---: |
| Trưởng Bộ Phận | commenter | chỉ xem và để lại nhận xét | tránh vô tình chỉnh sửa,xóa bỏ hoặc làm lộ thông tin của các ứng viên |
| Trưởng phòng nhân sự | editor | có quyền chỉnh sửa cập nhật thông tin hoặc thay đổi thông tin của các ứng viên | đảm bảo cập thông tin của các ứng viên liên tục |
| ứng viên bên ngoài | | không có quyền truy cập vào thông tin nội bộ | đảm bảo bảo mật thông tin của các ứng viên khác | 
# Quy trình 3 bước xử lý khi phát hiện dữ liệu bị chia sẻ sai quyền.
- Bước 1 : vô hiệu hóa link chia sẻ và chỉnh sửa quyền truy cập 
> - xóa quyền cá nhân ( truy cập quản lý chia sẻ và tìm tài khoản của ứng viên bên ngoài sau đó ấn remove để xóa quyền của ứng viên đó ngay lập tức )
> - chuyển quyền chia sẻ công khai sang chế độ người mời
- Bước 2 : kiểm tra nhật ký truy cập của ứng viên
> - kiểm tra trong khoảng thời gian ứng viên giữ quyền editor
> - kiểm tra ip truy cập của tài khoản đó
- Bước 3 : khôi phục
> - khôi phục dữ liệu : vào version history và chọn mốc thời gian xảy ra lỗi sau đó nhấn restore
