- Yêu cầu:
	+ PHP Version >=  5.2.8.
- Kiểm tra xem mod_rewrite có enable chưa, nếu chưa thì enable.
- CHMOD -R 777 thư mục 123host/app/tmp (chmod -R 777 123host/app/tmp).
- Config database trong 123host/app/Config/database.php.
- Tạo crontab có nội dung như sau:
	+ 0 9,21 * * * wget -O - http://112.78.1.166/sends/get_posts
	+ Giải thích: cứ vào lúc 9,21 giờ hàng này thì nó tự động call 1 request đến url trên.
			trong đó (http://112.78.1.166 được thay bằng page của bạn)
			- request này chỉ call được khi crontab được chạy ở đúng server chứa resource.







