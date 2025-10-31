# TrustVault Deployment Guide

## 🚀 Netlify Deployment

Your project has been configured for deployment on Netlify. Follow these steps to deploy:

### Option 1: Automatic Deployment (Recommended)

1. **Go to Netlify:**
   - Visit https://netlify.com
   - Sign in with your GitHub account (or create one)

2. **Connect Your Repository:**
   - Click "Add new site" → "Import an existing project"
   - Choose "GitHub" as your Git provider
   - Select your repository: `Herome12/TrustVault-master`

3. **Configure Build Settings:**
   - Build command: `npm run build`
   - Publish directory: `.next`
   - Netlify will automatically detect `netlify.toml` configuration

4. **Set Environment Variables:**
   In Netlify Dashboard → Site settings → Build & deploy → Environment:
   ```
   NEXT_PUBLIC_APPWRITE_ENDPOINT=https://your-appwrite-instance
   NEXT_PUBLIC_APPWRITE_API_KEY=your-api-key
   APPWRITE_API_KEY=your-api-key
   PLAID_CLIENT_ID=your-plaid-client-id
   PLAID_SECRET=your-plaid-secret
   DWOLLA_KEY=your-dwolla-key
   DWOLLA_SECRET=your-dwolla-secret
   SENTRY_AUTH_TOKEN=your-sentry-token (optional)
   ```

5. **Deploy:**
   - Click "Deploy site"
   - Netlify will build and deploy automatically
   - Your site will be live at: `https://your-site-name.netlify.app`

### Option 2: Render Deployment

If you prefer Render instead:

1. **Go to Render:**
   - Visit https://render.com
   - Sign up or log in

2. **Create New Web Service:**
   - Click "New +" → "Web Service"
   - Connect your GitHub repository
   - Select `TrustVault-master`

3. **Configure:**
   - **Name:** `trustvault` (or your preferred name)
   - **Environment:** Node
   - **Build Command:** `npm run build`
   - **Start Command:** `npm start`
   - **Node Version:** 18+ (match your `package.json` engines)

4. **Set Environment Variables:**
   Same as Netlify (see above)

5. **Deploy:**
   - Click "Create Web Service"
   - Your site will be live at: `https://trustvault.onrender.com`

## 📝 Environment Variables Required

Make sure to set these in your hosting platform:

### Appwrite (Backend)
- `NEXT_PUBLIC_APPWRITE_ENDPOINT` - Your Appwrite instance URL
- `NEXT_PUBLIC_APPWRITE_API_KEY` - Appwrite API key
- `APPWRITE_API_KEY` - Server-side Appwrite key

### Plaid (Bank Connection)
- `PLAID_CLIENT_ID` - Your Plaid client ID
- `PLAID_SECRET` - Your Plaid secret key

### Dwolla (Payment Processing)
- `DWOLLA_KEY` - Your Dwolla API key
- `DWOLLA_SECRET` - Your Dwolla secret

### Sentry (Error Tracking - Optional)
- `SENTRY_AUTH_TOKEN` - Your Sentry authentication token

## ✅ Build Configuration

The project includes:
- **netlify.toml** - Netlify-specific configuration
- **next.config.mjs** - Next.js configuration with Sentry integration
- **package.json** - Build and start scripts

## 🔗 Your Repository

**GitHub Repository:** https://github.com/Herome12/TrustVault-master

## 📊 Build Status

Build commands:
```bash
npm run build    # Production build
npm run dev      # Development server (localhost:3001)
npm start        # Start production server
```

## 🎯 Next Steps

1. Complete the deployment on your chosen platform (Netlify or Render)
2. Configure environment variables
3. Monitor build and deployment logs
4. Test all features (authentication, bank linking, payments)

## ⚠️ Important Notes

- The app requires valid Appwrite, Plaid, and Dwolla credentials to function fully
- Set proper environment variables before deployment
- Sentry configuration is included but optional
- The `.env.local` file is for local development only

---

**Questions?** Check the README.md in your repository or contact support.
