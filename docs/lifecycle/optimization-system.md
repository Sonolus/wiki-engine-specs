# Optimization System

Optimization system is responsible for optimizing nodes to improve code performance.

## Optimizations

Immutable blocks can no longer be modified from this point on, optimization system can use this information as well as behaviors of functions to optimize nodes in order to improve performance.

### Mathematical Functions

Mathematical node functions have no side effects, and when all arguments are known value nodes then the result can be precomputed.

```ts
Add(1, 2, 3)

// will be optimized into:
6
```

### Control Flow Functions

Depending on the logic of control flow node functions, some conditional branching can be simplified or trimmed.

```ts
And(
    1,
    2,
    DynamicArgument1,
    DynamicArgument2,
    0,
    DynamicArgument3,
    DynamicArgument4
)

// will be optimized into:
And(DynamicArgument1, DynamicArgument2, 0)
```

### Immutable Block Access

Access to immutable data can be precomputed.

```ts
Get(LevelData, ScreenAspectRatio)

// will be optimized into a value node with corresponding value
```

## Caveats

### No New Node Creation

Optimization system cannot create new nodes, it can only modify existing nodes.

```ts
// BAD:
Add(1, 2, DynamicArgument)

// CANNOT be optimized to:
Add(3, DynamicArgument)
// because it requires creating a new value node 3
```

```ts
// GOOD:
Add(Add(1, 2), DynamicArgument)

// will be optimized to:
Add(3, DynamicArgument)
```

## Remarks

Making use of optimization system can greatly improve performance, thus it is recommended to always code with it in mind.
