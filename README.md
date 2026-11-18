# Du Lịch Miền Bắc

Website giới thiệu điểm đến, đặc sản ẩm thực, tour tham khảo và đồ dùng du lịch tại ba địa phương: **Sơn La, Hòa Bình và Hạ Long (Quảng Ninh)**.

Dự án là một website tĩnh, được xây dựng bằng HTML, CSS và JavaScript thuần. Không yêu cầu framework, package manager, cơ sở dữ liệu hay máy chủ backend.

## Mục lục

- [Tính năng](#tính-năng)
- [Công nghệ và công cụ](#công-nghệ-và-công-cụ)
- [Cấu trúc dự án](#cấu-trúc-dự-án)
- [Yêu cầu hệ thống](#yêu-cầu-hệ-thống)
- [Cài đặt và chạy dự án](#cài-đặt-và-chạy-dự-án)
- [Sử dụng trong VS Code](#sử-dụng-trong-vs-code)
- [Trang và luồng điều hướng](#trang-và-luồng-điều-hướng)
- [Tùy chỉnh nội dung](#tùy-chỉnh-nội-dung)
- [Hình ảnh, video và tài nguyên ngoài](#hình-ảnh-video-và-tài-nguyên-ngoài)
- [Triển khai](#triển-khai)
- [Kiểm thử](#kiểm-thử)
- [Quản lý mã nguồn](#quản-lý-mã-nguồn)
- [Các giới hạn hiện tại](#gioi-han-hien-tai)
- [Liên hệ](#liên-hệ)

## Tính năng

- Menu điều hướng đồng nhất giữa các trang.
- Trang chủ giới thiệu ba khu du lịch và banner du lịch Miền Bắc.
- Phát và thay thế video YouTube, TikTok hoặc video trực tiếp bằng JavaScript.
- Lưu link video do người dùng nhập bằng `localStorage`.
- Trang vùng miền mô tả địa danh, điểm check-in và món ăn nổi bật.
- Trang ẩm thực chia nội dung theo Sơn La, Hòa Bình và Hạ Long.
- Chi tiết từng món ăn được điều hướng bằng tham số `?mon=<ten-mon>`.
- Trang chi tiết thịt trâu gác bếp độc lập.
- Danh sách tour có tìm kiếm, lọc khu vực, sắp xếp và xem chi tiết.
- Trang chi tiết tour hiển thị lịch trình, giá tham khảo, dịch vụ bao gồm và không bao gồm.
- Trang sản phẩm du lịch với danh mục và giá tham khảo.
- Giao diện responsive, hiệu ứng chuyển động, card và footer.
- Hỗ trợ giảm chuyển động với `prefers-reduced-motion`.

## Công nghệ và công cụ

### Công nghệ chính

| Công cụ | Vai trò |
|---|---|
| HTML5 | Cấu trúc trang và semantic markup |
| CSS3 | Bố cục, hiệu ứng, responsive và giao diện |
| JavaScript | Tìm kiếm tour, chi tiết món ăn, nhúng video và lưu dữ liệu local |
| YouTube iframe API/link nhúng | Hiển thị video giới thiệu |
| TikTok player | Hiển thị video TikTok |
| `localStorage` | Lưu link video do người dùng tự nhập |
| URLSearchParams | Đọc tham số `mon` và `tour` trên URL |

### Công cụ phát triển đề xuất

- **Visual Studio Code**
- **Live Server** extension để chạy và tự động reload website.
- **Git** để quản lý phiên bản.
- **GitHub** để lưu trữ và triển khai.
- **Chrome, Edge hoặc Firefox** để kiểm tra giao diện.
- **Developer Tools** để kiểm tra CSS, JavaScript, Console và responsive.
- Trình soạn thảo HTML/CSS/JavaScript có hỗ trợ syntax highlight.

### Công cụ triển khai tĩnh

Website có thể triển khai bằng GitHub Pages, Azure Static Web Apps, Netlify hoặc Vercel. Không cần Node.js, Docker hoặc cơ sở dữ liệu.

## Cấu trúc dự án

```text
Daphuongtien/
├── .vscode/
│   └── settings.json
├── index.html
├── vungmien.html
├── amthuc.html
├── amthuc-chi-tiet.html
├── amthuc-chi-tiet.js
├── thit-trau-gac-bep.html
├── dattour.html
├── sanpham.html
├── style.css
├── README.md
└── các file hình ảnh .jpg, .png, .jfif
```

### Vai trò các file chính

- `index.html`: Trang chủ, banner, khu du lịch và trình phát video.
- `vungmien.html`: Thông tin chi tiết Sơn La, Hòa Bình và Hạ Long.
- `amthuc.html`: Danh mục món ăn theo địa phương và video ẩm thực.
- `amthuc-chi-tiet.html`: Trang mẫu hiển thị chi tiết món ăn theo query string.
- `amthuc-chi-tiet.js`: Cơ sở dữ liệu JavaScript của món ăn, URL video và render nội dung.
- `thit-trau-gac-bep.html`: Trang chi tiết dành riêng cho đặc sản Sơn La.
- `dattour.html`: Danh sách, lọc, sắp xếp và chi tiết tour.
- `sanpham.html`: Danh mục đồ dùng du lịch.
- `style.css`: Toàn bộ kiểu dáng và responsive của dự án.
- `.vscode/settings.json`: Cấu hình cổng Live Server.

## Yêu cầu hệ thống

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại.
- VS Code khuyến nghị.
- Live Server extension khuyến nghị.
- Git khuyến nghị nếu cần quản lý phiên bản.
- Kết nối Internet để tải các hình ảnh hoặc video được trỏ tới từ nguồn bên ngoài.

## Cài đặt và chạy dự án

### Cách 1: Mở trực tiếp

1. Tải hoặc clone dự án.
2. Mở thư mục dự án.
3. Mở `index.html` bằng trình duyệt.

Lưu ý: Một số tính năng URL hoặc video có thể hoạt động ổn định hơn khi chạy qua HTTP thay vì mở file trực tiếp.

### Cách 2: Dùng Live Server trong VS Code

1. Mở thư mục dự án bằng VS Code.
2. Cài extension **Live Server**.
3. Mở `index.html`.
4. Nhấn chuột phải, chọn **Open with Live Server**.
5. Mở `http://127.0.0.1:5500` hoặc địa chỉ Live Server hiển thị.

Cấu hình hiện tại trong `.vscode/settings.json`:

```json
{
  "liveServer.settings.port": 5500,
  "liveServer.settings.host": "127.0.0.1",
  "liveServer.settings.useLocalIp": false
}
```

### Cách 3: Dùng terminal

Chạy một máy chủ HTTP đơn giản bằng Python:

```bash
cd duong-dan-den-thu-muc-Daphuongtien
python -m http.server 5500
```

Sau đó truy cập:

```text
http://localhost:5500
```

## Sử dụng trong VS Code

### Extension khuyến nghị

- Live Server.
- HTML CSS Support.
- JavaScript (ES6) code snippets.
- Prettier hoặc một extension formatter khác.
- GitLens nếu cần theo dõi lịch sử Git.

### Quy trình chỉnh sửa

1. Chỉnh nội dung trong các file `.html`.
2. Chỉnh giao diện chung trong `style.css`.
3. Chỉnh dữ liệu ẩm thực trong `amthuc-chi-tiet.js`.
4. Chỉnh danh sách tour trong phần `const tours` của `dattour.html`.
5. Mở Developer Tools để kiểm tra Console và lỗi tài nguyên.
6. Kiểm tra Desktop, tablet và mobile bằng chế độ responsive.

## Trang và luồng điều hướng

| Trang | File | Nội dung chính |
|---|---|---|
| Trang chủ | `index.html` | Banner, khu du lịch, video, giới thiệu |
| Vùng miền | `vungmien.html` | Sơn La, Hòa Bình, Hạ Long |
| Ẩm thực | `amthuc.html` | Danh mục món ăn và video |
| Chi tiết món ăn | `amthuc-chi-tiet.html?mon=<key>` | Nội dung render bằng JavaScript |
| Thịt trâu gác bếp | `thit-trau-gac-bep.html` | Trang chi tiết cố định |
| Đặt tour | `dattour.html` | Tìm kiếm, lọc, sắp xếp và chi tiết tour |
| Sản phẩm | `sanpham.html` | Sản phẩm du lịch |

Luồng tham khảo:

```text
index.html
├── vungmien.html
├── amthuc.html
│   ├── thit-trau-gac-bep.html
│   └── amthuc-chi-tiet.html?mon=<ma-mon>
├── dattour.html
│   └── dattour.html?tour=<ma-tour>
└── sanpham.html
```

## Tùy chỉnh nội dung

### Thay đổi menu

Menu được lặp lại trong từng file HTML. Cập nhật các thẻ trong cùng khối:

```html
<a href="index.html">Trang chủ</a>
<a href="vungmien.html">Vùng miền</a>
<a href="amthuc.html">Ẩm thực</a>
<a href="dattour.html">Đặt tour</a>
<a href="sanpham.html">Sản phẩm</a>
```

### Thêm món ăn

1. Thêm thẻ món mới vào `amthuc.html`.
2. Cung cấp đường dẫn dạng:

```text
amthuc-chi-tiet.html?mon=<ma-mon>
```

3. Thêm dữ liệu trong object `dishes` tại `amthuc-chi-tiet.js`.
4. Thêm URL video tại object `dishVideoUrls` nếu cần.

Ví dụ link món:

```html
<a href="amthuc-chi-tiet.html?mon=tao-meo">Táo mèo</a>
```

### Thêm tour

Trong `dattour.html`, thêm một object tour vào mảng `tours`:

```js
{
  id: "tour-moi",
  title: "Tên tour",
  region: "Sơn La",
  route: "Hà Nội - Sơn La",
  rating: "9.2",
  reviews: "100",
  duration: "3N2Đ",
  oldPrice: "3.500.000đ",
  price: "2.990.000đ",
  promo: "Ưu đãi",
  image: "ten-hinh-anh.jpg",
  departure: "Hà Nội",
  description: "Mô tả tour"
}
```

Sau đó thêm thông tin lịch trình tương ứng trong object `tourDetails`.

### Thêm sản phẩm

Thêm card mới trong `sanpham.html` theo mẫu:

```html
<div class="product">
    <img src="ten-hinh-anh.jpg" alt="Tên sản phẩm">
    <div class="product-content">
        <p>Tên sản phẩm</p>
        <div class="price">500.000₫</div>
        <a href="dattour.html" class="buy-btn">Đặt mua</a>
    </div>
</div>
```

## Hình ảnh, video và tài nguyên ngoài

### Hình ảnh trong dự án

- `100.jpg`: Logo/hình tiêu đề trên thanh điều hướng.
- `1.jpg`: Banner.
- `2.jpg`, `29.png`, `100.jpg`: Tài nguyên hình ảnh.
- `halong.jpg`, `phuquoc.jpg`, `vali.jpg`: Hình địa danh hoặc sản phẩm.
- `balodulich.png`, `aokhoac.jfif`, `binhnuocgiunhiet.jfif`, `giayleonui.png`: Hình đồ dùng du lịch.

Nhiều trang cũng sử dụng URL hình ảnh trực tiếp từ website bên ngoài. Khi deploy, cần kiểm tra các URL này vẫn còn truy cập được.

### Video

Các trình phát video hỗ trợ:

- YouTube:
  - `youtu.be/<video-id>`
  - `youtube.com/watch?v=<video-id>`
  - `youtube.com/embed/<video-id>`
  - `youtube.com/shorts/<video-id>`
- TikTok với đường dẫn video đầy đủ.
- Link MP4 hoặc WebM trực tiếp.

URL YouTube/TikTok chính có thể chỉnh tại phần `VIDEO_LINKS` trong `index.html` và `vungmien.html`. Trang ẩm thực có thể chỉnh trong `data-youtube-url`.

Link do người dùng nhập được lưu bằng key:

```text
destination-video:<ma-dia-diem>
```

Xóa dữ liệu bằng DevTools:

```js
localStorage.clear();
```

## Triển khai

Vì đây là website tĩnh, thư mục deploy cần chứa các file HTML, CSS, JavaScript và hình ảnh trong cùng cấu trúc.

### GitHub Pages

1. Tạo repository GitHub.
2. Push toàn bộ thư mục dự án.
3. Mở **Settings → Pages**.
4. Chọn nhánh `main` và thư mục `/root`.
5. Save và chờ GitHub cấp URL.

### Azure Static Web Apps

1. Đẩy dự án lên GitHub.
2. Tạo Azure Static Web Apps.
3. Kết nối repository.
4. Chọn build preset **Other**.
5. App location đặt `/`.
6. Để trống output location vì không có bước build.

### Netlify hoặc Vercel

1. Import repository.
2. Chọn thư mục gốc làm publish directory.
3. Để trống build command.
4. Deploy.

## Kiểm thử

Chạy ít nhất các bài kiểm tra sau:

### Kiểm tra trang

- [ ] `index.html` tải banner và menu đúng.
- [ ] Tất cả liên kết điều hướng mở đúng trang.
- [ ] Các link video YouTube/TikTok có thể nhúng.
- [ ] Link hình ảnh ngoài không bị lỗi.
- [ ] Trang chi tiết món ăn hiển thị khi có `?mon=`.
- [ ] Trang chi tiết tour hiển thị khi có `?tour=`.

### Kiểm tra chức năng

- [ ] Tìm kiếm tour theo tên, điểm đến hoặc lịch trình.
- [ ] Lọc tour theo khu vực.
- [ ] Sắp xếp tour theo giá.
- [ ] Thay đổi link video và reload trang để kiểm tra `localStorage`.
- [ ] Xóa `localStorage` khi cần reset video.

### Kiểm tra giao diện

- [ ] Desktop từ 1366 px trở lên.
- [ ] Tablet khoảng 768–800 px.
- [ ] Mobile khoảng 375–600 px.
- [ ] Menu không bị tràn.
- [ ] Card, bảng, footer và form không bị đè.
- [ ] Video có tỷ lệ 16:9 hoặc TikTok phù hợp.

### Kiểm tra trình duyệt

- Chrome
- Microsoft Edge
- Firefox
- Safari nếu có thiết bị Apple

Mở Developer Tools bằng phím `F12` hoặc `Ctrl+Shift+I`, kiểm tra tab Console để phát hiện lỗi JavaScript và tab Network để phát hiện tài nguyên không tải được.

## Quản lý mã nguồn

Lệnh Git cơ bản:

```bash
git status
git add .
git commit -m "Cap nhat website du lich"
git push origin main
```

Tạo nhánh chức năng:

```bash
git switch -c feature/them-noi-dung
```

Đưa nhánh trở lại `main`:

```bash
git switch main
git merge feature/them-noi-dung
```

Nên commit theo từng phần, ví dụ:

- `Them trang am thuc`
- `Bo sung tour Hạ Long`
- `Sua responsive mobile`
- `Cap nhat hinh anh va video`

<a id="gioi-han-hien-tai"></a>
## Các giới hạn hiện tại

- Không có backend, authentication hoặc database.
- Chưa có giỏ hàng hoặc thanh toán trực tuyến.
- Nút “Đặt mua” hiện chỉ điều hướng sang trang tour.
- Thông tin tour, lịch trình và giá là dữ liệu minh họa; cần xác minh trước khi sử dụng thương mại.
- Link hình ảnh và video phụ thuộc vào nguồn bên ngoài.
- Nội dung chi tiết món ăn chủ yếu được lưu trong JavaScript.
- Video TikTok và YouTube có thể bị giới hạn bởi chính sách nhúng hoặc mạng.
- Không có build pipeline, test framework hoặc CI/CD tự động trong trạng thái hiện tại.

## Liên hệ

- Hotline: `038 906 3632`
- Email: `duongmanhdung781@email.com`
- Địa chỉ: TP. Hà Nội
- Giờ làm việc: 8:00 – 22:00

---

*Dự án phục vụ mục đích học tập và giới thiệu văn hóa du lịch, ẩm thực Miền Bắc.*
