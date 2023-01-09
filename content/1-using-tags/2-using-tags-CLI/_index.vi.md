+++
title = "Sử dụng tag bằng CLI"
date = 2020
weight = 2
chapter = false
pre = "<b>1.2. </b>"
+++
#### Tổng quan

Trong bước này, bạn sẽ tập làm quen với các thao tác với tag trên AWS CLI.

{{% notice note %}}
Để làm được bước này, bạn cần cài đặt **AWS CLI** trên máy của bạn. Nếu bạn chưa cài đặt **AWS CLI**, bạn có thể tham khảo phần 1 và 2 của workshop [000011 - Sử dụng AWS CLI trên Windows/Ubuntu](https://000011.awsstudygroup.com/vi/)
{{% /notice %}}

**Nội dung:**
- [Tổng quan](#tổng-quan)
- [Thêm tag cho tài nguyên hiện có](#thêm-tag-cho-tài-nguyên-hiện-có)
- [Thêm tag cho tài nguyên mới](#thêm-tag-cho-tài-nguyên-mới)
- [Mô tả các tài nguyên được gắn tag](#mô-tả-các-tài-nguyên-được-gắn-tag)

#### Thêm tag cho tài nguyên hiện có
1. Sử dụng CLI *```create-tags```* với tham số *```--resources```* và *```--tags```* 
    ```bash
    aws ec2 create-tags --resources <ResourceID> --tags Key=<Key>,Value=<Value>
    ```
2. Ví dụ: bạn muốn tạo tag là **"Key=Environment,Value=Test"** cho tài nguyên là một EC2 instance. Vậy, tham số của bạn sẽ là:
    ```bash
    aws ec2 create-tags --resources i-01234example56789 --tags Key=Environment,Value=Test
    ```

![1.2_TagResource](../../../images/tag2/1cli.png?width=90pc)

#### Thêm tag cho tài nguyên mới

**Thêm tag cho máy ảo mới**

1. Sử dụng CLI *```run-instances```* để tạo máy ảo mới và dùng tham số *```--tag-spectifications```* để khai báo thông tin tag như sau:
    ```bash
    aws ec2 run-instances\
    --image-id <image-id> \
    --count 1 \
    --instance-type t2.micro \
    --key-name <YourKeyPair> \
    --subnet-id <YouSubnetID> \
    --tag-specifications ResourceType=instance,Tags=[{Key=Environment,Value=Test}] ResourceType=volume,Tags=[{Key=Environment,Value=Test}] 
    #Volume được tạo cùng instace cũng sẽ có tag "Key=Environment,Value=Test"
    ```
2. **Lưu ý**: Bạn sẽ phải thay thế những tham số phù hợp với tài khoản của bạn. Hình dưới đây là một ví dụ:

![1.2_CreateEC2](../../../images/tag2/2cli.png?width=90pc)

**Thêm tag cho ổ đĩa mới**

1. Sử dụng CLI *```create-volume```* để tạo volume mới và dùng tham số *```--tag-specifications```* để khai báo thông tin tag như sau:
    ```bash
    aws ec2 create-volume \
    --availability-zone ap-southeast-1a \
    --volume-type gp2 \
    --size 80 \
    --tag-specifications ResourceType=volume,Tags=[{Key=Environment,Value=Test},{Key=cost-center,Value=cc123}]
    #Volume được tạo sẽ được gán 2 tag là "Key=Environment,Value=Test" và "Key=cost-center,Value=cc123"
    ```
2. **Lưu ý**: Bạn sẽ phải thay thế những tham số phù hợp với tài khoản của bạn. Hình dưới đây là một ví dụ:

![1.2_CreateVolume](../../../images/tag2/3cli.png?width=90pc)

#### Mô tả các tài nguyên được gắn tag
1. Sử dụng CLI *```derscibe-instances```* với tham số *```--filters```*:
    ```bash
    aws ec2 describe-instances --filters Name=tag-key,Values=<SampleTagKey>
    ```
2. Hình dưới dây là một ví dụ:

![1.2_Describe](../../../images/tag2/4cli.png?width=90pc)

