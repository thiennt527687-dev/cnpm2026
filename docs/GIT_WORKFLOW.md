# GITHUB WORKFLOW – KAN-10

## 1. Mục đích

Quy trình GitHub được xây dựng để thống nhất cách tạo branch, commit, Pull Request, review và merge trong dự án.

Mục tiêu:

- Tránh chỉnh sửa trực tiếp trên branch ổn định.
- Theo dõi rõ đóng góp của từng thành viên.
- Liên kết source code với Jira.
- Giảm xung đột khi tích hợp.
- Đảm bảo thay đổi được review trước khi merge.

## 2. Mô hình branch

```text
main
└── develop
    ├── feature/KAN-xx-ten-chuc-nang
    ├── docs/KAN-xx-ten-tai-lieu
    ├── bugfix/KAN-xx-ten-loi
    ├── test/KAN-xx-ten-kiem-thu
    └── chore/KAN-xx-ten-cau-hinh
```

### `main`

Chứa phiên bản ổn định dùng cho demo và nghiệm thu.

### `develop`

Chứa phiên bản tích hợp công việc của Sprint.

### Branch công việc

Mỗi Jira Task dùng một branch riêng được tạo từ `develop`.

## 3. Quy trình làm việc

```text
Jira Task
→ In Progress
→ Tạo branch từ develop
→ Thực hiện công việc
→ Commit có mã Jira
→ Push branch
→ Pull Request vào develop
→ Review
→ Merge
→ Gắn link PR vào Jira
→ Done
```

## 4. Quy tắc branch

| Loại | Mẫu |
|---|---|
| Chức năng | `feature/KAN-<id>-<mo-ta>` |
| Tài liệu | `docs/KAN-<id>-<mo-ta>` |
| Sửa lỗi | `bugfix/KAN-<id>-<mo-ta>` |
| Kiểm thử | `test/KAN-<id>-<mo-ta>` |
| Cấu hình | `chore/KAN-<id>-<mo-ta>` |

Ví dụ Sprint 1:

```text
feature/KAN-4-database-design
docs/KAN-5-web-wireframe
docs/KAN-6-learning-flow
docs/KAN-8-srs
docs/KAN-9-system-architecture
chore/KAN-10-git-workflow
```

## 5. Quy tắc commit

```text
KAN-<id> <Mô tả thay đổi>
```

Ví dụ:

```text
KAN-8 Add SRS documentation
KAN-9 Add use case and architecture diagrams
KAN-10 Configure GitHub workflow
```

## 6. Pull Request

- Branch nguồn: branch công việc.
- Branch đích: `develop`.
- Tên PR phải có mã Jira.
- Phải sử dụng Pull Request template.
- Phải có ít nhất một người khác review.
- Không merge khi còn conflict.

## 7. Bảo vệ branch

### `main`

- Bắt buộc merge bằng Pull Request.
- Yêu cầu ít nhất một approval.
- Không cho force push.
- Không cho xóa branch.
- Chỉ nhóm trưởng merge.

### `develop`

- Bắt buộc merge bằng Pull Request.
- Yêu cầu ít nhất một approval.
- Không cho force push.
- Không cho xóa branch.

## 8. Trách nhiệm

### Người thực hiện

- Cập nhật Jira.
- Tạo branch đúng quy tắc.
- Commit có mã Jira.
- Tạo Pull Request.
- Sửa các vấn đề reviewer yêu cầu.
- Gắn link PR vào Jira.

### Reviewer

- Kiểm tra yêu cầu, code, tài liệu và kiểm thử.
- Approve hoặc Request changes.

### Nhóm trưởng

- Quản lý `main` và `develop`.
- Phân công reviewer.
- Xử lý conflict.
- Merge phiên bản Sprint vào `main`.

## 9. Kết quả bàn giao KAN-10

- Repository có cấu trúc thư mục thống nhất.
- Có branch `main` và `develop`.
- Có `README.md`.
- Có `CONTRIBUTING.md`.
- Có Pull Request template.
- Có Issue template.
- Có quy tắc bảo vệ branch.
- Có tài liệu GitHub Workflow trên Confluence.
