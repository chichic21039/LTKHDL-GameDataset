# 1. Project overview and team info
## 1.1 Project overview
-   Đồ án này thực hiện lại toàn bộ một quy trình khoa học dữ liệu từ thu thập dữ liệu, tiền xử lí, khám phá dữ liệu, xây dựng mô hình,... để giúp sinh viên hiểu hơn về một quy trình và vai trò của một nhà khoa học dữ liệu. Tập dữ liệu trong đồ án này có tên VGChart(Games Dataset) được lấy từ nguồn trên kaggle liên quan đến doanh số bán lẻ video game ở các khu vực và toàn thế giới
## 1.2 Group information

- Họ tên: Phạm Khánh Linh, MSSV: 23127083 <br>
- Họ tên: Võ Trung Hiếu, MSSV: 23127190<br>
- Họ tên: Võ Hoàng Thương,MSSV: 23127493<br>

# 2. Dataset source and description
## 2.1 Dataset source
- Nguồn dữ liệu được lấy trên kaggle:
- Link: https://www.kaggle.com/datasets/gsimonx37/vgchartz
- Tác giả: https://www.kaggle.com/gsimonx37
## 2.2 Dataset description
Tập dữ liệu được thu thập từ trang https://www.vgchartz.com/

Tập dữ liệu gồm các cột và ý nghĩa mỗi cột như sau:
- name: tên của trò chơi điện tử.
 - date: ngày phát hành trò chơi điện tử.
 - platform: nền tảng chơi game (All – tất cả nền tảng, Series – toàn bộ series game).
 - publisher: nhà phát hành.
 - developer: nhà phát triển.
 - shipped: số lượng bản đã xuất xưởng (chỉ áp dụng với các bản ghi có platform là All hoặc Series).
 - total: tổng số bản đã bán ra (tính theo triệu bản).
 - america: số bản bán tại khu vực Châu Mỹ (triệu bản).
 - europe: số bản bán tại khu vực Châu Âu (triệu bản).
 - japan: số bản bán tại Nhật Bản (triệu bản).
 - other: số bản bán ở các khu vực khác trên thế giới.
 - vgc: điểm đánh giá từ VGChartz.com.
 - critic: đánh giá từ giới phê bình.
 - user: đánh giá từ người dùng.

 # 3. Research questions list
 - Câu hỏi 1: Sự phối hợp giữa Publisher và Developer có ảnh hưởng đến hiệu quả game không?
 - Câu hỏi 2: Theo thời gian, platform nào phát triển, platform nào "chết"?
 - Câu hỏi 3: Các khu vực như Bắc Mỹ, châu Âu, Nhật Bản có mô hình tiêu thụ game khác nhau như thế nào giữa các nền tảng, và nền tảng nào thể hiện sự vượt trội rõ rệt tại từng khu vực?
 - Câu hỏi 4: Xu hướng phát hành và doanh số game thay đổi như thế nào theo từng năm? Liệu có thể quan sát được các mô hình dài hạn của thị trường game qua thời gian hay không?
- Câu hỏi 5: “Game được đánh giá cao (critic/user/VGC) có thực sự bán chạy hơn không, ở mức toàn cầu và từng khu vực?”
- Câu hỏi 6: Phân tích sức ảnh hưởng của các yếu tố định danh (Identity Factors) lên doanh số toàn cầu: Liệu danh tiếng, năm phát hành, nền tảng có đủ để đảm bảo thành công thương mại?

# 4. Key findings summary
1. Phân tích cho thấy chênh lệch doanh số mạnh nằm ở nhóm critic 9–10 so với phần còn lại.
- Nếu chi phí cho thiết kế game giúp game từ ~7–8 lên ~9–10 là hợp lý, đây có thể là khoản đầu tư có lợi về doanh số trung bình.
- Ngược lại, cố gắng kéo từ 6 → 7.5 nhưng vẫn không chạm 9 có thể không mang lại khác biệt doanh số rõ rệt.

