# Learning Android
Tự học lập trình Android
Các phần quan trọng cần chú ý để tiếp cận Lập trình Android:
+ Activity
+ Services
+ Broad Cast Receiver
+ Content Provider

Thành phần ứng dụng là khối kiến trúc cơ bản của ứng dụng Android. Các thành phần này được liên kết lỏng lẻo bởi các tập tin kê khai ứng dụng: AndroidManifest.xml, mô tả mỗi thành phần của ứng dụng và cách chúng tương tác.

4 thành phần chính được sử dụng trong ứng dụng Android:

 Activities: Ra lệnh cho giao diện và sử lý tương tác của người dùng với màn hình smartPhone.
 Services: Là thành phần chạy phía sau, chạy bên trong của mỗi ứng dụng.
 Broadcast Receivers: Xử lý việc giao tiếp giữa HĐH Android và ứng dụng.
 Content Providers: Xử lý dữ liệu và  các vấn đề về quản lý cơ sở dữ liệu.

##1. Activities

Một Activity đại diện cho một màn hình với một giao diện người dùng. VD: Một ứng dụng Email sẽ có một Activity để hiển thị tất cả các Email, một Activity khác để để soạn Email, một Activity khác để đọc Email. Nếu một ứng dụng có nhiều hơn 1 Activity thì một trong số chúng sẽ được đánh dấu là Activity hiển thị đầu tiên khi ứng dụng khởi chạy.

Một Activity là một Class con của Class Activities:

public class MainActivity extends Activity {
}

##2. Services

Một Service là một thành phần được chạy bên trong nền để xử lý các công việc trong thời gian dài. Một ứng dụng nghe nhạc có thể phát nhạc, trong khi đó người dùng đang ở giao diện của ứng dụng khác. Hoặc ứng dụng download có thể tải dữ liệu trên mạng về máy mà không ngăn chặn người dùng tương tác với các ứng dụng khác.

Một Service là một Class con của Class Service:

public class MyService extends Service {
}

##3. Broadcast Receivers

Broadcast Receivers chỉ đơn giản là xử lý và phát các thông điệp từ các ứng dụng khác hoặc từ hệ thống. Ví dụ: các ứng dụng có thể bắt đầu phát thông điệp đến các ứng dụng khác để cho biết rằng một số dữ liệu đã được tải thành công xuống thiết bị và sẵn sàng cho việc sử dụng, Broadcast Receivers sẽ đảm nhận việc thông báo vào đưa ra những hành động thích hợp.

A Broadcast Receiver được thực thi như là một class con của class BroadcastReceiver và mỗi thông điệp là một Intent.

public class MyReceiver extends BroadcastReceiver {
 }

##4. Content Providers

Một Content Providers chứa các thành phần cung cấp dữ liệu từ một ứng dụng đến một ứng dụng khác theo yêu cầu. Yêu cầu đó được sử lý bằng các phương thức của class ContentResolver. Dữ liệu được lưu trữ trong file hệ thống, trong cơ sở dữ liệu hoặc ở một nơi nào khác.
Một Content Providers được thực thi như là class con của class ContentProvider và phải thực thi theo tiêu chuẩn trong bộ các API để cho các ứng dụng khác có thể giao tiếp.

public class MyContentProvider extends ContentProvider { 
 
}

* Chúng ta sẽ đi vào chi tiết các thành phần này trong các phần sau.

##5. Một số thành phần khác.

Ngoài các thành phần chính nêu ở trên còn có một số thành phần khác. Các thành phần này sẽ bổ sung, tạo mối liên hệ logic giữa chúng.

+ Fragments: Đại diện cho một hành vi hoặc một phần của giao diện người dùng trong một Activity.
+ Views: Thành phần giao diện được vẽ trên màn hình bao gồm các button, textView, list,…
+ Layouts: Phân chia, định dạng màn hình, và sự thể hiện các Views.
+ Intents: Đóng gói các thông điệp.
+ Resources: Các phần tử bên ngoài: chuỗi, hằng số, hình ảnh, …
+ Manifest: Tập tin cấu hình của các ứng dụng.

[Nguồn tham khảo](https://laptrinhtuduy.wordpress.com/2014/04/20/cac-thanh-phan-cua-ung-dung-android/)

 

 
