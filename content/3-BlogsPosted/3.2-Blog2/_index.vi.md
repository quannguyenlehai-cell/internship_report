---
title: "Blog 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---
# MÌNH ĐÃ HỌC ĐƯỢC NHỮNG GÌ SAU KHI TRẢI NGHIỆM AWS IOT CORE.

Gần đây, mình có thời gian đào sâu nghiên cứu và áp dụng AWS IOT Core vào các dự án phần cứng và hệ thống nhúng. Từ lúc chuyển sang AWS IOT Core, tư duy làm hệ thống IOT của mình đã thay đổi khá nhiều. Dưới đây là một vài góc nhìn và bài học rút ra sau quá trình thực thi.

## Giao thức MQTT với độ trễ thấp.
Khi dùng các vi điều khiển như ESP32, tài nguyên phần cứng và băng thông là rào cản lớn. AWS IOT Core hỗ trợ MQTT một cách tối ưu cho các vi điều khiển , giúp việc gửi payload, hay nhận điều khiển actuator (như servo) diễn ra ngay mà không tốn tài nguyên.

## Bảo mật tốt với (X.509 Certificates và IAM Policy)
Mỗi thiết bị khi kết nối đều có X.509 Cryptographic Certificate, Âmzon Root CA, Fine-granted IAM Policies riêng để giới hạn thiết bị nào được phép Publish hay Subscibe vào topic nào. 

## Hệ sinh thái đồng bộ serverless
AWS IOT Core có khả năng kết nối không có khoảng cách với các dịch vụ Serverless. Với IOT Rules Engine, dữ liệu có thể được gửi qua AWS Lambda để xử lý logic cho backend mà không cần server hoạt động liên tục. IOT Core cũng có thể kết hợp với AWS RDS để lưu trữ thông tin người dùng và đẩy lên AWS Amplify.

Tóm lại. AWS IOT Core là cầu nối giữa phần cứng và hạ tầng cloud. Dù mất đôi chút thời gian để cấu hình Certificate và IAM Policy, nhưng hệ thống hoạt động mượt mà, đáng tin cậy và sẵn sàng scale up.

https://docs.aws.amazon.com/iot/latest/developerguide/what-is-aws-iot.html

[Link bài viết](https://www.facebook.com/share/p/1BhrwMoQHS/)