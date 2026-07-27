# MoHealth 🏥

**A health and wellness mobile app — appointment booking on an Expo client, backed by a Node.js API.**


---

## What it does

A React Native mobile client for browsing practitioners, booking appointments and tracking wellness data, talking to an Express + MongoDB backend.

---

## Stack

**Mobile client** (`mobile/`)
- Expo SDK 51 + Expo Router 3 (file-based routing)
- React Native 0.74, TypeScript
- React Navigation
- `@react-native-community/datetimepicker` — appointment slot selection
- AsyncStorage for local persistence
- Axios for API calls

**Server** (`server/`)
- Node.js + Express (ESM)
- MongoDB via Mongoose
- JWT auth with bcrypt
- `express-validator` + `validator` for input validation
- Moment for date handling
- OpenAI integration
- Swagger (`swagger-jsdoc` + `swagger-ui-express`) at `/api-docs`

---

## Repository layout

```
mohealth/
├── mobile/     # Expo / React Native client
└── server/     # Express API
```

---

## Running locally

**Prerequisites:** Node.js 18+, Expo CLI, a MongoDB database.

```bash
git clone https://github.com/vincedotcode/mohealth.git
cd mohealth
```

**Server**

```bash
cd server
npm install
cp .env.example .env
npm run dev
```

```bash
MONGODB_URI=
JWT_SECRET=
PORT=8080
OPENAI_API_KEY=
```

API docs at `http://localhost:8080/api-docs`.

**Mobile client**

```bash
cd ../mobile
npm install
npm start
```

Scan the QR code with Expo Go, or press `i` / `a` for a simulator.

```bash
EXPO_PUBLIC_API_URL=
```

---

## ⚠️ Attribution — action required

`server/package.json` currently contains:

```json
"description": "ApexBooking Health is a Doctor Appointment Booking App.",
"author": "Haris Mohanty",
"repository": "git+https://github.com/Haris-Mohanty/ApexBooking-Health.git",
"homepage": "https://github.com/Haris-Mohanty/ApexBooking-Health#readme",
"bugs": { "url": "https://github.com/Haris-Mohanty/ApexBooking-Health/issues" }
```

The backend is derived from [Haris-Mohanty/ApexBooking-Health](https://github.com/Haris-Mohanty/ApexBooking-Health). Leaving this in place while presenting the repo as your own work is the kind of thing a reviewer will notice, and it costs you more credibility than the repo earns you.

**Pick one before making this repo prominent:**

1. **Credit it properly.** Keep the code, replace the section above with a clear "the backend is adapted from ApexBooking-Health by Haris Mohanty, used under its licence" note, and check what that licence actually requires. Update the `author` field to reflect the adaptation rather than deleting the origin.
2. **Replace the backend.** Write your own API against the same client. You've done exactly this in MoTalent and MoKidSafe, so it isn't new ground.
3. **Take the repo private**, or delete it, if it isn't worth either of the above.

What you should not do is quietly strip the metadata — the git history still shows it, and a stripped attribution reads worse than an honest one.

---

## Contact

Vince Erkadoo — [vincedotcode.com](https://vincedotcode.com) · [vince@vincedotcode.com](mailto:vince@vincedotcode.com)
