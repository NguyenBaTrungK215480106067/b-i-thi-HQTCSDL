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

 **nhập dữ liệu bảng sản phẩm**
 
 INSERT INTO Products (ProductID, ProductName, ProductCategory, Unit, PricePerUnit, Description, Image)
VALUES
(1, 'Thịt bò tươi', 'Thịt', 'kg', 250000, 'Thịt bò tươi nhập khẩu', 'image_url_1'),
(2, 'Thịt gà ta', 'Thịt', 'kg', 180000, 'Thịt gà ta nuôi tự nhiên', 'image_url_2'),
(3, 'Hải sản tổng hợp', 'Hải sản', 'kg', 350000, 'Hải sản tổng hợp tươi ngon', 'image_url_3'),
(4, 'Nấm hương', 'Rau củ', 'kg', 90000, 'Nấm hương tươi từ Đà Lạt', 'image_url_4'),
(5, 'Rau cải xanh', 'Rau củ', 'kg', 30000, 'Rau cải xanh tươi', 'image_url_5'),
(6, 'Bắp cải', 'Rau củ', 'kg', 25000, 'Bắp cải tươi', 'image_url_6'),

** nhập dữ liệu bảng Chi tiết đơn hàng nhập kho**
 
 INSERT INTO PurchaseOrderDetails (PurchaseOrderDetailID, PurchaseOrderID, ProductID, Quantity, PricePerUnit)
VALUES
(1, 1, 1, 50, 250000),  -- Đơn hàng nhập 1, Sản phẩm 1 (Thịt bò tươi), số lượng 50 kg, giá 250,000 đồng/kg
(2, 1, 2, 30, 180000),  -- Đơn hàng nhập 1, Sản phẩm 2 (Thịt gà ta), số lượng 30 kg, giá 180,000 đồng/kg
(3, 1, 5, 100, 30000),  -- Đơn hàng nhập 1, Sản phẩm 5 (Rau cải xanh), số lượng 100 kg, giá 30,000 đồng/kg
(4, 2, 3, 20, 350000),  -- Đơn hàng nhập 2, Sản phẩm 3 (Hải sản tổng hợp), số lượng 20 kg, giá 350,000 đồng/kg
(5, 2, 7, 50, 40000),   -- Đơn hàng nhập 2, Sản phẩm 7 (Gia vị lẩu thái), số lượng 50 gói, giá 40,000 đồng/gói
(6, 3, 4, 40, 90000),   -- Đơn hàng nhập 3, Sản phẩm 4 (Nấm hương), số lượng 40 kg, giá 90,000 đồng/kg
(7, 3, 6, 60, 25000),   -- Đơn hàng nhập 3, Sản phẩm 6 (Bắp cải), số lượng 60 kg, giá 25,000 đồng/kg
(8, 4, 8, 70, 45000),   -- Đơn hàng nhập 4, Sản phẩm 8 (Gia vị lẩu hải sản), số lượng 70 gói, giá 45,000 đồng/gói
(9, 4, 9, 100, 20000),  -- Đơn hàng nhập 4, Sản phẩm 9 (Nước tương), số lượng 100 chai, giá 20,000 đồng/chai
(10, 5, 10, 150, 15000), -- Đơn hàng nhập 5, Sản phẩm 10 (Đồ uống có ga), số lượng 150 chai, giá 15,000 đồng/chai
(11, 5, 11, 200, 10000), -- Đơn hàng nhập 5, Sản phẩm 11 (Nước khoáng), số lượng 200 chai, giá 10,000 đồng/chai
(12, 6, 12, 50, 60000);  -- Đơn hàng nhập 6, Sản phẩm 12 (Trái cây tươi), số lượng 50 kg, giá 60,000 đồng/kg

**nhập dữ liệu đơn hàng nhập kho**

