# Media Tracker

I often watch multiple TV shows at the same time—some weekly, some slowly, some paused and resumed months later. Keeping track of where I left off, what I’m actively watching, and what’s finished became harder than it should be. This project is a small [web app](https://kcandost.github.io/tv-show-tracker/) I built to solve that problem.

The goal was to keep it simple, fast, and private.

<p align="center">
  <img src="https://github.com/kcandost/media-tracker/blob/main/ss.png?raw=true" alt="Screenshot" width="900" />
</p>



---

## What it does

- Search TV shows using the TVMaze API  
- Add shows to a personal list  
- Track progress by season and episode  
- See completion percentage and episodes remaining  
- Organize shows into Not Started, In Progress, and Completed  
- View upcoming episode air dates (when available)  
- Store where you’re watching a show (platform or URL)  
- Toggle between dark and light themes  

The entire app runs as a single static page.

---

## Privacy and data ownership

This app is designed so that each user fully owns their data.

- There is no shared database  
- Your watch history is not visible to anyone else  
- All data lives in your own Supabase project  
- GitHub login is used for authentication  
- Row Level Security ensures users can only access their own rows  

Even though the app itself is public, your data remains private.

---

## How it works

- Frontend: React (UMD), no build step  
- TV data: TVMaze public API  
- Backend: Supabase (PostgreSQL + Auth)  
- Auth: GitHub OAuth  
- Hosting: GitHub Pages  

---

## Using this project

This repository is meant to be forked and reused.

At a high level:
1. Fork the repo  
2. Create a Supabase project  
3. Run the provided SQL to create the table and security rules  
4. Enable GitHub OAuth in Supabase  
5. Deploy to GitHub Pages  
6. Open the site, paste your Supabase credentials once, sign in, and start using it  

Each fork uses its own database and authentication.

---

## Current limitations

- Assumes episodes are watched in order  
- Progress is approximated across seasons  
- No notifications yet  
- Minimal UI by design  
- No offline support  

This is intentionally a focused tracker, not a full media management system.

---

## Possible improvements

- Episode or season notifications  
- Watch-time statistics and summaries  
- Notes or personal ratings  
- Tags or custom categories  
- Multi-profile support  
- Mobile UI polish  
- Build step (Vite) for better performance  
- More accurate episode progress tracking  

---


