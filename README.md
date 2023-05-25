# DE_PROJECT_4
TODO: 
1. Tự tạo 1 báo cáo tổng quan về dữ liệu sản phẩm để cung cấp thông tin cho quyết định kinh doanh và báo cáo thị trường, về các xu hướng sản phẩm.
2. Crawl thêm các sàn thương mai khác như lazada, shopee những field chính như (name,category,price, số lượng ng mua, rating, origin) để mở rộng phạm vi.
3. Dựa vào productID, crawl toàn bộ feedback của khách hàng. Từ đó có thể phân tích những sản phẩm nào có số lượng tương tác nhiều nhất, và tương tác tốt/ xấu ntn để theo dõi hành vi của khách hàng.

**Yêu cầu**: 

1. Lấy **toàn bộ** sản phẩm đang hiển thị trên các danh mục của website tiki.vn. Dữ liệu lấy về sẽ lưu trong MongoDB. 
2. Tạo một bản sao lưu data gửi cho Coach để có thể Restore dữ liệu trên một hệ thống MongoDB khác.
3. Trích xuất các trường thông tin sau và lưu vào MySQL để cho team khác sử dụng:

fields name,short_description,description,short_url,rating_average,all_time_quantity_sold,price,id.

1. Product name: Tên sản phẩm.
2. Short description: Mô tả ngắn của sản phẩm.
3. Description: Mô tả chi tiết sản phẩm. Yêu cầu: **clean dữ liệu, lọc bỏ những tag html thừa trong mô tả.**
4. URL: Link sản phẩm.
5. Rating: Đánh giá trung bình về sản phẩm.
6. Số lượng bán.
7. Giá sản phẩm.
8. Category ID: ID của danh mục sản phẩm
1. Thống kê:
    1. Mỗi category (bao gồm cả sub-category) có bao nhiêu sản phẩm
    2. Tạo biểu đồ thống kê xuất xứ của các sản phẩm. Ví dụ từ biểu đồ có thể biết: Có bao nhiêu sản phẩm xuất xứ từ Trung Quốc. Từ đó so sánh tỉ lệ xuất xứ của các sản phẩm.
    3. Top 10 sản phẩm được bán nhiều nhất, có rating cao nhất và giá thấp nhất.
2. Lấy tất cả sản phẩm mà có thông tin “thành phần” trong mô tả. Lưu các thông tin dưới dạng CSV: product_id, ingredient.
Lưu ý, chỉ trích chọn ra thông tin miêu tả “Thành phần” trong Description, những thông tin khác không lấy. Thời gian truy vấn ra các sản phẩm có “Thành phần” trong Description phải nhanh nhất có thể
3. Download **toàn bộ** ảnh ở “base_url” của mỗi sản phẩm về lưu trong ổ cứng (mỗi sản phẩm có từ 3-5 ảnh). Format tên ảnh: productID_number. Ví dụ tên ảnh thứ nhất của sản phẩm 180001095 sẽ là 180001095_1.png. Thông tin đường dẫn ảnh của mỗi product được ghi thêm vào MySQL
4. Đưa ra idea cho leader về việc mình có thể làm gì tiếp theo với những dữ liệu này

[**Gợi ý nếu bạn gặp khó khăn**](https://www.notion.so/G-i-n-u-b-n-g-p-kh-kh-n-7a7014016e644e7bbef22aa0c48ff069)
