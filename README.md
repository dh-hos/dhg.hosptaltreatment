<div align="center">
<img src="https://raw.githubusercontent.com/dh-hos/dhg.hospitalprinter/main/Deploy_Tools/Logo.ico" alt="Simple Icons" width=70>
<h2>DHG.Hospital Treatment</h2>
</div>

## Nội dung cập nhật
##### [Treat4.2023.11.21v1](https://gofile.me/78TQg/TrYPkjx6X)
- [#167](https://github.com/dh-hos/dhg.hosptaltreatment/issues/167)
- <b>Lỗi:</b> Giấy hẹn tái khám in bị lấp chữ, bị thiếu chữ #167
  
##### [Treat4.2023.11.17v1](https://gofile.me/78TQg/dvkHO74sx)
- [#166](https://github.com/dh-hos/dhg.hosptaltreatment/issues/166)
- <b>Lỗi:</b> KHI KẾT THÚC ĐIỀU TRỊ CÁC TRƯỜNG HỌP VÀO VIỆN VÀ RA VIỆN CHƯA ĐỦ 24 GIỜ #166

##### [Treat4.2023.11.16v2](https://gofile.me/78TQg/bWxQBdKRO)
- [#116](https://github.com/dh-hos/To_Lap_Trinh/issues/116)
- <b>Yêu cầu:</b> Yêu cầu - Chức năng GCS theo đề án 06 theo địa chỉ của con #116
- <b>Cập nhât:</b>
    - Cập nhật DH.ThongTinKSK.dll lấy dữ liệu đúng yêu cầu
- <b>Áp dụng:</b> Tất cả bệnh viện

##### [Treat4.2023.11.14v3](https://gofile.me/78TQg/mQSDuzRWz)
- [#45](https://github.com/dh-hos/To_Lap_Trinh/issues/45)
- <b>Yêu cầu:</b> Yêu cầu - Tách phiếu thuốc theo Quyết toán riêng. #45
- <b>Cập nhât:</b>
    - Tổng hợp lãnh, trả thuốc tại khoa: tách thuốc, VTTH theo quyết toán riêng
- <b>Áp dụng:</b> Tất cả bệnh viện

##### [Treat4.2023.11.14v2](https://gofile.me/78TQg/Nz5oRyoCP)
- [#152](https://github.com/dh-hos/To_Lap_Trinh/issues/152)
- <b>Yêu cầu:</b> Bổ sung chức năng cho chọn lại cận làm sàng đã chỉ định để in
- <b>Cập nhât:</b>
    - Thêm cột in trên lưới chỉ định: người dùng có thể tùy chọn in hoặc không in CLS nào đó
    - Thêm check tất cả: chọn tất cả hoặc bỏ chọn CLS cần in
- <b>Đối tượng áp dụng:</b> Tất cả bệnh viện
- <b>Ngoại lệ:</b> Đối với BV TMĐ Tiền Giang in trưc tiếp ra máy in, các đơn vị còn lại PrintView

##### [Treat4.2023.11.14v1](https://gofile.me/78TQg/F3T2btsw8)
- [#38](https://github.com/dh-hos/To_Lap_Trinh/issues/38#event-10921913254)
- <b>Yêu cầu:</b> Xóa diễn biến #38
- <b>Cập nhât:</b> Khi xóa diễn biến kiểm tra có được sử dụng hay chưa? Chưa thì được xóa.
- <b>Đối tượng áp dụng:</b> Tất cả bệnh viện

##### [Treat4.2023.11.10v1](https://gofile.me/78TQg/CyP0mOHF7)
- [#165](https://github.com/dh-hos/dhg.hosptaltreatment/issues/165)
- <b>Lỗi:</b> Treatment Phiếu Trích BBHC hiển thị bị khuất tên Khoa điều trị ! #165
- <b>Cập nhât:</b> đổi sang mẫu biểu tự thiết kế
- <b>Áp dụng:</b> Tất cả bệnh viện
  
##### [Treat4.2023.11.06v1](https://gofile.me/78TQg/NLr4gIr00)
- [#164](https://github.com/dh-hos/dhg.hosptaltreatment/issues/164)
- <b>Lỗi:</b> Lỗi - Không hiển thị tên loại CLS trên phiếu XN #164
          - 
##### [Treat4.2023.11.03v2](https://gofile.me/78TQg/EL43crOed)
- [#65](https://github.com/dh-hos/To_Lap_Trinh/issues/65)
- <b>Yêu cầu:</b> Cảnh báo BN điều trị từ 04h đến dưới 24h #65
- <b>Thực hiện:</b>
     - Khi tổng giờ điều trị: >4 và <=24
          - Kiểm tra cận lâm sàn giường bệnh (bhyt) có số lượng > 1 --> cảnh báo.

##### [Treat4.2023.10.31v2](https://gofile.me/78TQg/Y8l7zLHkG)
- [#113](https://github.com/dh-hos/To_Lap_Trinh/issues/113)
- <b>Yêu cầu:</b> In phiếu chỉ định CLS tách theo Loại CLS #113
- <b>Thực hiện theo mô tả:</b> [mô tả](https://github.com/dh-hos/Mo-ta-he-thong/blob/main/Bi%20-%20Mo%20ta%20Phan%20phieu%20chi%20dinh%20theo%20nhom%20cac%20loai%20CLS.md)

##### [Treat4.2023.10.31v1](https://gofile.me/78TQg/0k9rudZeC)
- [#163](https://github.com/dh-hos/dhg.hosptaltreatment/issues/163)
- <b>Lỗi:</b> Không xuất viện được trường hợp bệnh nhân có toa và trả toa sau thời gian ra viện. (BV Thạnh Trị) #163
   - Nguyên nhân ra lỗi:
      - Theo yêu cầu kiểm soát đến giờ ra toa (cột ngaylap, ngayhd không có thông tin giờ) --> kiểm tra cột giolap để đáp ứng yêu cầu
      - Phiên bản cũ hơn ghi nhận giờ lập theo ngày giờ hệ thống khi lập phiếu
      - Phiên bản này sẽ cập nhật giờ lập theo ngày giờ ngày giờ ngày hóa đơn trên form
      - P/s: khắc phục lỗi cũ bằng script (nếu người dùng có cầu cụ thể)

##### [Treat4.2023.10.26v1](https://gofile.me/78TQg/32bPeTSXU)
- [#128](https://github.com/dh-hos/To_Lap_Trinh/issues/128)
- <b>Yêu cầu:</b> Bệnh nhân nội trú BHYT ra viện dưới 4h không bắt đối với cls ngày giường không thanh bhyt (BV Tâm Phúc) #128
   - Đối với CLS tiền gường không thanh BHYT:
      - Không kiểm tra khi giờ điều trị <=4h
      - Không kiểm tra ngày nhập kết quả 

##### [Treat4.2023.10.25v1](https://gofile.me/78TQg/491cE434B)
- [#162](https://github.com/dh-hos/dhg.hosptaltreatment/issues/162)
- <b>Lỗi:</b> Lỗi in phiếu tử vong tt24 #162
   - Không hiển thị đơn vị tính thời gian
- [#125](https://github.com/dh-hos/dhg.hospitalprinter/issues/125)
- <b>Lỗi:</b> Không phục hồi được toa nhà thuốc đã bấm Không lấy thuốc của toa nội trú. #125

##### [Treat4.2023.10.24v1](https://gofile.me/78TQg/zaZQXoAkL)
- [#162](https://github.com/dh-hos/dhg.hosptaltreatment/issues/162)
- <b>Lỗi:</b> Lỗi - Lỗi in phiếu tử vong tt24 #162
  
##### [Treat4.2023.10.18v1](https://gofile.me/78TQg/PgoLtI0PI)
- [#127](https://github.com/dh-hos/To_Lap_Trinh/issues/127)
- <b>Yêu cầu:</b> Bắt buộc nhập sinh hiệu và định mức tồn kho (BV Trà Cú) #127
- <b>Thực hiện theo mô tả:</b> [mô tả kiểm tra sinh hiệu](https://github.com/dh-hos/Mo-ta-he-thong/blob/main/THAM_SO_HE_THONG/ktsinhhieu.md)

##### [Treat4.2023.10.17v1](https://gofile.me/78TQg/SXN1JXjIp)
- [#126](https://github.com/dh-hos/To_Lap_Trinh/issues/126)
- <b>Yêu cầu:</b> Cấp license thêm mã đơn vị triển khai mới - BV Đa Khoa Tâm Minh Đức Tiền Giang
- [#123](https://github.com/dh-hos/To_Lap_Trinh/issues/123)
- <b>Yêu cầu:</b> Cho chỉnh sửa (nếu chưa gởi liên thông), không cho xóa.
