# Ecourse Web Development

This repository contains the landing page for our comprehensive web development online course. The course is designed to take students from complete beginners to job-ready developers through six comprehensive modules.

## Features

- Responsive design
- Interactive curriculum overview
- Student testimonials
- Pricing plans
- FAQ section
- Registration form
- Promo modal

## Technologies Used

- HTML5
- Tailwind CSS
- JavaScript
- Font Awesome icons

## Getting Started

To get a local copy up and running, follow these steps:

1. Clone the repository
   ```
   git clone https://github.com/your-username/ecourse-web-development.git
   ```

2. Navigate to the project directory
   ```
   cd ecourse-web-development
   ```

3. Install dependencies
   ```
   npm install
   ```

4. Install development dependencies
   ```
   npm install -D tailwindcss postcss autoprefixer html-minifier
   ```

5. Initialize Tailwind CSS
   ```
   npx tailwindcss init -p
   ```

6. Update `tailwind.config.js` file in your project root:
   ```javascript
   module.exports = {
     purge: ['./**/*.html'],
     darkMode: false,
     theme: {
       extend: {},
     },
     variants: {
       extend: {},
     },
     plugins: [],
   }
   ```

7. Create or update `styles.css` file in your project root:
   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

8. Update your `package.json` with the following scripts:
   ```json
   "scripts": {
     "build:css": "tailwindcss -i ./styles.css -o ./dist/styles.min.css --minify",
     "minify-html": "html-minifier --collapse-whitespace --remove-comments --remove-optional-tags --remove-redundant-attributes --remove-script-type-attributes --remove-tag-whitespace --use-short-doctype --minify-css true --minify-js true -o index.min.html ecourse-coding.html",
     "build": "npm run build:css && npm run minify-html"
   }
   ```

9. Run the build process
   ```
   npm run build
   ```

10. The optimized files will be:
    - `./dist/styles.min.css` (minified CSS)
    - `index.min.html` (minified HTML)

## Optimization Steps

1. Minify HTML:
   - This is handled by the `minify-html` script in `package.json`.

2. Optimize images:
   - Use a tool like ImageOptim or TinyPNG to compress images without significant quality loss.
   - Consider using WebP format for better compression.

3. Lazy load images:
   - Add `loading="lazy"` attribute to `<img>` tags that are below the fold.

4. Optimize fonts:
   - Use `font-display: swap` for custom fonts.
   - Consider using system fonts instead of custom fonts where possible.

5. Remove unused CSS:
   - Tailwind's purge option in `tailwind.config.js` handles this.

## Deployment to GitHub Pages

1. Create a new repository on GitHub.

2. Initialize git in your local project folder (if not already done):
   ```
   git init
   ```

3. Add your files to git:
   ```
   git add .
   ```

4. Commit your changes:
   ```
   git commit -m "Initial commit"
   ```

5. Add your GitHub repository as a remote:
   ```
   git remote add origin https://github.com/your-username/your-repo-name.git
   ```

6. Push your code to GitHub:
   ```
   git push -u origin main
   ```

7. Rename `index.min.html` to `index.html`:
   ```
   mv index.min.html index.html
   ```

8. In your GitHub repository settings, navigate to the "Pages" section.

9. Under "Source", select the branch you want to deploy (usually `main`).

10. Click "Save". GitHub will provide you with a URL where your site is published.

## Maintenance

To update your site:

1. Make changes to `ecourse-coding.html` or `styles.css`.
2. Run `npm run build` to regenerate optimized files.
3. Rename `index.min.html` to `index.html`.
4. Commit and push changes to GitHub.

Remember to update this README as your project evolves. Good luck with your Ecourse Web Development landing page!