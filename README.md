# Train Timing Website

This folder contains the GitHub Pages website for the Train Timing app, hosted at: [https://adnan-devs777.github.io/train-timing-privacy/](https://adnan-devs777.github.io/train-timing-privacy/)

## 📁 Files Overview

- **index.html** - Main landing page with app info, features, privacy policy, and contact
- **css/styles.css** - Responsive styles for the website
- **images/** - Placeholder folder for app screenshots

## 🚀 Deployment Instructions

### Step 1: Copy Files to Your GitHub Repository

1. Clone your `train-timing-privacy` repository:
   ```bash
   git clone https://github.com/adnan-devs777/train-timing-privacy.git
   cd train-timing-privacy
   ```

2. Copy all files from this `website` folder to the repository root:
   ```bash
   # From the TrainTiming project root
   cp -r website/* ../train-timing-privacy/
   ```

3. Commit and push the changes:
   ```bash
   cd ../train-timing-privacy
   git add .
   git commit -m "Add Train Timing landing page with privacy policy"
   git push origin main
   ```

### Step 2: Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/adnan-devs777/train-timing-privacy`
2. Click **Settings** → **Pages** (in the left sidebar)
3. Under **Source**, select:
   - Branch: `main` (or `master`)
   - Folder: `/ (root)`
4. Click **Save**
5. Wait a few minutes for deployment
6. Your site will be live at: `https://adnan-devs777.github.io/train-timing-privacy/`

### Step 3: Add App Screenshots

1. Take screenshots of your app (4-8 screenshots recommended)
2. Resize them to a consistent size (e.g., 1080x2340px for modern Android phones)
3. Save them in the `images/` folder with names like:
   - `screenshot-1-home.png`
   - `screenshot-2-search.png`
   - `screenshot-3-details.png`
   - `screenshot-4-station.png`

4. Update `index.html` to replace the placeholder divs with actual images:

   **Find this section:**
   ```html
   <div class="screenshot-placeholder">
       <p>Screenshot 1<br>Home Screen</p>
   </div>
   ```

   **Replace with:**
   ```html
   <img src="images/screenshot-1-home.png" alt="Home Screen" class="screenshot-image">
   ```

5. Add this CSS to `css/styles.css`:
   ```css
   .screenshot-image {
       width: 100%;
       height: auto;
       border-radius: 20px;
       box-shadow: var(--shadow);
   }
   ```

### Step 4: Update App Links

1. Once your app is published on Google Play Store, update the download link in `index.html`:

   **Find:**
   ```html
   <a href="#" class="btn btn-primary">Download on Google Play</a>
   ```

   **Replace with:**
   ```html
   <a href="YOUR_PLAY_STORE_URL" class="btn btn-primary" target="_blank">Download on Google Play</a>
   ```

2. Also update the contact section if you have social media links.

## 📱 Google Play Store Requirements

This website meets Google Play Store requirements for:

### Data Safety Section
- ✅ Privacy policy publicly accessible via web link
- ✅ Clear explanation of data collection (feedback: name, email, message)
- ✅ Data deletion instructions (in-app feature)
- ✅ Third-party services disclosed (Firebase)

### Privacy Policy Checklist
The privacy policy on this website covers:
- [x] What data is collected
- [x] How data is used
- [x] How data is stored (Firebase)
- [x] Third-party services (Firebase, Pakistan Railways)
- [x] User rights (access, deletion, opt-out)
- [x] Data deletion process (in-app)
- [x] Children's privacy
- [x] Contact information

### To Add to Play Store Console:
1. Go to Play Console → Your App → Policy → App content
2. Under "Privacy Policy", enter: `https://adnan-devs777.github.io/train-timing-privacy/`
3. Under "Data Safety", declare:
   - **Data collected**: Email, Name, Feedback messages
   - **Purpose**: App functionality, Customer support
   - **Data sharing**: Not shared with third parties
   - **Data deletion**: Available (via in-app feature)

## 🔧 Customization

### Change Colors
Edit the CSS variables in `css/styles.css`:
```css
:root {
    --primary-color: #1976D2;      /* Main blue color */
    --secondary-color: #FFC107;     /* Gold accent color */
    /* ... other colors */
}
```

### Add More Sections
Add new sections in `index.html` before the footer:
```html
<section id="new-section" class="new-section">
    <div class="container">
        <h2 class="section-title">Your Title</h2>
        <!-- Your content -->
    </div>
</section>
```

### Update Privacy Policy
The privacy policy is integrated into the main page. To update:
1. Find the `<section id="privacy">` in `index.html`
2. Modify the content as needed
3. Update the "Last Updated" date

## 📊 Data Deletion Feature

The website explains that data deletion is handled **in the Android app**:

### User Flow:
1. User reads privacy policy on website
2. User downloads app
3. User submits feedback (with optional email)
4. Later, user can delete their data:
   - Open app → Settings → Privacy & Data → Delete My Data
   - Enter email used for feedback
   - Confirm deletion
   - Data permanently deleted from Firebase

### Developer Responsibilities:
- The `DataDeletionViewModel.kt` handles Firebase data deletion
- Queries Firebase by email address
- Deletes all matching feedback entries
- Shows success/error messages to user

## 🐛 Troubleshooting

### Website not loading?
- Check GitHub Pages settings in repository
- Ensure `index.html` is in the root directory (or configured folder)
- Wait 5-10 minutes after pushing changes
- Clear browser cache and try again

### Screenshots not showing?
- Verify image paths are correct (`images/screenshot-1.png`)
- Check file extensions match (PNG vs png)
- Ensure images are committed to git repository

### Need to update content?
1. Edit the HTML/CSS files locally
2. Test by opening `index.html` in your browser
3. Commit and push changes to GitHub
4. Wait a few minutes for GitHub Pages to rebuild

## 📧 Support

If you need help with deployment or customization:
- Email: droidclics@gmail.com
- Check GitHub Pages documentation: https://pages.github.com/

## 📝 License

This website template is part of the Train Timing project.
© 2025 MMD Projects. All rights reserved.
