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
![image](https://github.com/NguyenBaTrungK215480106067/b-i-thi-HQTCSDL/assets/170510747/7aece371-1bb1-4550-baa1-6ad821464bbe)

 








  
