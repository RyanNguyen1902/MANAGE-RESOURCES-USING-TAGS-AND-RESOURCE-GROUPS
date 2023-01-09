+++
title = "Quản lý tài nguyên bằng Tag"
date = 2021
weight = 1
chapter = false
+++

# Quản lý tài nguyên bằng Tag và Resource Groups

#### Tổng quan

Để giúp quản lý các máy ảo, ổ đĩa và các tài nguyên khác của EC2, bài lab này sẽ giúp bạn thực hành gán các metadata của mỗi tài nguyên dưới dạng **Tag** (*Thẻ*) và sử dụng **Resource Group** .

#### Tag (thẻ)

**Tag (Thẻ)** là nhãn mà bạn gán cho tài nguyên AWS. Mỗi thẻ bao gồm một khóa (Key) và một giá trị tùy chọn (Value). 

Thẻ cho phép phân loại tài nguyên AWS của mình theo nhiều cách khác nhau: theo mục đích, theo chủ sở hữu hoặc môi trường. Điều này trở nên hữu ích khi có nhiều tài nguyên cùng loại, giúp nhanh chóng xác định một tài nguyên cụ thể dựa trên các tag đã được gán cho nó. 

#### AWS Resource Groups
**AWS Resource Groups** là một tính năng cho phép bạn quản lý và tự động hóa các thao tác cho nhiều tài nguyên cùng một lúc. Một **Resoucre Group** là một nhóm các tài nguyên được phân loại theo **thẻ** (*Tag-based*) hoặc theo CloudFormation stack (*CloudFormation stack-based*).


#### Nội dung
1. [Sử dụng tag](1-write-contents)
2. [Tạo một Resource Group](2-resource-group)
3. [Dọn dẹp tài nguyên](3-cleanup)
