# BREB Smart Meter Payment

A feature-rich mobile financial services application for utility bill payments with secure PIN entry and transaction management.

## Features

- Multi-step payment flow (Home → Customer Details → Amount Entry → Summary → PIN Entry → Success)
- Dark mode support
- Secure PIN entry
- Transaction management
- Responsive mobile-first design
- Material Design icons
- Tailwind CSS styling

## Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- Git
- GitHub account

## Run Locally

1. Install dependencies:
   ```bash
   npm install
   ```

2. Set the `GEMINI_API_KEY` in `.env.local`:
   ```
   GEMINI_API_KEY=your_actual_api_key_here
   ```

3. Run the development server:
   ```bash
   npm run dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

## Deploy to GitHub Pages (Free)

### Method 1: Automatic Deployment with GitHub Actions (Recommended)

1. **Create a GitHub repository:**
   - Go to [GitHub](https://github.com) and create a new repository
   - Name it `breb-smart-meter-payment` (or any name you prefer)
   - Don't initialize with README

2. **Update the base path in `vite.config.ts`:**
   - Open `vite.config.ts`
   - Replace `/breb-smart-meter-payment/` with `/your-repo-name/` (line 10)

3. **Push your code to GitHub:**
   ```bash
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/your-repo-name.git
   git push -u origin main
   ```

4. **Add API Key as GitHub Secret (if needed):**
   - Go to your repository on GitHub
   - Click `Settings` → `Secrets and variables` → `Actions`
   - Click `New repository secret`
   - Name: `GEMINI_API_KEY`
   - Value: Your actual Gemini API key
   - Click `Add secret`

5. **Enable GitHub Pages:**
   - Go to `Settings` → `Pages`
   - Under "Build and deployment"
   - Source: Select `GitHub Actions`
   - Save

6. **Trigger deployment:**
   - The workflow will automatically run on every push to `main`
   - Or go to `Actions` tab and manually trigger the workflow
   - Wait for the workflow to complete (green checkmark)

7. **Access your deployed site:**
   - Your site will be available at: `https://YOUR_USERNAME.github.io/your-repo-name/`

### Method 2: Manual Deployment with gh-pages

1. **Create a GitHub repository** (same as Method 1, steps 1-3)

2. **Install gh-pages package:**
   ```bash
   npm install
   ```

3. **Deploy manually:**
   ```bash
   npm run deploy
   ```

4. **Enable GitHub Pages:**
   - Go to `Settings` → `Pages`
   - Source: Select `Deploy from a branch`
   - Branch: Select `gh-pages` and `/(root)`
   - Save

5. **Access your site:**
   - Your site will be available at: `https://YOUR_USERNAME.github.io/your-repo-name/`

## Environment Variables

The application uses the following environment variables:

- `GEMINI_API_KEY` - Your Gemini API key for AI features

## Tech Stack

- **Framework:** React 19.2.3
- **Language:** TypeScript 5.8.2
- **Build Tool:** Vite 6.2.0
- **Styling:** Tailwind CSS (CDN)
- **Icons:** Material Icons & Material Symbols
- **Fonts:** Google Fonts (Inter)

## Project Structure

```
breb-smart-meter-payment/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions workflow
├── screens/
│   ├── Home.tsx                # Home screen
│   ├── CustomerDetails.tsx     # Customer details entry
│   ├── AmountEntry.tsx         # Amount entry screen
│   ├── BillSummary.tsx         # Bill summary screen
│   ├── PinEntry.tsx            # PIN entry screen
│   ├── PaymentSuccess.tsx      # Success confirmation
│   └── Loading.tsx             # Loading screen
├── App.tsx                     # Main app component
├── index.tsx                   # Entry point
├── types.ts                    # TypeScript types
├── constants.tsx               # App constants
├── index.html                  # HTML template
├── vite.config.ts              # Vite configuration
├── tsconfig.json               # TypeScript configuration
├── package.json                # Dependencies
└── .env.local                  # Environment variables

```

## Troubleshooting

### Blank page after deployment
- Check the `base` path in `vite.config.ts` matches your repository name
- Ensure GitHub Pages is enabled and pointing to the correct source

### API Key issues
- For local development: Update `.env.local`
- For GitHub Pages: Add `GEMINI_API_KEY` to repository secrets

### 404 errors for assets
- Verify the `base` path in `vite.config.ts` is correct
- Clear browser cache and try again

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is open source and available under the MIT License.

## Contact

For questions or support, please open an issue in the GitHub repository.

---

Built with React, TypeScript, and Vite. Deployed on GitHub Pages.
