# Input System

Input system is responsible for processing user inputs for active entities.

## `touch` Callback

System loops through all input events happened in current update cycle. For each input event, system loops through all active entities sequentially based on their `touch` callback order. For each entity `touch` callback is executed.

## Remarks

Due to the sequential nature of input system, it is recommended to reduce workload in `touch` callback to increase performance. For example, use a single dedicated entity to process input events instead, and process its result from `updateParallel` callback.
