1. Huấn luyện mô hinh
Có 2 tình huóng được đưa ra trong bài:
- Biết trước số lượng class: chạy folder "fix", trong folder chạy file main_known.py
- Không biết trước số lượng class: chạy folder "idk", trong folder chạy file main_idk.py 

Trong mỗi file main: có các biến sau cần thay đổi:
- curdir: địa chỉ folder chứa code định chạy, để mặc định là './'
- sourcedir: địa chỉ chứa frame của OAKDATA, thường là folder 'Raw' trong 'OAK_FRAME' 
- res_dir: địa chỉ folder chứa kết quả của các file thống kê dạng txt

Trong mỗi file util.py:
- config_fp: địa chỉ file config của faster rcnn: là file 'otherfile/faster_rcnn_R_50_C4.yaml'
- pretrained_fp: địa chỉ file weight đã được huấn luyện sẵn trên PascalVOC

2. Kiểm thử mô hình
Các file dưới đây cơ bản có cùng cấu hình về biến giống với các file ở phần train,
quan trọng nhất là phần save_dir chính là result_dir ở phần trước đó 
- Chạy file 'inf_fix.py' hoặc 'inf_idk.py' ở folder 'test' để  lấy kết quả thử  nghiệm với từng step
- Chạy file 'cat_inf.py' để  tạo ra một file test tổng thể toàn bộ tất cả các step trong 1 file báo cáo
Lưu ý: path của label và frame đều nằm ở OAK_TEST
- Chạy file 'result_analysis.py' để  lấy các thông số như bwt/fwt và cap


