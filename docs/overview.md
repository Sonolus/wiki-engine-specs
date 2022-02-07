# Overview

An overview of Sonolus engines.

## Purpose

Engine is the driver of a level.

Engine's main responsibility is to provide behavioral logics such as drawing of gameplay elements, playing of SFX, input handling, and judging player performance. A level is then able to provide data, and combining with engine's logic it can create a full gameplay experience for players.

An engine consists of configuration and data.

## Configuration

Engine configuration allows players to customize the gameplay experience of a level.

Engine configuration consists of options and UI.

### Options

An engine can provide a list of adjustable options for players.

These options are engine defined. Some engines may have many options to allow players to better customize their gameplay experience, while some engine may have none.

Some common options are:

-   Level Speed: how fast/slow the level is being played at.
-   Note Size: how big the notes are.
-   Random: whether the level is randomized.

### UI

UI is standardized options for UI elements.

These UI options are always available and allow engines to adjust UI based on players' input.

## Data

Engine data is the brain of an engine.

Engine data consists of archetypes, scripts, nodes, and buckets.

### Archetypes

Archetypes are abstractions of entities.

For example, an engine may have a "tap note" archetype, which is a note needs to be tapped by players. A level can have multiple "tap note" entities all using the same "tap note" archetype, but with different entity data.

In OOP, an archetype would be a class, and an entity would be an instance of a class.

### Scripts

Scripts are behavioral abstractions of archetypes.

For example, an engine may have a "tap note" script, which is a script that handles the behavior of a tap note. Multiple archetypes ("red tap note", "green tap note") can use the same "tap note" script, but with different archetype data.

In OOP, a script would be all the methods of a class.

### Nodes

Nodes are flattened AST (abstract syntax tree) of code.

For example, an engine may have a "Add" function node with a "5" number node and a "10" number node as its arguments. When engine executes this "Add" function node, it will add the two numbers together.

In most programming languages, a node would be a syntactic token.

### Buckets

Buckets are categories of playable entities.

It is optional and used by engines to provide player judgement graphs of each category at result screen.

For example, an engine may have a "tap note" bucket which shows judgment graphs of player's performance on tap notes in milliseconds, and similarly a "release note" bucket.
