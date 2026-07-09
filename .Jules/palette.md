## 2026-07-09 - Fix Dark Mode Contrast in Programmatic UI
**Learning:** Programmatic UIs that explicitly set background colors (like `Color.WHITE`) but leave text colors default can become completely illegible in Dark Mode due to theme overriding.
**Action:** Always explicitly define text and hint colors (e.g., `Color.BLACK`, `Color.GRAY`) when the background color is explicitly defined in dynamically generated Android views.
