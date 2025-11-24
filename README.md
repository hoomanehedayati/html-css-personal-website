# HTML/CSS Personal Website

A modern, responsive personal portfolio website built with HTML, CSS, and JavaScript. Features a clean design with smooth animations and a mobile-friendly layout.

## Features

- 🎨 **Modern Design**: Clean and professional layout with gradient backgrounds
- 📱 **Fully Responsive**: Works perfectly on desktop, tablet, and mobile devices
- ✨ **Smooth Animations**: Fade-in effects and smooth scrolling
- 🎯 **Interactive Navigation**: Sticky navbar with active section highlighting
- 📊 **Project Showcase**: Display your projects with tags and descriptions
- 💼 **Skills Section**: Showcase your technical skills with icons
- 📧 **Contact Section**: Easy ways to get in touch

## Sections

1. **Hero Section**: Eye-catching introduction with call-to-action buttons
2. **About Section**: Personal information and statistics
3. **Projects Section**: Grid layout showcasing featured projects
4. **Skills Section**: Technical skills with icons
5. **Contact Section**: Social links and contact information

## Technologies Used

- HTML5
- CSS3 (with CSS Grid and Flexbox)
- JavaScript (Vanilla JS)
- Font Awesome Icons

## Getting Started

1. Clone or download this repository
2. Open `index.html` in your web browser
3. Customize the content in `index.html`:
   - Update your name and title
   - Add your projects
   - Update skills and contact information
   - Modify colors in `styles.css` if desired

## Deployment to GitHub Pages

This website is ready to be deployed on GitHub Pages:

1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under **Source**, select:
   - **Branch**: `main`
   - **Folder**: `/ (root)`
4. Click **Save**
5. Wait 5-10 minutes for GitHub to build your site
6. Your site will be live at: `https://[your-username].github.io/html-css-personal-website`

**Note**: The `.nojekyll` file is included to ensure GitHub Pages serves the site correctly without Jekyll processing.

## Customization

### Changing Colors

Edit the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #6366f1;
    --secondary-color: #8b5cf6;
    /* ... other colors */
}
```

### Adding Projects

Add new project cards in the projects section:

```html
<div class="project-card">
    <div class="project-image">
        <i class="fas fa-icon-name"></i>
    </div>
    <h3 class="project-title">Project Name</h3>
    <p class="project-description">Project description</p>
    <div class="project-tags">
        <span class="tag">Technology</span>
    </div>
</div>
```

### Adding Skills

Add new skill items in the skills section:

```html
<div class="skill-item">
    <i class="fab fa-technology-icon"></i>
    <span>Technology Name</span>
</div>
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

This project is open source and available for educational purposes.

## Contributing

Feel free to submit issues or pull requests if you have suggestions for improvements!

