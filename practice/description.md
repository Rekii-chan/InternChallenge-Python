# Phân Tích Dữ Liệu SEO/Marketing

## Mô Tả

Công ty ABC đang vận hành một nền tảng trực tuyến với mục tiêu tối ưu hóa các chiến dịch SEO và marketing của mình. Công ty đã thu thập một lượng lớn dữ liệu từ các chiến dịch marketing trực tuyến để phân tích và tối ưu hóa hiệu quả. Bạn được giao nhiệm vụ viết một chương trình Python để phân tích dữ liệu này và đưa ra những phân tích có ý nghĩa.

## Yêu Cầu

### Xử Lý Dữ Liệu Truy Cập:

- Tính tổng số lượt truy cập cho từng nguồn truy cập.
- Phân loại các trang có hiệu suất cao nhất dựa trên tỷ lệ chuyển đổi.

### Phân Tích Chiến Dịch Marketing:

- Xác định chiến dịch marketing có ROI cao nhất.
- Phân loại các chiến dịch dựa trên hiệu quả của chúng.

### Tối Ưu Hóa Từ Khóa:

- Tìm từ khóa có số lượt tìm kiếm và chuyển đổi cao nhất.
- Đưa ra danh sách từ khóa tiềm năng cần tối ưu.

### Phân Tích Khách Hàng:

- Xác định nhóm khách hàng mục tiêu dựa trên dữ liệu nhân khẩu học.
- Phân loại khách hàng theo hành vi truy cập.

## Chi Tiết Yêu Cầu

### 1. Xử Lý Dữ Liệu Truy Cập

**Tính Tổng Lượt Truy Cập:** Tạo một hàm `calculate_total_visits(data)` để tính tổng số lượt truy cập từ từng nguồn (organic, direct, referral, social).

**Phân Loại Hiệu Suất Trang Web:** Tạo một hàm `classify_page_performance(data)` để phân loại các trang có hiệu suất cao nhất dựa trên tỷ lệ chuyển đổi. Tỷ lệ chuyển đổi được tính bằng công thức:

`Conversion Rate` = (`Number of Conversions` / `Number of Visits`) \* 100

- **Trang Hiệu Suất Cao:** Tỷ lệ chuyển đổi > 20%
- **Trang Trung Bình:** 10% <= Tỷ lệ chuyển đổi <= 20%
- **Trang Hiệu Suất Thấp:** Tỷ lệ chuyển đổi < 10%

### 2. Phân Tích Chiến Dịch Marketing

**Xác Định Chiến Dịch ROI Cao Nhất:** Tạo một hàm `find_highest_roi_campaign(data)` để tìm chiến dịch có `Return on Investment (ROI)` cao nhất. ROI được tính theo công thức:

`ROI` = ((`Revenue` − `Cost`) / `Cost`) \* `100`

**Phân Loại Chiến Dịch Marketing:** Tạo một hàm `classify_marketing_campaigns(data)` để phân loại chiến dịch thành các nhóm dựa theo `campaign_name`:

trả về dict với content như sau:

- **Số lượng Chiến Dịch Hiệu Quả Cao:** ROI > 50%
- **Số lượng Chiến Dịch Trung Bình:** 20% <= ROI <= 50%
- **Số lượng Chiến Dịch Kém Hiệu Quả:** ROI < 20%

```python
{
    'Number of Good Campaigns': int,
    'Number of Medium Campaigns': int,
    'Number of Bad Campaigns': int,
}
```

### 3. Phân Tích Chiến Dịch Marketing với ROI và Phân Loại Ngân Sách

Viết một hàm `analyze_marketing_campaigns(data)` nhận đầu vào là một danh sách chứa thông tin về các chiến dịch marketing.

### Phân loại các chiến dịch thành các loại ngân sách dựa trên chi phí:

- **High Budget**: Chi phí > 1000
- **Medium Budget**: 500 <= Chi phí <= 1000
- **Low Budget**: Chi phí < 500

### Tìm chiến dịch có ROI cao nhất trong mỗi loại ngân sách:

- High Budget
- Medium Budget
- Low Budget

## Kết Quả

Trả về một `dict` với cấu trúc sau:

```python
{
    'High Budget': {
        'campaign_id': str,
        'campaign_name': str,
        'cost': int,
        'revenue': int,
        'roi': float
    },
    'Medium Budget': {
        'campaign_id': str,
        'campaign_name': str,
        'cost': int,
        'revenue': int,
        'roi': float
    },
    'Low Budget': {
        'campaign_id': str,
        'campaign_name': str,
        'cost': int,
        'revenue': int,
        'roi': float
    }
}
```
