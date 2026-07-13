## 2024-07-13 - Expensive RoomDatabase Instantiation Bottleneck
**Learning:** Instantiating `RoomDatabase` via `Room.databaseBuilder(...).build()` is highly expensive. Repeatedly creating new instances per query rather than caching the connection/instance leads to severe performance degradation and potential memory/connection leaks.
**Action:** Always cache the `RoomDatabase` instance or its underlying `SupportSQLiteDatabase` connection after initial creation, rather than recreating it for every execution.
