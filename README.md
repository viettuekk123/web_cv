# web_cv — IT Job Platform

Backend cho nền tảng tuyển dụng IT, xây dựng bằng NestJS, TypeScript, TypeORM và PostgreSQL. Dự án có các module tài khoản, công ty, việc làm, kỹ năng, CV và đơn ứng tuyển.

## Phạm vi hiện tại

- Mã backend nằm trong `backend/`.
- Docker Compose ở thư mục gốc khởi chạy PostgreSQL 15 và nạp `database.sql` khi tạo dữ liệu database lần đầu.
- Backend gọi một NER service bên ngoài qua `NER_SERVICE_URL` để trích xuất thông tin CV.
- Frontend và mã NER service được mô tả trong đặc tả, nhưng chưa có thư mục triển khai tương ứng trong repo này.

## Cấu trúc repo

| Đường dẫn | Nội dung |
| --- | --- |
| [backend/](backend/) | API NestJS và hướng dẫn chạy backend |
| [backend/src/modules/](backend/src/modules/) | Auth, users, companies, jobs, skills, CV, applications và admin |
| [database.sql](database.sql) | Schema và dữ liệu khởi tạo database |
| [docker-compose.yml](docker-compose.yml) | PostgreSQL cho môi trường phát triển local |
| [API_DOCUMENTATION.md](API_DOCUMENTATION.md) | Tài liệu endpoint dành cho bên tích hợp API |
| [PROJECT_SPECIFICATION.md](PROJECT_SPECIFICATION.md) | Đặc tả chức năng và kiến trúc dự kiến |

## Bắt đầu

Xem [hướng dẫn backend](backend/README.md) để cài dependencies, cấu hình môi trường và chạy API.

Khi backend chạy với cổng mặc định:

- API: `http://localhost:4000/api`
- Swagger: `http://localhost:4000/api/docs`
- File CV: `http://localhost:4000/uploads/cvs/{filename}`

Nếu thay đổi `PORT`, dùng cổng tương ứng cho các URL trên.

## Đọc tài liệu

Đọc [đặc tả dự án](PROJECT_SPECIFICATION.md) để hiểu mục tiêu tổng thể và [tài liệu API](API_DOCUMENTATION.md) để tích hợp. Đối chiếu với code hiện tại khi triển khai các tính năng được mô tả trong đặc tả.
