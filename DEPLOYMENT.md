# SHWE-PAY Website Deployment Guide

## Overview
This repository contains a professional single-page HTML website for SHWE-PAY, a Solana SPL payment token.

## Features
- ✅ Dark modern crypto design with responsive CSS
- ✅ Phantom wallet integration (read-only)
- ✅ SOL balance display with RPC fallback
- ✅ Jupiter exchange integration
- ✅ Comprehensive tokenomics section
- ✅ Step-by-step purchase guide
- ✅ Whitepaper download (placeholder)
- ✅ Legal disclaimer for compliance
- ✅ English/Burmese language switcher
- ✅ Mobile-responsive design

## Deployment

### Option 1: GitHub Pages
1. Go to repository Settings
2. Navigate to Pages section
3. Select branch: `copilot/create-single-page-website`
4. Select folder: `/ (root)`
5. Click Save
6. Website will be available at: `https://sengawng2020.github.io/shwe-pay/`

### Option 2: Any Static Host
Simply upload the `index.html` file to any static hosting service:
- Netlify: Drag and drop the file
- Vercel: Deploy via GitHub integration
- AWS S3: Upload to bucket with static hosting enabled
- Cloudflare Pages: Connect GitHub repository

### Option 3: Local Testing
```bash
# Using Python
python3 -m http.server 8000

# Using Node.js
npx http-server

# Then open http://localhost:8000/index.html
```

## Configuration

### Update Token Contract Address
When you have a Solana token contract address, update the Jupiter link:
```html
<!-- Line ~410 in index.html -->
<a href="https://jup.ag/swap/SOL-YOUR_TOKEN_ADDRESS" ...>
```

### Add Whitepaper PDF
1. Create your whitepaper PDF
2. Place it in the repository (e.g., `whitepaper.pdf`)
3. Update the download link:
```javascript
// Around line 617 in index.html
downloadWhitepaper.addEventListener('click', (e) => {
    e.preventDefault();
    window.open('whitepaper.pdf', '_blank');
});
```

## Security Notes
- Frontend-only, no backend required
- Read-only wallet connection (cannot execute transactions)
- Pinned Solana Web3.js version for stability
- Multiple RPC endpoints for reliability
- No private key handling or storage

## Browser Compatibility
- Chrome/Edge: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- Mobile browsers: ✅ Fully responsive

## Support
For issues or questions, please open an issue in the GitHub repository.
