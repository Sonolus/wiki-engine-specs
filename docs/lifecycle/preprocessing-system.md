# Preprocessing System

Preprocessing system is responsible for setting up or modifying blocks to be used throughout the gameplay.

## `preprocess` Callback

System loops through all entities in level sequentially based on their `preprocess` callback order. For each entity `preprocess` callback is executed.

## Remarks

`preprocess` callback is the only callback where writing to normally immutable blocks is allowed. Therefore it is great for preparing data that are unknown at compile time, yet required at runtime.

Due to the nature of preprocessing system running only once before the start of a level, it is recommended to use `preprocess` callback to do all needed calculations that are required at runtime instead of doing them at runtime, to improve performance.

However, because optimization system is not yet run, code in `preprocess` callback are not optimized and perform worse. It is important to keep preprocessing reasonable to avoid overly long preprocessing time.
