# ⚡ QuizArena Live - Đấu Trường Trắc Nghiệm Thời Gian Thực (Multiplayer)

> **Web trắc nghiệm đấu trường trực tuyến thời gian thực (Real-time Synchronized)**, hỗ trợ từ 2 đến 60+ người cùng chơi đồng bộ trên điện thoại và máy tính. Chạy trực tiếp 100% trên **GitHub Pages** mà không cần thuê server hay cài đặt backend phức tạp!

---

## 🌟 Tính Năng Nổi Bật

- ⏱️ **Đồng bộ thời gian thực chuẩn từng mili-giây**: Tất cả điện thoại và màn hình máy chiếu đều nhảy đồng hồ đếm ngược cùng một giây, cùng hiện câu hỏi và cùng khóa đáp án.
- 👑 **Màn hình Quản Trò / Máy Chiếu (Host View)**:
  - Hiển thị mã PIN phòng siêu to kèm **Mã QR trực tiếp** trên màn hình để thí sinh quét camera điện thoại vào phòng trong 2 giây.
  - Theo dõi danh sách thí sinh vào phòng theo thời gian thực (hiệu ứng bóng bóng avatar nảy).
  - Thanh tiến độ trả lời trực tiếp: *"18 / 20 thí sinh đã gửi đáp án"*.
  - Biểu đồ cột phân bố tỷ lệ chọn các đáp án A, B, C, D ngay sau khi hết giờ.
  - Bảng xếp hạng vòng thi động với hiệu ứng thăng hạng và chuỗi combo lửa (🔥 Combo x3).
  - Lễ vinh danh Quán quân (Bục Podium Top 3 vàng, bạc, đồng) kèm pháo hoa giấy (Canvas Confetti).
- 📱 **Màn hình Thí Sinh / Điện Thoại (Player View)**:
  - Tự động nhận diện mã phòng qua link chia sẻ (`?room=MÃ_PHÒNG`) hoặc quét QR.
  - Tùy chọn 12 Avatar ngộ nghĩnh (🦊, 🐼, 🐯, 🦄, 🚀, 🤖...).
  - Giao diện 4 nút màu sắc lớn trực quan (Đỏ ▲, Lam ◆, Vàng ●, Lục ■) bấm cực nhạy trên mọi dòng iPhone, Android, iPad hay laptop.
  - Khóa đáp án tức thì chống bấm 2 lần và phản hồi kết quả cá nhân (Điểm cộng tốc độ + Điểm thưởng combo).
- 🔒 **Chống gian lận tuyệt đối (Anti-cheat)**: Đáp án chính xác được giữ an toàn tại Host và chỉ phát tán sau khi hết giờ thi. Thí sinh không thể soi mã nguồn (F12) để tìm đáp án trước.
- 🎵 **Hệ thống âm thanh tự động (Web Audio Synthesizer)**: Tự tạo nhạc nền Synthwave/Kahoot sôi động, tiếng tích tắc gấp rút 5 giây cuối, chuông đúng/sai và nhạc vinh danh mà **không cần tải bất kỳ file MP3 nào**.
- 🤖 **Mô phỏng Thí Sinh Ảo (Bot Simulator)**: Nút bấm thêm nhanh 5, 20 hoặc 60 bot ảo với thuật toán trả lời ngẫu nhiên để bạn có thể kiểm thử không khí thi đấu đông đúc bất kỳ lúc nào.
- 📚 **Kho câu hỏi tích hợp sẵn & Quản trị**:
  - Gói Mặc Định: *GenAI & Công Cụ AI Sư Phạm* (20 câu hỏi chuẩn mực từ file `questions.json` về LLM, Prompting CRAC/Zero/Few-shot, ChatGPT, Gemini, Copilot, DeepSeek, Claude, Suno, ElevenLabs, Veo...)
  - Gói 1: *Kiến Thức Chung & Khoa Học* (10 câu)
  - Gói 2: *Công Nghệ Thông Tin & AI* (10 câu)
  - Gói 3: *Việt Nam Lịch Sử & Danh Lam* (10 câu)
  - Gói 4: *Đố Vui Trí Tuệ Vui Nhộn* (10 câu)
  - Trình tạo câu hỏi riêng, hỗ trợ nút **Nhập file JSON** / **Xuất file JSON** trực tiếp và tải kết quả thi đấu sang định dạng CSV (Excel).

---

## 🚀 Hướng Dẫn Đưa Lên GitHub Pages (3 Phút)

Website này được lập trình dưới dạng ứng dụng tĩnh (Single Page Application) sử dụng công nghệ kết nối **MQTT over Secure WebSocket (WSS)** công cộng và **BroadcastChannel**, nên **hoàn toàn tương thích và miễn phí 100% trên GitHub Pages**.

### Cách 1: Tải trực tiếp trên giao diện Web của GitHub (Dễ nhất - Không cần cài gì)

