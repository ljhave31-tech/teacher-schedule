# Connect Teacher Schedule to Firebase

Until you finish this, the app still works and saves on each device only. Once it is connected, teachers and HR share live data.

## 1. Create the project
1. Go to https://console.firebase.google.com and click **Create a project**. Google Analytics is not needed.
2. On the project home page, click the **</>** (Web) icon, give the app a name, and register it. Skip Firebase Hosting.
3. Copy the `firebaseConfig` values it shows you into **firebase-config.js** (replace every `PASTE_...`).

## 2. Turn on sign-in (anonymous)
**Build → Authentication → Get started → Sign-in method → Anonymous → Enable → Save.**
The app signs each device in quietly, with no login screen.

## 3. Create the database
**Build → Firestore Database → Create database.**
- Pick a location close to your users, for example `asia-southeast1` (Singapore). The location cannot be changed later.
- Start in **production mode**.

## 4. Add the security rules
Open the **Rules** tab, replace everything with the contents of **firestore.rules**, and click **Publish**.

## 5. Upload and test
Upload the changed files to GitHub (at least `index.html`, `firebase-config.js`, `sw.js`). Open the site, enter a name, open a few slots, then check **Firestore Database → Data**. You should see `teachers`, and later `assignments` and `hr`.
The small label at the top right of the app shows **Saved** or **Live** when it is connected, and **This device** when it is not.

## 6. Protect your key (recommended)
The Firebase key is not a secret, but you can limit where it works.
Google Cloud Console → **APIs & Services → Credentials** → the *Browser key* → **Application restrictions: Websites** → add `https://YOUR-NAME.github.io/*`.

## Good to know
- The free Spark plan is plenty for a small team.
- Anyone who opens the site is signed in anonymously and can read and write the data, and HR is chosen by typing the name Reizsa. This is fine for a trusted team, but it is not private. Real logins for teachers and HR are the next upgrade.
- If devices keep showing an old version after you upload changes, change `teacher-schedule-v2` to `v3` in `sw.js`.
