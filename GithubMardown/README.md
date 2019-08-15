# Report Github
## 1.Cách thức hoạt động của Github

- GitHub là sự kết hợp giữa 2 từ, Git – hệ thống quản lý dự án và phiên bản code và Hub – một mạng xã hội cho lập trình viên.
- GitHub được sử dụng chủ yếu cho dự án có nhiều người cùng hợp tác và cần giám sát toàn bộ thay đổi của dự án,
cũng như để ngõ khả năng khôi phục code khi cần thiết. 
- Khi sử dụng GitHub, ngoài các công việc chính như tạo Branch, tạo Pull Request và Fork một Repository, bạn có thể theo dõi, tương tác với người khác như một mạng xã hội thông thường.
## 2.Các khái niệm: Add, Remove, Commit, Push, Pull, Fetch, Clone, Fork, Star, Watch.
- Add

>Thêm vào index (Đề xuất thay đổi)

- Remove

>Để xoá 1 thư mục hay một file nào đó có thể xoá ở máy local

- Commit

>Là thao tác thông báo cho hệ thống lưu lại trạng thái hiện hành và ghi nhận lại lịch sử các xử lý file hay thư mục trên repository

- Push
>Dùng để đưa nội dung cập nhật repository cục bộ lên server

- Pull

>Lấy toàn bộ dữ liệu từ repository trên server về branch hiện tại

- Fetch
>Truy cập repository trên server và kéo toàn bộ dữ liệu từ repository đó về

- Clone 
>Sao chép một repository đã tồn tại

- Fork
>Sao chép một repository đã tồn tại, tạo ra các thay đổi cần thiết và lưu phiên bản mới này dưới dạng một repository dưới dạng độc lập hoàn toàn mới. (Tạo dự án mới trên dự án cũ)

- Star
>Là công cụ đánh dấu 1 project

- Watch
>Theo dõi một repository để nhận thông báo cho các yêu cầu mới và các vấn đề được tạo mới của repository đó

## 3.Các lệnh Git
### a.Settinh up Git
- Tải và và cài đặt bản mới nhất của Git
- [Git](https://git-scm.com/downloads)
- Tạo user name để xác thực cá nhân
- open terminal
- set a git user

$ git config --global user.name "Mona Lisa"


- Confirm that you have set the Git username correctly:

$ git config --global user.name
> Mona Lisa
- Tạo email 
- Open Terminal.
- Set a email address in git

$ git config --global user.email "email@example.com"
- Confirm that you have set the email address correctly in Git:

$ git config --global user.email
email@example.com
- Add the email address to your GitHub account by setting your commit email address, so that your commits are attributed to you and appear in your contributions graph.
### b.Generate and add SSH key
<ol>
<li> KIỂM TRA XEM MÁY BẠN CÓ SSH KEY NÀO CHƯA </li>

- Mở cửa sổ dòng lệnh (terminal) và chạy lệnh:

Is -al~/.ssh
<li> SINH RA 1 SSH KEY MỚI

- Chạy lệnh sau trên terminal

ssh–keygen –t rsa –b 4096 –C “email_cua_ban@example.com”
- Nhấn Enter nơi lưu key

Enter file in which to save the key (/Users/binhcq/.ssh/id_rsa): 
- nhập mật khẩu cho key của bạn

Enter passphrase (empty for no passphrase): [Type a passphrase]
# Enter same passphrase again: [Type passphrase again]
<li> THÊM KEY CỦA BẠN VÀO SSH-AGENT</li>

- Đảm bảo rằng ssh-agent đã được kích hoạt bằng lệnh:

eval “$(ssh-agent -s)”
# Agent pid 59566
- Add ssh key của bạn vào ssh-agent:

ssh –add ~/.ssh/id_rsa
<li>THÊM SSH PUBLIC KEY VÀO TÀI KHOẢN TRÊN SERVER CỦA BẠN (GITHUB, BITBUCKET…)</li>

- Copy ssh key vào clipboard:

pbcopy < ~/.ssh/id_rsa.pub
- Sau đó lên tài khoản của bạn, vào mục setting, tìm tới mục Add ssh key và dán nội dung đã copy lúc nãy vào
<li> KIẾM TRA LẠI XEM MỌI THỨ ĐÃ OK CHƯA:

ssh –T git@bitbucket.org
- Với github thì là :

ssh -T git@github.com
- Có thể bạn sẽ nhận được thông báo về việc thêm host bitbucket vào danh sách tin cậy
- Bạn chỉ việc gõ yes vào terminal rồi Enter là được.
Và bạn sẽ nhận được dòng thông báo thành công:

logged in as CaoQuangBinh.
- Hoặc với github

Hi BinhCQ! You‘ve successfully authenticated, but GitHub does not
# provide shell access.

### c.Caching -your GitHub password in Git.
- Install Git and the osxkeychain helper and tell Git to use it.
- Find out if Git and the osxkeychain helper are already installed:

$ git credential osxkeychain
> xcode-select: note: no developer tools were found at '/Applications/Xcode.app',
> requesting install. Choose an option in the dialog to download the command line developer tools.
- Tell Git to use osxkeychain helper using the global credential.helper config:

$ git config --global credential.helper osxkeychain
# Set git to use the osxkeychain credential helper

# REPORT MARKDOWN
## 1. Markdown là gì và dùng để làm gì
- Markdown là một ngôn ngữ đánh dấu với cú pháp văn bản thô [5], được thiết kế để có thể dễ dàng chuyển thành HTML và nhiều định dạng khác [6] sử dụng một công cụ cùng tên. 
- Nó thường được dùng để tạo các tập tin readme, viết tin nhắn trên các diễn đàn, và tạo văn bản có định dạng bằng một trình biên tập văn bản thô.
## 2. Các cú pháp thường gặp
### 1.Thẻ tiêu đề

# Tiêu đề 1

# Tiêu đề 1

## Tiêu đề cấp 2
## Tiêu đề cấp 2

###### Tiêu đề cấp 6
###### Tiêu đề cấp 6

### 2. Chèn link chèn ảnh

![Alt text][id]

### 3.Ký tự in đậm, in nghiêng
- Để in đậm một đoạn text bạn chỉ cần làm như sau:

**từ cần in đậm**

**từ cần in đậm**
- Để in nghiên một đoạn text bạn chỉ cần làm như sau:

*từ cần in nghiêng*
*từ cần in nghiêng*

### 4. Trích dẫn, bo chữ
- Để bo một đoạn text thì bạn chỉ cần sử dụng cú pháp sau:

`đoạn cần bo`

`đoạn cần bo`
- Để làm nổi bật một đoạn, chẳng hạn như một đoạn shell hay file cấu hình bạn có thể sử dụng cú pháp như ví dụ sau:

```sh        
auto eth0
iface eth0 inet static
```

```sh        
auto eth0
iface eth0 inet static
```
### 5. Gạch đầu dòng
- Gạch đầu dòng thứ nhất

- Thụt với đầu dòng 1

- Thụt với đầu dòng 1

- Gạch đầu dòng thứ hai

- Thụt với đầu dòng 2

- Thụt với đầu dòng 2

- Gạch đầu dòng thứ nhất

- Thụt với đầu dòng 1

- Thụt với đầu dòng 1

- Gạch đầu dòng thứ hai

- Thụt với đầu dòng 2

- Thụt với đầu dòng 2
### 6. Tạo bảng

| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |

| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |

## 3.Cài đặt Sublime Text và tìm kiếm, cài đặt các công cụ hỗ trợ markdown (export HTML, markdown preview, ...)


