INSERT INTO PurchaseOrders (PurchaseOrderID, SupplierID, OrderDate, ExpectedDeliveryDate, ActualDeliveryDate, Status, TotalAmount, Notes)
VALUES
(1, 1, '2024-06-01', '2024-06-05', '2024-06-04', 'Đã nhận', 18500000, 'Đơn hàng thịt và rau củ từ nhà cung cấp A'),
(2, 2, '2024-06-03', '2024-06-07', '2024-06-06', 'Đã nhận', 15000000, 'Đơn hàng hải sản và gia vị từ nhà cung cấp B'),
(3, 3, '2024-06-05', '2024-06-10', '2024-06-09', 'Đã nhận', 5100000, 'Đơn hàng nấm và bắp cải từ nhà cung cấp C'),
(4, 4, '2024-06-07', '2024-06-12', '2024-06-11', 'Đã nhận', 5900000, 'Đơn hàng gia vị và nước tương từ nhà cung cấp D'),
(5, 5, '2024-06-10', '2024-06-15', '2024-06-14', 'Đã nhận', 6000000, 'Đơn hàng đồ uống từ nhà cung cấp E'),

**nhập dữ liệu đơn hàng xuất kho**

INSERT INTO SalesOrders (SalesOrderID, OrderDate, DeliveryDate, Status, TotalAmount, Notes)
VALUES
(1, '2024-06-15', '2024-06-16', 'Đã giao', 12000000, 'Đơn hàng xuất cho chi nhánh A'),
(2, '2024-06-16', '2024-06-17', 'Đã giao', 8500000, 'Đơn hàng xuất cho chi nhánh B'),
(3, '2024-06-17', '2024-06-18', 'Đã giao', 15000000, 'Đơn hàng xuất cho chi nhánh C'),
(4, '2024-06-18', '2024-06-19', 'Đã giao', 5000000, 'Đơn hàng xuất cho chi nhánh D'),
(5, '2024-06-19', '2024-06-20', 'Đã giao', 7000000, 'Đơn hàng xuất cho chi nhánh E'),

**nhập dữ liệu kho hàng**

INSERT INTO Inventory (InventoryID, ProductID, BatchNumber, StockQuantity, ExpiryDate, StorageLocation, LastUpdated, Notes)
VALUES
(1, 1, 'BATCH001', 100, '2024-12-31', 'Kho lạnh 1', '2024-06-15', 'Lô thịt bò tươi nhập từ nhà cung cấp A'),
(2, 2, 'BATCH002', 60, '2024-11-30', 'Kho lạnh 2', '2024-06-16', 'Lô thịt gà ta nhập từ nhà cung cấp B'),
(3, 3, 'BATCH003', 30, '2024-07-15', 'Kho lạnh 3', '2024-06-17', 'Lô hải sản tổng hợp nhập từ nhà cung cấp C'),
(4, 4, 'BATCH004', 40, '2024-08-01', 'Kho mát 1', '2024-06-18', 'Lô nấm hương tươi nhập từ nhà cung cấp D'),
(5, 5, 'BATCH005', 120, '2024-06-30', 'Kho mát 2', '2024-06-19', 'Lô rau cải xanh nhập từ nhà cung cấp E'),
(6, 6, 'BATCH006', 80, '2024-07-05', 'Kho mát 3', '2024-06-20', 'Lô bắp cải nhập từ nhà cung cấp F'),

**nhập dữ liệu nhà cung cấp**
  INSERT INTO Suppliers (SupplierID, SupplierName, ContactPerson, PhoneNumber, Email, Address, Description)