2. Thị trường nền tảng cho video game đang thu hẹp, ghi nhận gần nhất chỉ có 6 platform đang phổ biến.
- Có 2 platform có vẻ tiềm năng: PS5 và XS. 
- PS5 được marketing khá mạnh nên có vẻ được giới trẻ biết đến rất nhiều, doanh số cũng có xu hướng tăng.
- Nhà phát hành và phát triển muốn chạy theo xu thế nên làm game trên hai platform này.
3. Platform ưa thích (dựa theo doanh số) của mỗi khu vực là khác nhau:
- America: GEN
- Europe: GBC
- Japan: NES 
- Other: PS4
Nếu bạn là nhà phát hành/phát triển mới, nên lựa chọn platform ưa thích của từng khu vực.
4. Thị trường video game bùng nổ nhất vào năm 2010-2011, lúc đó doanh số toàn cầu ghi nhận là hơn 200 triệu bản, sau giai đoạn đó giảm mạnh đến 2020. 
- Sau 2020 không có data nên không khẳng định được, nhưng có thể đoán được thị trường video game giảm mạnh đến vậy do sự phát triển của điện thoại, laptop, dần dần video game sẽ tốn kém hơn nhiều so với các game trên app hay trên web. Tuy nhiên video game vẫn luôn có chỗ đứng trong giới game thủ.
5. Danh tiếng nhà phát hành và nhà phát triển hay platform của game hay năm phát triển chỉ giải thích được 25% cho doanh số bán ra, trong đó danh tiếng của nhà phát triển chiếm vị trí quan trọng nhất 75% còn lại có thể thuộc về những phần không có trong dataset này như thể loại game, kinh phí marketing, ...

# 5. File structure explanation
- Thư mục data: Lưu dữ liệu gốc và dữ liệu đã tiền xử lí
- Thư mục raw: Lưu dữ liệu của tập dữ liệu gốc trên kaggle
- Thư mục processed: Lưu dữ liệu đã tiền xử lí (chỉ khác với dữ liệu gốc là loại bỏ các dòng thiếu developer và điền data bằng trung vị của nền tàng)
- Thư mục notebooks: Gồm các file ipynb dùng để code
- File notebooks/1_Exporation.ipynb: Trong file này chủ yếu mô tả, khám phá tổng quan và tiền xử lí dữ liệu sau đó lưu vào trong data/processed để phục vụ trả lời câu hỏi và modelling trong file notebooks/2_Analysis.ipynb
- File notebooks/2_Analysis.ipynb: Dùng để khám phá trả lời các câu hỏi và modelling từ tập dữ liệu đã tiền xử lí

# 6. How to run instructions

Để chạy các notebook và phân tích dữ liệu, hãy làm theo các bước sau:

1. **Clone repository**
   ```
   git clone https://github.com/yourusername/LTKHDL-GameDataset.git
   cd LTKHDL-GameDataset
   ```

2. **Cài đặt môi trường Python**
   - Cài đặt các thư viện yêu cầu:
     ```
     pip install -r requirements.txt
     ```
3. **Chạy Jupyter Notebook**
   ```
   jupyter notebook
   ```
   và mở lần lượt các notebook trong thư mục `notebooks` để thực hiện phân tích:
   - `notebooks/1_Exploration.ipynb` (khám phá, tiền xử lý, lưu dữ liệu)
   - `notebooks/2_Analysis.ipynb` (trả lời câu hỏi và modeling)

4. **Dữ liệu**
   - Dữ liệu gốc nằm trong `data/raw`
   - Dữ liệu đã tiền xử lý sẽ được lưu vào `data/processed` sau khi chạy notebook 1.

5. **Lưu ý**
   - Nếu gặp lỗi thiếu dữ liệu, hãy chạy lại notebook 1 trước khi sang notebook 2.
   - Có thể chỉnh sửa đường dẫn file nếu thay đổi cấu trúc thư mục.

**Tóm tắt:**  
Cài Python + Package, chạy Jupyter Notebook, thực thi từng notebook theo thứ tự trong folder `notebooks` để phân tích.

# 7. Dependencies list

Dưới đây là danh sách các thư viện Python cần thiết để chạy các notebook trong project này:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `jupyter`
- `scikit-learn`

Bạn có thể cài đặt bằng lệnh:

```
pip install -r requirements.txt
```


