## 2024-06-25 - Programmatic UI Accessibility
**Learning:** In purely programmatic Android UIs, standard XML accessibility attributes are missing by default. For forms, screen readers fail to associate generic `TextView`s with `EditText` inputs unless explicitly linked.
**Action:** Always use `androidx.core.view.ViewCompat.setLabelFor(labelView, inputView.getId())` when generating form layouts dynamically in Java to maintain accessibility parity with XML `<label>` elements.
