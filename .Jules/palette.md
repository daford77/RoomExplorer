## 2024-05-24 - Dynamic Android Views and Default Text
**Learning:** In dynamically generated Android UIs (like `RoomExplorerActivity` adding `TextView` directly from code without layout files), setting alarmist default messages like "Error Messages will be displayed here" causes poor initial impressions and potential confusion, as users might think an error occurred just by opening the view. Also, typographical errors in success messages can harm trust in developer-tools.
**Action:** When working with dynamically created views, ensure placeholder texts reflect a neutral/ready state ("Status messages will be displayed here") and double-check spelling in hardcoded strings.

## 2024-05-24 - Dynamic Live Regions for Screen Readers
**Learning:** When text views in a UI dynamically update to show success/error status messages (e.g., executing queries), screen reader users are completely blind to these changes unless the views are marked as "live regions". In dynamic layouts (where views are instantiated programmatically rather than inflated from XML), you must explicitly set this via code to ensure inclusive feedback.
**Action:** Always apply `ViewCompat.setAccessibilityLiveRegion` to programmatically created text views that convey transient status updates or important feedback in Android apps.

## 2024-06-29 - Missing Content Descriptions on Programmatic Views
**Learning:** When UI elements are generated programmatically (e.g., using `new EditText` or `new Button`), they lack the built-in accessibility descriptions that might be provided or prompted when using XML layouts. Screen reader users can struggle to understand the purpose of these elements without explicit `setContentDescription` calls.
**Action:** Always add `setContentDescription` to programmatically created interactive elements to ensure they are accessible to screen readers.
## 2026-07-01 - Dynamic Views labelFor property
**Learning:** For programmatic view generation, labels aren't implicitly associated with inputs via their hierarchy like they often are in XML or web frameworks. Screen readers won't know the purpose of the input.
**Action:** Always use `androidx.core.view.ViewCompat.setLabelFor(labelView, inputView.getId())` when generating dynamic `TextView` labels mapped to `EditText` inputs in Android UIs.

## 2024-07-08 - Explicit Text Colors for Programmatic Views
**Learning:** When generating UI elements programmatically (like `TextView` or `Button`) inside a layout with a hardcoded background color (e.g., `Color.WHITE`), omitting an explicit text color can cause text to become invisible if the user's device is in Dark Mode (which defaults text colors to white/light).
**Action:** Always explicitly set the text color (e.g., `setTextColor(Color.parseColor("#000000"))`) on programmatic views when the container has a hardcoded background, ensuring visibility across system themes.
