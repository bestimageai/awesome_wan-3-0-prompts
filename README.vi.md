<p align="center"><a href="https://bestimage.ai/"><img src="assets/bestimage-logo.svg" width="72" alt="Biểu trưng bestimage.ai"></a></p>

# Bộ sưu tập câu lệnh video Wan 3.0 — Hướng dẫn tiếng Việt

**148 bản hướng dẫn dàn dựng video thuộc 14 nhóm**.

[Trang chính tiếng Anh](README.md) · [Đủ 15 ngôn ngữ](locales/README.md) · [Mục lục toàn bộ cảnh](prompts/README.md)

![Hình ý tưởng: người quản lý tư liệu mở bản đồ sao trong phòng bản đồ của đài thiên văn lúc bình minh](assets/wan-3-prompt-collection-hero.png)

*Đây là hình tĩnh được tạo bằng công cụ tạo ảnh tích hợp, không phải đầu ra video của Wan 3.0. Xem [câu lệnh tạo ảnh và nguồn gốc](assets/README.md).*

## Phạm vi và cách bắt đầu

Có hướng dẫn nhập môn và bản dịch của cùng một câu lệnh đối chiếu bằng 15 ngôn ngữ, **không phải bản dịch đầy đủ của cả 148 mục**. Sáu nhóm đầu dùng tiếng Trung, tám nhóm còn lại dùng tiếng Anh. Câu lệnh đối chiếu và các bản dịch không được tính thành mục bổ sung.

Chọn một bản hướng dẫn từ mục lục, thay các chi tiết có thể điều chỉnh và chuẩn bị đủ đầu vào. Mô tả tài liệu tham chiếu nói về vai trò, không có nghĩa kho cung cấp sẵn các tệp đó. Đặt thời lượng, tỷ lệ khung hình, độ phân giải và âm thanh trong giao diện hoặc trường yêu cầu đã chọn; chỉ ghi trong câu lệnh không cấu hình được yêu cầu API. Thử với quy mô nhỏ rồi kiểm tra hành động, hình học, nhận dạng, thời điểm và âm thanh.

## Cấu trúc câu lệnh tám lớp

```text
[Đầu ra] thời lượng + tỷ lệ khung hình + hình thức thể hiện
[Chủ thể] đặc điểm nhận dạng cố định + trang phục hoặc chất liệu + chi tiết không được đổi
[Bối cảnh] thời gian + địa điểm + thời tiết + các lớp không gian
[Hành động] nguyên nhân → chuyển động liên tục → kết quả nhìn thấy
[Máy quay] cỡ cảnh + vị trí + một đường di chuyển + bố cục cuối
[Hình ảnh] ánh sáng + màu sắc + bề mặt + nhòe chuyển động
[Âm thanh] âm môi trường + âm hành động + nhạc + ngôn ngữ lời thoại (nếu được hỗ trợ)
[Ràng buộc] yếu tố phải giữ + vấn đề cần tránh
```

## Câu lệnh đối chiếu đầy đủ

**Chế độ:** văn bản thành video · **Thiết lập:** 10 giây, 16:9, bật âm thanh · **Đầu vào:** không có

```text
Tạo một cảnh quay tài liệu dài 10 giây, tỷ lệ 16:9, tại điểm cho mượn dụng cụ cộng đồng yên tĩnh. Một tình nguyện viên trưởng thành tóc xoăn ngắn, mặc tạp dề vàng mù tạt và áo sơ mi xanh hải quân xắn tay, sửa chiếc quạt bàn nhỏ màu đỏ trong khi phích cắm luôn được rút khỏi ổ điện. Từ 0–3 giây, người này đặt lồng bảo vệ đã tháo xuống cạnh chiếc quạt đứng yên. Từ 3–7 giây, dùng khăn mềm lau bụi trên một cánh quạt, đồng thời máy quay trượt chậm sang phải ở độ cao mặt bàn. Từ 7–10 giây, đặt khăn xuống và căn lồng bảo vệ khớp với vỏ quạt, không cắm điện hay bật quạt. Ánh sáng cửa sổ làm rõ bề mặt kim loại đã mòn và chất vải bông. Âm thanh: tiếng khăn cọ, một tiếng tách khẽ của lồng bảo vệ và âm nền căn phòng yên tĩnh; không lời nói, không nhạc. Giữ nguyên cùng một người, cùng một chiếc quạt, ba cánh quạt, vỏ màu đỏ và dây nguồn luôn chưa cắm điện. Không có cánh quạt quay, dụng cụ bổ sung, nhãn đọc được, phụ đề hay chuyển cảnh cắt.
```

**Có thể thay đổi:** màu tạp dề, màu quạt, ánh sáng phòng. **Kiểm tra:** phích cắm luôn được rút và quạt luôn đứng yên; số cánh và sự tiếp xúc của tay nhất quán. Đây là ý tưởng sáng tạo, không phải hướng dẫn sửa thiết bị điện.