1. Đăng nhập vào [GitHub.com](https://github.com) và bấm nút **New** (hoặc truy cập [github.com/new](https://github.com/new)).
2. Đặt tên cho Repository (ví dụ: `quizarena` hoặc `gamevui`), chọn chế độ **Public**, sau đó nhấn **Create repository**.
3. Tại trang vừa tạo, nhấn vào dòng chữ **"uploading an existing file"**.
4. Kéo thả file `index.html` và `README.md` từ thư mục máy tính của bạn vào khung tải lên, sau đó nhấn nút xanh **Commit changes**.
5. Kích hoạt GitHub Pages:
   - Nhấn vào tab **Settings** (ở thanh menu trên cùng của repository).
   - Chọn mục **Pages** ở cột danh mục bên trái.
   - Tại phần **Build and deployment** &rarr; **Branch**: chọn nhánh `main` (hoặc `master`), thư mục giữ nguyên `/ (root)`.
   - Nhấn **Save**.
6. Đợi khoảng 1-2 phút, GitHub sẽ hiển thị đường link trang web của bạn:
   ```text
   https://<tên-tài-khoản-github>.github.io/<tên-repository>/
   ```
   *Ví dụ: `https://nguyenvana.github.io/quizarena/`*

---

### Cách 2: Sử dụng Git qua Terminal / Dòng lệnh

Nếu máy tính của bạn đã cài sẵn `git`:

```bash
# 1. Di chuyển vào thư mục dự án
cd d:\gamevui

# 2. Khởi tạo git và thêm file
git init
git add index.html README.md
git commit -m "Khoi tao QuizArena Live Multiplayer"

# 3. Đổi tên nhánh chính thành main
git branch -M main

# 4. Liên kết với kho lưu trữ GitHub của bạn
git remote add origin https://github.com/<tên-tài-khoản>/<tên-repo>.git

# 5. Đẩy code lên GitHub
git push -u origin main
```
Sau đó vào **Settings &rarr; Pages &rarr; chọn branch main** như bước 5 ở trên.

---

## 🎮 Hướng Dẫn Cách Chơi Cùng Nhau

### Với Chủ Phòng / MC / Giáo Viên (Host):
1. Truy cập đường link website trên máy tính hoặc laptop (kết nối máy chiếu hoặc TV nếu có).
2. Nhấn vào thẻ **👑 TẠO PHÒNG MỚI (MC)**.
3. Chọn gói câu hỏi muốn thi và thời gian cho mỗi câu (mặc định 15s).
4. Chiếu màn hình có **Mã PIN** và **Mã QR** lên cho mọi người.
5. Khi thấy các thí sinh đã vào phòng đầy đủ, bấm **BẮT ĐẦU TRẬN ĐẤU (ĐỒNG BỘ)**.

### Với Thí Sinh / Người Chơi (Players):
1. Dùng điện thoại quét mã QR trên màn hình của Host, hoặc truy cập theo đường link được chia sẻ.
2. Chọn Avatar, nhập Tên của bạn và nhấn **Tham Gia Ngay**.
3. Khi MC bấm bắt đầu, màn hình điện thoại sẽ tự động đếm ngược `3.. 2.. 1..` và hiện ra 4 nút bấm tương ứng:
   - 🔴 **Tam giác đỏ (A)**
   - 🔵 **Hình thoi xanh (B)**
   - 🟡 **Hình tròn vàng (C)**
   - 🟢 **Hình vuông lục (D)**
4. Bấm thật nhanh đáp án bạn cho là đúng để nhận tối đa điểm thưởng tốc độ!

### Mẹo Thử Nghiệm Ngay Lập Tức:

#### Cách 1: Thử nghiệm giữa 2 Tab trên cùng máy tính
- Tab 1: Nhấn *Tạo Phòng Mới* (làm Quản Trò MC).
- Tab 2: Mở một cửa sổ ẩn danh (Incognito) hoặc tab mới, nhấn *Vào Phòng Thi Đấu* và nhập mã phòng PIN của Tab 1.
- Bạn sẽ thấy hai tab kết nối và đồng bộ ngay lập tức!

#### Cách 2: Thử nghiệm giữa Điện Thoại và Máy Tính qua mạng Wi-Fi (Không cần chờ GitHub)
1. Trên máy tính, mở terminal tại thư mục dự án và chạy:
   ```bash
   python -m http.server 8080 --bind 0.0.0.0
   ```
2. Trên máy tính mở: `http://localhost:8080` rồi bấm **Tạo Phòng Mới**.
3. Tại ô *"Đang mở file cục bộ"* dưới mã QR trên máy tính, nhập IP mạng Wi-Fi của bạn: `http://192.168.1.5:8080` và bấm **Đổi QR**.
4. Dùng điện thoại (kết nối cùng Wi-Fi) quét mã QR hoặc mở trình duyệt điện thoại gõ `http://192.168.1.5:8080` &rarr; Nhập mã PIN và bấm **Tham Gia Ngay**!

#### Cách 3: Đưa lên GitHub Pages (Chơi Toàn Cầu Bằng 4G/5G/Wi-Fi)
- Xem hướng dẫn chi tiết ở mục **Hướng Dẫn Đưa Lên GitHub Pages** bên trên. Chỉ cần kéo thả file `index.html` lên GitHub là ai cũng có thể chơi từ bất kỳ đâu!

---

## ⚙️ Cấu Trúc Dự Án

```text
├── index.html       # Ứng dụng toàn diện (Giao diện, Sound Engine, MQTT Sync, Game Logic)
└── README.md        # Tài liệu hướng dẫn sử dụng và triển khai
```

- Không cần chạy `npm install` hay cài bất kỳ thư viện node_modules nào.
- Tất cả thư viện (Tailwind CSS, Phosphor Icons, Canvas Confetti, MQTT.js, QRCode.js) đều được tải tự động qua CDN tốc độ cao.

---

Chúc bạn có những trận đấu trắc nghiệm bùng nổ và hào hứng cùng bạn bè, đồng nghiệp và học sinh! 🏆

