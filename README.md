# AMBO Field — the agents' app

Same shape as the responder repo. A separate GitHub repository, because it builds a
separate APK with its own app id (`ng.ambodesk.field`), so both can sit on one phone.

## Set it up

1. New repository. Upload `index.html`, `package.json`, `capacitor.config.json`,
   `.gitignore` and the `android-icons` folder.
2. The workflow lives in a hidden folder, so use **Add file → Create new file** and type
   the path `.github/workflows/build-apk.yml`, then paste the contents in.
3. **Settings → Secrets and variables → Actions** — add `AMBO_BACKEND_URL` (your
   `/exec` URL) and `AMBO_SECRET`. The build injects them, so agents never type them.
4. Push. **Actions** builds `AMBO-Field-APK` in about five minutes.

## What agents need

Nothing but the APK and their phone number on the Agents list. It arrives already
pointed at your desk.

Grant **location** when it asks, and **camera** the first time they attach a photo.
Neither is required to file a report — both make the report more useful.

## Adding agents

Dashboard → **Control centre → Field agents → Add agent**. Phone number, name, and
whether they cover one polling unit, a ward, or a whole LGA.

The first handset to use a number claims it. If someone changes phone, press
**Release** on their row.
