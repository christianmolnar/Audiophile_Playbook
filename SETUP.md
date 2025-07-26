# Audiophile Playbook - Development Setup Guide

## Overview
This is a static HTML/CSS/JavaScript website for audiophile DAP and headphone EQ settings. The site requires minimal setup and has very few external dependencies.

## Prerequisites
To work on this project on any computer, you need:

### Operating System Compatibility
- ✅ **Windows** (any version with modern browser)
- ✅ **macOS** (any version with modern browser)
- ✅ **Linux** (any distribution with modern browser)
- ✅ **Chrome OS** (with developer mode for local server)

### Required Software
1. **Web Browser** (Chrome, Firefox, Safari, or Edge)
2. **Text Editor or IDE** (VS Code recommended)
3. **Local Web Server** (for development)

### Optional but Recommended
1. **Git** - for version control
   - Windows: Download from git-scm.com
   - macOS: Install via Xcode Command Line Tools or Homebrew
   - Linux: `sudo apt install git` (Ubuntu/Debian) or equivalent
2. **VS Code Extensions**:
   - Live Server (for local development server)
   - HTML CSS Support
   - JavaScript (ES6) code snippets
3. **Excel/LibreOffice** (optional) - for viewing/editing the XLSX EQ data file

## Project Structure
```
├── index.html              # Main homepage
├── kann_max.html           # Kann Max DAP page
├── acroca1000t.html        # ACRO CA1000T DAP page
├── kenwood_kd500.html      # Kenwood turntable page
├── story.html              # Story page with animations
├── cartridge_guide.html    # Cartridge guide
├── style.css               # Main stylesheet
├── kann_max_peq_values.csv # EQ data (CSV format)
├── kann_max_peq_values.xlsx # EQ data (Excel format)
├── assets/                 # Images, videos, and text files
├── .vscode/                # VS Code configuration
└── README.md               # Basic project description
```

## External Dependencies

### 1. Google Fonts
- **Service**: Google Fonts CDN
- **Font**: Montserrat (weights: 300, 400, 700)
- **Implementation**: CSS `@import` in `style.css`
- **Fallback**: Arial, sans-serif
- **Internet Required**: Yes (for font loading)

### 2. Formspree.io Contact Forms
- **Service**: Formspree form handling service
- **Endpoint**: `https://formspree.io/f/xovdeqpa`
- **Usage**: Contact forms on all pages
- **Account Required**: Yes (already configured)
- **Internet Required**: Yes (for form submissions)

### 3. Local Development Server
- **Purpose**: Serving files locally for development
- **Port**: 8080 (configured in `.vscode/launch.json`)
- **Options**:
  - VS Code Live Server extension
  - Python: `python -m http.server 8080`
  - Node.js: `npx http-server -p 8080`
  - Any other static file server

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/christianmolnar/Audiophile_Playbook.git
cd Audiophile_Playbook
```

### 2. Set Up Local Development Server

#### Option A: VS Code with Live Server Extension
1. Install VS Code
2. Install "Live Server" extension
3. Open project folder in VS Code
4. Right-click on `index.html`
5. Select "Open with Live Server"

#### Option B: Python Server (Cross-Platform)
```bash
# Check if Python is installed
python --version
# or
python3 --version

# Python 3 (recommended)
python -m http.server 8080
# or on some systems
python3 -m http.server 8080

# Python 2 (legacy)
python -m SimpleHTTPServer 8080
```

#### Option C: Node.js Server (Cross-Platform)
```bash
# Check if Node.js is installed
node --version

# Install http-server globally (one-time setup)
npm install -g http-server

# Start server
http-server -p 8080
```

#### Option D: Other Options
- XAMPP, WAMP, or MAMP
- Any static file server

### 3. Access the Site
Open your browser and navigate to:
- `http://localhost:8080`

## Development Workflow

### File Editing
- All files are standard HTML, CSS, and JavaScript
- No build process required
- Changes are immediately visible after browser refresh

### Key Files to Understand
1. **`style.css`** - Contains all styling and CSS custom properties
2. **`kann_max.html`** - Contains complex JavaScript for EQ graphs and tables
3. **`index.html`** - Main homepage with project story
4. **Assets folder** - All images, videos, and supporting files

### Interactive Features
- **EQ Graphs**: Custom Canvas-based graphs (no external charting library)
- **Dropdown Navigation**: Pure CSS/JavaScript implementation
- **Contact Forms**: Uses Formspree.io service
- **Responsive Design**: CSS media queries

## No Build Process Required
This project intentionally uses:
- ✅ Pure HTML, CSS, JavaScript
- ✅ No package.json or npm dependencies
- ✅ No webpack, gulp, or other build tools
- ✅ No preprocessing (Sass, TypeScript, etc.)
- ✅ Self-contained with minimal external dependencies
- ✅ Cross-platform compatible (Windows, macOS, Linux)
- ✅ No database or server-side code required

## Deployment
Since this is a static site, it can be deployed to:
- GitHub Pages
- Netlify
- Vercel
- Any web hosting service
- CDN (CloudFront, etc.)

Simply upload all files to your web hosting provider.

## Browser Compatibility
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Uses HTML5 Canvas for graphs
- Uses CSS Grid and Flexbox
- JavaScript ES6+ features

## Internet Requirements
### Required for Full Functionality:
- Google Fonts loading
- Contact form submissions (Formspree)

### Works Offline:
- All core functionality
- Navigation and content
- EQ graphs and tables
- Responsive design

## Troubleshooting

### Common Issues:
1. **Fonts not loading**: Check internet connection or use system fonts
2. **Local server not working**: Try different port or server method
3. **Forms not submitting**: Verify Formspree endpoint is correct
4. **Images not displaying**: Check file paths and case sensitivity

### Browser Developer Tools
Use F12 to access:
- Console for JavaScript errors
- Network tab for loading issues
- Elements tab for CSS debugging

## Contributing
1. Make changes to HTML, CSS, or JavaScript files
2. Test locally using development server
3. Commit changes to Git
4. Deploy updated files to hosting provider

## Support
For questions about the setup process, check:
1. Browser developer console for errors
2. This documentation
3. Project README.md
4. Contact form on the website (when deployed)

## Complete Installation Checklist
Before starting development, ensure you have:
- [ ] A modern web browser installed
- [ ] A text editor or IDE (VS Code recommended)
- [ ] Git installed (for cloning the repository)
- [ ] A method to run a local web server:
  - [ ] Python (any version) OR
  - [ ] Node.js (for http-server) OR  
  - [ ] VS Code with Live Server extension OR
  - [ ] XAMPP/WAMP/MAMP OR
  - [ ] Any other static file server
- [ ] Internet connection (for Google Fonts and contact forms)

**That's it!** No additional software, libraries, frameworks, or build tools are required.
