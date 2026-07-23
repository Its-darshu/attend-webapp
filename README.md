# Attend — iOS Web App (CS&E VII, Section A & B)

Attendance tracker that iPhone users install from **Safari → Share → Add to Home Screen**.
No App Store, no Apple Developer account needed. All data stays on the phone (localStorage) — no server, works offline after first load.

## Features
- First launch: choose **Section A** or **Section B** → that section's timetable is loaded
- Dashboard: overall attendance %, pending "did you attend?" prompts (✓/✗), today's classes, per-subject stats
- Timetable: view/add/edit/delete classes per weekday
- Calendar: 2026 academic holidays pre-loaded; tap any date to mark holiday/working; default weekday toggles
- History: every record with subject/status filters; tap to correct
- Installable PWA: offline support, standalone full-screen on iOS home screen

## Put it online (GitHub Pages)

```bash
cd webapp-ios
gh repo create attend-webapp --public --source=. --push
# or manually:
#   create an empty repo "attend-webapp" on github.com, then:
#   git remote add origin git@github.com:Its-darshu/attend-webapp.git
#   git push -u origin main
```

Then on GitHub: **Settings → Pages → Branch: `main` / root → Save.**
Your app goes live at: `https://its-darshu.github.io/attend-webapp/`

Share that link with classmates — on iPhone they open it in **Safari**, tap **Share → Add to Home Screen**, and it behaves like an app.

## Limitation to know
iOS does not let a web app fire scheduled local notifications on its own (that needs a push server).
So unlike the Android APKs, the web app shows pending attendance prompts **when opened**, not at class time.

## Switching section
Calendar tab → "Switch section / reset" (erases local data and shows the picker again).
