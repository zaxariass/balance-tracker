# Balance Tracker (local-only, move data with LocalSend)

No server, no accounts. Each device keeps its own data; you move one JSON file between them.

## 1. Host the app (once)
Put this folder on any static HTTPS host, e.g. GitHub Pages (repo → Settings → Pages). The page contains no data, only code.
Use the same URL on all three devices.

## 2. Install
- **Android (Chrome):** open the URL, then ⋮ → Install app.
- **Arch / Zorin (Chrome, Chromium or Edge):** open the URL, then click the install icon in the address bar. (Firefox works as a normal tab but can't install it.)

Everything works offline after the first visit.

## 3. Moving data
1. On the device you just used, tap **Export**.
   - Android opens the share sheet: choose **LocalSend**.
   - On a PC the file `balance-tracker.json` downloads: send it with LocalSend.
2. On the other device, accept the file in LocalSend, then in the app tap **Import** and pick it.
3. Choose **Replace** (device becomes identical to the file) or **Merge** (adds only transactions/groups missing here).

The import dialog shows when the file and this device were last changed and warns if the file is older than your data.

## Tips
- Work on one device, then send; don't edit on two devices between transfers. If you did, use **Merge** on one of them, then Export from it and **Replace** on the others.
- Merge can't tell a deleted transaction from a missing one: anything you reverted here but still exists in the file comes back.
- Browser data is per site and per browser. Clearing site data erases the app's data, so Export now and then as a backup.