VALUES
(1, 'Công ty Thực phẩm An Bình', 'Nguyễn Văn A', '0901234567', 'nguyenvana@anbinhfood.com', '123 Đường ABC, Quận 1, TP.HCM', 'Chuyên cung cấp thịt bò và thịt gà tươi.'),
(2, 'Hải Sản Tươi Ngon', 'Trần Thị B', '0902345678', 'tranthib@haisantuoingon.com', '456 Đường DEF, Quận 2, TP.HCM', 'Chuyên cung cấp hải sản tươi sống.'),
(3, 'Rau Củ Sạch Đà Lạt', 'Lê Văn C', '0903456789', 'levanc@raucusachdalat.com', '789 Đường GHI, Quận 3, TP.HCM', 'Chuyên cung cấp rau củ sạch từ Đà Lạt.'),
(4, 'Nấm Hương Đà Lạt', 'Phạm Thị D', '0904567890', 'phamthid@namhuongdalat.com', '321 Đường JKL, Quận 4, TP.HCM', 'Chuyên cung cấp nấm hương tươi từ Đà Lạt.'),
(5, 'Gia Vị Ngon', 'Hoàng Văn E', '0905678901', 'hoangvane@giavivngon.com', '654 Đường MNO, Quận 5, TP.HCM', 'Chuyên cung cấp gia vị các loại.'),
(6, 'Đồ Uống Hảo Hạng', 'Nguyễn Thị F', '0906789012', 'nguyenthif@douonghaohang.com', '987 Đường PQR, Quận 6, TP.HCM', 'Chuyên cung cấp đồ uống các loại.'),

## XÂY DỰNG CÁC THỦ TỤC THEO CÁC CHỨC NĂNG MONG MUỐN

 **Tạo bảng sản phẩm**

CREATE TABLE Products (
    ProductID INT PRIMARY KEY AUTO_INCREMENT,
    ProductName VARCHAR(100) NOT NULL,
    ProductCategory VARCHAR(50),
    Unit VARCHAR(20),
    PricePerUnit DECIMAL(10, 2),
    Description TEXT,
    Image VARCHAR(255)
);
** để thêm hàng hóa mới**

DELIMITER //

CREATE PROCEDURE ThemSanPham (
    IN p_TenSanPham VARCHAR(100),
    IN p_LoaiSanPham VARCHAR(50),
    IN p_DonViTinh VARCHAR(20),
    IN p_GiaMoiDonVi DECIMAL(10, 2),
    IN p_MoTa TEXT,
    IN p_HinhAnh VARCHAR(255)
)
BEGIN
    INSERT INTO Products (ProductName, ProductCategory, Unit, PricePerUnit, Description, Image)
    VALUES (p_TenSanPham, p_LoaiSanPham, p_DonViTinh, p_GiaMoiDonVi, p_MoTa, p_HinhAnh);
END //

DELIMITER ;
** để sửa thông tin hàng hóa**

DELIMITER //

CREATE PROCEDURE SuaSanPham (
    IN p_MaSanPham INT,
    IN p_TenSanPham VARCHAR(100),
    IN p_LoaiSanPham VARCHAR(50),
    IN p_DonViTinh VARCHAR(20),
    IN p_GiaMoiDonVi DECIMAL(10, 2),
    IN p_MoTa TEXT,
    IN p_HinhAnh VARCHAR(255)
)
BEGIN
    UPDATE Products
    SET 
        ProductName = p_TenSanPham,
        ProductCategory = p_LoaiSanPham,
        Unit = p_DonViTinh,
        PricePerUnit = p_GiaMoiDonVi,
        Description = p_MoTa,
        Image = p_HinhAnh
    WHERE ProductID = p_MaSanPham;
END //

DELIMITER ;
  **để xóa hàng hóa****

DELIMITER //

CREATE PROCEDURE XoaSanPham (
    IN p_MaSanPham INT
)
BEGIN
    DELETE FROM Products
    WHERE ProductID = p_MaSanPham;
END //

DELIMITER ;

**Thêm hàng hóa mới**

CALL ThemSanPham('Thịt bò', 'Thịt', 'kg', 200000, 'Thịt bò tươi ngon', 'bo.jpg');
Sửa thông tin hàng hóa

CALL SuaSanPham(1, 'Thịt bò Úc', 'Thịt', 'kg', 250000, 'Thịt bò Úc chất lượng cao', 'bo_uc.jpg');
**Xóa hàng hóa**

