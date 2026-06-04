# Chirp AI — Background Sync

This repo's only job is a GitHub Actions workflow that pings the Chirp AI
`/api/cron` endpoint every 5 minutes. That endpoint:

1. Syncs every connected user's Google Calendar
2. Auto-sends the **Chirp AI** bot to meetings starting now
3. Fetches transcripts for finished meetings and stores them in Supabase

It runs server-side with no one logged in. No app code or secrets live here —
the cron URL and shared secret are stored as GitHub Actions **secrets**.

To run it on demand: **Actions → Chirp AI Background Sync → Run workflow**.
