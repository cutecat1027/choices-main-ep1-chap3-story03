# Sylus Interactive Story Reader

Trang đọc truyện tương tác dạng cuộn dọc, responsive, chạy trực tiếp trên GitHub Pages.

## Cấu trúc

- `index.html`: khung HTML
- `style.css`: màu sắc, kiểu chữ, responsive
- `script.js`: dữ liệu truyện và chức năng tương tác
- `assets/`: nơi đặt ảnh truyện

## Chạy thử

Mở `index.html` bằng trình duyệt hoặc chạy bằng Live Server trong VS Code.

## Đăng lên GitHub Pages

1. Giải nén file ZIP.
2. Upload **các file và thư mục bên trong**, không upload nguyên ZIP, lên thư mục gốc repository.
3. Vào Settings > Pages > Deploy from a branch > main > /(root) > Save.
4. Chờ GitHub Pages xuất bản.

## Sửa truyện

Mở `script.js`, thay nội dung trong mảng `STORY`. Có thể dùng các loại `narration`, `dialogue`, `image`, `sound`, `choices`, `divider`.

Để thêm ảnh: chép ảnh vào `assets/`, sau đó thêm vào STORY:

```js
{type:'image',src:'assets/scene.jpg',alt:'Bối cảnh'}
```

Các nút lựa chọn hiển thị phần `result` tương ứng bên dưới.

## Wix

Trang gửi `{type:'STORY_HEIGHT',height:...}` qua `postMessage`. Wix cần mã xử lý ở phía trang nhúng để tự thay đổi chiều cao; Rich Content iframe không tự hỗ trợ tính năng này.

Nội dung hiện tại chỉ là minh họa. Chưa kết nối Wix CMS.
