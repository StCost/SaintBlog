# Saint Blog

A super quick and simple GitHub Pages blog built with Vite + React, featuring dark mode and markdown support.

## Features

- 🌙 **Dark Mode**: Beautiful GitHub-inspired dark theme
- 📝 **Markdown Support**: Write posts in markdown format
- 🔄 **Auto-sorting**: Posts sorted by number in filename (descending)
- ⚡ **Fast**: Built with Vite for lightning-fast development
- 🚀 **GitHub Pages Ready**: Deploy easily with GitHub Actions
- 🔗 **Hash Routing**: Works perfectly with GitHub Pages

## Quick Start

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start development server:**
   ```bash
   npm run dev
   ```

3. **Build for production:**
   ```bash
   npm run build
   ```

## Adding Blog Posts

1. Create a new markdown file in `public/posts/`
2. Name it with a number prefix: `004-my-new-post.md`
3. Higher numbers appear first in the list
4. Update the `blogPosts` array in `src/components/BlogList.jsx`

### Example Post Structure

```markdown
# My Blog Post Title

Your content here...

## Subheading

More content with **bold** and *italic* text.

```javascript
// Code blocks are supported
console.log('Hello, World!')
```

> Blockquotes work too!

- Lists
- Are
- Supported
```

### Updating the Post List

Edit `src/components/BlogList.jsx` and add your new post to the `blogPosts` array:

```javascript
const blogPosts = [
  { 
    filename: '004-my-new-post.md', 
    title: 'My New Blog Post',
    excerpt: 'A brief description of the post...'
  },
  // ... existing posts
]
```

## GitHub Pages Deployment

### Automatic Deployment

The repo includes a GitHub Actions workflow that automatically deploys to GitHub Pages when you push to the `main` branch.

### Manual Deployment

You can also deploy manually:

```bash
npm run build
npm run deploy
```

### Setup GitHub Pages

1. Go to your repository settings
2. Navigate to "Pages" section
3. Set source to "GitHub Actions"
4. The site will be available at `https://yourusername.github.io/SaintBlog/`

## Project Structure

```
SaintBlog/
├── public/
│   └── posts/           # Markdown blog posts
│       ├── 001-first-post.md
│       ├── 002-second-post.md
│       └── 003-third-post.md
├── src/
│   ├── components/
│   │   ├── BlogList.jsx # Post listing page
│   │   └── BlogPost.jsx # Individual post viewer
│   ├── App.jsx          # Main app component
│   ├── main.jsx         # React entry point
│   └── index.css        # Dark theme styles
├── .github/
│   └── workflows/
│       └── deploy.yml   # GitHub Actions deployment
├── package.json
├── vite.config.js
└── index.html
```

## Customization

### Styling

Edit `src/index.css` to customize the dark theme colors and layout.

### Blog Info

Update the blog title and description in `src/components/BlogList.jsx`:

```javascript
<header className="header">
  <h1>Your Blog Name</h1>
  <p>Your blog description</p>
</header>
```

### Base URL

If your repository name is different, update the `base` in `vite.config.js`:

```javascript
export default defineConfig({
  plugins: [react()],
  base: '/YourRepoName/',
  // ...
})
```

## Technologies Used

- **React 18** - UI framework
- **Vite** - Build tool and dev server
- **React Router** - Hash-based routing
- **React Markdown** - Markdown rendering
- **GitHub Actions** - Automatic deployment
- **GitHub Pages** - Free hosting

## License

MIT License - feel free to use this for your own blog!

---

Happy blogging! 🚀 