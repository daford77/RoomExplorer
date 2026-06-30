## 2024-05-18 - Avoid repeated RoomDatabase instantiation in Android
**Learning:** Instantiating `RoomDatabase` is highly expensive and doing so per query in Android applications causes severe performance bottlenecks.
**Action:** Always cache the `RoomDatabase` instance or its underlying `SupportSQLiteDatabase` connection rather than recreating it on every query execution.
