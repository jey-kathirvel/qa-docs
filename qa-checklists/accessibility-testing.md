# Accessibility Testing Checklist

Use this checklist to verify that your product meets basic accessibility standards (e.g., WCAG‑aligned).

---

## 1. Structure & Semantics

- [ ] Pages / screens use proper heading hierarchy (`h1 → h2 → h3`, no skipped levels). [web:114][web:118]  
- [ ] Landmarks and ARIA roles are used appropriately (e.g., `main`, `navigation`, `banner`). [web:111][web:113]  
- [ ] Every page has a clear, descriptive title or app name. [web:112][web:118]  
- [ ] Lists are marked as `ul` / `ol`; tables are marked as `table` with headers when needed. [web:114][web:118]  

---

## 2. Navigation & Keyboard

- [ ] All interactive elements (links, buttons, form fields) are keyboard‑accessible. [web:115][web:118]  
- [ ] Tab order follows a logical, left‑to‑right / top‑to‑bottom flow. [web:112][web:118]  
- [ ] Keyboard focus is visible (focus ring / outline), and there are no keyboard traps. [web:115][web:118]  
- [ ] Users can skip repeated navigation blocks (e.g., “Skip to main content” links). [web:118][web:120]  

---

## 3. Forms & Inputs

- [ ] Every form field has a programmatically associated label (via `<label>` or `aria-label`). [web:112][web:114]  
- [ ] Required fields are clearly indicated (visually and in code).  
- [ ] Validation messages are programmatically linked to the relevant field. [web:112][web:118]  
- [ ] Error messages describe the problem and how to fix it (e.g., “Enter a valid email address”). [web:115][web:118]  

---

## 4. Color & Visual Design

- [ ] Text and background have sufficient contrast (WCAG AA minimum, 4.5:1 for normal text). [web:115][web:118]  
- [ ] Information is not conveyed by color alone (e.g., red = error + icon / text). [web:111][web:118]  
- [ ] Color‑blind‑safe patterns are used (icons, underlines, shapes). [web:115][web:180]  
- [ ] Text sizing and zoom up to 200% do not break the layout or hide content. [web:112][web:118]  

---

## 5. Images, Icons & Non‑Text Content

- [ ] All meaningful images have appropriate alternative text (`alt`, `aria-label`, or `aria‑described`). [web:111][web:118]  
- [ ] Purely decorative images are hidden from assistive tech (CSS background / `aria‑hidden`). [web:118][web:117]  
- [ ] Icons and buttons with no visible text have accessible labels. [web:113][web:118]  
- [ ] Charts and data visuals provide alternative text or a data‑table description. [web:118][web:120]  

---

## 6. Multimedia & Motion

- [ ] Audio / video content has captions or transcripts when necessary. [web:114][web:118]  
- [ ] Automatic animations or carousels can be paused, stopped, or hidden. [web:115][web:119]  
- [ ] Content that flashes complies with the “less than 3 flashes in one second” rule. [web:115][web:180]  
- [ ] Time‑dependent content (e.g., auto‑logouts) gives users a way to extend or pause. [web:115][web:118]  

---

## 7. Screen Reader & AT Validation

- [ ] Page/screen structure is logical when read by a screen reader (e.g., JAWS, NVDA, VoiceOver). [web:114][web:119]  
- [ ] Links and buttons use descriptive text (not “click here” or “read more” without context). [web:111][web:118]  
- [ ] Hidden or off‑screen content is not announced unnecessarily to screen‑reader users. [web:118][web:120]  
- [ ] Dynamic content updates (e.g., live regions, notifications) are announced when they change. [web:114][web:119]  

---

## 8. Mobile‑Specific Accessibility

- [ ] Touch targets are large enough (≥ 44×44pt recommended) and have adequate spacing. [web:113][web:119]  
- [ ] Touch gestures are consistent and documented (e.g., swipe, tap, double‑tap). [web:113][web:119]  
- [ ] Dynamic text size and bold text settings from the OS are respected. [web:113][web:119]  
- [ ] App icons and labels are usable when VoiceOver/TalkBack is on. [web:113][web:119]  

---

## 9. Tools & Manual Checks

- [ ] Use automated tools (e.g., WAVE, axe, Lighthouse) as a baseline check. [web:117][web:118]  
- [ ] Verify issues manually with keyboard and a screen reader (e.g., ChromeVox, VoiceOver, NVDA). [web:114][web:119]  
- [ ] Test with real users with disabilities (if possible) for realistic feedback. [web:111][web:119]  

---

## 10. Accessibility Status Table (Optional)

Example table to track coverage:

| Screen / Page          | Keyboard Nav | Screen Reader | Color Contrast | Forms & Labels | Notes |
|------------------------|--------------|---------------|----------------|----------------|-------|
| Login Screen           | ✅           | ✅            | ✅             | ✅             | [e.g., “All good”] |
| Product List           | ✅           | ✅            | ⏳             | ✅             | [e.g., “Low contrast badge label”] |
| Checkout Flow          | ✅           | ✅            | ✅             | ✅             | [e.g., “Ready for WCAG AA”] |
