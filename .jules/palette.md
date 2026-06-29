## 2024-05-24 - Dynamic Android Views and Default Text
**Learning:** In dynamically generated Android UIs (like `RoomExplorerActivity` adding `TextView` directly from code without layout files), setting alarmist default messages like "Error Messages will be displayed here" causes poor initial impressions and potential confusion, as users might think an error occurred just by opening the view. Also, typographical errors in success messages can harm trust in developer-tools.
**Action:** When working with dynamically created views, ensure placeholder texts reflect a neutral/ready state ("Status messages will be displayed here") and double-check spelling in hardcoded strings.

## 2024-05-24 - Dynamic Live Regions for Screen Readers
**Learning:** When text views in a UI dynamically update to show success/error status messages (e.g., executing queries), screen reader users are completely blind to these changes unless the views are marked as "live regions". In dynamic layouts (where views are instantiated programmatically rather than inflated from XML), you must explicitly set this via code to ensure inclusive feedback.
**Action:** Always apply `ViewCompat.setAccessibilityLiveRegion` to programmatically created text views that convey transient status updates or important feedback in Android apps.
