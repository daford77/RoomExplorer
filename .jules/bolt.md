## 2024-07-04 - Caching Room Database Connections
**Learning:** In Android Room development, instantiating `RoomDatabase` is highly expensive and can become a severe performance bottleneck if done per query execution.
**Action:** Always cache the `RoomDatabase` instance or its underlying `SupportSQLiteDatabase` connection to reuse it for subsequent queries.
