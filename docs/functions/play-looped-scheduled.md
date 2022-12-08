# `PlayLoopedScheduled`

Play a looping effect clip precisely at a scheduled time in the future.

## Arguments

| Argument | Description     |
| -------- | --------------- |
| id       | Clip identifier |
| t        | Time            |

## Return

A unique identifier of the looping effect clip instance.

## Remarks

`PlayLoopedScheduled` automatically accounts for audio offset to sync up with BGM timeline.

To ensure that the clip starts looping at the scheduled time, it must be scheduled at least 0.5 seconds in advance.

Returned identifier can be used to control the effect clip instance using `StopLooped` and `StopLoopedScheduled` functions.
