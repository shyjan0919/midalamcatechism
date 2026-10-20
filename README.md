St. Joseph's Faith — Teacher Profile Module (early build)

Replace these files in the ROOT of the GitHub Pages repository:
- index.html
- sw.js (cache version may be updated below)
- manifest.webmanifest
- midalam-logo.png

Publish firestore.rules in Firebase Console > Firestore Database > Rules.

This module adds teacher profile records (name, email, one assigned class/group) to Firestore. It does NOT create Firebase Authentication accounts, send invitations, or grant teacher access to student records. Do not treat a saved teacher profile as an authorized login.

Security setup already assumed:
- A Firestore document users/{your Firebase Auth UID} exists with role="admin".
- The published rules verify admin role using that document.
- Only admins can read/write teacher profiles and manage classes.
- All other collections remain denied.

After publishing rules and uploading files, sign in as admin, open Teachers, add a test profile, then verify it appears in Registered teacher profiles. Do not enter passwords into the teacher form.
