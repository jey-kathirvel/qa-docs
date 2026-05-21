# Mobile Testing Checklist

Use this checklist to validate functionality, UI/UX, performance, and compatibility during mobile app testing.

---

## 1. Installation & Setup

- [ ] App installs successfully on supported OS versions (Android, iOS). [web:101][web:107]  
- [ ] App icon and name display correctly on the home screen.  
- [ ] First‑time launch shows onboarding / welcome screens as expected.  
- [ ] Permissions (camera, location, contacts, notifications) are requested and handled correctly. [web:104][web:110]  

---

## 2. Basic Functionality

- [ ] Core user flows work end‑to‑end (e.g., login, search, checkout, profile edit). [web:104][web:106]  
- [ ] Buttons, links, and gestures respond with appropriate feedback.  
- [ ] Forms validate input and show clear error messages.  
- [ ] Data is correctly saved and displayed between screens and sessions. [web:101][web:107]  

---

## 3. UI & UX

- [ ] Layout adapts to different screen sizes and orientations (portrait / landscape). [web:103][web:109]  
- [ ] Text is readable and not truncated or overlapping.  
- [ ] Icons, images, and touch targets are crisp and sized appropriately for mobile. [web:104][web:107]  
- [ ] Navigation (tabs, bottom nav, side menu) is consistent and intuitive.  

---

## 4. Device & OS Compatibility

- [ ] App runs on a matrix of devices and OS versions (e.g., latest and 1–2 older versions). [web:103][web:107]  
- [ ] Behavior is consistent across low‑end and high‑end devices.  
- [ ] Orientation changes do not crash the app or reset state.  
- [ ] Keyboard and soft‑input layout do not overlap key fields. [web:104][web:110]  

---

## 5. Network & Connectivity

- [ ] App works on Wi‑Fi, 4G/5G, and 3G (if supported). [web:103][web:106]  
- [ ] App gracefully handles poor or no network (offline states, retry options).  
- [ ] Critical screens show loading states during data fetch.  
- [ ] Large downloads do not block UI or consume excessive data without warning.  

---

## 6. Performance & Stability

- [ ] App starts within acceptable time on cold and warm start. [web:101][web:110]  
- [ ] Screen transitions and interactions feel smooth (no lag or jank).  
- [ ] App does not crash under normal usage or after rapid navigation.  
- [ ] Memory and CPU usage are within acceptable limits. [web:104][web:106]  

---

## 7. Background & Foreground Behavior

- [ ] App resumes correctly after coming back from background.  
- [ ] Notifications open the correct screen when tapped.  
- [ ] In‑app interruptions (phone call, messaging, notifications) do not corrupt flow.  
- [ ] App state is preserved where relevant (e.g., cart, form progress). [web:103][web:107]  

---

## 8. Security & Data

- [ ] Sensitive data (tokens, passwords) is not logged or exposed in UI. [web:105][web:108]  
- [ ] Storage (local cache, files, keychain/SharedPrefs) is secure and cleared on logout. [web:102][web:105]  
- [ ] Deep links and social logins redirect correctly and securely.  
- [ ] Jailbroken / rooted device detection (if applicable) works as designed. [web:102][web:108]  

---

## 9. Accessibility & Usability

- [ ] App supports basic accessibility features (screen reader, large text, voice commands). [web:101][web:109]  
- [ ] Color contrast and font size are usable for most users.  
- [ ] Touch targets are large enough for thumb navigation.  
- [ ] Voice‑assisted navigation (if any) behaves as expected.  

---

## 10. Regression & Exploratory

- [ ] Core flows are re‑tested after each build change. [web:104][web:107]  
- [ ] Random navigation and rapid tapping do not trigger unexpected behavior.  
- [ ] Upgrade from previous version preserves data and settings (if upgrade‑testing is in scope).  

---

## 11. Test Coverage Table (Optional)

Example table to track per device / OS:

| Device / OS            | Installation | Core Flows | UI/UX | Network | Performance | Security | Notes |
|------------------------|------------|------------|-------|---------|------------|----------|-------|
| Android 14 (Pixel)     | ✅         | ✅         | ✅    | ✅      | ✅         | ✅       | [e.g., “All good”] |
| Android 13 (Samsung)   | ✅         | ✅         | ✅    | ✅      | ⏳         | ✅       | [e.g., “Minor lag in image gallery”] |
| iOS 17 (iPhone 14)     | ✅         | ✅         | ✅    | ✅      | ✅         | ✅       | [e.g., “Ready for UAT”] |
| iOS 16 (iPhone 13)     | ✅         | ✅         | ✅    | ✅      | ✅         | ✅       | [e.g., “Minor spacing issue in profile card”] |
