# Construction Toolkit

Bộ công cụ xây dựng — chạy hoàn toàn trên trình duyệt (static site, không cần backend).

🔗 **Live demo:** `https://<your-username>.github.io/<repo-name>/`

## Modules

| Tool | File | Mô tả |
|------|------|-------|
| 📊 **Định Mức RSMeans v6.0** | `dinh-muc-rsmeans.html` | Tra cứu định mức năng suất xây dựng theo chuẩn RSMeans |
| 📈 **Biểu Đồ Huy Động** | `bieu-do-huy-dong.html` | Tạo biểu đồ huy động nhân lực & máy móc, xuất PDF |
| ⚙️ **Metal Calculator** | `metal-calculator.html` | Tính khối lượng thép hình (H, I, U, L, hộp, ống...) |
| ✅ **Checklist Tầng Hầm** | `checklist-tang-ham.html` | Checklist QA/QC thi công tầng hầm, in được trên A4 |
| 🧹 **Excel Cleaner** | `excel-cleaner.html` | Làm sạch file Excel: bỏ formatting thừa, ô trống... |

## Deploy lên GitHub Pages

### Cách 1 — Qua giao diện web (đơn giản nhất)

1. Tạo repository mới trên GitHub (ví dụ: `construction-toolkit`)
2. Upload toàn bộ file trong thư mục này lên repo (kéo-thả vào trình web)
3. Vào **Settings → Pages**
4. Mục **Source**, chọn branch `main` (hoặc `master`), folder `/ (root)`
5. Bấm **Save**. Sau ~1 phút, site sẽ live tại `https://<username>.github.io/<repo-name>/`

### Cách 2 — Qua git command line

```bash
# Khởi tạo repo
git init
git add .
git commit -m "Initial: construction toolkit"

# Kết nối với GitHub repo đã tạo
git branch -M main
git remote add origin https://github.com/<username>/<repo-name>.git
git push -u origin main
```

Sau đó vào **Settings → Pages** trên GitHub để bật Pages như cách 1.

## Cấu trúc

```
.
├── index.html                  # Landing page dashboard
├── dinh-muc-rsmeans.html       # RSMeans v6.0
├── bieu-do-huy-dong.html       # Biểu đồ huy động
├── metal-calculator.html       # Tính thép
├── checklist-tang-ham.html     # Checklist QA/QC
├── excel-cleaner.html          # Excel cleaner
├── .nojekyll                   # Tắt Jekyll processing
└── README.md
```

## Lưu ý

- Tất cả các app dùng CDN cho thư viện (Chart.js, jsPDF, JSZip, html2canvas, Google Fonts) → **cần internet** lần đầu load.
- File `.nojekyll` quan trọng — đảm bảo GitHub Pages không bỏ qua file/folder bắt đầu bằng `_`.
- Toàn bộ xử lý dữ liệu (Excel, PDF) chạy trên client → an toàn, không upload đi đâu.
