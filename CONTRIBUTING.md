# CONTRIBUTING

## 1. Nguyên tắc

- Không push trực tiếp lên `main`.
- Không push trực tiếp lên `develop`.
- Mỗi Jira Task sử dụng một branch riêng.
- Branch, commit và Pull Request phải chứa mã Jira.
- Pull Request phải được ít nhất một thành viên khác review.
- Chỉ merge khi không còn conflict và đã kiểm thử.

## 2. Branch chính

### `main`

Chứa phiên bản ổn định dùng cho demo, release hoặc nghiệm thu.

### `develop`

Chứa phiên bản đang tích hợp trong Sprint.

## 3. Tên branch

| Loại | Cú pháp | Ví dụ |
|---|---|---|
| Chức năng | `feature/KAN-<id>-<mo-ta>` | `feature/KAN-22-user-login` |
| Tài liệu | `docs/KAN-<id>-<mo-ta>` | `docs/KAN-8-srs` |
| Sửa lỗi | `bugfix/KAN-<id>-<mo-ta>` | `bugfix/KAN-31-login-error` |
| Kiểm thử | `test/KAN-<id>-<mo-ta>` | `test/KAN-40-backend-api` |
| Cấu hình | `chore/KAN-<id>-<mo-ta>` | `chore/KAN-10-git-workflow` |

Quy tắc:

- Viết chữ thường.
- Dùng dấu gạch ngang.
- Không dùng dấu tiếng Việt hoặc khoảng trắng.
- Bắt buộc có mã Jira.

## 4. Thực hiện Task

```bash
git checkout develop
git pull origin develop
git checkout -b feature/KAN-22-user-login
```

Sau khi hoàn thành:

```bash
git add .
git commit -m "KAN-22 Implement user login"
git push -u origin feature/KAN-22-user-login
```

Tạo Pull Request:

```text
feature/KAN-22-user-login → develop
```

## 5. Commit

Cú pháp:

```text
KAN-<id> <Động từ> <Nội dung thay đổi>
```

Ví dụ:

```text
KAN-4 Add PostgreSQL schema
KAN-8 Add SRS documentation
KAN-9 Add use case diagrams
KAN-10 Configure GitHub workflow
```

Không dùng commit mơ hồ như `update`, `fix`, `done`, `sua loi`.

## 6. Pull Request

- Base branch: `develop`.
- Tên PR phải có mã Jira.
- Phải điền đầy đủ template.
- Phải có ít nhất một approval.
- Không merge khi còn conflict hoặc Request changes.

## 7. Review

Reviewer kiểm tra:

- Công việc có đúng yêu cầu Jira không.
- Code hoặc tài liệu có dễ đọc không.
- Có kiểm thử hoặc minh chứng không.
- Có ảnh hưởng module khác không.
- Có chứa mật khẩu hoặc API key không.
- Tài liệu liên quan đã cập nhật chưa.

## 8. Merge

- Branch công việc chỉ merge vào `develop`.
- Nên dùng **Squash and merge**.
- Xóa branch sau khi merge.
- Cuối Sprint tạo Pull Request `develop → main`.
- Chỉ nhóm trưởng merge vào `main`.

## 9. Definition of Done

Task chỉ chuyển sang Done khi:

- Hoàn thành đúng phạm vi Jira.
- Có commit chứa mã Jira.
- Có Pull Request.
- Đã được review.
- Không còn conflict.
- Đã kiểm thử.
- Đã cập nhật tài liệu.
- Đã merge vào `develop`.
- Đã gắn link PR hoặc tài liệu vào Jira.
