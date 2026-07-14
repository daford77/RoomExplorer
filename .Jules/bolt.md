## 2024-05-19 - Caching RoomDatabase instances

**Learning:** In Android Room development, building a `RoomDatabase` instance is highly expensive since it processes annotations and sets up the database. Creating a new instance per query can cause a severe performance bottleneck.
**Action:** Always cache the `RoomDatabase` instance (e.g., using a class-level variable or singleton pattern) instead of recreating it for every execution to ensure performance efficiency.
