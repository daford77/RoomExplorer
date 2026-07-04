## 2026-07-04 - Expensive RoomDatabase instantiations in getData()
**Learning:** RoomDatabase instantiation via Room.databaseBuilder() is very expensive, creating significant latency if invoked repeatedly.
**Action:** Cache the database instance or SupportSQLiteDatabase connection inside the Activity and reuse it rather than calling Room.databaseBuilder() inside frequently called methods.
