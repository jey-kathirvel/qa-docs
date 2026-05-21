# UI/UX Testing Checklist

Use this checklist during UI/UX validation for each screen, flow, or release.

---

## 1. General Layout & Consistency

- [ ] Layout matches the latest design mock / Figma / Zeplin.  
- [ ] Spacing, padding, and alignment are consistent across screens.  
- [ ] All UI components (buttons, cards, inputs) follow the style guide (size, radius, shadows).  
- [ ] Font family, size, and color match the design system.  

---

## 2. Text & Content

- [ ] No spelling or grammar mistakes in labels, headings, buttons, and messages.  
- [ ] Text is readable and not truncated on all viewport sizes.  
- [ ] Placeholder text is clear and not confusing.  
- [ ] Error, success, and warning messages are user‑friendly and specific.  

---

## 3. Navigation & Flow

- [ ] Main navigation (top menu, footer, side menu) works and highlights active section.  
- [ ] Breadcrumbs, back buttons, and “close” icons work as expected.  
- [ ] Users can move forward and backward through multi‑step flows without issues.  
- [ ] Empty states and “no data” screens are handled gracefully.  

---

## 4. Buttons & Interactions

- [ ] All buttons respond to clicks with proper visual feedback (active / hover states).  
- [ ] Disabled buttons are visually distinct and cannot be clicked.  
- [ ] Primary / secondary / tertiary buttons are clearly differentiated.  
- [ ] Icons and labels align correctly and are consistent across screens.  

---

## 5. Forms & Inputs

- [ ] Fields are aligned and labels are clearly associated with inputs.  
- [ ] Focus states and caret visibility are obvious.  
- [ ] Required fields are marked; optional fields are not over‑marked.  
- [ ] Validation appears at the right time and location (e.g., inline vs top message).  

---

## 6. Responsiveness & Cross‑Device

- [ ] Layout adapts correctly on mobile, tablet, and desktop viewports. [web:81][web:86]  
- [ ] No horizontal overflow or elements cut off on smaller screens.  
- [ ] Scrollbars appear only when needed.  
- [ ] Touch targets are large enough for mobile (no cramped buttons).  

---

## 7. Visual & Aesthetic Checks

- [ ] Colours meet contrast requirements for readability (no low‑contrast text). [web:89]  
- [ ] Icons and images are crisp, not pixelated, and correctly sized.  
- [ ] Images do not break or show broken placeholders.  
- [ ] Overlapping or stacking elements do not cause visual confusion.  

---

## 8. Loading, States & Feedback

- [ ] Loading spinners / skeletons are shown during API calls.  
- [ ] Success states (toast, badges, status indicators) are visible and clear.  
- [ ] Error states show actionable guidance (e.g., “Try again” or “Contact support”).  
- [ ] Empty, loading, and success states are consistent across similar components.  

---

## 9. Accessibility Basics (UI/UX‑focused)

- [ ] Sufficient color contrast between text and background. [web:89]  
- [ ] Text size and spacing are comfortable for most users.  
- [ ] UI does not rely solely on color to convey information (e.g., error icons + text).  
- [ ] Keyboard navigation is logical (tabs move in expected order).  

---

## 10. UX Flow & Usability

- [ ] Users can complete core tasks without unnecessary steps.  
- [ ] Important actions are easy to find; low‑risk actions are not too prominent.  
- [ ] Micro‑interactions (e.g., button press, toggle, swipe) feel smooth and intuitive.  
- [ ] Onboarding / first‑use flows are clear and not overwhelming.  

---

## 11. Cross‑Browser / Cross‑App Consistency

- [ ] UI looks and behaves consistently on major browsers (Chrome, Firefox, Safari, Edge). [web:84][web:86]  
- [ ] Critical differences in behavior or layout are documented and discussed with design.  

---

## 12. Checklist Status per Screen / Flow

Example table to track coverage:

| Screen / Flow          | Layout | Text | Navigation | Forms | Responsiveness | Accessibility | Notes |
|------------------------|--------|------|------------|-------|----------------|--------------|-------|
| Login Page             | ✅     | ✅   | ✅         | ✅    | ✅             | ✅           | [e.g., “Good; font size slightly small on mobile”] |
| Product Listing        | ✅     | ✅   | ✅         | ❌    | ✅             | ⏳           | [e.g., “Filter reset bug; investigate spacing on mobile”] |
| Checkout Flow          | ✅     | ✅   | ✅         | ✅    | ✅             | ✅           | [e.g., “Ready for UAT”] |
