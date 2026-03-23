# AKS Pilot Ops

Part 135 pilot operations dashboard for Alaska Seaplanes — flight/duty compliance, crew qualifications, weather overlay, and operational stats.

## Deploy to Vercel (5 minutes)

### Step 1 — Push to GitHub
```bash
git init
git add .
git commit -m "Initial deploy"
# Create a new repo at github.com, then:
git remote add origin https://github.com/YOUR_USERNAME/aks-pilot-ops.git
git push -u origin main
```

### Step 2 — Deploy on Vercel
1. Go to [vercel.com](https://vercel.com) → **Continue with GitHub**
2. Click **Add New Project** → import `aks-pilot-ops`
3. Framework: **Vite** (auto-detected)
4. Click **Deploy**

That's it. Your URL will be `https://aks-pilot-ops.vercel.app` (or similar).

### Step 3 — Add to Home Screen (iOS)
Open the Vercel URL in Safari → Share → **Add to Home Screen** → it behaves like a native app.

## Local Dev
```bash
npm install
npm run dev
```

## Data Storage
Each device stores data in its own `localStorage`. Import a fresh flight log export daily via the IMPORT tab. The bulk drop zone accepts all three files at once:
- `Flight_Log_Export.xlsx`
- `Pilot_Status_Board.xlsx`  
- `Pilot_Aircraft_Board.xlsx`

## Notes
- No backend required — fully static
- All data stays on-device (localStorage)
- For shared data across devices → Supabase integration planned
