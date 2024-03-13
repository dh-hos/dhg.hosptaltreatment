<div align="center">
<img src="https://raw.githubusercontent.com/dh-hos/dhg.hospitalprinter/main/Deploy_Tools/Logo.ico" alt="Simple Icons" width=70>
<h2>DHG.Hospital Treatment</h2>
</div>

## Nội dung cập nhật
##### [Treat4.2024.03.13v1]()
- [#275](https://github.com/dh-hos/To_Lap_Trinh/issues/275)
- <b>Cập nhật yêu cầu: </b> Hỗ trợ người dùng kiểm tra tiền giường theo ngày điều trị. #275
- <b>Nội dung cập nhật: </b>
     - <b>Cách tính số ngày giường BHYT: </b>
          - SUM(chidinhcls.soluong), thỏa điều kiện:
          - dmcls.kho = 'GB'
          - chidinhcls.bhyt = 1
          - dmdoituong.bhyt = 1 hoặc 2
     - <b>Tóm tắt cách tính số này điều trị theo TT22 và điều kiện cộng 1 ngày: </b>
          - Songngay_congthem = 1 KHI: dmxutri.cong = 1 và dmketqua.cong = 1 ngược lại = 0
          - Số giờ điều trị <= 4 giờ: ngaydt = 0
          - Số giờ điều trị > 4 giờ và <=24 giờ: ngaydt = 1
          - Ngược lại ngaydt = ngày ra - ngày vào + songay_congthem
          ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/1fd802ba-5db7-4718-8931-b4f1585ba6f9)


##### [Treat4.2024.03.12v1](https://gofile.me/78TQg/OfuL2KsGQ)
- [#214](https://github.com/dh-hos/dhg.hosptaltreatment/issues/214)
- <b>Fix lỗi: </b>Chỉnh đối tượng không được. #214


##### [Treat4.2024.03.08v2](https://gofile.me/78TQg/E1PrdSriV)
- [#210](https://github.com/dh-hos/dhg.hosptaltreatment/issues/210)
- <b>Yêu cầu: </b>Bổ sung phiếu phục hồi chức năng #210
     - Chạy script bổ sung (xem mô tả)
     - Lập phiếu PT/TT
       ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/d37f6d53-dc16-46ea-8980-af2dfcfd6be6)

     - Lập phiếu PHCN (chỉ load những CLS đã lập phiếu PT-TT và có Ê kíp)
       ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/abb82f52-1495-4337-b9d1-cebbe88134ef)
     - Chỉnh: cập thêm giá trị phút và mô tả
     - In: chỉ in những CLS nào có cập nhật số phút
       ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/12846d5a-f16e-411b-b0f5-340dbc2849f5)

       P/s:
       - ngày = ngày bắt đầu phẫu thuật/ thủ thuật
       - bs thực hiện = bs trong êkip
       

       
       
  
