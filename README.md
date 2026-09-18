# 🥡 Urban Lunch — Mobile QA

**Mobile Testing · Manual QA · Android** — TripleTen Bootcamp Project (2026)
> 🎓 Sprint Project

---

## 🎯 Problem

Manual quality assurance of the Urban.Lunch mobile app's complete ordering flow — from pickup-point selection through order tracking and delivery confirmation. The goal was to verify that every screen matched the product requirements document, and to document any defects found in a way the development team could act on directly.

---

## 📊 Results & Impact

| Metric              | Value        |
| -------------------- | ------------- |
| Test cases executed  | **62**        |
| Passed                | **54 (87%)**  |
| Failed                | **8 (13%)**   |
| Defects reported      | **8**         |
| Screens covered       | **5** + general checks |

---

## ⚙️ What I Did

- Designed and executed a 62-case checklist covering the full order flow: pickup-point selection, dish selection, order confirmation, order tracking/pickup, and order-sent confirmation, plus general checks (geolocation, connectivity, screen rotation)
- Tested on an emulated Pixel 10 Pro XL (Android 17) across WiFi and mobile data
- Isolated 8 defects, 7 of which concentrated in the item-counter and total-amount logic — the core of the app's ordering functionality
- Documented each defect with a clear description and the affected screen, and tracked them through Jira (IDs referenced in the report; the original board is no longer accessible)
- Wrote a formal test report with an executive summary, per-section breakdown, and a go/no-go recommendation for production

### Results by Section

| Section                          | Total | Passed | Failed | Success |
| ---------------------------------- | ----- | ------ | ------ | ------- |
| 1. Pickup-point selection          | 12    | 12     | 0      | 100%    |
| 2. Dish selection                  | 21    | 17     | 4      | 81%     |
| 3. Order confirmation              | 9     | 6      | 3      | 67%     |
| 4. Order tracking                  | 11    | 11     | 0      | 100%    |
| 5. Order sent                      | 4     | 3      | 1      | 75%     |
| 6. General (geolocation, WiFi/data, rotation) | 5 | 5   | 0      | 100%    |

---

## 🐞 Key Defects

| ID       | Description                                                     | Section              |
| -------- | ----------------------------------------------------------------- | --------------------- |
| S6QG6-1  | "-" button doesn't correctly remove an item from the list         | Dish selection        |
| S6QG6-2  | Counter allows negative values to display                         | Dish selection        |
| S6QG6-3  | Item detail quantity doesn't match the main list                  | Dish selection        |
| S6QG6-4  | Quantities reset when scrolling the list                          | Dish selection        |
| S6QG6-5  | Order confirmation quantities don't match the previous
