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
Việc này giúp chúng ta không cần phải nghĩ xem form này chúng ta nên very sao, sẽ giúp chúng ta tiết kiệm khá nhiều thời gian... \

### Chi tiết

```markdown
**Lưu ý:** Đây là chia sẻ cá nhân

#### 1. Tải thư viện về [tại đây](https://github.com/thanhdat19521/liberty_velidator)
- form giao diện không cần bó buộc theo mẫu, phần html && css trong thư viện chỉ để demo
#### 2. Quy chuẩn code
- form phải theo quy chuẩn nhất định: 
    <form id>
    ...
        <div (class)>
            <label></label> (Không bắt buộc)
            <input name rules /> (thẻ input cân verydate)
            <span (class)></span> (báo lỗi nếu có)
        </div>
    ...
    </form>
- Phần form đặt một id để định danh form
- Phần div đặt một class để định danh xem đang very ở đâu
- Phần span đăt một class để định dánh xem đang very ở đâu, là nơi hiển thị lỗi nếu có
**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/thanhdat19521/thanhdat19521.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
