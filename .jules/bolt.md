## 2024-06-25 - RoomDatabase Instantiation Performance Bottleneck
**Learning:** In Android Room development, instantiating `RoomDatabase` (via `Room.databaseBuilder(...).build()`) is a highly expensive operation. Recreating it on every query execution causes severe performance bottlenecks.
**Action:** Always cache the `RoomDatabase` instance (and its underlying `SupportSQLiteDatabase` connection) after its first initialization, rather than instantiating it per query.
