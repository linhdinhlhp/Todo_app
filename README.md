# Todo_app

## Tạo một cái app todo với thư viện Novu , ngôn ngữ react,express

Trong bài viết này, bạn sẽ học được cách tạo 1 app-todo phù hợp với bạn. Mục đích cơ bản của app ban đầu là thúc đẩy năng suất làm việc của chính bạn , có những công việc được hoàn thành và giúp bản thân tập trung hơn.

![Logo Dự Án](https://res.cloudinary.com/practicaldev/image/fetch/s--Ko66FLyq--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_800/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8pfv0blptsn474mf8gco.png)



Hãy thắt chặt dây an toàn và bắt đầu cuộc hành trình. 🚀
Vì sao? 🤔
Trong thời đại của cảm giác bão thông tin mà chúng ta đang sống, việc sản xuất và tập trung vào một nhiệm vụ một lúc là điều mà không nhiều người giỏi. Để vượt qua điều này, một trong những phương pháp rộng rãi được chấp nhận là có một danh sách công việc (todo list) về các nhiệm vụ bạn muốn hoàn thành.
Đây cũng là cách tiếp cận của tôi, nhưng theo thời gian, tôi bắt đầu cảm thấy hạn chế với các tính năng cơ bản và thấy mình phải dùng nhiều ứng dụng khác nhau để thực hiện các chức năng khác nhau.


**Các trường hợp sử dụng chính của tôi bao gồm:**


Một nơi để lên kế hoạch cho tuần của tôi.
Phân chia nhiệm vụ hàng ngày về những gì tôi muốn đạt được trong ngày.
Biết thời gian và ngày hiện tại.
Được truyền cảm hứng để hành động và cảm thấy thành công khi hoàn thành một nhiệm vụ.
Gửi nhắc nhở qua tin nhắn thông thường cho những người tôi đã giao nhiệm vụ.
Gửi nhắc nhở qua email chính thức cho đồng nghiệp làm việc.
Ứng dụng cần phải sẵn có ở mọi nơi.
Để thực hiện những điều này, tôi phải dùng nhiều ứng dụng khác nhau: một ứng dụng quản lý công việc chạy trên nhiều nền tảng (điều này khá khó khăn để tìm), một ứng dụng lịch, một ứng dụng trích dẫn, một ứng dụng nhắn tin và một ứng dụng email.




Không cần phải nói, việc chuyển đổi giữa nhiều ứng dụng như vậy đã làm mất mục đích ban đầu của việc sử dụng ứng dụng: tối ưu hóa năng suất cá nhân trong một môi trường không bị xao lấy.
Khi tôi thấy rằng không có ứng dụng nào có đủ tất cả các tính năng mà tôi cần, tôi quyết định xây dựng ứng dụng riêng của mình. 


Nhưng có một vấn đề: tôi có thể xây dựng một ứng dụng quản lý công việc tốt, nhưng vấn đề của tôi là gửi nhắc nhở cho người khác về nhiệm vụ được giao vẫn chưa được giải quyết.

**signUp:**

Kiểm tra xem người dùng đã tồn tại hay chưa bằng cách tìm trong cơ sở dữ liệu.
Kiểm tra tính đúng đắn của mật khẩu và xác nhận mật khẩu.
Sử dụng bcrypt để băm mật khẩu trước khi lưu vào cơ sở dữ liệu.
Tạo một người dùng mới trong cơ sở dữ liệu và trả về thông tin người dùng cùng với JWT.

**signIn:**

Kiểm tra xem người dùng có tồn tại hay không bằng cách tìm trong cơ sở dữ liệu.
Kiểm tra tính đúng đắn của mật khẩu bằng cách so sánh với mật khẩu được lưu trong cơ sở dữ liệu.
Nếu mật khẩu đúng, tạo JWT và trả về thông tin người dùng cùng với token.


Nhập cuộc với Novu!

Novu đã giúp tôi giải quyết vấn đề lớn nhất của quy trình làm việc của tôi - việc lấy điện thoại để gửi tin nhắn nhắc nhở ai đó về một nhiệm vụ họ cần phải thực hiện. Hãy nhớ rằng việc giữ môi trường không bị xao lấy là quan trọng đối với tôi, và việc lấy điện thoại là như mở cửa cho sự sao nhãng lấy bởi những thứ lôi cuốn và quyến rũ.

Nhưng với Novu, tôi có thể xây dựng một ứng dụng quản lý công việc từ đó, tôi có thể gửi nhắc nhở qua tin nhắn không chính thức đến bạn bè cũng như gửi email chính thức đến đồng nghiệp của mình.

Novu - Hệ thống thông báo mã nguồn mở dành cho nhà phát triển:

Novu là một hệ thống thông báo mã nguồn mở dành cho nhà phát triển. Nó giúp bạn quản lý tất cả các thông báo về sản phẩm, cho dù đó là thông báo trong ứng dụng (giống như biểu tượng chuông thông báo có trong Facebook), Email, SMS, Discord và những gì cần thiết.
Hãy bắt đầu với ứng dụng của chúng ta, Moonshine:
Chúng ta sẽ xây dựng ứng dụng của mình trong hai giai đoạn - phía sau (backend) và phía trước (front-end). Cả hai sẽ được lưu trữ trong các kho lưu trữ GitHub riêng biệt, và tôi cũng sẽ hướng dẫn bạn cách triển khai Moonshine lên web, cho phép chúng ta truy cập nó từ bất kỳ đâu.
Hãy bắt đầu với phía sau trước.

***

Bắt đầu với cài đặt cơ bản:
Chúng ta sẽ bắt đầu bằng một Git repo trống. Tạo một kho lưu trữ Git trống, nhập tất cả các thông tin liên quan và công bố nó lên GitHub. Sau đó, mở nó trong môi trường phát triển tích hợp của bạn (tôi sẽ sử dụng VS Code):

``` (npm init -y) 
Bước đầu tiên ở đây sẽ là cài đặt tất cả các gói cần thiết. Chúng ta sẽ phụ thuộc vào một số gói từ npm (Node Package Manager).
//npm i dotenv novu bcryptjs body-parser cors express jsonwebtoken mongoose nodemon
Để bắt đầu quá trình này, chúng ta sẽ tạo một tệp package.json bằng lệnh sau:
```


```bash
npm install
```
>Viết dấu 


–Dòng 1
–Dòng 2
–Dòng 3


