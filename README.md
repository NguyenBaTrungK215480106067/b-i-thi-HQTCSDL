# CHƯƠNG TRÌNH QUẢN LÝ KHO HÀNG NHÀ HÀNG LẨU NƯỚNG
Mô tả bài toán quản lý: Quản lý kho hàng cho một nhà hàng lẩu nướng là một bài toán phức tạp, bao gồm nhiều khía cạnh từ theo dõi hàng tồn kho, đặt hàng, tiếp nhận hàng hóa, kiểm kê, đến quản lý hạn sử dụng của các nguyên liệu. Bài tập sử dụng ngôn ngữ SQl để quản lý lượng kho hàng.

## Những chức năng xây dựng để quản lý kho hàng lẩu nướng:
1. Quản lý danh mục hàng hóa
-   Thêm/sửa/xóa hàng hóa: Cho phép quản lý thêm mới, chỉnh sửa thông tin và xóa hàng hóa khỏi danh mục.
Danh mục hàng hóa: Quản lý các thông tin cơ bản của hàng hóa như tên, mã hàng, đơn vị tính, nhóm hàng (thịt, rau, gia vị, đồ uống, v.v.).
2. Quản lý tồn kho
- Theo dõi tồn kho: Hiển thị số lượng hiện tại của từng mặt hàng, cập nhật tự động khi có giao dịch nhập/xuất kho.
Cảnh báo tồn kho: Thiết lập ngưỡng cảnh báo (tồn kho tối thiểu/tối đa) để hệ thống tự động thông báo khi hàng hóa gần hết hoặc dư thừa.
3. Quản lý nhập hàng
- Lập đơn hàng nhập: Tạo và quản lý các đơn đặt hàng từ nhà cung cấp.
Tiếp nhận hàng hóa: Xác nhận số lượng và chất lượng hàng hóa nhập kho, cập nhật số liệu tồn kho.
4. Quản lý tiêu thụ nguyên liệu
- Ghi nhận tiêu thụ hàng ngày: Ghi nhận lượng nguyên liệu tiêu thụ hàng ngày từ bếp.
Phân tích tiêu thụ: Tạo các báo cáo phân tích tiêu thụ nguyên liệu để dự báo nhu cầu.
## Nhập xuất và báo cáo các thông tin liên quan đến kho hàng nhà hàng lẩu nướng:
1. Quản lý nhập kho
- Kiểm tra hàng hóa: Kiểm tra chất lượng, số lượng hàng hóa thực tế so với phiếu nhập kho.
- Cập nhật tồn kho: Sau khi kiểm tra, số lượng hàng hóa sẽ được cập nhật vào hệ thống tồn kho.
2. Quản lý xuất kho
- Kiểm tra hàng hóa: Kiểm tra số lượng hàng hóa cần xuất theo phiếu xuất kho.
- Cập nhật tồn kho: Sau khi xuất kho, số lượng hàng hóa sẽ được cập nhật vào hệ thống tồn kho.
3. Quản lý tồn kho
- Cập nhật tồn kho: Tự động cập nhật số lượng tồn kho khi có giao dịch nhập/xuất kho.
- Kiểm kê tồn kho: Lập kế hoạch và thực hiện kiểm kê định kỳ hoặc đột xuất, ghi nhận kết quả kiểm kê vào hệ thống.
   Như vậy, dựa theo những thông tin mà ta đã thu thập được chúng ta sẽ xây dựng các bảng đáp ứng yêu cầu quản lý kho hàng nhà hàng lẩu nướng.
  Tạo các bảng như mô tả trong SQL Sever:

1. Bảng sản phẩm

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/002b0e36-ebc9-4b8a-90bf-950f49c13e54)

2. nhà cung cấp

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/bda66f54-fc52-4549-9842-0e2929ce7f22)


3. đơn hàng nhập kho

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/074317dc-e0f9-4d03-b24d-b0fe7b96ec50)

4. chi tiết đơn hàng nhập kho

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/8551b2de-56f9-4933-8fd8-870214bdb78c)

5. đơn hàng xuất kho

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/11db1fe4-1a6a-4efa-bf66-03ed62114b12)

6. chi tiết đơn hàng xuất kho

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/b3022fc3-d5f8-456e-8df2-76eaa71ba4b7)

7. kho hàng

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/58b50146-1ac0-48f2-80da-6608cf72e0db)

Tạo sơ đồ thực thể liên kết giữa các bảng:

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/db3e6f74-301d-4e40-96a6-d4b51f9e9aa2)

 **nhập dữ liệu bảng sản phẩm**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/49cee195-f2f7-4cc7-9566-13ad0770daaf)


** nhập dữ liệu bảng Chi tiết đơn hàng nhập kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/79a1a904-8b13-41de-8614-45b88d1a948e)

**nhập dữ liệu đơn hàng nhập kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/ea67fc44-3d05-464f-b51a-ff48743d5145)

**nhập dữ liệu đơn hàng xuất kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/1f665b58-b4a1-46aa-97db-013e728ef970)

**nhập dữ liệu kho hàng**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/1d638421-a25d-4621-99f7-e1e2f9c5dc42)

**nhập dữ liệu nhà cung cấp**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/2f16d218-ab88-458c-bace-a1a9751413f6)


## XÂY DỰNG CÁC THỦ TỤC THEO CÁC CHỨC NĂNG MONG MUỐN

 **Tạo bảng sản phẩm**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/1be389d9-b12a-4a86-872a-c7510140052c)

