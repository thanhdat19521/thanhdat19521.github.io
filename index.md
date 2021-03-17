# Giới thiệu thiệu thư viện verydator form

##### Tác giả: [Nguyễn Thành Đạt](https://github.com/thanhdat19521)
### Giới thiệu
<!-- You can use the [editor on GitHub](https://github.com/thanhdat19521/thanhdat19521.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.\ -->
Khi làm frontend chúng ta chắc hẳn hay gặp những trường hơp cần verydate form.\
Ví du: \
    - very form đăng nhập.\
    - very form đăng ký.\
    - very các trườn nhập dữ liệu.\
    ...

Nếu mỗi khi gặp những trường hợp trên ta lại đi viết code verydator có phải mất khá nhiều thời gian không?\
Ta đặt ra câu hỏi: Tại sao ta không tạo ra một thư viện nhỏ dùng để verydator form, có tính tái sử dụng cao\
Việc này giúp chúng ta không cần phải nghĩ xem form này chúng ta nên very sao, sẽ giúp chúng ta tiết kiệm khá nhiều thời gian...

### Chi tiết

```markdown
**Lưu ý:** Đây là chia sẻ cá nhân

1. Tải thư viện về:
    - Link tải: https://github.com/thanhdat19521/liberty_velidator
    - form giao diện không cần bó buộc theo mẫu, phần html && css trong thư viện chỉ để demo

2. Quy chuẩn code
    - form phải theo quy chuẩn nhất định: 
        <form id>
            ...
            <div class>
                <label></label> (Không bắt buộc)
                <input name rules /> (thẻ input cân verydate)
                <span class></span> (báo lỗi nếu có)
            </div>
            ...
        </form>
    - Phần <form> đặt một id để định danh form
    - Phần <div> đặt một class để định danh xem đang very ở đâu
    - Phần <span> đăt một class để định dánh xem đang very ở đâu, là nơi hiển thị lỗi nếu có

3. Sử dụng

Gọi phương thức very
    - Ở mỗi thẻ input muốn very thì thêm atrb rules
    - thêm các phương thức cho rules

    **Lưu ý** hỗ trợ kiểm tra không bỏ trống, email, số điện thoại, nhập lại mật khẩu,
    kiểm tra ký tự nập vào min max.

    Phương thức hỗ trợ:
        required: yêu câu phải nhập
        email: kiểm tra định dạng email
        phone: kiểm tra định dạng số điên thoại
        retypePassword: kiểm tra password nhập lại
        min:[số ký tự] : kiểm tra giá trị nhập vào nhỏ hơn [số ký tư]
        max:[số ký tự] : kiểm tra giá trị nhập vào lớn hơn [số ký tư]

Sử dụng bình bình thường:
    - Gọi hàm Validator()
    - Truyên tham số: id form, class form input, class message error
    Validator(id form, class from input, class message error)

Sự dụng dạng single pages app:
    - Gọi hàm Validator()
    - truyền các tham số vào hàm: id form, class form input, class message error, object
    Validator('#form-2', '.form-group', '.form-message', {
                onSubmit: function (data) {
                    console.log(data)
                }
            });
    

4. Giải thích:

Sử dụng bình thường:
    - Truyên id form để nhận biết cần very form nào
    - Truyền class form input để biết đang thao tác very với input nào
    - Truyền class message error để biết nơi hiểu thị lỗi

Sử dụng dạng single pages app:
    - Truyên object để nhận lại data của form khi qua form không có lỗi
```

### Demo

#### 1: Phần form (html)

    <form id="form_demo">
        ...
        <div class="form-group">
            <label for="email">Email</label>
            <input type="text" name="email" rules="required|email">
            <span class="form-message"></span>
        </div>
        <div class="form-group">
            <label for="password">Mật khẩu</label>
            <input type="password" name="password" rules="required|min:6">
            <span class="form-message"></span>
        </div>
        <div class="form-group">
            <button class="form-submit">Đăng nhập</button>
        </div>
        ...
    </form>

#### 2: Gọi hàm (javascript)

    - Cách thường: sẽ loaded lại trang
        Validator('#form-demo', '.form-group', '.form-message');

    - Single pages app: không loaded lại trang
        Validator('#form-demo', '.form-group', '.form-message', {
                onSubmit: function (data) {
                    console.log(data)
                }
            });

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
