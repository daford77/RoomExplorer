## 2024-11-20 - Caching RoomDatabase Instance
**Learning:** In Android Room development, instantiating `RoomDatabase` is highly expensive. Re-creating the instance per query causes a severe performance bottleneck.
**Action:** Always cache the `RoomDatabase` instance or its underlying `SupportSQLiteDatabase` connection instead of recreating it per query execution.
