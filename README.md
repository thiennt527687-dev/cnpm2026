# AI Personalized Learning Platform

Hệ thống cá nhân hóa lộ trình học và luyện thi Đánh giá năng lực tích hợp AI.

## Mục tiêu

- Đánh giá năng lực đầu vào.
- Xác định điểm mạnh và điểm yếu.
- Tạo hồ sơ năng lực học sinh.
- Tạo và cập nhật lộ trình học cá nhân hóa.
- Luyện tập thích ứng và thi thử.
- Hỗ trợ bằng AI Tutor và RAG.
- Theo dõi tiến độ và dự đoán khả năng đạt điểm mục tiêu.

## Cấu trúc repository

```text
.
├── backend/
├── web-portal/
├── student-app/
├── ai-service/
├── database/
├── tests/
├── docs/
│   ├── requirements/
│   ├── diagrams/
│   ├── architecture/
│   └── meeting-minutes/
├── .github/
├── CONTRIBUTING.md
└── README.md
```

## Quy trình branch

```text
main
└── develop
    ├── feature/KAN-xx-ten-chuc-nang
    ├── docs/KAN-xx-ten-tai-lieu
    ├── bugfix/KAN-xx-ten-loi
    ├── test/KAN-xx-ten-kiem-thu
    └── chore/KAN-xx-ten-cau-hinh
```

Mọi thay đổi phải được thực hiện trên branch riêng và đưa vào `develop` qua Pull Request.