CALL XoaSanPham(1);

## Để quản lý tồn kho, chúng ta cần theo dõi số lượng hiện tại của từng mặt hàng và thiết lập các cảnh báo tồn kho khi hàng hóa gần hết hoặc dư thừa. Dưới đây là cách thực hiện quản lý tồn kho trong hệ thống quản lý kho hàng nhà hàng lẩu nướng bằng SQL.

1. Tạo bảng Tồn kho

CREATE TABLE Inventory (
    InventoryID INT PRIMARY KEY AUTO_INCREMENT,
    ProductID INT,
    StockQuantity INT,
    MinStock INT,
    MaxStock INT,
    LastUpdated DATETIME,
    Notes TEXT,
    FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
);
2.  để cập nhật tồn kho khi có giao dịch nhập/xuất kho
Nhập kho

DELIMITER //

CREATE PROCEDURE NhapKho (
    IN p_ProductID INT,
    IN p_SoLuongNhap INT
)
BEGIN
    DECLARE currentStock INT;
    
    SELECT StockQuantity INTO currentStock
    FROM Inventory
    WHERE ProductID = p_ProductID;
    
    IF currentStock IS NULL THEN
        INSERT INTO Inventory (ProductID, StockQuantity, MinStock, MaxStock, LastUpdated)
        VALUES (p_ProductID, p_SoLuongNhap, 10, 100, NOW());
    ELSE
        UPDATE Inventory
        SET StockQuantity = StockQuantity + p_SoLuongNhap, LastUpdated = NOW()
        WHERE ProductID = p_ProductID;
    END IF;
END //

DELIMITER ;
**Xuất kho**

DELIMITER //

CREATE PROCEDURE XuatKho (
    IN p_ProductID INT,
    IN p_SoLuongXuat INT
)
BEGIN
    DECLARE currentStock INT;
    
    SELECT StockQuantity INTO currentStock
    FROM Inventory
    WHERE ProductID = p_ProductID;
    
    IF currentStock IS NOT NULL AND currentStock >= p_SoLuongXuat THEN
        UPDATE Inventory
        SET StockQuantity = StockQuantity - p_SoLuongXuat, LastUpdated = NOW()
        WHERE ProductID = p_ProductID;
    ELSE
        SIGNAL SQLSTATE '45000'
        SET MESSAGE_TEXT = 'Không đủ hàng trong kho để xuất';
    END IF;
END //

DELIMITER ;

3. Cảnh báo tồn kho
Thủ tục kiểm tra tồn kho tối thiểu

DELIMITER //

CREATE PROCEDURE KiemTraTonKhoToiThieu ()
BEGIN
    SELECT ProductID, StockQuantity, MinStock
    FROM Inventory
    WHERE StockQuantity < MinStock;
END //

DELIMITER ;
**Thủ tục kiểm tra tồn kho tối đa**

DELIMITER //

CREATE PROCEDURE KiemTraTonKhoToiDa ()
BEGIN
    SELECT ProductID, StockQuantity, MaxStock
    FROM Inventory
    WHERE StockQuantity > MaxStock;
END //

DELIMITER ;
Sử dụng các thủ tục lưu trữ
**Nhập kho**

CALL NhapKho(1, 50);  -- Nhập thêm 50 đơn vị sản phẩm có ID là 1
Xuất kho

CALL XuatKho(1, 20);  -- Xuất 20 đơn vị sản phẩm có ID là 1
**Kiểm tra tồn kho tối thiểu**

CALL KiemTraTonKhoToiThieu();  -- Kiểm tra các sản phẩm có tồn kho dưới mức tối thiểu
**Kiểm tra tồn kho tối đa**

CALL KiemTraTonKhoToiDa();  -- Kiểm tra các sản phẩm có tồn kho vượt mức tối đa

Dưới đây là mã SQL để quản lý nhập hàng, bao gồm việc lập đơn hàng nhập và tiếp nhận hàng hóa.

