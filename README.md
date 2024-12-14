# Intermittent Firebase Realtime Database Quota Exceeded Error

This repository demonstrates a bug where the Firebase Realtime Database throws a `FirebaseError: Quota exceeded` error even when the project's usage is well below the free tier limits. The error is intermittent and difficult to reproduce consistently.

## Bug Description

The application uses the Firebase Realtime Database to store and retrieve data.  Intermittently, it throws a `Quota exceeded` error despite showing significantly low usage in the Firebase console.  No obvious pattern or trigger has been identified.

## Solution

While the root cause remains elusive, implementing more robust error handling and potentially adjusting database rules for read/write optimizations have mitigated the issue.

## How to reproduce (Not Guaranteed):

1. Set up a Firebase project.
2. Clone this repository.
3. Run `npm install`.
4. Configure Firebase credentials in `firebase.js`.
5. Run `node bug.js` repeatedly. Observe the console and Firebase console usage. 

The error may or may not appear. It is particularly tricky to reproduce.