** để thêm hàng hóa mới**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/1be389d9-b12a-4a86-872a-c7510140052c)
![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/69251b11-7461-4843-9d3f-54b8b2d4371b)


Thêm thông tin hàng hóa thành công

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/9dcc5815-9955-43d1-b7ff-c0b339238b76)


** để sửa thông tin hàng hóa**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/6c7a5476-a751-437d-a62f-9e1c786e94ea)

Sửa thông tin hàng hóa thành thành công

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/01dd905f-9dc6-415c-a698-15e9d7605103)


  **để xóa hàng hóa****

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/3ad3048d-dbd5-4dd5-b390-40119cc02670)

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/16b0470e-f699-4600-8a7f-f45e49278915)

**Xóa hàng hóa**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/123e10a0-0c89-44de-9d87-347c2f00d9a7)

xóa hàng hóa thành công

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/6903401b-e61e-427d-b6ce-c92f40b88f5e)



## Để quản lý tồn kho, chúng ta cần theo dõi số lượng hiện tại của từng mặt hàng và thiết lập các cảnh báo tồn kho khi hàng hóa gần hết hoặc dư thừa. Dưới đây là cách thực hiện quản lý tồn kho trong hệ thống quản lý kho hàng nhà hàng lẩu nướng bằng SQL.

1. Tạo bảng Tồn kho

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/85d2b324-05c3-477a-b9ce-bfc6fe0ab6b8)

2.  để cập nhật tồn kho khi có giao dịch nhập/xuất kho
**Nhập kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/870cfdad-a089-4fc9-b119-8e91a127d51b)


**Xuất kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/669fff5d-03fb-4ed4-aeba-64f3fffb3274)


3. Cảnh báo tồn kho

Thủ tục kiểm tra tồn kho tối thiểu

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/80b2e3ad-3be2-492c-a87b-a39ca16cecc0)

**Thủ tục kiểm tra tồn kho tối đa**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/4fe4b9d5-61bb-4e23-bf13-d30ddf9dd7d3)

Sử dụng các thủ tục lưu trữ

**Nhập kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/71a119dd-3437-48b8-8b71-cbab56237165)


**Kiểm tra tồn kho tối thiểu**   

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/699efea2-5b00-40b2-920f-4290c580297c)

**Kiểm tra tồn kho tối đa**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/af7aa3c7-07fc-4b36-9b66-275e436c2e94)


Dưới đây là mã SQL để quản lý nhập hàng, bao gồm việc lập đơn hàng nhập và tiếp nhận hàng hóa.

**1. Tạo bảng (Đơn hàng nhập kho)**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/7dc7b366-b3d4-4a8e-8404-8588bf53aa27)

**Bảng Chi tiết đơn hàng nhập kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/32c694c2-471c-4aa3-97ee-410f4dacc414)

**2.  để lập đơn hàng nhập kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/82bc2151-c3ef-4627-ab7e-f0c9534471f0)


**3. Stored Procedure để thêm chi tiết đơn hàng nhập kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/9dcbc35b-70f2-4c4c-ac1f-078e27e57907)


**4. Stored Procedure để tiếp nhận hàng hóa và cập nhật tồn kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/bdeb3cd2-e611-4739-8228-166431a52bc5)

**Lập đơn hàng nhập kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/dee614db-f670-4ec9-a3f4-a3806aa61744)

**Thêm chi tiết cho đơn hàng nhập kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/8f4043bc-7b22-4232-bdca-e2edaeb3d500)


**Tiếp nhận hàng hóa và cập nhật tồn kho**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/5cebbb7a-2a0d-49e5-b106-9eebc75ab988)

kết quả của xuất và nhập kho

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/0af06bbf-75fe-4262-ab3d-289bdcbec51f)


## Để quản lý tiêu thụ nguyên liệu, chúng ta cần ghi nhận lượng nguyên liệu tiêu thụ hàng ngày và tạo các báo cáo phân tích tiêu thụ nguyên liệu để dự báo nhu cầu. Dưới đây là các bước thực hiện:

**1. Tạo bảng để ghi nhận tiêu thụ hàng ngày**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/c22721d8-6b5c-4433-a2aa-28a18aae7b5f)

**2.  để ghi nhận tiêu thụ hàng ngày**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/a5e2100b-67a3-433f-84d3-a5f444ebcac2)


**3. Báo cáo phân tích tiêu thụ nguyên liệu**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/020b1748-74f4-46e4-b025-2042c73c9273)

**Báo cáo tiêu thụ hàng tháng**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/775d6e41-2e23-4879-ad9f-bd79f4da95e3)

**Ghi nhận tiêu thụ hàng ngày**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/cbd754bd-fb84-4b68-ab81-f0f1347b9a2b)

**Báo cáo tiêu thụ hàng ngày
**
![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/56d6360a-49a1-4427-8706-02f33953628c)

thêm báo cáo tiêu thụ hàng ngày thành công
![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/a7d46b6f-12bf-418b-9b8c-961cb2ec47c9)


**Báo cáo tiêu thụ hàng tháng**

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/5408a0de-8e5e-45d9-b1c6-c25a3cb7760d)

kết quả báo cáo tiêu thụ hàng tháng

![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/748f4f8d-6a7c-40cb-af8b-7b5de5b79ad5)

 
