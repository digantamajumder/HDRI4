# HDRI - Human Development & Research Institute

This is the official website for Human Development & Research Institute (HDRI), a non-profit NGO founded in Kolkata in 1985.

## Deployment Instructions for Netlify

### Automatic Deployment

1. Push your code to a GitHub repository
2. Log in to Netlify and click "New site from Git"
3. Select your GitHub repository
4. Use the following build settings:
   - Build command: `npm run build`
   - Publish directory: `dist`
5. Click "Deploy site"

### Manual Deployment

1. Build the project locally:
   ```
   npm run build
   ```
2. Drag and drop the `dist` folder to Netlify's manual deploy section

## Important Files for Deployment

- `netlify.toml`: Contains build settings and redirect rules
- `public/_redirects`: Ensures client-side routing works correctly
- `index.html`: Main entry point for the application

## Troubleshooting Deployment Issues

1. **404 errors on page refresh or direct URL access**:
   - Make sure the `_redirects` file is in the `public` folder
   - Verify the `netlify.toml` file has the correct redirect rules

2. **Missing assets**:
   - Check that all referenced assets exist in the `public` folder
   - Ensure paths in HTML files use absolute paths (starting with `/`)

3. **Build failures**:
   - Check the build logs in Netlify
   - Verify that all dependencies are correctly installed
   - Make sure the Node.js version is compatible with your project