## 2026-07-01 - Cached RoomDatabase in RoomExplorer
**Learning:** Instantiating `RoomDatabase` via `Room.databaseBuilder(...).build()` is highly expensive in Android due to parsing and initializing connections. Doing this per SQL query execution causes severe performance drops.
**Action:** Always cache the `RoomDatabase` instance or its underlying `SupportSQLiteDatabase` connection to prevent recreating it per query, particularly in interactive database explorers.
