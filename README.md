# site/ — website "Phượng Hoàng Capital" (hư cấu) phục vụ OSINT

Deploy lên host thật (domain BTC mua — ví dụ `phuonghoang.vn` hoặc `phcap-vn.xyz`), robots.txt để **Allow** (không chặn archive!).

## Các trang và bài dùng

| Trang | Bài | Vai trò |
|---|---|---|
| `/index.html` | — | Trang chủ, trông thật |
| `/doi-ngu.html` | **O4** | Mã NV Hân `PH-EMP-0223`. **SPN ngay khi deploy**, sau đó **XÓA KHỎI SITE SỐNG** trước sự kiện (chỉ còn trên Wayback) |
| `/tuyendung/tho-phan-mem-2026.html` | **O15** | Email `tuyen.dung@phcap-vn.xyz` + tên công ty mẹ **Golden Phoenix Group Ltd.** SPN xong cũng xóa khỏi site sống |
| `/app/hoan-tien/privacy.html` | **O15** | Privacy policy app PhoenixBack trỏ về email ở trên |
| `/blog/an-da-lat-2024.html` + `anh-da-lat.jpg` | **O14** | Nguồn avatar "ăn cắp" (BTC thay ảnh có giấy phép/người thật cho chụp). Phải được Google/Yandex index |
| `/raovat/ban-do-go-cu.html` | **O12** | Rao vặt cùng SĐT 0901 555 239 → tên thật **Tòng Văn Mười**. Phải index |
| `/du-an/phoenix-heights.html` (+ brochure PDF) | **X1** | Mặt bằng 24 căn/tầng → đối chiếu ảnh trong nhà tìm đúng mã căn |
| `/danh-muc-san-pham.txt` | **M7** | Bản công khai byte-identical với file trong ZIP tang vật (bkcrack) |

## Checklist sau deploy (T−8 → T−6 tuần)

1. `Save Page Now` (web.archive.org) cho: `/`, `/doi-ngu.html`, `/tuyendung/...`, `/du-an/...` — **3 đợt cách nhau vài ngày**.
2. Submit `/blog/...` và `/raovat/...` lên Google (Search Console) + để Yandex crawl — verify bằng tài khoản sạch T−2 tuần: reverse image phải ra blog, search SĐT phải ra rao vặt.
3. Trước sự kiện: xóa `doi-ngu.html` và `tuyendung/...` khỏi site sống (đã có bản Wayback). KHÔNG xóa blog/raovat.
4. `anh-da-lat.jpg` — ảnh placeholder hiện tại; BTC thay bằng ảnh thật có giấy phép trước khi SPN/index.
5. Brochure PDF: sinh từ `challenges/tools/gen.py` bản X1 (khi có ảnh thật) hoặc BTC tự thiết kế — phải khớp mã căn đúng đáp án X1.

Số điện thoại 0901 555 237/239 là số hư cấu dạng "555" — không trùng số thật.
