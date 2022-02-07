# Presentation System

Presentation system is responsible for presenting skin sprites, effect clips, and particle effects.

## Skin Sprites

All skin sprites from `Draw` function calls are drawn.

## Effect Clips

All effect clips from `Play` function calls are played.

## Particle Effects

All particle effects from `SpawnParticleEffect`, `MoveParticleEffect`, and `DestroyParticleEffect` function calls are spawned, moved, and destroyed.

## Remarks

All function calls are processed regardless whether the source entity is still active or not.
