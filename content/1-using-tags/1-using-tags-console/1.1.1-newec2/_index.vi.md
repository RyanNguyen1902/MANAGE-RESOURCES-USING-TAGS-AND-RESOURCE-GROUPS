+++
title = "Tạo EC2 Instance có tag"
date = 2021
weight = 1
chapter = false
pre = "<b>1.1.1 </b>"
+++


#### Tạo EC2 Instance có tag

{{%notice tip%}}
Trong workshop này, chúng ta sẽ sử dụng Region Singapore ( ap-southeast-1 ). Nếu bạn muốn sử dụng Region khác , hãy đảm bảo chuyển Region về Region bạn muốn sử dụng khi tạo các tài nguyên liên quan tới workshop.
{{%/notice%}}

![region](/images/tag/1region.png?width=90pc)

1. Truy cập [**EC2 Management Console**](https://ap-southeast-1.console.aws.amazon.com/ec2/v2/home?region=ap-southeast-1#Instances).
  + Click **Launch Instances**.

![Tag](/images/tag/1ec2.png?width=90pc)


2. Trong giao diện **Launch Instances**.
  +	Chọn **Add additional tags**

![Tag](/images/tag/2ec2.png?width=90pc)

3. Thực hiện **Add tags** theo hình hướng dẫn.
  + Click **Add tags**.

| Key           | Value       |
| ------------- | ----------- |
| Owner         | Yourname    |
| Service       | Yourservice |
| Environment   | UAT         |

![Tag](/images/tag/3ec2.png?width=90pc)

{{%notice tip%}}
Bạn có thể tải về tham khảo tài liệu best practices hướng dẫn cách sử dụng tagging bên dưới.
{{%/notice%}}

{{%attachments style="orange" title="AWS Tagging Best practices" pattern=".*(pdf)"/%}}

4. Đối với **Amazon Machine Image**.
  + Các bạn giữ cấu hình mặc định.

![Tag](/images/tag/4ec2.png?width=90pc)


5. Đối với key pair, chọn **Create new key pair** .
  + Đặt tên **Key pair name** là **TestTagging**.
  + Chọn **Create new key pair** 

![Tag](/images/tag/5ec2.png?width=90pc)

6. Điền **Key pair name** là TestTagging. Sau đó chọn **Create key pair**. 

![Tag](/images/tag/6ec2.png?width=90pc)

7. Đối với phần **Networking**, giữ mặc định và chọn tick như hình hướng dẫn.

![Tag](/images/tag/7ec2.png?width=90pc)


8. Kiểm tra lại cấu hình và chọn **Launch instance**.
  + Click **Launch instance**.
  
  ![Tag](/images/tag/8ec2.png?width=90pc)

9. Hoàn thành **Launch instance**

  ![Tag](/images/tag/9ec2.png?width=90pc)

10. Quay lại giao diện **EC2**. Chọn **Instance** chọn instances vừa tạo.
  + Click tab **Tags** để kiểm tra các tag đã tạo.

  ![Tag](/images/tag/10ec2a.png?width=90pc)

11. Lặp lại các bước từ 1 - 10 để tạo thêm EC2 Instance có Tag như sau:

| Key | Value |
| ------ | ----------- |
| Owner   | Yourname |
| Service   | Yourservice |
| Environment   | Test |

 {{%notice tip%}}
Lưu ý ở bước cuối sau khi click **Launch** tại trang **Review Instance Launch**: \
\
 Chọn **Choose an existing key pair**. \
 Chọn key pair **TestTagging**. \
 Click chọn **I acknowledge that I have access to the corresponding private key file, and that without this file, I won't be able to log into my instance.** \
 Click **Launch**. \
 Click **View Instance**. \
\
 Chúng ta không cần tạo thêm key pair mới mà sử dụng key pair đã tạo trước đó để khởi tạo EC2 instance thứ 2.
{{%/notice%}}
![Tag](/images/tag/10ec2.png?width=90pc)
Bước tiếp theo chúng ta sẽ thực hiện thêm các Tag mới cho EC2 instance của chúng ta.
