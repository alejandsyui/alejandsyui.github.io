# GitHub Pages Setup Guide

This guide explains how GitHub Pages is configured for this Microsoft homepage clone.

## Repository Configuration

- **Repository Name**: `alejandsyui.github.io`
- **Type**: User/Organization site
- **URL**: `https://alejandsyui.github.io`

## GitHub Pages Settings

### Source Configuration
- **Branch**: `master`
- **Path**: `/` (root directory)
- **Build Type**: `legacy`

### Why Legacy Build Type?
For user/organization sites serving static HTML/CSS/JS files, the `legacy` build type is used instead of `workflow`. This prevents Jekyll processing and serves files as-is.

## Deployment Process

### Automatic Deployment
1. Push changes to the `master` branch
2. GitHub Pages automatically detects changes
3. Site rebuilds (may take 5-20 minutes)
4. Updated site is live

### Manual Deployment Triggers
- Push any commit to `master`
- The `.nojekyll` file ensures no Jekyll processing
- GitHub Actions workflow can also trigger builds

## File Structure for GitHub Pages

```
├── index.html          # Main homepage (served as root)
├── .nojekyll          # Prevents Jekyll processing
├── .github/
│   └── workflows/     # Optional: GitHub Actions workflows
├── docs/              # Documentation (not served)
└── assets/            # Static assets (if any)
```

## Troubleshooting

### Site Not Updating
1. Check build status in repository Settings > Pages
2. Verify files are committed and pushed to `master`
3. Wait 10-15 minutes for build completion
4. Check browser cache (hard refresh)

### Build Failures
- Ensure `index.html` exists in root
- Check for syntax errors in HTML/CSS
- Verify external resources are accessible

### Custom Domain (if applicable)
- Add `CNAME` file to root with domain
- Configure DNS settings
- Update GitHub Pages settings

## Performance Optimization

- Use CDN links for external resources (Font Awesome, images)
- Minimize CSS and HTML
- Optimize images
- Enable gzip compression (automatic on GitHub Pages)

## Security Considerations

- All content is publicly accessible
- No server-side processing
- HTTPS enforced by default
- No user data storage

## Monitoring

- Check repository Settings > Pages for build status
- Monitor site availability
- Review GitHub Actions logs (if using workflows)
