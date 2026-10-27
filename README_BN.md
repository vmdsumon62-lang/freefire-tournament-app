# Free Fire Tournament App — Starter

এটি Flutter দিয়ে তৈরি একটি cross-platform starter UI। Android, iOS এবং Web-এর জন্য Flutter থেকে build করা যায়।

## এই সংস্করণে আছে
- Tournament home screen
- Solo / Duo / Squad demo tournament
- Join button ও joined list
- Local result list
- Local-only admin demo mode: tournament create, room details, result publish
- SharedPreferences দিয়ে একই ডিভাইসে local persistence

## গুরুত্বপূর্ণ সীমাবদ্ধতা
এটি এখনো production-ready tournament service নয়। ডেটা শুধু একই ডিভাইসে থাকে; অন্য ব্যবহারকারী দেখতে পাবে না। Admin mode নিরাপদ নয়, কারণ login/role security নেই। কোনো payment, wallet withdrawal, real-time room delivery, push notification বা online database যুক্ত করা হয়নি। Room password public build-এ প্রকাশ করার আগে নিরাপদ backend ও access rules দরকার।

## প্রয়োজনীয় সফটওয়্যার
1. Flutter SDK
2. Android Studio (Android SDK সহ)
3. VS Code ঐচ্ছিক
4. Play Store প্রকাশের জন্য Google Play Console account

## চালানোর নিয়ম
টার্মিনালে project folder-এ গিয়ে:
```bash
flutter pub get
flutter run
```

## Web build
```bash
flutter config --enable-web
flutter build web
```
`build/web` folder একটি static hosting service-এ deploy করতে হবে।

## Android build
```bash
flutter build apk --release
```
Play Store-এর জন্য সাধারণত Android App Bundle:
```bash
flutter build appbundle --release
```

## iOS build
iOS build/signing-এর জন্য macOS ও Xcode প্রয়োজন:
```bash
flutter build ios --release
```

## পরের ধাপ: production backend
- Firebase Authentication (user sign-in)
- Cloud Firestore (tournaments, registrations, results)
- Firebase Security Rules (admin-only actions)
- Firebase App Check, abuse protection, server-side validation
- Privacy policy, support contact, data deletion/account deletion flow
- Payment/prize handling-এর আগে স্থানীয় আইন এবং Google Play policy যাচাই

## Free Fire trademark/assets
এটি fan-made, unofficial project। Garena-র অনুমোদন আছে এমন দাবি করবেন না। অনুমতি ছাড়া official logos, artwork বা game assets ব্যবহার করবেন না।
