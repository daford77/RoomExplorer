## 2024-05-24 - RoomDatabase Initialization Bottleneck
**Learning:** In Android Room development, instantiating `RoomDatabase` is highly expensive. Creating a new instance per query (as seen in `getData()`) causes severe performance degradation, especially during rapid UI updates or heavy database operations.
**Action:** Always cache the `RoomDatabase` instance or its underlying `SupportSQLiteDatabase` connection at the class or application level instead of recreating it per query execution.
