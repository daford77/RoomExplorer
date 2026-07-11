## 2024-05-24 - RoomDatabase Initialization is Expensive
**Learning:** Recreating RoomDatabase instances per query causes severe performance bottlenecks due to reflection, validation, and connection pool setup overhead.
**Action:** Always cache RoomDatabase instances, especially in Activities or singletons, to reuse the open connection pool.
