# Deploy Portfolio - 3 Cách Nhanh

## Cách 1: Netlify Drop (NHANH NHẤT - 30 giây, không cần account)

1. Mở https://app.netlify.com/drop trong browser
2. Kéo thả nguyên folder `portfolio` vào ô drop
3. Netlify trả về link dạng `https://random-name-12345.netlify.app`
4. Paste link đó vào ô Portfolio của PICKDI form

**Ưu**: nhanh nhất, link public ngay, không cần account
**Nhược**: link random, hết hạn sau ~24h nếu không login

---

## Cách 2: GitHub Pages (link đẹp + permanent)

### Bước 1: Tạo repo trên GitHub
1. Vào https://github.com/new
2. Repository name: `portfolio`
3. Visibility: **Public**
4. KHÔNG tick "Add a README file"
5. Click "Create repository"

### Bước 2: Push code (chạy trong PowerShell tại folder portfolio)
```powershell
cd C:\Users\Administrator\Downloads\job-system\job-system\portfolio
git init
git add index.html
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/hieunm132/portfolio.git
git push -u origin main
```

### Bước 3: Enable GitHub Pages
1. Vào repo: https://github.com/hieunm132/portfolio
2. Settings → Pages
3. Source: "Deploy from a branch"
4. Branch: `main` / `(root)` → Save
5. Đợi ~1 phút, link sẽ là: **https://hieunm132.github.io/portfolio/**

---

## Cách 3: Vercel (cũng nhanh, cần account)

1. https://vercel.com/new → import từ GitHub (cần làm Cách 2 trước)
2. Hoặc cài Vercel CLI: `npm i -g vercel` → `vercel` trong folder

---

# SAU KHI DEPLOY

1. Mở link portfolio xem có chạy không
2. **QUAN TRỌNG**: Edit `index.html` để sửa các phần có `placeholder` (màu vàng):
   - Tên course/topic thật mày từng làm
   - Channel/blog đã publish content
   - Bất cứ chi tiết thật nào về experience LMS
3. Re-deploy (Netlify auto-update khi mày drag lại, GitHub: `git push`)
4. Paste link vào ô Portfolio của PICKDI form thay cho "n.a"
