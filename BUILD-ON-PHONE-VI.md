# Build APK ngay trên điện thoại (không cần Android Studio)

Bạn có thể dùng GitHub Actions để biên dịch trên máy chủ GitHub. Cần có tài khoản GitHub và kết nối Internet.

1. Mở https://github.com trên Chrome Android và đăng nhập.
2. Tạo repository mới (New repository), đặt tên `GarenaAutoAndroid`; chọn Public hoặc Private, rồi Create repository.
3. Trong repository, chọn **Add file → Upload files**. Giải nén ZIP này trước bằng ứng dụng quản lý tệp, sau đó tải toàn bộ nội dung bên trong thư mục `GarenaAutoAndroid` lên repository (bao gồm thư mục ẩn `.github`). Nếu giao diện di động không tải được thư mục `.github`, dùng GitHub web ở chế độ Desktop site hoặc GitHub Codespaces.
4. Commit các file lên nhánh `main`.
5. Mở tab **Actions** của repository. Chọn workflow **Build Android APK**, bấm **Run workflow** nếu chưa tự chạy.
6. Chờ job hoàn tất màu xanh. Mở lần chạy đó, kéo xuống **Artifacts**, tải `GarenaAuto-Android-debug-apk`.
7. Giải nén artifact ZIP để lấy `app-debug.apk`, rồi mở file APK trên Android để cài. Có thể cần bật quyền cài ứng dụng từ nguồn này.

Nếu workflow không xuất hiện, kiểm tra đã tải lên đúng đường dẫn `.github/workflows/build-apk.yml` và repository đã commit file.

APK này là bản debug để cài thử, không phải bản phát hành đã ký. Ứng dụng chỉ hỗ trợ thao tác thủ công trên trang Garena; không vượt CAPTCHA hay xác minh.