##### [Treat4.2024.03.08v1](https://gofile.me/78TQg/mnBQpuOJv)
- [#213](https://github.com/dh-hos/dhg.hosptaltreatment/issues/213)
- <b>Fix: </b>Không mở lên được form đánh giá dinh dưỡng #213

##### [Treat4.2024.03.07v2](https://gofile.me/78TQg/TEkqQ0Zc7)
- [#209](https://github.com/dh-hos/dhg.hosptaltreatment/issues/209)
- <b>Fix: </b>QT điều trị không cấn trừ thuốc đã trả #209
     - Tờ điều trị sắp xếp tăng dần theo thời gian cho diễn biến
     - Chỉ cấn trừ thuốc khi trong cùng một diễn biến
     - Dấu trừ (-) thể hiện số lượng trả (dễ nhận biết)
     - Fix: chỉnh đối tượng: thông tuyến, trái tuyến được hưởng cùng tuyến

##### [Treat4.2024.03.06v3](https://gofile.me/78TQg/fwyApowbd)
- [#209](https://github.com/dh-hos/dhg.hosptaltreatment/issues/209)
- <b>Fix: </b>QT điều trị không cấn trừ thuốc đã trả #209
- [#212](https://github.com/dh-hos/dhg.hosptaltreatment/issues/212)
- <b>Fix: </b>Treatment Phiếu hẹn tái khám lý do vào viện trái tuyến nhưng phiếu hẹn lại check cùng tuyến #212

##### [Treat4.2024.03.06v2](https://gofile.me/78TQg/X8P7mDwfV)
- [#211](https://github.com/dh-hos/dhg.hosptaltreatment/issues/211)
- <b>Fix: </b>Load lại thông tin cân nặng cũ khi lập phiếu đánh giá dinh dưỡng. #211

##### [Treat4.2024.03.06v1](https://gofile.me/78TQg/xhztM2vnI)
- [#207](https://github.com/dh-hos/dhg.hosptaltreatment/issues/207)
- <b>Fix: </b>Sai chi phí BNCCT khi không nhập ngày kết thúc miễn chi trả #207
    - Khi không nhập ngày kết thúc miễn thì phần mềm tự hiển thị ngày 3/1/2013
      ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/8609030f-c84d-4ea7-b4ae-456c16c14264)

    - Phần mềm không tính đúng chi phí BNCCT ( ví dụ: bệnh nhân có chi phí CLS GI20 trong thời gian miễn chi trả không được tính miễn như trong mô tả - không có ngày kết thúc miễn thì được miễn hết từ ngày miễn chi trả)
      ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/943243ba-35c1-4339-9d11-983fd868cf1b)


##### [Treat4.2024.03.05v1](https://gofile.me/78TQg/2B13ZGqsC)
- [#206](https://github.com/dh-hos/dhg.hosptaltreatment/issues/206)
- <b>Fix: </b>Không nhập được mã thẻ tạm thông tin con #206
    - Module cũ: sau khi nhập giấy CS hoặc không --> đóng/mở mã thẻ để nhập
    - Fix: bỏ qua bước trên --> mở mã thẻ để nhập
  
##### [Treat4.2024.03.04v1](https://gofile.me/78TQg/y0mrx8dcV)
- [#204](https://github.com/dh-hos/dhg.hosptaltreatment/issues/204)
- <b>Fix lỗi: </b>Toa thuốc nhà thuốc không thể hiện tuổi bệnh nhân #204
  
##### [Treat4.2024.02.21v2](https://gofile.me/78TQg/LA21eMaXT)
- [#243](https://github.com/dh-hos/To_Lap_Trinh/issues/243)
- <b>Yêu cầu: </b>Group các dòng chi phí đối với bảng kê chi phí nội bộ (BV Phụ Sản)

##### [Treat4.2024.02.21v1](https://gofile.me/78TQg/jaXZtmFP7)
- [#202](https://github.com/dh-hos/dhg.hosptaltreatment/issues/202)
- <b>Fix lỗi: </b>Chưa nhập thông tin cần thiết nhưng vẫn lưu được phiếu đánh giá dinh dưỡng. #202

##### [Treat4.2024.02.08v1](https://gofile.me/78TQg/3DBoyTBS1)
- [#201](https://github.com/dh-hos/dhg.hosptaltreatment/issues/201)
- <b>Fix lỗi: </b>Chỉnh thông tin bệnh nhân nội trú (BV Đặng Thùy Trâm) #201
     
##### [Treat4.2024.02.06v4](https://gofile.me/78TQg/xze60sqE9)
- [#157](https://github.com/dh-hos/dhg.hospitalfees/issues/157)
- <b>Fix lỗi: </b>Báo cáo chi tiết theo dịch vụ không tách chi phí dịch vụ sang tab hóa đơn (BV Phụ Sản CT) #157
   - Khóa cột: chenhlech, thanhtien

##### [Treat4.2024.02.06v1](https://gofile.me/78TQg/7lqfLzLQa)
- [#157](https://github.com/dh-hos/dhg.hospitalfees/issues/157)
- <b>Fix lỗi: </b>Báo cáo chi tiết theo dịch vụ không tách chi phí dịch vụ sang tab hóa đơn (BV Phụ Sản CT) #157
   - Các dịch vụ không có tiền chênh lệch nếu có check dịch vụ:
   - Thực hiện thao tác bỏ check và check lại dịch vụ:
     ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/ccfcbe7c-cbe0-4854-935d-d59ca9635730)

  

##### [Treat4.2024.02.02v1](https://gofile.me/78TQg/DvuvczBwJ)
- [#239](https://github.com/dh-hos/To_Lap_Trinh/issues/239)
- <b>Yêu cầu: </b>Bổ sung mã bệnh viện mới. #239

##### [Treat4.2024.02.01v1](https://gofile.me/78TQg/vKkGxhxTD)
- [#200](https://github.com/dh-hos/dhg.hosptaltreatment/issues/200)
- <b>Fix Lỗi: </b>Toa tủ trực cũ không check "Lấy tại tủ trực cấp" sau khi cập nhật cấu trúc và Treatment mới #200
  
##### [Treat4.2024.01.31v1](https://gofile.me/78TQg/cX4iaGcFN)
- [#199](https://github.com/dh-hos/dhg.hosptaltreatment/issues/199)
- <b>Fix Lỗi: </b>Chỉnh trạng thái cấp cứu -> Bình thường phần mềm ghi nhận sai lý do vào viện của bệnh nhân (BV phụ sản) #199
       
##### [Treat4.2024.01.26v4](https://gofile.me/78TQg/ljAetvcMh)
- [#195](https://github.com/dh-hos/dhg.hosptaltreatment/issues/195)
- <b>Fix Lỗi: </b>Lỗi chỉnh đối tượng (BV Phụ Sản) #195
     - Fix: hiển thị sai trạng thái trái tuyến/cùng tuyến
     - ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/1eb30ba7-296c-4307-ab02-2a0d27f3cf9f)


##### [Treat4.2024.01.26v3](https://gofile.me/78TQg/gMQkmQn0t)
- [#22](https://github.com/dh-hos/To_Lap_Trinh/issues/22)
- <b>Yêu cầu: </b>Bộ CLS mặc định số lượng #22
  
 <b>P/s: chạy script hỗ trợ</b>
  
##### [Treat4.2024.01.23v1](https://gofile.me/78TQg/rvnPX12wm)
- [#197](https://github.com/dh-hos/dhg.hosptaltreatment/issues/197)
- <b>Fix Lỗi: </b>Trang in phiếu đánh giá dưỡng không hiển thị được chiều cao. #197

##### [Treat4.2024.01.22v1](https://gofile.me/78TQg/yJfYLAXJT)
- [#198](https://github.com/dh-hos/dhg.hosptaltreatment/issues/198)
- <b>Fix Lỗi: </b>Sai mức hưởng đối với bệnh nội trú có nhập thẻ 2 (BV Tim Mạch AG)


##### [Treat4.2024.01.18v1](https://gofile.me/78TQg/nRqiKwvTS)
- [#195](https://github.com/dh-hos/dhg.hosptaltreatment/issues/195)
- <b>Fix Lỗi: </b>Lỗi chỉnh đối tượng (BV Phụ Sản) #195
     - Fix: hiển thị sai trạng thái trái tuyến/cùng tuyến

##### [Treat4.2024.01.17v3](https://gofile.me/78TQg/t5Lsr6cQW)
- [#195](https://github.com/dh-hos/dhg.hosptaltreatment/issues/195)
- <b>Fix Lỗi: </b>Lỗi chỉnh đối tượng (BV Phụ Sản) #195

##### [Treat4.2024.01.17v2](https://gofile.me/78TQg/XcW4fdUdP)
- [#194](https://github.com/dh-hos/dhg.hosptaltreatment/issues/194)
- <b>Fix Lỗi: </b>CThông tin trạng thái vào viện giữa các Form không đồng bộ (BV Phụ Sản) #194
  
##### [Treat4.2024.01.17v1](https://gofile.me/78TQg/V7sMGkMmg)
- [#193](https://github.com/dh-hos/dhg.hosptaltreatment/issues/193)
- <b>Fix Lỗi: </b>Chỉnh thông tin bệnh nhân ghi nhận sai lý do vào viện (BV Phụ Sản) #193

##### [Treat4.2024.01.16v1](https://gofile.me/78TQg/t1NFcF9yb)
- [#192](https://github.com/dh-hos/dhg.hosptaltreatment/issues/192)
- <b>Lỗi: </b>Hiển thị sai năm sinh của BN #192
  
      - Hiển thị năm sinh (nếu bn chỉ có năm sinh), ngược lại hiển thị ngày/tháng/năm sinh
  
##### [Treat4.2024.01.15v1](https://gofile.me/78TQg/1JCh6PLNP)
- [#203](https://github.com/dh-hos/To_Lap_Trinh/issues/203)
- <b>Yêu cầu: </b>Hỗ trợ chức năng tách phiếu thu CLS nội bộ #203
  
      - Hiển thị chi phí nội bộ lên form

##### [Treat4.2024.01.11v2](https://gofile.me/78TQg/P5W0P4s2w)
- [#190](https://github.com/dh-hos/To_Lap_Trinh/issues/190)
- <b>Yêu cầu: </b>Mở chức năng ra toa nhiều tủ trực #190
- - [#Mô tả thay đổi cách ghi dữ liệu](https://github.com/dh-hos/Mo-ta-he-thong/blob/main/Vuong-mo%20ta%20thuc%20hien%20tu%20truc%20vat%20tu%20ver2.md)

##### [Treat4.2024.01.10v1](https://gofile.me/78TQg/LrDDSSx0s)
- [#185](https://github.com/dh-hos/dhg.hosptaltreatment/issues/185)
- <b>Lỗi: </b>Trình tự TT/PT quá dài phiếu Phẫu thuật không hiển thị hết nội dung

##### [Treat4.2024.01.08v1](https://gofile.me/78TQg/n5kXBjIVH)
- [#201](https://github.com/dh-hos/To_Lap_Trinh/issues/201)
- <b>Yêu cầu: </b>Mô tả thực hiện quản lý bệnh án ngày #201
     - Trang bìa chưa đúng theo yêu cầu

  
##### [Treat4.2024.01.05v2](https://gofile.me/78TQg/I22gkLWgz)
- [#216](https://github.com/dh-hos/To_Lap_Trinh/issues/216)
- <b>Yêu cầu: </b>Bổ sung thêm thông tin khi lập phiếu Tình trạng dinh dưỡng. #216

##### [Treat4.2024.01.05v1](https://gofile.me/78TQg/oo4OHcA4a)
- [#205](https://github.com/dh-hos/To_Lap_Trinh/issues/205)
- <b>Yêu cầu: </b>Lập phiếu chuyển viện tuyến dưới hỗ trợ điều trị lao #205
     - Nút chuyển viện lao không phụ thuộc vào xử trí

##### [Treat4.2024.01.04v2](https://gofile.me/78TQg/PvnKMwNF8)
- [#188](https://github.com/dh-hos/dhg.hosptaltreatment/issues/188)
- <b>Lỗi: </b>Toa thuốc tủ trực, chỉ định cls (BV Thốt Nốt) #188
     - Fix mất chữ "PHIẾU IN LẠI" khi in lần 2
- [#190](https://github.com/dh-hos/dhg.hosptaltreatment/issues/190)
- <b>Lỗi: </b>Giấy chứng sinh lỗi khi ngày sinh và ngày lập giấy chứng sinh khác tháng-năm kế toán #190

##### [Treat4.2024.01.03v4](https://gofile.me/78TQg/2IIB6c46T)
- [#188](https://github.com/dh-hos/dhg.hosptaltreatment/issues/188)
- <b>Lỗi: </b>Toa thuốc tủ trực, chỉ định cls (BV Thốt Nốt) #188
  
##### [Treat4.2024.01.03v3](https://gofile.me/78TQg/qSKbMI8rP)
- [#190](https://github.com/dh-hos/dhg.hosptaltreatment/issues/190)
- <b>Lỗi: </b>Giấy chứng sinh lỗi khi ngày sinh và ngày lập giấy chứng sinh khác tháng-năm kế toán #190
  
##### [Treat4.2024.01.03v2](https://gofile.me/78TQg/Rr0dVsLZG)
- [#189](https://github.com/dh-hos/dhg.hosptaltreatment/issues/189)
- <b>Lỗi: </b>Lấy lại toa sai kho cấp phát thuốc khi check lấy tủ trực nhà thuốc #189

##### [Treat4.2024.01.03v1](https://gofile.me/78TQg/CRLm8Amxa)
- [#205](https://github.com/dh-hos/To_Lap_Trinh/issues/205)
- <b>Yêu cầu: </b>Lập phiếu chuyển viện tuyến dưới hỗ trợ điều trị lao #205

##### [Treat4.2024.01.02v2](https://gofile.me/78TQg/FdBUHICj5)
- [#185](https://github.com/dh-hos/dhg.hosptaltreatment/issues/187)
- <b>Lỗi: </b>Miễn cùng chi trả chi phí ngoài thời gian được miễn chi trả #187
- Thực hiện thao tác chỉnh đối tượng để cập nhật

##### [Treat4.2024.01.02v1](https://gofile.me/78TQg/0430lCn3T)
- [#205](https://github.com/dh-hos/To_Lap_Trinh/issues/205)
- <b>Yêu cầu: </b>Lập phiếu chuyển viện tuyến dưới hỗ trợ điều trị lao #205

##### [Treat4.2023.12.28v3](https://gofile.me/78TQg/hmNEyJtvC)
- [#184](https://github.com/dh-hos/dhg.hosptaltreatment/issues/184)
- <b>Lỗi: </b>Chỉnh ngày ra viện không kiểm soát được chi phí trong thời gian điều trị. #184
  
##### [Treat4.2023.12.28v2](https://gofile.me/78TQg/xO4U4a5qZ)
- [#183](https://github.com/dh-hos/dhg.hosptaltreatment/issues/183)
- <b>Lỗi: </b>Load toa mẫu - toa VTYT kèm theo (BV Thốt Nốt) #183
  
##### [Treat4.2023.12.28v1](https://gofile.me/78TQg/UOqeckGK4)
- [#205](https://github.com/dh-hos/To_Lap_Trinh/issues/205)
- <b>Yêu cầu: </b>Lập phiếu chuyển viện tuyến dưới hỗ trợ điều trị lao #205
  ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/92500290-cca8-49d5-b8d4-30b89aaad5c2)


##### [Treat4.2023.12.27v2](https://gofile.me/78TQg/oHuDteK7B)
- [#181](https://github.com/dh-hos/dhg.hosptaltreatment/issues/181)
- <b>Lỗi: </b>Sai mức hưởng trên phiếu 6556
- [#182](https://github.com/dh-hos/dhg.hosptaltreatment/issues/182)
- <b>Lỗi: </b>Phiếu đánh giá dinh dưỡng không có tên SYT và tên BV #182

##### [Treat4.2023.12.26v2](https://gofile.me/78TQg/8647oiyVh)
- [#201](https://github.com/dh-hos/To_Lap_Trinh/issues/201)
- <b>Yêu cầu: </b>Mô tả thực hiện quản lý bệnh án ngày #201
    - Bổ sung check cho phép điều chỉnh trạng thái của bệnh án
      ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/9442282b-a706-4dc8-ab74-95e1146cfd79)
- [#203](https://github.com/dh-hos/To_Lap_Trinh/issues/203)
- <b>Yêu cầu: </b>Hỗ trợ chức năng tách phiếu thu CLS nội bộ #203
   - Bổ sung para mabn


##### [Treat4.2023.12.25v1](https://gofile.me/78TQg/Sf1uXIRby)
- [#201](https://github.com/dh-hos/To_Lap_Trinh/issues/201)
- <b>Yêu cầu: </b>Mô tả thực hiện quản lý bệnh án ngày #201
    - Fix load nhập viện từ ngoại trú (check cả tháng)
      
##### [Treat4.2023.12.22v3](https://gofile.me/78TQg/WDIKbhJFE)
- [#201](https://github.com/dh-hos/To_Lap_Trinh/issues/201)
- <b>Yêu cầu: </b>Mô tả thực hiện quản lý bệnh án ngày #201
    - Fix load nhập viện từ ngoại trú

##### [Treat4.2023.12.22v2](https://gofile.me/78TQg/9057McL6E)
- [#180](https://github.com/dh-hos/dhg.hosptaltreatment/issues/180)
- <b>Lỗi: </b>Không cập nhật được giá khi chuyển giá. #180
  
##### [Treat4.2023.12.21v1](https://gofile.me/78TQg/Tn37VekLj)
- [#201](https://github.com/dh-hos/To_Lap_Trinh/issues/201)
- <b>Yêu cầu: </b>Mô tả thực hiện quản lý bệnh án ngày #201
   - Lưu ý: chạy script tạo cột bangay
   - Thay đổi màu trên danh sách điều trị
     ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/dc5f82e2-8dde-4be4-a919-3413a47b472a)

   - Bộ lọc trên sổ:
        - Xuất viện, chuyển viện, trốn viện, tử vong, theo dõi
          ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/74edcd78-b244-4f5c-8f4d-c9a4a169abba)


##### [Treat4.2023.12.20v2](https://gofile.me/78TQg/NfgoKIEsr)
- [#179](https://github.com/dh-hos/dhg.hosptaltreatment/issues/179)
- <b>Lỗi: </b>Không cho nhập số con còn sống có độ dài > 1 #179
   - Lưu ý: chạy script tạo cột bangay và mở rộng độ dài

##### [Treat4.2023.12.19v1](https://gofile.me/78TQg/D1zLOnf48)
- [#203](https://github.com/dh-hos/To_Lap_Trinh/issues/203)
- <b>Yêu cầu: </b>Hỗ trợ chức năng tách phiếu thu CLS nội bộ #203
   - Khi in phiếu 6556: tách chi phí nội bộ trong một bảng kê riêng
  
##### [Treat4.2023.12.13v1](https://gofile.me/78TQg/iIgbupfuU)
- [#178](https://github.com/dh-hos/dhg.hosptaltreatment/issues/178)
- <b>Lỗi: </b>PHIẾU CHĂM SÓC CHƯA CÓ DỮ LIỆU VẪN BẤM CHỈNH ĐƯỢC #178

##### [Treat4.2023.12.12v1](https://gofile.me/78TQg/lQq0Gjcvt)
- [#199](https://github.com/dh-hos/To_Lap_Trinh/issues/199)
- <b>Yêu cầu: </b>Hiển thị Mã GCS trên giấy chứng sinh #199
- Áp dụng: Tất cả
  
      - Mã GSC = A + .GSC. + B + C
      - Trong đó: A = 5 ký tự ký cuối số CS. B = mã số bệnh viện. C = 2 ký tự cuối năm kế toán
      - VD: 00001.GCS.92003.23

  P/s: Bên gửi giấy chứng sinh cũng lấy mã GCS theo cấu trúc này

##### [Treat4.2023.12.11v3](https://gofile.me/78TQg/NX6DMDKHP)
- [#197](https://github.com/dh-hos/To_Lap_Trinh/issues/197)
- <b>Yêu cầu: </b>Thực hiện hợp đồng - Phiếu tình trạng dinh dưỡng #197
- Áp dụng: BV Nhi Cần Thơ (92003)
  
      - Chỉ cho phép ra thuốc/chỉ định cls sau khi lập phiếu tình trạng dinh dưỡng

##### [Treat4.2023.12.11v2](https://gofile.me/78TQg/R2TLllvsm)
- [#177](https://github.com/dh-hos/dhg.hosptaltreatment/issues/177)
- <b>Lỗi: </b>Giấy chuyển tuyến Chỉ định CLS sai tiêu đề#177

##### [Treat4.2023.12.11v1](https://gofile.me/78TQg/IoY693cON)
- [#197](https://github.com/dh-hos/To_Lap_Trinh/issues/197)
- <b>Yêu cầu: </b>Thực hiện hợp đồng - Phiếu tình trạng dinh dưỡng #197
- Áp dụng: BV Nhi Cần Thơ (92003)
  
      - Chỉ cho phép ra thuốc/chỉ định cls sau khi lập phiếu tình trạng dinh dưỡng
  
##### [Treat4.2023.12.10v1](https://gofile.me/78TQg/JT3gxk2wx)
- [#197](https://github.com/dh-hos/To_Lap_Trinh/issues/197)
- <b>Yêu cầu: </b>Thực hiện hợp đồng - Phiếu tình trạng dinh dưỡng #197
- Hướng dẫn:
    - Thêm/chỉnh tình trạng dinh dưỡng:
      
      ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/98461080-d852-44d9-b9a3-1138616b2363)
      
    
    - Xem báo cáo:
      
      ![image](https://github.com/dh-hos/dhg.hosptaltreatment/assets/32563776/7f1e7731-78f7-4a4e-b4d4-d93a776ef013)



##### [Treat4.2023.12.08v1](https://gofile.me/78TQg/bK1i5R68H)
- [#192](https://github.com/dh-hos/To_Lap_Trinh/issues/192)
- <b>Yêu cầu: </b>1.7 Module Treatment cập nhật ngay5nam (QĐ 130)
- Script hỗ trợ test:

ALTER TABLE current.ttcon
ADD COLUMN ngay5nam DATE;
COMMENT ON COLUMN current.ttcon.ngay5nam
IS 'Ngày 5 năm liên tuc';

P/s: Trên bảng bnnoitru đã có cột này

##### [Treat4.2023.12.06v1](https://gofile.me/78TQg/91zFh1fLy)
- [#190](https://github.com/dh-hos/To_Lap_Trinh/issues/190)
- <b>Yêu cầu: </b>Mở chức năng ra toa nhiều tủ trực #190
- Áp dụng: BV Thốt Nốt - Cần Thơ(92010)

##### [Treat4.2023.12.05v4](https://gofile.me/78TQg/l30cseppC)
- [#171](https://github.com/dh-hos/dhg.hosptaltreatment/issues/171)
- <b>Lỗi: </b>Nút in Chỉ định CLS chuyển tuyến trên không tác dụng và Cập nhật nội dung Lý do chuyển theo NĐ75 #171

##### [Treat4.2023.12.05v3](https://gofile.me/78TQg/jHecVPNRu)
- [#175](https://github.com/dh-hos/dhg.hosptaltreatment/issues/175)
- <b>Lỗi: </b>Phiếu hẹn tái khám không check được trái tuyến. #175


##### [Treat4.2023.12.05v2](https://gofile.me/78TQg/j0Ce3dnCB)
- [#172](https://github.com/dh-hos/dhg.hosptaltreatment/issues/172)
- <b>Lỗi: </b>Thành tiền tính sai đối với CLS DV #172
- [#173](https://github.com/dh-hos/dhg.hosptaltreatment/issues/173)
- <b>Lỗi: </b>Tổng kết chi phí và bảng kê 6556 sai số tiền BV ( khi vật tư y tế có trần thanh toán) #173

##### [Treat4.2023.12.04v2](https://gofile.me/78TQg/BBNYozSeb)
- [#171](https://github.com/dh-hos/dhg.hosptaltreatment/issues/171)
- <b>Lỗi: </b>Nút in Chỉ định CLS chuyển tuyến trên không tác dụng và Cập nhật nội dung Lý do chuyển theo NĐ75 #171

  
##### [Treat4.2023.12.03v1](https://gofile.me/78TQg/AtUA6kr6w)
- [#190](https://github.com/dh-hos/To_Lap_Trinh/issues/190)
- <b>Yêu cầu: </b>Mở chức năng ra toa nhiều tủ trực #190
- Áp dụng: BV Thốt Nốt - Cần Thơ(92010)
  
##### [Treat4.2023.12.01v5](https://gofile.me/78TQg/GOy1iJU5U)
- [#189](https://github.com/dh-hos/To_Lap_Trinh/issues/189)
- <b>Yêu cầu: </b>Load thêm các cận lâm sàng có check "CP Nội bộ" lên bảng kê
- Áp dụng: BV Phụ Sản Cần Thơ (92118)
     
##### [Treat4.2023.12.01v4](https://gofile.me/78TQg/FMFbMoj84)
- [#131](https://github.com/dh-hos/To_Lap_Trinh/issues/131)
- <b>Yêu cầu: </b>Bổ sung mẫu giấy hẹn tái khám và Chuyển viện theo công văn 75/2023/NĐ-CP #131
   - Giấy hẹn tái khám (bật tham số nt.giayhena5 = 4)
   - Check đồng thời cấp cứu và đúng tuyến (tham khảo tham số: nt.checkcapcuu)
   - Giấy chuyển viện: (bật tham số cv.thongtu14 = 3)
   - Cập nhật phiếu chỉ định tự thiết kế BV Sa Đéc
   
     P/s: Chạy script cập nhật nội dung tham số
     
##### [Treat4.2023.12.01v2](https://gofile.me/78TQg/1VqHOILaz)
- [#131](https://github.com/dh-hos/To_Lap_Trinh/issues/131)
- <b>Yêu cầu: </b>Bổ sung mẫu giấy hẹn tái khám và Chuyển viện theo công văn 75/2023/NĐ-CP #131
   - Giấy hẹn tái khám (bật tham số nt.giayhena5 = 4)
   - Check đồng thời cấp cứu và đúng tuyến (tham khảo tham số: nt.checkcapcuu)
   - Giấy chuyển viện: (bật tham số cv.thongtu14 = 3)
   
     P/s: Chạy script cập nhật nội dung tham số

- [#131](https://github.com/dh-hos/To_Lap_Trinh/issues/131)
- <b>Yêu cầu: </b>Bổ sung mẫu giấy hẹn tái khám và Chuyển viện theo công văn 75/2023/NĐ-CP #131
   - Giấy hẹn tái khám (bật tham số nt.giayhena5 = 4)
   - Check đồng thời cấp cứu và đúng tuyến (tham khảo tham số: nt.checkcapcuu)
   - Giấy chuyển viện: đang thực hiện
   - 
##### [Treat4.2023.11.30v1](https://gofile.me/78TQg/tcTEyWblk)
- [#131](https://github.com/dh-hos/To_Lap_Trinh/issues/131)
- <b>Yêu cầu: </b>Bổ sung mẫu giấy hẹn tái khám và Chuyển viện theo công văn 75/2023/NĐ-CP #131
   - Giấy hẹn tái khám (bật tham số nt.giayhena5 = 4)
   - Giấy chuyển viện: đang thực hiện


##### [Treat4.2023.11.29v2](https://gofile.me/78TQg/Osml6ZZ8E)
- [#169](https://github.com/dh-hos/dhg.hosptaltreatment/issues/169)
- <b>Lỗi: </b>Gửi giấy chứng sinh theo đề án 06 (BV Sadec) #169
- [#170](https://github.com/dh-hos/dhg.hosptaltreatment/issues/170)
- <b>Lỗi: </b>Toa xuất viện chẩn đoán bị lập lại #170
  

##### [Treat4.2023.11.29v1](https://gofile.me/78TQg/ULfRAGlcy)
- [#169](https://github.com/dh-hos/dhg.hosptaltreatment/issues/169)
- <b>Lỗi: </b>Gửi giấy chứng sinh theo đề án 06 (BV Sadec) #169

##### [Treat4.2023.11.28v1](https://gofile.me/78TQg/bKLgCGccn)
- [#169](https://github.com/dh-hos/dhg.hosptaltreatment/issues/169)
- <b>Lỗi: </b>Gửi giấy chứng sinh theo đề án 06 (BV Sadec) #169
  
##### [Treat4.2023.11.22v2](https://gofile.me/78TQg/y9a4ZvNLd)
- [#157](https://github.com/dh-hos/To_Lap_Trinh/issues/157)
- <b>Yêu cầu: </b> Treatment Lấy toa nhà thuốc hỗ trợ đúng mẫu Nghiện Hướng thần giống ngoại trú #157


##### [Treat4.2023.11.21v2](https://gofile.me/78TQg/cyvWjwX7P)
- [#116](https://github.com/dh-hos/To_Lap_Trinh/issues/116)
- <b>Yêu cầu:</b>Chức năng GCS theo đề án 06 theo địa chỉ của con #116
- [#157](https://github.com/dh-hos/To_Lap_Trinh/issues/157)
- <b>Yêu cầu:</b>Treatment Lấy toa nhà thuốc hỗ trợ đúng mẫu Nghiện Hướng thần giống ngoại trú #157

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
