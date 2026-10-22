# Tiếng Anh 5 - Tân Hưng Primary School

Ứng dụng ôn tập Tiếng Anh 5: từ vựng, mẫu câu, nghe và nhắc lại, tình huống giao tiếp, trò chơi, bài tập, chấm phát âm. Toàn bộ ứng dụng nằm trong `index.html`; bài học nằm trong `lessons.json`.

## Các tệp

| Tệp | Dùng để |
| --- | --- |
| `index.html` | Ứng dụng (không cần sửa) |
| `lessons.json` | Bài học, tên trường, link Google Sheets, giọng đọc tạo sẵn, khóa AI dùng chung. Mỗi lần soạn bài xong, giáo viên xuất tệp mới và tải lên thay tệp này |
| `.nojekyll` | Giúp GitHub Pages phục vụ tệp nguyên vẹn |

## Đưa lên mạng lần đầu

1. Tạo kho mới trên GitHub.
2. Bấm **uploading an existing file**, kéo các tệp trên vào, bấm **Commit changes**.
3. Chọn một cách:
   - **GitHub Pages:** Settings > Pages > Deploy from a branch > main > /(root) > Save.
   - **Vercel:** Add New > Project > chọn kho này > Deploy.

## Giáo viên

Bấm nút xanh ở góc phải, nhập mã PIN giáo viên. Mã PIN chỉ để học sinh không vào nhầm trang giáo viên; người thay đổi được bài học là người tải được `lessons.json` lên kho này.

Lần đầu trên máy giáo viên, vào **Cài đặt**:

1. **Google Sheets:** cài mã `Code.gs` (dán vào Apps Script, chọn hàm setup, bấm Chạy để tạo 3 trang KẾT QUẢ, TỔNG HỢP, THEO UNIT; rồi Triển khai ứng dụng web, Bất kỳ ai). Dán link `/exec` vào đây, Kiểm tra kết nối, Lưu đường dẫn.
2. **Giọng đọc:** bấm Tạo giọng đọc còn thiếu (giọng đọc tạo sẵn chạy trên mọi máy, kể cả Android không có giọng tiếng Anh).
3. **Xuất bài học**, tải `lessons.json` lên GitHub thay tệp cũ.

Soạn bài mới: Tải Unit mới (tên Unit + ảnh trang sách) > AI quét > kiểm tra trong Quản lý Unit > Tạo giọng đọc còn thiếu > Xuất bài học > tải `lessons.json` lên GitHub. Học sinh nhận bài mới sau vài phút.

## Khóa AI dùng chung

`lessons.json` đang có khóa Gemini dùng chung, để máy học sinh được AI chấm phát âm đủ 4 tiêu chí và tự tạo giọng cho câu chưa có sẵn. Khóa này **công khai**: ai mở trang cũng đọc được, có thể dùng hết lượt của khóa, và Google có thể tự khóa nó khi phát hiện trên GitHub.

- Nên giới hạn khóa chỉ cho tên miền của trang (Google Cloud Console > APIs & Services > Credentials > chọn khóa > Application restrictions: Websites, thêm địa chỉ trang).
- Đổi hoặc gỡ khóa: Cài đặt > Khóa dùng chung cho mọi máy học sinh > Lưu hoặc Gỡ, rồi Xuất bài học và tải lên lại.
- Khi khóa bị khóa hoặc gỡ, ứng dụng vẫn chạy: giọng đọc tạo sẵn vẫn phát, chấm phát âm chuyển sang chấm theo từ nhận dạng được.

## Mở bằng Chrome

Ứng dụng đưa mọi học sinh sang Chrome:
- Android (Zalo, Facebook, Samsung Internet, Cốc Cốc...): tự mở Chrome; máy chưa có Chrome thì mở trang cài Chrome trên CH Play.
- iPhone (Safari, Zalo, Facebook...): tự mở Chrome; máy chưa có Chrome thì hiện nút cài từ App Store.
- Máy tính (Edge, Firefox, Cốc Cốc, Safari...): trang web không tự mở được trình duyệt khác, nên hiện hướng dẫn mở bằng Chrome (sao chép đường dẫn, tải Chrome).
- Trong hướng dẫn có cách đặt Chrome làm trình duyệt mặc định cho từng loại máy.
- Muốn tắt việc này cho một link, thêm `?stay=1` vào cuối đường dẫn.
