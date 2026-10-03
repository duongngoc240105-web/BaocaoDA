**BÁO CÁO TỔNG QUAN VỀ HỆ THỐNG WEB VÀ CÔNG VIỆC CỤ THỂ**

**Giảng viên hướng dẫn: Tô Hải Thiên**
**Sinh viên thực hiện:Dương Thị Ngọc**
**Nhánh Git (Branch)**: Hopdongthue
**Dự án: Hệ thống Web Quản lý Phòng trọ**
**I. TỔNG QUAN VỀ DỰ ÁN**

**1. Thực trạng & Thách thức trong quản lý trọ truyền thống**
Hiện nay, phần lớn các chủ dãy trọ và chung cư mini vẫn quản lý thông tin khách thuê và hợp đồng bằng sổ sách chép tay hoặc file Excel rời rạc. Phương pháp này tồn tại 3 hạn chế lớn:
**Tốn thời gian & Dễ sai sót:** Khâu lưu trữ thông tin cá nhân (CCCD, địa chỉ thường trú, SĐT người thân) và thiết lập điều khoản hợp đồng (tiền cọc, giá thuê, ngày chốt tiền) hoàn toàn thủ công. Điều này khiến chủ trọ mất nhiều thời gian rà soát và dễ nhầm lẫn khi tra cứu. 
**Rủi ro pháp lý & Thiếu minh bạch:** Thông tin định danh của khách thuê không được quản lý tập trung, gây khó khăn khi đăng ký tạm trú với cơ quan công an. Khách thuê cũng khó chủ động tra cứu chi tiết điều khoản hợp đồng hay danh sách thành viên ở cùng phòng. 
**Thất thoát & Khó kiểm soát hợp đồng:** Chủ trọ gặp khó khăn trong việc theo dõi thời hạn hợp đồng, dẫn đến tình trạng hợp đồng hết hạn nhưng chưa được gia hạn hoặc thanh lý. Bên cạnh đó, việc quản lý trạng thái phòng trống / đang thuê khi có sự thay đổi khách thuê cũng dễ bị xáo trộn. 
**2. Giải pháp của hệ thống (Module Khách thuê & Hợp đồng)**
Hệ thống Web Quản lý Phòng trọ cung cấp giải pháp số hóa tập trung, giúp tối ưu hóa quy trình quản lý khách thuê và hợp đồng cho cả Chủ trọ và Người thuê:
**Số hóa hồ sơ & Quản lý tập trung:** Tự động hóa việc lưu trữ thông tin định danh (CCCD, nơi cấp, ngày cấp, SĐT khẩn cấp) và tự động liên kết với tài khoản người dùng của khách thuê để phục vụ tra cứu. 
**Minh bạch thông tin & Tự động đồng bộ:** Khách thuê có tài khoản riêng để chủ động xem hợp đồng điện tử, thông tin đại diện và danh sách thành viên ở chung. Đồng thời, hệ thống tự động cập nhật trạng thái phòng (DANG_THUE / TRONG) ngay khi lập hoặc thanh lý hợp đồng. 
**Quản lý hợp đồng & Ràng buộc chặt chẽ:** Hỗ trợ lập hợp đồng nhanh chóng theo quy trình, theo dõi thời hạn hợp đồng, quản lý tiền đặt cọc và thanh lý hợp đồng chính xác, giúp hạn chế tối đa rủi ro tranh chấp và thất thoát dữ liệu. 
**II. BÁO CÁO PHÂN CÔNG CÔNG VIỆC CÁ NHÂN & TIẾN ĐỘ THỰC HIỆN**

**Sinh viên phụ trách: Dương Thị Ngọc**
**Phân hệ đảm nhận: **Module Quản lí hồ sơ khách hàng& hợp đồng khách hàng
**1. Vai trò & Phân công Trách nhiệm trong Nhóm**

**Vai trò: **UI Frontend Developer & Backend Designer cho Hồ sơ&Hợp đồng của khách hàng
**Trách nhiệm đảm nhận:**
oThiết kế Giao diện người dùng (UI/UX) cho màn hình Quản lý Hồ sơ (tenants), Hợp đồng thuê trọ (contracts), Danh sách người ở cùng (contract_members), Lịch sử thuê.
oXây dựng cấu trúc Cơ sở dữ liệu (Database Schema) cho 3 bảng: (tenants, contracts, contract_members).
oĐặc tả chi tiết logic nghiệp vụ và kịch bản xử lý API cho phân hệ tài chính.
**2. Chi tiết Nghiệp vụ & Giao diện Phụ trách**

**A. Màn hình Quản lý Hồ sơ khách thuê(tenants)**

Giao diện & Chức năng: Thiết kế màn hình cho phép chủ trọ nhập tay thông tin cá nhân của khách thuê.
Nghiệp vụ xử lý: Nhằm lưu trữ, cập nhật và quản lý toàn bộ thông tin định danh pháp lý cũng như thông tin liên hệ của những người thuê trọ. 
       +Đối với Chủ trọ / Quản lý: Đảm bảo chính xác thông tin pháp lý để đăng ký tạm trú/tạm vắng với cơ quan công an, dễ dàng liên hệ khẩn cấp khi có sự cố. 
+Đối với Khách thuê: Tự động liên kết tài khoản cá nhân để xem thông tin hợp đồng, hóa đơn và gửi phản hồi/sự cố cho chủ trọ.
B. Màn hình Quản lý Hợp đồng (contracts)

 **Tổng quan & Bộ lọc danh sách hợp đồng:**
