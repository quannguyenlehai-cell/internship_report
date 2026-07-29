---
title: "Blog 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

Những gì mình học được sau 2 tháng "mò mẫm" AWS 
Lambda 
Là 1 sinh viên mới nhập môn Cloud được chưa đầy 2 tháng, thú thât là ban đầu mình thấy AWS khá "khoai". Hàng trăm dịch vụ với đống thuật ngữ tiếng Anh phức tạp làm mình rất ngợp. Tuy nhiên, khi bắt đầu làm bài tập với AWS Lambda, mọi thứ dần trở nên dễ hiểu hơn rất nhiều.
Dưới đây là những bài học cơ bản nhất mình rút ra được sau vài tuần tự học.
1. Không cần quản lý máy chủ (Serverless)
Bình thường khi làm bài tập lớn, chúng mình hay phải chạy 1 server ở máy local và để nó chạy liên tục 24/7 để chờ ứng dụng gọi đến.
Nhưng đối với AWS Lambda, bạn chỉ cần quăng đoạn code của mình lên cloud. AWS sẽ tự lo phần máy chủ bên dưới. Bạn không cần cài hệ điều hành, không cần lo vasloiox hệ thống hay sợ máy chủ bị quá tải.
2. Code chỉ chạy khi có "sự kiên"(Trigger)
Hàm Lambda không ngồi chạy vĩnh viễ. Nó chỉ "thức dậy" khi có 1 sự kiện nào đó kích hoạt:
- Có người tải 1 flie  lên hệ thống.
- Có  người bấm nút trên giao diện web/app.
- Có dữ liệu được thêm vào database.
Ngay khi sự kiện xảy ra, Lambda sẽ chạy code của bạn, trả về  kết quả rồi tự động tắt.
3. Cực kì phù hợp với túi tiền sinh viên
Vì lambda chỉ chạy khi có sự kiện, nên bạn chỉ trả tiền cho đúng số mili-s mà code thực sự chạy
- nếu không ai dùng app của bạn - chi phí = 0 đồng.
- AWS còn có gói free tier cho dùng thử miễn phí khá nhiều mỗi tháng, nên làm đồ án khá thoải mái không sợ bị trừ tiền oan.
4. Kinh nghiệm cá nhân - đừng viết code quá tham
Lúc mới học, sai lầm của mình là bê nguyên cả cái backend nhét hết vô 1 hàm Lambda, khiến code vừa chậm vừa khó fix.
Sau 2 tháng, mình nhận ra nên chia nhỏ công việc:
- 1 hàm đăng kí tài khoản
- 1 hàm làm nhiệm vụ lưu dữ liệu 
- ...
Tóm lại là...
Nếu bạn mỡi học Cloud và chỉ có thời gian ngắn để chuẩn bị. AWS Lambda là phần rất đáng để thử. Bạn không cần là chuyên gia về hạ tầng mạng hay máy chủ chỉ cần tập trung viết đúng đoạn code cần là xong— với Lehaiquan Nguyên.

[Link Bài viết](httpshttpswww.facebook.com/groups/awsstudygroupfcj/permalink/2225735151524778/?rdid=LGtwaQotLkeDI1a7#)