# 📝 How to Get Google Review Links for Your Shops

## 🎯 Overview
Each shop in Galiyara needs its own Google Business Profile to collect reviews. This guide will help you set up Google Review links for all 9 outlets.

---

## 📍 Step 1: Create Google Business Profiles (If Not Done)

### For Each Shop:
1. Go to: https://business.google.com
2. Click **"Manage now"**
3. Enter your business details:
   - Business name (e.g., "Burger Hub - Galiyara")
   - Category (e.g., "Fast Food Restaurant")
   - Location: Patarkar Colony, Jaipur, Rajasthan
   - Phone number
   - Website (your GitHub Pages URL)
4. Verify your business (Google will send a postcard or call)

### Important Notes:
- Each shop should have its own separate profile
- Use descriptive names: "Shop Name - Galiyara Food Court"
- Same address for all shops (Patarkar Colony, Jaipur)
- Different phone numbers if available

---

## 🔗 Step 2: Get Review Links for Each Shop

### Method 1: Using Google Business Profile (Recommended)

1. **Login to Google Business Profile**:
   - Go to: https://business.google.com
   - Select your business

2. **Get the Review Link**:
   - Click on "Home" in the left menu
   - Scroll down to "Get more reviews"
   - Click "Share review form"
   - Copy the link (looks like: `https://g.page/r/XXXXX/review`)

3. **Repeat for all 9 shops**

### Method 2: Manual Construction

If you can't find the link, construct it manually:

**Format:**
```
https://search.google.com/local/writereview?placeid=YOUR_PLACE_ID
```

**How to get Place ID:**
1. Search your business on Google Maps
2. Open the business listing
3. Look at the URL, you'll see something like:
   `https://www.google.com/maps/place/.../@...data=!4m2!3m1!1s0x0:PLACE_ID_HERE`
4. OR use this tool: https://developers.google.com/maps/documentation/places/web-service/place-id

---

## 📋 Step 3: Update Your Website

Once you have all 9 review links, update `index.html`:

### Find and Replace:

**Shop 1 - Burger Hub:**
```html
Replace: 'https://g.page/r/YOUR_PLACE_ID_1/review'
With: 'https://g.page/r/ACTUAL_PLACE_ID/review'
```

**Shop 2 - Chai & Snacks Corner:**
```html
Replace: 'https://g.page/r/YOUR_PLACE_ID_2/review'
With: 'https://g.page/r/ACTUAL_PLACE_ID/review'
```

...and so on for all 9 shops.

### Example:
```html
<!-- Before -->
onclick="openMenu('Burger Hub', '🍔', 'menus/burgers-menu.pdf', 'https://g.page/r/YOUR_PLACE_ID_1/review')"

<!-- After -->
onclick="openMenu('Burger Hub', '🍔', 'menus/burgers-menu.pdf', 'https://g.page/r/CbK8pM9hN2dR/review')"
```

---

## 🎨 Alternative: Use a Single Review Link for Entire Food Court

If creating 9 separate profiles is too much work, you can:

1. Create ONE Google Business Profile for "Galiyara Food Court"
2. Get its review link
3. Use the SAME link for all 9 shops
4. Replace all `YOUR_PLACE_ID_X` with the same ID

**Update in index.html:**
```javascript
// All shops use the same review link
const galiyaraReviewLink = 'https://g.page/r/YOUR_GALIYARA_ID/review';

// Update all shop cards to use this link
onclick="openMenu('Burger Hub', '🍔', 'menus/burgers-menu.pdf', galiyaraReviewLink)"
```

---

## ✅ Testing Your Review Links

### Test Each Link:
1. Click the review button on your website
2. You should see Google's review page
3. Try leaving a test review (you can delete it later)
4. Make sure it's going to the correct business

### Common Issues:
- ❌ Link shows "Page not found" → Business not verified yet
- ❌ Wrong business appears → Wrong Place ID
- ❌ Button doesn't work → Check JavaScript syntax

---

## 📊 Recommendation: Which Approach to Use?

### Option A: Separate Profiles for Each Shop ⭐ RECOMMENDED
**Pros:**
- Each shop gets its own reviews
- Better for SEO and local search
- More professional
- Customers can see specific shop ratings

**Cons:**
- More setup work (9 profiles)
- Need to verify each business
- Manage 9 different review sections

### Option B: Single Profile for Galiyara Food Court
**Pros:**
- Quick and easy setup (just 1 profile)
- All reviews in one place
- Easier to manage

**Cons:**
- Can't track which shop gets which review
- Less specific for customers
- Might confuse customers

---

## 🚀 Quick Start (Option A - Separate Profiles)

1. **Create Profiles for All Shops** (1-2 hours)
   - Burger Hub - Galiyara
   - Chai & Snacks Corner - Galiyara
   - Juice Junction - Galiyara
   - Pizza Palace - Galiyara
   - Rolls & Wraps - Galiyara
   - Ice Cream Factory - Galiyara
   - Sandwich Station - Galiyara
   - Chinese Wok - Galiyara
   - South Indian Express - Galiyara

2. **Get Review Links** (10 minutes)
   - Collect all 9 review links
   - Keep them in a document

3. **Update Website** (5 minutes)
   - Edit index.html
   - Replace all `YOUR_PLACE_ID_X`
   - Commit changes to GitHub

4. **Test Everything** (10 minutes)
   - Click each shop's review button
   - Verify correct business appears

---

## 🚀 Quick Start (Option B - Single Profile)

1. **Create One Profile** (10 minutes)
   - Name: "Galiyara Food Court"
   - Category: "Food Court"
   - Add all details

2. **Get Review Link** (2 minutes)
   - Copy the review link

3. **Update Website** (2 minutes)
   - Replace ALL instances of `YOUR_PLACE_ID_X` with the same ID
   - OR create a variable at the top of your script

4. **Done!** (Much faster)

---

## 📝 Sample Code for Single Review Link

If using Option B, update your index.html like this:

```html
<script>
    // Configuration
    const GALIYARA_REVIEW_URL = 'https://g.page/r/YOUR_ACTUAL_PLACE_ID/review';
    
    let currentPdfUrl = '';
    let currentShopReviewUrl = '';
    let lastScrollPosition = 0;

    // Then all shops use GALIYARA_REVIEW_URL instead of individual links
</script>
```

Then update all shop cards:
```html
onclick="openMenu('Burger Hub', '🍔', 'menus/burgers-menu.pdf', GALIYARA_REVIEW_URL)"
```

---

## 🎯 Next Steps After Setup

1. **Respond to Reviews**: Check Google Business Profile regularly
2. **Encourage Reviews**: Train staff to ask satisfied customers
3. **Display Reviews**: Consider adding review widgets to website
4. **Monitor Ratings**: Track which shops need improvement

---

## 🆘 Need Help?

- **Google Business Support**: https://support.google.com/business
- **Place ID Finder**: https://developers.google.com/maps/documentation/javascript/examples/places-placeid-finder
- **Video Tutorials**: Search "How to get Google review link" on YouTube

---

Good luck with your Google Reviews! 🌟
