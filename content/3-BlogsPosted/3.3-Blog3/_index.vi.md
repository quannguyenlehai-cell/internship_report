---
title: "Blog 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---
Đồ án 2 tháng thực tập: Hệ thống mở cửa bằng khuôn mặt

Đây là một hệ thống kiểm soát cửa ra vào thông minh kết hợp giữa phần cứng AI giá rẻ (Edge-AI) và hạ tầng đám mây (AWS Serverless)
1. Ý tưởng
Trong thực tế, các cách khóa cửa hiện tại đều có nhược điểm riêng:
- Chìa khóa cơ & thẻ từ: Dễ mất, dễ quên hoặc bị copy.
- Mật khẩu PIN: Dễ bị nhìn lén.
- Khóa quét mặt trên đám mây: Thường đắt đỏ, bị trễ.
Mục tiêu: Làm ra một hệ thống quét mặt mở cửa siêu rẻ (tiền phần cứng chưa tới 400k), quản trị viên quản lý ra vào từ xa qua web.
2. Cách hệ thống hoạt động
Mô hình được chia làm 2 phần chính:
- Tại cửa (ESP32-CAM)
Mọi việc nhận diện khuôn mặt đều được xử lý ngay trên con chip ESP32-CAM
Đứng trước camera->Chip quét mặt ->Khớp dữ liệu -> Mở khóa (độ trễ chưa tới 0.5 s).
- Tại đám mây (Hạ tầng AWS)
AWS IoT Core: nhận dữ liệu từ thiết bị.
AWS Lambda: Tự động "thức dậy" nhận dữ liệu.
AWS Amplify & API Gateway: Tạo 1 trang web cho quản trị viên xem ai vừa ra vào, thêm người dùng mới, hoặc đóng mở từ xa.

3. Những điểm nổi bật của dự án
Gía thành siêu hạt dẻ: chi phí phần cứng cho 1 cụm cửa chỉ khoảng 400k - rẻ hơn gần 90% so với các bộ khóa thông minh thương mại.
Tối ưu chi phí cloud: Nhờ dùng backend serverless, hệ thống tự động mở rộng khi có người dùng và gần như không tốn chi phí khi nhàn rỗi
Độ trễ siêu thấp: Việc xử lý AI ngay tại thiết bị đầu cuối giúp kích hoạt mở ngay lập tức.
Lời kết
Chỉ sau 2 tháng, từ 1 sinh viên còn bỡ ngỡ với khái niệm cloud, việc tự tay xây dựng 1 dự án kết hợp Iot và Serverless đã giúp mình hiểu hơn rất nhiều về kiến thức hệ thống thực tế.
— với Lehaiquan Nguyên.

[Link Facebook](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2225859081512385/?rdid=edl9gIuvqI9LEabB#)