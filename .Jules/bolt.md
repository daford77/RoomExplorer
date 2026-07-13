## 2024-05-24 - RoomDatabase Initialization Bottleneck
**Learning:** In Android Room, instantiating `RoomDatabase` (`Room.databaseBuilder(...).build()`) is extremely expensive and incurs significant performance penalties if performed redundantly per query.
**Action:** Always cache the `RoomDatabase` instance or its underlying `SupportSQLiteDatabase` connection rather than recreating it on every database interaction.
