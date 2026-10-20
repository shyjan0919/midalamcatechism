St. Joseph’s Faith — Firebase sign-in build

Files: index.html, manifest.webmanifest, sw.js, midalam-logo.png.

This build connects the existing login form to Firebase Authentication (Email/Password) and password-reset email. It does NOT yet connect student records, Firestore, roles, QR scanning, geofence enforcement, leave approvals, or reports to a live database.

Deploy all files together to the existing GitHub Pages repository. Keep Firestore rules deny-all until role and access rules have been reviewed and tested. Do not enter real student information in this early build.
