# rubiconsoft.net

A modern "Coming Soon" landing page for rubiconsoft.net with email waitlist functionality.

## Overview

This is a static landing page featuring a clean, gradient-styled design with an integrated HubSpot form for collecting visitor emails. The page serves as a placeholder while the full website is being developed.

## Features

- 🎨 Modern gradient design with glassmorphism effects
- 📧 HubSpot form integration for email collection
- 📱 Fully responsive layout
- ⚡ Fast loading with minimal dependencies
- 🚀 Deployed on Vercel

## Tech Stack

- HTML5
- CSS3 (with custom gradients and animations)
- HubSpot Forms API
- Vercel (deployment platform)

## File Structure

```
.
├── index.html      # Main landing page
├── vercel.json     # Vercel deployment configuration
├── .gitignore      # Git ignore rules
└── README.md       # This file
```

## Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/PresidentAnderson/rubiconsoft.net.git
   cd rubiconsoft.net
   ```

2. Open `index.html` in your browser:
   ```bash
   open index.html
   # or
   python -m http.server 8000
   # Then visit http://localhost:8000
   ```

## Deployment

This project is configured for automatic deployment on Vercel. Any push to the main branch will trigger a new deployment.

### Manual Deployment

If you need to deploy manually:

```bash
vercel --prod
```

## HubSpot Configuration

The page uses HubSpot Forms with the following configuration:
- Portal ID: `43986063`
- Form ID: `waitlist-rubiconsoftnet`
- Region: `na1`

A fallback form is provided in case the HubSpot API is unavailable.

## Customization

To customize the page:

1. **Colors**: Update the gradient values in the `<style>` section
2. **Content**: Modify the text in the `.container` div
3. **Form**: Update the HubSpot configuration in the `<script>` section

## License

© 2026 AXAI Innovations · All rights reserved

## Contact

For inquiries, please use the waitlist form on [rubiconsoft.net](https://rubiconsoft.net)