## Chọn API Wan 3.0 trên bestimage.ai

| Lựa chọn (trang mô hình bằng tiếng Anh) | Đầu vào và điểm cần kiểm tra |
|---|---|
| [Văn bản thành video](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/) | Mô tả một sự kiện trọn vẹn gồm nguyên nhân, hành động trung gian và kết quả nhìn thấy |
| [Ảnh thành video](https://bestimage.ai/models/alibaba/wan-3-0-image-to-video/) | Theo tài liệu của nền tảng này, cần ảnh đầu **và ảnh cuối**; giải thích quá trình chuyển đổi vật lý và giữ cấu trúc, bố cục |
| [Tham chiếu thành video](https://bestimage.ai/models/alibaba/wan-3-0-reference-to-video/) | Gán một vai trò rõ ràng cho từng tham chiếu về nhân vật, vật thể, không gian, chuyển động hoặc âm thanh |
| [Chỉnh sửa video](https://bestimage.ai/models/alibaba/wan-3-0-video-edit/) | Cung cấp video nguồn và một thay đổi có phạm vi giới hạn; giữ diễn xuất, thời lượng, máy quay và mọi vùng còn lại |

Trang mô hình cung cấp giao diện hiện tại và các ví dụ yêu cầu công khai. Các sản phẩm Wan không nhất thiết có cùng tùy chọn điều khiển. Xem [khả năng và giới hạn](guides/model-capabilities.md).

[Hướng dẫn quy trình API và kiểm soát chi phí](guides/bestimage-wan-3-api.md) bằng tiếng Anh trình bày yêu cầu, truy vấn trạng thái định kỳ, kiểm tra đầu vào và kế hoạch thử. **Máy chủ API của bestimage.ai là `https://api.flaq.ai`.** Hãy dùng khóa API được cấp qua tài khoản bestimage.ai của bạn. Kiểm tra giá và điều kiện mới nhất trên trang mô hình và tài khoản trước khi dùng tín dụng.

## Chuẩn bị ảnh tham chiếu bằng GPT Image 2

[GPT Image 2](https://bestimage.ai/models/openai/gpt-image-2/) tạo ảnh tĩnh; [GPT Image 2 Edit](https://bestimage.ai/models/openai/gpt-image-2-edit/) chỉnh sửa ảnh và kết hợp các tham chiếu hình ảnh. Dùng chúng để chuẩn bị bảng thiết kế nhân vật, ảnh tham chiếu sản phẩm hoặc bố cục đầu và cuối đã được duyệt. Xuất và kiểm tra ảnh trước khi đưa vào lựa chọn Wan phù hợp.

Đây là **các mô hình ảnh riêng biệt**, không phải điểm cuối video Wan. Kho không tự động hóa bước chuyển tiếp này, cũng không khẳng định các hình ý tưởng được tạo qua những API đó. Xem [quy trình chuẩn bị khung hình tham chiếu](guides/bestimage-wan-3-api.md#gpt-image-2-reference-frame-workflow).

## Hướng dẫn và đóng góp

[Hướng dẫn viết câu lệnh](guides/prompting-guide.md), [khả năng mô hình](guides/model-capabilities.md) và [khắc phục sự cố](guides/troubleshooting.md) dùng tiếng Trung giản thể; hướng dẫn API dùng tiếng Anh. Không phải mọi hướng dẫn đều đã được dịch. Danh sách nhóm và số lượng có trong [trang chính tiếng Anh](README.md).

Đọc [hướng dẫn đóng góp](CONTRIBUTING.md) trước khi chia sẻ. Ghi rõ thiết lập chính xác, vai trò đầu vào, quyền sử dụng, quan sát và trạng thái đã thử hoặc chưa thử một cách trung thực. Không chia sẻ thông tin xác thực, tài liệu riêng tư hay URL nội dung có chữ ký sẽ hết hạn.

## Giới thiệu bestimage.ai

Đội ngũ [bestimage.ai](https://bestimage.ai/) tuyển chọn và duy trì thư viện câu lệnh này, kết nối quy trình sáng tạo với API của các mô hình hình ảnh và video.

## Kiếm hoa hồng với chương trình tiếp thị liên kết bestimage.ai

Bạn làm hướng dẫn, chia sẻ câu lệnh hay xuất bản ví dụ tích hợp API? Tham gia [chương trình tiếp thị liên kết bestimage.ai](https://bestimage.ai/affiliate-program/) và nhận hoa hồng khi giới thiệu bestimage.ai đến độc giả, người xem của bạn.

- **20%** cho đơn hàng trả phí hợp lệ đầu tiên của người dùng được giới thiệu.
- **10%** cho các đơn hàng trả phí hợp lệ tiếp theo trong **60 ngày sau khi người dùng đó đăng ký**.

Điều kiện đơn hàng và việc thanh toán tuân theo [thỏa thuận tiếp thị liên kết hiện hành](https://bestimage.ai/affiliate-agreement/).

## Giấy phép

[MIT](LICENSE).
