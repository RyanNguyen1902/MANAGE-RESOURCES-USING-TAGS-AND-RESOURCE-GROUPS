+++
title = " Tạo một Resource Group"
date = 2021-07-09T14:42:20+07:00
weight = 2
chapter = false
pre = "<b>2. </b>"
+++


#### Tạo một Resource Group 
Ở bước này, bạn sẽ tạo một Resource Group được phân loại theo thẻ.
1. Truy cập vào [AWS Resource Group Console](https://console.aws.amazon.com/resource-groups)
2. Ở thanh bên trái, click chọn **Create Resource Group**
3. Ở trang **Create query-based group**, dưới mục **Group type**, chọn **Tag-based** để tạo một Resource Group được phân loại theo thẻ. 
4. Ở mục **Grouping criteria**, làm theo hướng dẫn sau:
    - Chọn **Resource types** (*loại tài nguyên*) là **AWS::EC2::Instance**. Bạn có thể chọn tối đa 20 loại tài nguyên.

![Tag](/images/2/1gr.png?width=90pc)

5. Dưới **Tags**, nhập thẻ **"Key=BusinessUnit,Value=Marketing"** và sau đó nhấn **Add** để thêm thẻ.
6. Click **Preview group resources** để thể hiện ở mục **Group Resources** các tài nguyên có loại tài nguyên và thẻ đã nêu ở trên.


![Tag](/images/2/2gr.png?width=90pc)


7. Ở mục **Group details**, nhập các thông số sau:
    - Group name: **MarketingBU**
    - Group description - optional: nhập mô tả cho Resource Group (ví du: **Servers of Marketing BU**)
    - Kiểm tra và click **Create group**.

![Tag](/images/2/3gr.png?width=90pc)  

{{%notice tip%}}

Ở mục **Group tags - optional**, chúng ta tạm thời bỏ qua.\
Tuy nhiên, nếu bạn muốn Resource Group đang được tạo trở thành con của một Resource Group lớn hơn, bạn có thể thêm thẻ cho Resource Group. (Ví dụ: **"Key=Organization,Value=AWS"**)
{{%/notice%}}


8. Sau khi Resource Group đã tạo thành công.
  + Click **Saved Resource Group** để xem các Resource Group chúng ta đã tạo.

![Tag](/images/2/5gr.png?width=90pc)  

![Tag](/images/2/6gr.png?width=90pc)  

9. Click vào Resource Group **MarketingBU**.

10. Kéo xuống mục **Group resources**, bạn sẽ thấy tất cả các tài nguyên thuộc Resource Group này.

![Tag](/images/2/7gr.png?width=90pc)  



