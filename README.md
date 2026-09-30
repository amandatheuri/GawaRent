# GawaRent
A ReactNative roommate matching app to help people match with potential roommates.
# GawaRent — Full-Stack Roommate Matching Platform

> **GawaRent** is an aesthetic, full-stack React Native mobile app designed for the Kenyan market (students and young professionals). It solves roommate matching and house-finding pain points by eliminating expensive third-party broker fees and connecting verified room seekers and hosts directly.

---

## Highlights & UI Design
* **TikTok-Style Snap Feed:** Full-screen vertical scrolling for roommate profiles.
* **Claymorphism Aesthetic:** Modern, UI featuring custom soft pastel theme system.
* **Real-Time In-App Chat:** Safe, private 1-on-1 messaging powered by WebSockets (Socket.IO).
* **Compatibility Engine:** Algorithmic compatibility scoring based on lifestyle choices, habits, and budgets.
* **Privacy-First Design:** Direct user contact information is kept hidden on public feeds to prevent spam.

---

## 🛠️ Tech Stack & Architecture

### **Frontend (Mobile)**
* **Framework:** React Native (Expo)
* **Real-Time Layer:** Socket.IO Client
* **Chat UI:** React Native Gifted Chat
* **Styling:** Custom Claymorphism Design System (React Native StyleSheet)

### **Backend (API & Database)**
* **Runtime:** Node.js & Express.js
* **Database:** MongoDB Atlas (Mongoose ODM)
* **Real-Time Engine:** Socket.IO Server
* **Media Handling:** Cloudinary API

---

## System Architecture & Database Schema

```text
┌──────────────┐         REST API / HTTP        ┌──────────────┐
│  React Native│ ─────────────────────────────> │  Node.js /   │
│   Expo App   │ <───────────────────────────── │ Express API  │
└──────┬───────┘                                └──────┬───────┘
       │                                               │
       │               WebSockets                      │ Database
       └─────────── < Socket.IO > ─────────────────────┼────────────┐
                                                       ▼            ▼
                                                ┌────────────┐ ┌────────────┐
                                                │ MongoDB    │ │ Cloudinary │
                                                │ Atlas DB   │ │ Image Storage
                                                └────────────┘ └────────────┘