**1. Tạo bảng (Đơn hàng nhập kho)**

CREATE TABLE PurchaseOrders (
    PurchaseOrderID INT PRIMARY KEY AUTO_INCREMENT,
    SupplierID INT,
    OrderDate DATE,
    ExpectedDeliveryDate DATE,
    ActualDeliveryDate DATE,
    Status VARCHAR(20),
    TotalAmount DECIMAL(10, 2),
    Notes TEXT,
    FOREIGN KEY (SupplierID) REFERENCES Suppliers(SupplierID)
);
**Bảng Chi tiết đơn hàng nhập kho**

CREATE TABLE PurchaseOrderDetails (
    PurchaseOrderDetailID INT PRIMARY KEY AUTO_INCREMENT,
    PurchaseOrderID INT,
    ProductID INT,
    Quantity INT,
    PricePerUnit DECIMAL(10, 2),
    TotalPrice AS (Quantity * PricePerUnit),
    FOREIGN KEY (PurchaseOrderID) REFERENCES PurchaseOrders(PurchaseOrderID),
    FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
);
**2.  để lập đơn hàng nhập kho**

DELIMITER //

CREATE PROCEDURE LapDonHangNhap (
    IN p_SupplierID INT,
    IN p_OrderDate DATE,
    IN p_ExpectedDeliveryDate DATE,
    IN p_Status VARCHAR(20),
    IN p_TotalAmount DECIMAL(10, 2),
    IN p_Notes TEXT,
    OUT p_PurchaseOrderID INT
)
BEGIN
    INSERT INTO PurchaseOrders (SupplierID, OrderDate, ExpectedDeliveryDate, Status, TotalAmount, Notes)
    VALUES (p_SupplierID, p_OrderDate, p_ExpectedDeliveryDate, p_Status, p_TotalAmount, p_Notes);
    
    SET p_PurchaseOrderID = LAST_INSERT_ID();
END //

DELIMITER ;
**3. Stored Procedure để thêm chi tiết đơn hàng nhập kho**

DELIMITER //

CREATE PROCEDURE ThemChiTietDonHangNhap (
    IN p_PurchaseOrderID INT,
    IN p_ProductID INT,
    IN p_Quantity INT,
    IN p_PricePerUnit DECIMAL(10, 2)
)
BEGIN
    INSERT INTO PurchaseOrderDetails (PurchaseOrderID, ProductID, Quantity, PricePerUnit)
    VALUES (p_PurchaseOrderID, p_ProductID, p_Quantity, p_PricePerUnit);
END //

DELIMITER ;
**4. Stored Procedure để tiếp nhận hàng hóa và cập nhật tồn kho**

DELIMITER //

CREATE PROCEDURE TiepNhanHangHoa (
    IN p_PurchaseOrderID INT,
    IN p_ActualDeliveryDate DATE
)
BEGIN
    DECLARE done INT DEFAULT 0;
    DECLARE v_ProductID INT;
    DECLARE v_Quantity INT;
    DECLARE cur CURSOR FOR 
        SELECT ProductID, Quantity 
        FROM PurchaseOrderDetails
        WHERE PurchaseOrderID = p_PurchaseOrderID;
        
    DECLARE CONTINUE HANDLER FOR NOT FOUND SET done = 1;
    
    OPEN cur;
    
    read_loop: LOOP
        FETCH cur INTO v_ProductID, v_Quantity;
        IF done THEN
            LEAVE read_loop;
        END IF;
        
        CALL NhapKho(v_ProductID, v_Quantity);
    END LOOP;
    
    CLOSE cur;
    
    UPDATE PurchaseOrders
    SET ActualDeliveryDate = p_ActualDeliveryDate, Status = 'Đã nhận'
    WHERE PurchaseOrderID = p_PurchaseOrderID;
END //

DELIMITER ;
Sử dụng các Stored Procedures
**Lập đơn hàng nhập kho**

