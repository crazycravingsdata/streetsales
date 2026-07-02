# 🚐 Crazy Cravings — Street Sales Manager

Internal web platform for managing daily street sales across all Crazy Cravings vehicles.

---

## 🔗 Access

> **[Open Street Sales Manager →](https://YOUR-USERNAME.github.io/crazycravings-streetsales/)**

Password: `crazy@admin`

---

## ✨ Features

- **Dashboard** — Total revenue, current month summary, active vehicles count, average per entry, monthly bar chart and per-vehicle donut chart
- **Entries** — Log multiple sales per day per vehicle, with optional location (school, park, event, etc.), filter by vehicle or month, and delete entries
- **Vehicles** — Add, rename, activate/deactivate or delete vehicles dynamically — no fixed list

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML + CSS + Vanilla JS (single file) |
| Database | Firebase Firestore |
| Hosting | GitHub Pages |
| Charts | Chart.js 4 |

---

## 🗄 Firebase Collections

| Collection | Description |
|---|---|
| `streetSalesVehicles` | Registered vehicles (name, active status, createdAt) |
| `streetSalesEntries` | Daily sales entries (date, vehicleId, vehicleName, amount, location) |

Uses the same Firebase project as the other Crazy Cravings internal apps (`crazy-cravings-data`).

---

## 🚀 Deployment (GitHub Pages)

1. Create a new repository named `crazycravings-streetsales`
2. Upload `index.html` to the root
3. Go to **Settings → Pages**
4. Set source to **Deploy from a branch → main → / (root)**
5. Save — the app will be live at `https://YOUR-USERNAME.github.io/crazycravings-streetsales/`

> Update the access URL at the top of this README after deployment.

---

## 🔒 Firebase Firestore Rules

Make sure the following collections are allowed in your Firestore rules:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /streetSalesVehicles/{doc} {
      allow read, write: if true;
    }
    match /streetSalesEntries/{doc} {
      allow read, write: if true;
    }
  }
}
```

---

## 📦 Related Apps

| App | Repository |
|---|---|
| 🧾 Invoice & Quote Manager | `crazycravings-app` |
| ⏱ Employee Timesheet | `crazycravings-timesheet` |
| 🚐 Street Sales Manager | `crazycravings-streetsales` ← you are here |

---

*Crazy Cravings — Mobile Ice Cream Parlour · Ontario, Canada*  
