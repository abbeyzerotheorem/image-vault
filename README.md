# GitHub Image Storage

A fully-featured image storage website that uses GitHub as a free, permanent backend. Upload, view, and manage your images directly from your browser, with all data stored in your GitHub repository.

## 🌟 Features

- **Free Permanent Storage**: Uses GitHub's free 100GB storage
- **Full CRUD Operations**: Upload, view, download, and delete images
- **Drag & Drop Interface**: Easy file upload with drag & drop support
- **Image Gallery**: Beautiful responsive gallery with search functionality
- **GitHub Integration**: Direct connection to your GitHub repository
- **Progress Indicators**: Visual feedback during uploads
- **Secure**: Personal access token stored only in browser localStorage
- **Responsive Design**: Works on desktop, tablet, and mobile

## 🚀 Quick Start

### Prerequisites
- A GitHub account (free)
- A web browser

### Setup Instructions

1. **Create a GitHub Repository**
   - Go to [github.com](https://github.com)
   - Click "+" → "New repository"
   - Name it (e.g., "image-storage")
   - Set to Public (Private also works)
   - Click "Create repository"

2. **Generate Personal Access Token**
   - Go to GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Click "Generate new token" → "Generate new token (classic)"
   - **Token name**: "Image Storage"
   - **Select scopes**: `repo` and `workflow`
   - Click "Generate token"
   - **IMPORTANT**: Copy the token immediately (you won't see it again!)

3. **Launch the Website**
   - Download the `index.html` file
   - Open it in your browser
   - Enter your GitHub username, repository name, and personal access token
   - Click "Connect to GitHub"

## 📁 Project Structure

```
github-image-storage/
├── index.html          # Main HTML file (contains all code)
└── README.md           # This documentation
```

## 🛠️ Technologies Used

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Backend**: GitHub REST API
- **Storage**: GitHub Repository (images stored in `/images/` folder)
- **Styling**: Custom CSS with GitHub's color scheme
- **Icons**: Font Awesome 6.4.0

## 🔧 How It Works

### Image Upload
1. Images are converted to base64
2. Uploaded to GitHub repository via API
3. Stored in `/images/` folder with timestamp prefix
4. Images are publicly accessible via GitHub's CDN

### Image Management
- **View**: Opens image in new tab via raw.githubusercontent.com
- **Download**: Direct download from GitHub
- **Delete**: Removes file from GitHub repository via API
- **Search**: Filter images by filename

### Data Flow
```
Browser → GitHub API → GitHub Repository → GitHub CDN → Browser
```

## 💾 Storage Details

- **Max file size**: 25MB per image (GitHub limit: 100MB)
- **Total storage**: 100GB free (GitHub free tier)
- **File types**: JPG, PNG, GIF, WEBP
- **Location**: `/images/` folder in your GitHub repository

## 🔒 Security

- Personal access token stored only in browser's localStorage
- Token never leaves your computer
- GitHub API handles authentication
- Repository can be set to Private for additional privacy
- All operations require valid token authentication

## 📱 Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 11+
- Edge 79+
- Opera 47+

## 🚨 Limitations

- GitHub API rate limit: 5000 requests/hour
- File size limit: 25MB per image (configurable)
- Requires internet connection
- Initial setup requires GitHub account

## 🆘 Troubleshooting

### Common Issues

1. **"Repository not found"**
   - Check repository name spelling
   - Ensure repository exists
   - Try creating repository from the app

2. **"Authentication failed"**
   - Regenerate personal access token
   - Ensure token has `repo` scope
   - Token might have expired (tokens don't expire by default)

3. **Upload fails**
   - Check file size (max 25MB)
   - Check internet connection
   - GitHub might be experiencing issues

4. **Images not loading**
   - Clear browser cache
   - Check GitHub status at [status.github.com](https://www.githubstatus.com/)
   - Repository might be set to Private (images won't be publicly accessible)

## 🔄 Updating

Since this is a single HTML file, updates are simple:

1. Replace the existing `index.html` with the new version
2. Refresh your browser
3. Your GitHub credentials will be preserved (stored in localStorage)

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 🙏 Acknowledgments

- GitHub for providing free API and storage
- Font Awesome for icons

---

**Note**: This application stores images in your GitHub repository. Be mindful of:
- Repository visibility (Public/Private)
- Copyright and licensing of uploaded images
- GitHub's Acceptable Use Policy

---

Made with ❤️ using GitHub's API | [Live Demo](#) | [Report Bug](https://github.com/yourusername/image-storage/issues)
