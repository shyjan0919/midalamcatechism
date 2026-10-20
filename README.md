St. Joseph's Faith — Admin foundation (early build)

Upload these files to the ROOT of the GitHub Pages repository:
- index.html
- sw.js
- manifest.webmanifest
- midalam-logo.png

firestore.rules is provided separately for publishing in Firebase Console > Firestore Database > Rules.

IMPORTANT: Do not publish the rules until the first admin profile is seeded:
1. Firebase Console > Authentication > Users > open your admin user and copy the UID.
2. Firestore Database > Data > Start collection:
   Collection ID: users
   Document ID: paste that exact Authentication UID
   Field: role (string) = admin
   Optional field: email (string) = your account email
3. After the document exists, publish firestore.rules from this package.
4. Refresh/sign out and sign back in. The badge should say ADMIN and Admin navigation should appear.

The first admin document must be created manually in Firebase Console because the client must not be allowed to promote itself. Never create a public rule that allows anyone to write users/{uid} or set role=admin.

This build adds admin-role lookup and basic class record create/list functionality. It does NOT yet implement student records, teacher creation/assignment, attendance, QR scanning, geofence enforcement, leave approvals, or live reports. Keep student data out of the app until those collections have dedicated tested rules.
