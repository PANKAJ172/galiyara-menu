# Galiyara Food Court - Digital QR Menu

A modern, responsive digital menu system for Galiyara Food Court featuring 9 food outlets with Google Review integration.

## ✨ Features
- 📱 Fully responsive design (mobile, tablet, desktop)
- 🍔 9 individual food outlet menus
- 📄 PDF menu viewer
- 📶 WiFi information for all outlets
- ⭐ **Google Review integration for each shop**
- 🔄 **Smart scroll position memory** (returns to where you were)
- 🎨 Warm, food court themed design
- 🚀 Fast loading and easy to use

## 🚀 Live Demo
Once deployed, your website will be live at: `https://YOUR-USERNAME.github.io/galiyara-menu/`

## 📁 Project Structure
```
galiyara-menu/
├── index.html          # Main website file
├── menus/             # Folder for PDF menu files
│   ├── burgers-menu.pdf
│   ├── chai-snacks-menu.pdf
│   ├── juice-menu.pdf
│   ├── pizza-menu.pdf
│   ├── rolls-menu.pdf
│   ├── icecream-menu.pdf
│   ├── sandwich-menu.pdf
│   ├── chinese-menu.pdf
│   └── southindian-menu.pdf
└── README.md          # This file
```

## 🔧 Deployment Instructions (GitHub Pages)

### Step 1: Create a GitHub Account
1. Go to [github.com](https://github.com)
2. Click "Sign up" if you don't have an account
3. Follow the registration process

### Step 2: Create a New Repository
1. Click the "+" icon in the top right corner
2. Select "New repository"
3. Name it: `galiyara-menu` (or any name you prefer)
4. Make sure it's set to **Public**
5. Click "Create repository"

### Step 3: Upload Your Files

**Option A: Using GitHub Web Interface (Easiest)**
1. On your new repository page, click "uploading an existing file"
2. Drag and drop the `index.html` file
3. Click "Commit changes"
4. Create a folder called `menus`:
   - Click "Add file" → "Create new file"
   - Type `menus/placeholder.txt`
   - Add some text (like "PDF files go here")
   - Click "Commit changes"

**Option B: Using Git Command Line**
```bash
# Navigate to your project folder
cd /path/to/your/folder

# Initialize git
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit - Galiyara Menu"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR-USERNAME/galiyara-menu.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click "Settings" (top menu)
3. Click "Pages" (left sidebar)
4. Under "Source", select "main" branch
5. Click "Save"
6. Wait 2-3 minutes for deployment

### Step 5: Access Your Website
Your website will be live at:
```
https://YOUR-USERNAME.github.io/galiyara-menu/
```

## 📄 Adding PDF Menus

### Method 1: Upload via GitHub Web Interface
1. Go to your repository
2. Click on the `menus` folder
3. Click "Add file" → "Upload files"
4. Drag and drop your PDF files
5. Make sure they are named correctly:
   - `burgers-menu.pdf`
   - `chai-snacks-menu.pdf`
   - `juice-menu.pdf`
   - etc.
6. Click "Commit changes"

### Method 2: Using Git Command Line
```bash
# Add PDF files to menus folder
git add menus/*.pdf

# Commit
git commit -m "Add PDF menus"

# Push to GitHub
git push
```

## 🎨 Customization Guide

### Update Shop Names
Edit `index.html` and find the shop cards section. Update:
```html
<div class="shop-name">YOUR SHOP NAME</div>
<div class="shop-category">YOUR CATEGORY</div>
```

### Update WiFi Information
Find the WiFi modal section and update:
```html
<div class="wifi-value">YOUR-WIFI-NAME</div>
<div class="wifi-value">YOUR-PASSWORD</div>
```

### Change Colors
In the `<style>` section at the top, modify the color variables:
```css
:root {
    --primary-bg: #F5F1E8;      /* Background color */
    --accent-color: #D2691E;     /* Primary accent */
    --accent-light: #E89E6C;     /* Light accent */
}
```

### Update Operating Hours & Location
Find and edit these lines:
```html
<span>10 AM - 11 PM</span>
<span>Patarkar Colony, Jaipur</span>
```

## 📱 Generate QR Code

Once your website is live:

1. **Using QR Code Generator Websites:**
   - Go to [qr-code-generator.com](https://www.qr-code-generator.com)
   - Paste your GitHub Pages URL
   - Download the QR code image
   - Print and display it

2. **Using Google Chrome:**
   - Visit your website
   - Click the share icon or right-click
   - Select "Create QR Code"
   - Download and print

## ⭐ Setting Up Google Reviews

Each shop can have its own Google Review button! See **GOOGLE-REVIEW-GUIDE.md** for detailed instructions.

**Quick Setup:**
1. Create Google Business Profiles for each shop (or one for Galiyara)
2. Get review links from Google Business Profile
3. Update `index.html` - replace `YOUR_PLACE_ID_X` with actual Place IDs
4. Customers can now leave reviews with one tap!

**Two Options:**
- **Option A**: Separate profiles for each shop (recommended for better tracking)
- **Option B**: Single profile for entire food court (faster setup)

Detailed guide: See `GOOGLE-REVIEW-GUIDE.md`

## 📋 Testing Checklist

Before going live, test:
- ✅ All shop cards are clickable
- ✅ Back button works
- ✅ WiFi modal opens and closes
- ✅ PDF menus load correctly (after uploading PDFs)
- ✅ Responsive design on mobile
- ✅ All information is accurate

## 🔄 Updating Content

To update any content:
1. Edit the `index.html` file on GitHub (click the pencil icon)
2. Make your changes
3. Click "Commit changes"
4. Changes will be live in 1-2 minutes

## 🆘 Troubleshooting

**Website not showing?**
- Wait 5-10 minutes after enabling GitHub Pages
- Check that repository is set to Public
- Verify the file is named exactly `index.html`

**PDF not loading?**
- Check PDF file names match exactly (case-sensitive)
- Ensure PDFs are in the `menus/` folder
- Check PDF file size (should be < 25MB for best performance)

**QR Code not working?**
- Verify the URL is correct
- Test the URL in a browser first
- Make sure there are no typos

## 💡 Tips

- Keep PDF file sizes small (under 5MB) for faster loading
- Test on multiple devices before printing QR codes
- Update menu PDFs regularly
- Consider adding special offers to the banner

## 📞 Support

For issues or questions:
- Check GitHub Pages documentation: [docs.github.com/pages](https://docs.github.com/pages)
- Create an issue in your repository

---

Made with ❤️ for Galiyara Food Court