Hiển thị các thẻ thống kê nhanh (Dashboard mini): Tổng số hợp đồng, Hợp đồng đang hiệu lực, Hợp đồng sắp hết hạn và Hợp đồng đã thanh lý. 
Thanh tìm kiếm thông minh và bộ lọc linh hoạt theo: Mã hợp đồng, Số phòng, Người đại diện hoặc Trạng thái hợp đồng (HIEU_LUC / DA_THANH_LY). 
** Form Lập hợp đồng mới (Quy trình 3 bước trực quan):**
Bước 1 (Thông tin hợp đồng): Chọn phòng thuê (chỉ liệt kê các phòng có trạng thái TRONG), nhập Giá thuê (rental_price), Tiền đặt cọc (deposit_amount), Thời hạn thuê (start_date đến end_date) và Ngày chốt tiền hàng tháng (billing_cycle_day). 
Bước 2 (Người đại diện): Tìm kiếm và chọn 01 Khách thuê làm người đại diện pháp lý chính trên hợp đồng (representative_tenant_id). 
Bước 3 (Thành viên ở cùng): Thêm danh sách các thành viên ở chung phòng vào hợp đồng (contract_members). 
Tự động hóa: Ngay khi lưu hợp đồng, hệ thống tự động chuyển trạng thái hợp đồng sang HIEU_LUC và cập nhật trạng thái phòng thuê từ TRONG -> DANG_THUE. 
**3. Thiết kế CSDL & Định hướng Nghiệp vụ Backend (Sẵn sàng lập trình API)**

  **Cấu trúc Cơ sở dữ liệu (MySQL):**
 **Bảng tenants:** Lưu trữ thông tin định danh cá nhân và liên hệ của người thuê trọ (tenant_id, user_id, identity_card_number, issue_date, issue_place, permanent_address, emergency_contact). 
 **Bảng contracts:** Lưu chi tiết các điều khoản hợp đồng thuê phòng giữa chủ trọ và khách thuê (contract_id, room_id, representative_tenant_id, rental_price, deposit_amount, start_date, end_date, billing_cycle_day, status). 
 **Bảng contract_members:** Lưu danh sách các thành viên ở cùng phòng thuộc một hợp đồng (id, contract_id, tenant_id). 
 ** Định hướng Logic API sẽ triển khai:**
 POST /api/v1/tenants: Tiếp nhận thông tin định danh khách thuê từ giao diện, kiểm tra tính duy nhất của số CCCD/CMND (identity_card_number) trước khi tạo hồ sơ mới. 
POST /api/v1/contracts: Khởi tạo hợp đồng mới, kiểm tra điều kiện phòng phải có trạng thái TRONG, tự động đồng bộ chuyển trạng thái phòng sang DANG_THUE và đặt trạng thái hợp đồng thành HIEU_LUC. 
 PUT /api/v1/contracts/{id}/terminate: Tiếp nhận yêu cầu thanh lý hợp đồng, cập nhật trạng thái hợp đồng thành DA_THANH_LY và tự động trả trạng thái phòng về lại TRONG. 
**  III. DỰ KIẾN XỬ LÝ CÁC TRƯỜNG HỢP NGOẠI LỆ (EDGE CASES)**

Trong bước phát triển logic backend tiếp theo, em thiết lập các quy tắc ràng buộc chặt chẽ sau:
1. Ràng buộc tạo hợp đồng & trạng thái phòng: Khóa không cho phép lập hợp đồng mới nếu phòng đang chọn không ở trạng thái TRONG (đã có hợp đồng HIEU_LUC khác). Ngày kết thúc hợp đồng (end_date) bắt buộc phải lớn hơn ngày bắt đầu (start_date). 
2. Chống trùng lặp dữ liệu định danh: Ràng buộc Unique cho số CCCD/CMND (identity_card_number) trong bảng tenants để tránh việc nhập trùng một hồ sơ khách thuê nhiều lần. Ràng buộc mối quan hệ 1-1 giữa tài khoản người dùng (user_id) và hồ sơ khách thuê. 
3. Quản lý khóa hợp đồng khi thanh lý: Khi hợp đồng chuyển sang trạng thái DA_THANH_LY, hệ thống sẽ khóa không cho phép sửa đổi thông tin điều khoản thuê (giá thuê, ngày chốt tiền). Đồng thời, tự động cập nhật chuyển trạng thái phòng từ DANG_THUE về lại TRONG ngay khi bấm thanh lý thành công. 
4. Ràng buộc an toàn dữ liệu khách thuê: Chặn không cho xóa cứng hồ sơ khách thuê (tenants) nếu họ đang làm người đại diện hoặc đang là thành viên trong một hợp đồng còn hiệu lực (HIEU_LUC). 

**IV. HÌNH ẢNH MINH HỌA GIAO DIỆN ĐÃ THIẾT KẾ**

1. Giao diện Màn hình Khách thuê(tenants)


2. Giao diện Màn hình Hợp đồng(contracts)


V. CÔNG CỤ SỬ DỤNG & QUY TRÌNH QUẢN LÝ CODE

Công nghệ UI: ReactJS, HTML/CSS, Tailwind CSS / Bootstrap.
Quản lý mã nguồn (Git Flow):
oTất cả các file giao diện và cấu hình được làm việc trên nhánh cá nhân linh.
oLệnh Git thực hiện:
git checkout hopdongthue
git add .
git commit -m "Thêm gd hợp đồng&hồ sơ "
git push origin hopdongthue
o

