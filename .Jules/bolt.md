## 2024-05-18 - [Cache RoomDatabase instance to avoid expensive recreation per query]
**Learning:** In Android Room development, instantiating `RoomDatabase` is highly expensive. Creating a new instance using `Room.databaseBuilder` for every database operation causes severe performance bottlenecks.
**Action:** Always cache the `RoomDatabase` instance and its underlying `SupportSQLiteDatabase` connection (e.g., lazily instantiating it as a class field) instead of recreating it per query execution to prevent severe performance bottlenecks.
