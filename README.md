<p align="center">
  <img src="https://img.shields.io/badge/Robot-Kinematics-blue?style=for-the-badge&logo=probot&logoColor=white" />
  <img src="https://img.shields.io/badge/3D-Simulation-orange?style=for-the-badge&logo=three.js&logoColor=white" />
  <img src="https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />
</p>

<h1 align="center">🤖 D-H Robot Kinematics Simulator</h1>

<p align="center">
  <b>Bộ giải mã Động học Robot — Mô phỏng 3D thời gian thực</b><br/>
  Công cụ trực quan hóa động học thuận (Forward Kinematics) dựa trên bảng Denavit-Hartenberg
</p>

<p align="center">
  <a href="https://bangrbt.github.io/D-H-WEB/">🌐 <b>Dùng thử ngay →</b></a>
</p>

---

## ✨ Tính năng chính

| Tính năng | Mô tả |
|---|---|
| 📋 **Bảng D-H động** | Thêm/xóa/sửa thông số Denavit-Hartenberg trực tiếp |
| 🧊 **Mô phỏng 3D realtime** | Xem mô hình robot 3D, kéo xoay, zoom tự do |
| 🕹️ **Điều khiển khớp** | Thanh trượt điều khiển từng khớp quay & tịnh tiến |
| 📊 **Ma trận biến đổi** | Hiển thị ma trận symbolic (công thức) & numeric (số) |
| 📷 **AI Vision** | Upload ảnh bảng D-H → AI tự động nhận dạng thông số |
| ⚙️ **Tùy chỉnh trực quan** | Bật/tắt khung tọa độ, dựng đứng robot, khâu gập vuông |
| 📱 **Responsive** | Chạy tốt trên cả điện thoại, tablet và máy tính |

## 🚀 Demo trực tuyến

👉 **[https://bangrbt.github.io/D-H-WEB/](https://bangrbt.github.io/D-H-WEB/)**

Mở link trên bất kỳ trình duyệt nào — không cần cài đặt!

## 🎮 Hướng dẫn sử dụng

### 1. Nhập bảng D-H
- Sửa trực tiếp các ô trong bảng thông số
- Hoặc nhấn **"Tải ảnh bảng D-H"** để AI tự nhận dạng
- Góc nhập dạng: `pi/2`, `-pi/2`, `pi`
- Biến nhập dạng: `q1`, `q2`, `d3`

### 2. Điều khiển Robot
- Kéo **thanh trượt** để thay đổi góc khớp quay (°) hoặc hành trình tịnh tiến (mm)
- Điều chỉnh **hằng số kích thước** (chiều dài khâu, offset...)

### 3. Xem mô phỏng 3D
- 🖱️ **Kéo chuột** → Xoay camera
- 🔄 **Cuộn chuột** → Zoom vào/ra
- Quan sát tọa độ **đầu công tác (End Effector)** ở góc phải

### 4. Xem ma trận
- Chuyển đổi giữa **Công thức gốc** (symbolic) và **Ma trận số** (numeric)
- Xem ma trận từng khâu `A₁, A₂, ...` và ma trận tổng hợp `T`

## 🏗️ Công nghệ sử dụng

| Công nghệ | Vai trò |
|---|---|
| [React 18](https://react.dev/) | UI Framework |
| [Three.js](https://threejs.org/) | 3D Rendering Engine |
| [Tailwind CSS](https://tailwindcss.com/) | Styling |
| [Babel](https://babeljs.io/) | JSX Compiler (in-browser) |
| [Gemini API](https://ai.google.dev/) | AI Vision (nhận dạng ảnh) |

## 📐 Lý thuyết Denavit-Hartenberg

Quy ước D-H mô tả quan hệ giữa các khâu liên tiếp trong robot bằng 4 thông số:

| Thông số | Ký hiệu | Ý nghĩa |
|---|---|---|
| **Góc khớp** | θᵢ | Góc quay quanh trục Zᵢ₋₁ |
| **Offset khớp** | dᵢ | Khoảng cách dọc trục Zᵢ₋₁ |
| **Chiều dài khâu** | aᵢ | Khoảng cách dọc trục Xᵢ |
| **Góc xoắn khâu** | αᵢ | Góc quay quanh trục Xᵢ |

Ma trận biến đổi thuần nhất giữa 2 khâu liên tiếp:

```
        ┌ cos(θ)  -sin(θ)cos(α)   sin(θ)sin(α)   a·cos(θ) ┐
  Aᵢ =  │ sin(θ)   cos(θ)cos(α)  -cos(θ)sin(α)   a·sin(θ) │
        │   0        sin(α)          cos(α)           d      │
        └   0          0               0              1      ┘
```

## 📁 Cấu trúc dự án

```
D-H-WEB/
├── index.html      # 🌐 Ứng dụng chính (single-file)
├── web.html        # 📄 File web phụ
├── README.md       # 📖 Tài liệu
└── .gitignore      # 🚫 Git ignore rules
```

## 🤝 Đóng góp

Mọi đóng góp đều được chào đón! Hãy:

1. **Fork** repo này
2. Tạo branch mới: `git checkout -b feature/tinh-nang-moi`
3. Commit: `git commit -m "Thêm tính năng mới"`
4. Push: `git push origin feature/tinh-nang-moi`
5. Tạo **Pull Request**

## 📄 License

Dự án được phân phối dưới giấy phép [MIT](LICENSE). Tự do sử dụng cho mục đích học tập và nghiên cứu.

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/bangrbt">bangrbt</a>
</p>
