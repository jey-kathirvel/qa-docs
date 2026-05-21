# Cross Browser Testing Checklist

Use this checklist to validate UI and behavior across target browsers and devices.

---

## 1. Browser & Environment Setup

- [ ] List of browsers and versions to test (e.g., Chrome, Firefox, Safari, Edge, mobile Safari, Chrome Mobile). [web:94][web:97]  
- [ ] Operating systems covered (Windows, macOS, Linux, iOS, Android).  
- [ ] Emulators/simulators and real devices prepared for mobile testing.  
- [ ] Test on all supported resolutions (desktop, tablet, mobile breakpoints). [web:91][web:99]  

---

## 2. Layout & Responsiveness

- [ ] Page layout renders correctly on each browser (no broken grids or misaligned elements). [web:91][web:94]  
- [ ] No horizontal overflow or unwanted scrollbars.  
- [ ] Content re‑flows properly on various viewport sizes (desktop, tablet, mobile). [web:99][web:97]  
- [ ] Zoom in / zoom out does not break the layout.  

---

## 3. Text & Styling

- [ ] Fonts, sizes, and colors render consistently across browsers. [web:91][web:94]  
- [ ] Text is not cut off, overlapping, or misaligned.  
- [ ] Line heights and spacing look comfortable and readable.  
- [ ] CSS effects (shadows, rounded corners, transitions) are consistent. [web:91][web:99]  

---

## 4. Forms, Inputs & Interactions

- [ ] Text fields, dropdowns, checkboxes, and radio buttons align correctly. [web:91][web:96]  
- [ ] Placeholders, labels, and validation messages are visible and readable.  
- [ ] Hover, focus, and active states work as expected.  
- [ ] Tooltips and popups appear in the correct position and are not blocked. [web:91][web:96]  

---

## 5. Links, Buttons & Navigation

- [ ] All links navigate to the correct pages or anchors.  
- [ ] Buttons are clickable and respond with visual feedback.  
- [ ] Menu items, breadcrumbs, and pagination work correctly. [web:91][web:94]  
- [ ] Back / forward / refresh behavior is consistent across browsers.  

---

## 6. Media & Assets

- [ ] Images and icons load and display without distortion. [web:91][web:99]  
- [ ] Videos and embedded media (if any) play correctly.  
- [ ] Broken images or missing assets do not appear.  
- [ ] Image alt‑text and accessibility cues are preserved.  

---

## 7. Functionality & Behavior

- [ ] Core features (e.g., login, search, checkout) work the same in all browsers. [web:95][web:97]  
- [ ] Ajax / dynamic content loads and updates correctly. [web:91][web:94]  
- [ ] File upload / download works without errors.  
- [ ] Sessions and cookies behave consistently across browsers. [web:91][web:99]  

---

## 8. Performance & Load

- [ ] Page loads within acceptable time limits on each browser. [web:95][web:97]  
- [ ] No excessive CPU or memory usage in long‑running views.  
- [ ] Long‑running operations show loading states until complete.  

---

## 9. Accessibility & Usability

- [ ] Color contrast and text size are usable on all browsers and devices. [web:97][web:99]  
- [ ] Focus order and keyboard navigation are consistent.  
- [ ] Screen reader‑friendly behavior is preserved where applicable.  

---

## 10. Reporting & Coverage Table

Example table to track coverage:

| Browser / Device       | Layout | Forms | Links / Nav | Media | Functionality | Notes |
|------------------------|--------|-------|-------------|-------|--------------|-------|
| Chrome (Win)           | ✅     | ✅    | ✅          | ✅    | ✅           | [e.g., “All good”] |
| Firefox (Win)          | ✅     | ✅    | ✅          | ✅    | ✅           | [e.g., “Minor padding difference in profile card”] |
| Safari (macOS)         | ✅     | ✅    | ✅          | ✅    | ⏳           | [e.g., “Investigate login redirect delay”] |
| Chrome Mobile (Android)| ✅     | ✅    | ✅          | ✅    | ✅           | [e.g., “Ready for UAT”] |
| Safari Mobile (iOS)    | ✅     | ✅    | ✅          | ✅    | ✅           | [e.g., “Small touch‑target spacing on filters”] |
