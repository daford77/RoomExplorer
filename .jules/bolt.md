## 2024-07-02 - RoomDatabase instantiation bottleneck
**Learning:** In Android Room development, instantiating `RoomDatabase` is highly expensive and creating it per query is a massive performance issue.
**Action:** Always cache the instance or its underlying `SupportSQLiteDatabase` connection instead of recreating it per query execution to prevent severe performance bottlenecks.
