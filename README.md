# Family Secret Santa

A small web app for running a Secret Santa draw. Everyone adds their own name and wish list, the organizer runs the draw, and each person sees who they drew along with that person's wish list.

It is a static page (`index.html`) hosted on GitHub Pages, with a free Firebase Firestore database storing names, wish lists and the draw.

## Setup

1. Create a Firebase project and a Firestore database, then paste the web app config into `FIREBASE_CONFIG` in `index.html`.
2. Set `ORGANIZER_CODE` in `index.html` to a code only you know.
3. In Firestore **Rules**, allow reads and writes (see below) and publish.
4. Upload `index.html` to a public GitHub repo and enable **Settings → Pages** (deploy from `main`, `/ (root)`).

Firestore rules for a small, trusted group:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```

## Using it

- **Join:** enter your name, a 4-digit PIN and your wish list. Use the same name and PIN to edit later.
- **Organizer:** unlock with the organizer code, add optional "don't draw each other" pairs, and run the draw once everyone has joined.
- **My match:** pick your name, enter your PIN, and see who you're buying for.

## Privacy

PINs and wish lists are stored as plain text and the database is open to anyone with the site's config. That is fine for a family gift exchange, but don't use it for anything sensitive. Anyone technical could read the draw, and so could the organizer.
