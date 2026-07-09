## 2024-05-24 - Expensive Query Execution Bottleneck
**Learning:** Recreating `RoomDatabase` instances inside loops or frequently called methods (like `getData()`) causes a massive performance bottleneck.
**Action:** Always cache `RoomDatabase` or the underlying `SupportSQLiteDatabase` instances instead of rebuilding them repeatedly.
