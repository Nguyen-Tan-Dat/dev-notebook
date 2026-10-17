---
title: "Choose PostgreSQL over MySQL"
created: 2026-10-17
updated: 2026-10-17
tags: [decision, adr, database, postgresql]
status: accepted
---
# ADR: Choose PostgreSQL over MySQL
## Context
Dự án A cần database quan hệ cho ứng dụng có nhiều truy vấn phức tạp, JSON, và full-text search.
## Options Considered
1. MySQL 8
2. PostgreSQL 16
3. MariaDB
## Decision
Chọn PostgreSQL 16.
## Rationale
- Hỗ trợ JSONB tốt hơn MySQL.
- Full-text search mạnh hơn.
- Extension phong phú (pg_trgm, PostGIS, ...).
- Cộng đồng lớn, tài liệu tốt.
## Consequences
### Positive
- Truy vấn phức tạp dễ viết hơn.
- Có thể mở rộng sang GIS nếu cần.
### Negative
- Team chưa quen, cần thời gian học.
- Một số tool MySQL-specific không dùng được.
## References
- [[project-a-overview]]
- https://www.postgresql.org/docs/