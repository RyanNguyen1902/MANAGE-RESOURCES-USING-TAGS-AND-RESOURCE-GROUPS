+++
title = "Thêm hoặc xóa tag "
date = 2020
weight = 2
chapter = false
pre = "<b>1.1.2 </b>"
+++


**Nội dung:**
- [Thêm hoặc xóa tag trên các tài nguyên đơn lẻ](#thêm-hoặc-xóa-tag-trên-các-tài-nguyên-đơn-lẻ)
- [Thêm hoặc xóa tag trên các nhóm các tài nguyên](#thêm-hoặc-xóa-tag-trên-các-nhóm-các-tài-nguyên)

#### Thêm hoặc xóa tag trên các tài nguyên đơn lẻ

**Thêm tag trên tài nguyên đơn lẻ:**
1. Truy cập **[Amazon EC2 Console](https://console.aws.amazon.com/ec2/)**.
2. Tại thanh điều hướng phía trên, chọn **Region** cần thao tác ( Hiện tại chúng ta đang dùng Region Singapore nư ở bước trước)
3. Tại thanh bên trái, chọn loại tài nguyên muốn gắn tag (ví dụ: **Instances**)
4. Click chọn tài nguyên cần gắn tag từ danh sách các tài nguyên, chọn vào tab **Tags**, và chọn **Manage tags**

![Tag](/images/tag/11ec2.png?width=90pc)

5. Chọn tiếp **Add tag**. Nhập thông tin *Key* và *Value* cho tag như hình dưới và nhấn **Save**.
 + Chúng ta đã thêm tag giúp xác định hệ điều hành cho EC2 Instance.
![Tag](/images/tag/12ec2.png?width=90pc)

#### Thêm hoặc xóa tag trên các nhóm các tài nguyên

1. Truy cập **[Amazon EC2 Console](https://console.aws.amazon.com/ec2/)**.
2. Tại thanh bên trái, chọn **Tags**
3. Chọn **Manage Tags**


![Tag](/images/tag/13ec2.png?width=90pc)

4. Tại trang **Manage Tags**, chọn loại tài nguyên cần lọc tại **Filter** (ví dụ: **Instances**)
5. Để thêm tag trên nhóm các tài nguyên:
    - Chọn các tài nguyên muốn gắn tag
    - Tại **Add Tag**, điền thông tin *Key* và *Value* của tag và chọn **Add Tag**

![Tag](/images/tag/14ec2.png?width=90pc)

6. Để xóa tag trên nhóm các tài nguyên:
    - Chọn các tài nguyên muốn xóa tag
    - Tại **Remove Tag**, điền thông tin *Key* và chọn **Remove Tag**.



