## 2026-06-28 - Caching RoomDatabase instances
**Learning:** Found that `RoomExplorerActivity` was building a new `RoomDatabase` instance on every single database query via `Room.databaseBuilder(...).build()`. RoomDatabase instantiation is an expensive operation and Android documentation explicitly recommends using a singleton pattern.
**Action:** Always cache the `RoomDatabase` instance or its underlying `SupportSQLiteDatabase` connection rather than recreating it on every query to prevent significant performance degradation.
