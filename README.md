# Báo cáo: Xây dựng Honeypot/Honeynet để bẫy hacker

## Giới thiệu
Đây là báo cáo môn học "An toàn mạng máy tính" của Nhóm 5 về đề tài "Xây dựng Honeypot/Honeynet để bẫy hacker". Dự án tập trung vào việc thiết lập một môi trường giả lập nhằm thu hút, ghi lại và phân tích các hành vi tấn công từ hacker.

## Mục tiêu
* **Tổng quát:** Xây dựng và triển khai hệ thống Honeypot sử dụng Cowrie để giả lập dịch vụ SSH, ghi nhận các hành vi truy cập trái phép.
* **Cụ thể:**
    * Nghiên cứu vai trò của Honeypot trong giám sát và phát hiện tấn công.
    * Thiết kế, triển khai Honeypot để phát hiện tấn công brute-force và thu thập log.
    * Quan sát hành vi tấn công và đề xuất biện pháp bảo mật.

## Kiến trúc hệ thống
Hệ thống được thiết kế theo mô hình phân vùng mạng gồm ba khu vực:
1.  **Mạng bên ngoài (Internet/Attacker):** Máy tấn công dùng Kali Linux.
2.  **Vùng trung gian (DMZ):** Nơi đặt Honeypot (Cowrie) và Web Server (Apache) để bẫy và chuyển hướng tấn công.
3.  **Mạng nội bộ (Internal LAN):** Khu vực được bảo vệ bởi Firewall.

## Công cụ thực hiện
* **pfSense:** Router trung gian, cấu hình NAT và Virtual IP để bẻ lái lưu lượng tấn công.
* **Cowrie:** Honeypot giả lập SSH/Telnet để ghi lại hành vi tấn công.
* **Kali Linux:** Máy tấn công, sử dụng các công cụ như Nmap để quét và thực hiện tấn công.
* **Apache:** Web Server phục vụ dịch vụ web.

## Kết quả thực nghiệm
* Hệ thống đã triển khai thành công mô hình bẫy hacker.
* Các hoạt động tấn công như quét cổng, thử đăng nhập SSH (brute-force) và thực thi lệnh đều được ghi nhận chi tiết trong file log của Cowrie.
* Mô hình thực nghiệm đã đáp ứng đúng mục tiêu đề ra ban đầu.

## Thông tin nhóm thực hiện
* **Nhóm:** Nhóm 5 - Lớp: 14DHBM02
* **Thành viên:**
    * Đào Thị Khánh Chi - 2033230035
    * Lê Ngọc Phương Quỳnh - 2033230247
    * Trương Lê Trúc Quỳnh – 2033230246
    * Tống Lạc Lan Viên - 2033230322
* **Giảng viên hướng dẫn:** Đinh Huy Hoàng
