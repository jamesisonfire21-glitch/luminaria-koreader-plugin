# Luminaria Sync — KOReader Plugin

Sync your KOReader highlights to [Luminaria](https://luminaria.uk) — a private, beautiful web app for browsing your reading highlights by book, with full-text search, favourites, and export to PDF, Notion and Obsidian.

---

## What it does

- **Manual sync** — tap *Sync highlights now* in the menu and your highlights upload to Luminaria in seconds
- **Auto-sync on WiFi** *(paid feature)* — when your device connects to WiFi, the plugin automatically exports and syncs your highlights silently in the background. If a book is open while the sync runs, no notification is shown so your reading isn't interrupted
- **Smart change detection** — the plugin hashes your highlights before uploading. If nothing has changed since the last sync, the upload is skipped automatically to save battery and bandwidth

---

## Sync limits

| Plan | Manual syncs | Auto-sync |
|------|-------------|-----------|
| Free | 2 per week | Not included |
| Premium (£2.99/mo) | Unlimited | ✓ Included |

The weekly limit resets every Monday. If you hit the limit, the plugin will show a message prompting you to upgrade. Auto-syncs that find no new highlights don't count against the limit.

---

## Installation

1. Download this repository as a ZIP
2. On your Kobo, navigate to:
   ```
   mnt/onboard/.adds/koreader/plugins/
   ```
3. Create a folder called `luminaria.koplugin`
4. Copy `main.lua` and `_meta.lua` into the folder
5. Restart KOReader fully

The plugin will appear under **Menu → Tools → Luminaria Sync**.

---

## Setup

1. Get a free sync token at [luminaria.uk/signup](https://luminaria.uk/signup)
2. In KOReader go to **Menu → Tools → Luminaria Sync → Link device (6-digit code)**
3. Go to [luminaria.uk/link](https://luminaria.uk/link) on your computer, enter your token, and get a 6-digit code
4. Enter the code on your device to link it automatically

Alternatively, enter your token manually via **Menu → Tools → Luminaria Sync → Settings**.

---

## Syncing your highlights

### Manual sync

Tap **Menu → Tools → Luminaria Sync → Sync highlights now**

The plugin will export all highlights from your reading history and upload them. You'll see:

- *Exporting highlights…*
- *Syncing N highlights from N books…*
- *✓ Synced!* — or a rate limit message if you've used both syncs for the week

Free users are limited to **2 manual syncs per week**. Upgrade to Premium for unlimited syncs.

### Auto-sync on WiFi (Premium — £2.99/month)

With an active subscription, every time your device connects to WiFi the plugin automatically syncs your highlights in the background. If you're reading when the sync runs, no notification is shown — it happens completely silently.

To enable: subscribe at [luminaria.uk/upgrade](https://luminaria.uk/upgrade), then toggle **Auto-sync on WiFi** in the plugin menu.

---

## Viewing your highlights

1. Open [luminaria.uk](https://luminaria.uk) in any browser
2. Enter your token in the toolbar
3. Tap **↻ Sync from KOReader** to pull your latest highlights

Your highlights appear organised by book, with full-text search, favourites, and export to PDF, Notion and Obsidian.

---

## Menu options

| Option | Description |
|--------|-------------|
| Sync highlights now | Manually export and sync all highlights |
| Link device (6-digit code) | Link your device to your token via luminaria.uk/link |
| Auto-sync on WiFi | Toggle automatic background sync on WiFi connect (paid) |
| Settings | Configure your token and export folder |
| About | Plugin info and links |

---

## Settings

| Setting | Default | Description |
|---------|---------|-------------|
| Upload Token | *(empty)* | Your personal token from luminaria.uk |
| Highlights export folder | `/mnt/onboard/.adds/koreader/clipboard/` | Where exported .md files are saved locally |
| Auto-sync on WiFi | true | Whether to auto-sync when WiFi connects (paid only) |

---

## Supported devices

Tested on Kobo Libra with KOReader. Should work on any Kobo device running KOReader. May also work on Kindle and other devices running KOReader but has not been tested.

---

## Links

- [Luminaria](https://luminaria.uk)
- [Get a free token](https://luminaria.uk/signup)
- [Upgrade for unlimited sync](https://luminaria.uk/upgrade)
- [KOReader](https://koreader.rocks)