CALL LapDonHangNhap(1, '2024-06-19', '2024-06-25', 'Chờ nhận', 1000000, 'Đơn hàng từ nhà cung cấp ABC', @NewPurchaseOrderID);
**Thêm chi tiết cho đơn hàng nhập kho**

CALL ThemChiTietDonHangNhap(@NewPurchaseOrderID, 1, 50, 20000); -- Thêm 50 đơn vị sản phẩm có ID là 1 với giá 20,000 mỗi đơn vị
CALL ThemChiTietDonHangNhap(@NewPurchaseOrderID, 2, 30, 15000); -- Thêm 30 đơn vị sản phẩm có ID là 2 với giá 15,000 mỗi đơn vị
**Tiếp nhận hàng hóa và cập nhật tồn kho**

CALL TiepNhanHangHoa(@NewPurchaseOrderID, '2024-06-26'); -- Cập nhật ngày nhận thực tế và tồn kho
## Để quản lý tiêu thụ nguyên liệu, chúng ta cần ghi nhận lượng nguyên liệu tiêu thụ hàng ngày và tạo các báo cáo phân tích tiêu thụ nguyên liệu để dự báo nhu cầu. Dưới đây là các bước thực hiện:

**1. Tạo bảng để ghi nhận tiêu thụ hàng ngày**

CREATE TABLE DailyConsumption (
    ConsumptionID INT PRIMARY KEY AUTO_INCREMENT,
    ProductID INT,
    ConsumptionDate DATE,
    QuantityConsumed INT,
    Notes TEXT,
    FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
);
**2.  để ghi nhận tiêu thụ hàng ngày**

DELIMITER //

CREATE PROCEDURE GhiNhanTieuThuHangNgay (
    IN p_ProductID INT,
    IN p_ConsumptionDate DATE,
    IN p_QuantityConsumed INT,
    IN p_Notes TEXT
)
BEGIN
    INSERT INTO DailyConsumption (ProductID, ConsumptionDate, QuantityConsumed, Notes)
    VALUES (p_ProductID, p_ConsumptionDate, p_QuantityConsumed, p_Notes);
    
    -- Cập nhật tồn kho
    CALL XuatKho(p_ProductID, p_QuantityConsumed);
END //

DELIMITER ;
**3. Báo cáo phân tích tiêu thụ nguyên liệu**
Báo cáo tiêu thụ hàng ngày

CREATE PROCEDURE BaoCaoTieuThuHangNgay (
    IN p_ReportDate DATE
)
BEGIN
    SELECT dc.ProductID, p.ProductName, dc.QuantityConsumed, dc.ConsumptionDate
    FROM DailyConsumption dc
    JOIN Products p ON dc.ProductID = p.ProductID
    WHERE dc.ConsumptionDate = p_ReportDate;
END //
**Báo cáo tiêu thụ hàng tháng**

CREATE PROCEDURE BaoCaoTieuThuHangThang (
    IN p_Year INT,
    IN p_Month INT
)
BEGIN
    SELECT dc.ProductID, p.ProductName, SUM(dc.QuantityConsumed) AS TotalConsumed, COUNT(dc.ConsumptionDate) AS DaysRecorded
    FROM DailyConsumption dc
    JOIN Products p ON dc.ProductID = p.ProductID
    WHERE YEAR(dc.ConsumptionDate) = p_Year AND MONTH(dc.ConsumptionDate) = p_Month
    GROUP BY dc.ProductID, p.ProductName;
END //

**Ghi nhận tiêu thụ hàng ngày**

CALL GhiNhanTieuThuHangNgay(1, '2024-06-19', 10, 'Tiêu thụ thịt bò');
**Báo cáo tiêu thụ hàng ngày
**
CALL BaoCaoTieuThuHangNgay('2024-06-19');
**Báo cáo tiêu thụ hàng tháng**

CALL BaoCaoTieuThuHangThang(2024, 6);
 
