# Qyntel Technologies — Home

Single-file static homepage for Qyntel Technologies (the parent brand behind QureQ, GoVoiceQ, ConnectQ, and MyVoicz).

Everything — fonts links aside — is self-contained in `index.html`: all logos are embedded as base64, so there are no external image files and no build step.

## Deploy on Render

This repo includes a `render.yaml`, so Render can deploy it automatically as a Blueprint:

1. Push this repo to GitHub (see commands below).
2. In the Render dashboard: **New → Blueprint**.
3. Select this repo. Render reads `render.yaml` and creates the static site automatically.
4. Once live, go to **Settings → Custom Domains** and add `qyntel.in`.
5. Add the CNAME/A record Render gives you to your domain's DNS.

If you'd rather set it up manually instead of using the Blueprint: **New → Static Site**, connect this repo, leave Build Command blank, set Publish Directory to `.`.

## Push this repo to GitHub

```bash
cd qyntel-home-repo
git init
git add .
git commit -m "Qyntel Technologies homepage"
git branch -M main
git remote add origin https://github.com/Qyntel/qyntel-home.git
git push -u origin main
```

(Create the empty `Qyntel/qyntel-home` repo on GitHub first, then run the above from inside this folder.)
