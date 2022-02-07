# Blocks

Blocks are continuous memories of floating point numbers.

## Communication Mechanism

Blocks are the main communication mechanism between Sonolus and engine.

For example, Sonolus can pass current time information to engine by updating the 0th value of Level Data block; engine can pass judgment information to Sonolus by updating the 0th value of Entity Input block.

## Accessing Blocks

Blocks can be accessed using `Get` and `Set` functions.

## Read Access Table

| Block                      | `preprocess` | `spawnOrder` | `shouldSpawn` | `initialize` | `updateSequential` | `touch` | `updateParallel` | `terminate` |
| -------------------------- | :----------: | :----------: | :-----------: | :----------: | :----------------: | :-----: | :--------------: | :---------: |
| Level Memory               |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Level Data                 |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Level Option               |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Level Transform            |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Level Background           |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Level UI                   |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Level Bucket               |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Level Score                |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Level Life                 |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Level UI Configuration     |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Entity Info Array          |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Entity Data Array          |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Entity Shared Memory Array |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Entity Info                |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Entity Memory              |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Entity Data                |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Entity Input               |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Entity Shared Memory       |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Archetype Life             |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Temporary Memory           |              |              |               |              |                    |    ✔    |                  |             |
| Temporary Data             |              |              |               |              |                    |    ✔    |                  |             |

## Write Access Table

| Block                      | `preprocess` | `spawnOrder` | `shouldSpawn` | `initialize` | `updateSequential` | `touch` | `updateParallel` | `terminate` |
| -------------------------- | :----------: | :----------: | :-----------: | :----------: | :----------------: | :-----: | :--------------: | :---------: |
| Level Memory               |      ✔       |      ✔       |      ❌       |      ❌      |         ✔          |    ✔    |        ❌        |     ❌      |
| Level Data                 |      ✔       |      ✔       |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Level Option               |      ✔       |      ✔       |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Level Transform            |      ✔       |      ✔       |      ❌       |      ❌      |         ✔          |    ✔    |        ❌        |     ❌      |
| Level Background           |      ✔       |      ✔       |      ❌       |      ❌      |         ✔          |    ✔    |        ❌        |     ❌      |
| Level UI                   |      ✔       |      ✔       |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Level Bucket               |      ✔       |      ✔       |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Level Score                |      ✔       |      ✔       |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Level Life                 |      ✔       |      ✔       |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Level UI Configuration     |      ✔       |      ✔       |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Entity Info Array          |      ❌      |      ❌      |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Entity Data Array          |      ✔       |      ✔       |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Entity Shared Memory Array |      ✔       |      ✔       |      ❌       |      ❌      |         ✔          |    ✔    |        ❌        |     ❌      |
| Entity Info                |      ❌      |      ❌      |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Entity Memory              |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Entity Data                |      ✔       |      ✔       |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Entity Input               |      ✔       |      ✔       |       ✔       |      ✔       |         ✔          |    ✔    |        ✔         |      ✔      |
| Entity Shared Memory       |      ✔       |      ✔       |      ❌       |      ❌      |         ✔          |    ✔    |        ❌        |     ❌      |
| Archetype Life             |      ✔       |      ✔       |      ❌       |      ❌      |         ❌         |   ❌    |        ❌        |     ❌      |
| Temporary Memory           |              |              |               |              |                    |    ✔    |                  |             |
| Temporary Data             |              |              |               |              |                    |   ❌    |                  |             |
