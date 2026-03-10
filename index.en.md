---
layout: page
title: "Debuggingless Development"
permalink: /en/
---

[🇰🇷 한국어](/engineering-notes/)

Debuggingless Development is a development approach focused on  
**designing systems where bugs are difficult to create in the first place, rather than relying on debugging to resolve them later.**

In many projects, this cycle becomes normal:

write code → run → find bug → debug → patch → repeat

The longer this becomes routine, the more likely it is that the real problem is not a single defect, but the **structure of the system itself**.

My preferred approach is the opposite.  
Instead of improving debugging as the primary tool, I try to build systems where **debugging becomes rare**.

## Principles

### 1. Architecture First

The system should be designed so that **invalid states are difficult to represent**.

- clear ownership of data
- explicit state transitions
- controlled mutation points
- clear lifecycle boundaries

Good architecture does not merely fix classes of bugs.  
It prevents them from appearing.

### 2. Deterministic Execution

Core systems should follow **predictable execution flows**.

Deterministic behavior makes it easier to:

- understand behavior
- reproduce issues
- compare builds
- detect regressions

This is especially important in game frameworks where many systems interact continuously.

### 3. Structural Logging

Logs should not be temporary debug output.  
They should be treated as **part of the architecture**.

Important events should always emit logs:

- initialization
- state transitions
- entity lifecycle
- major triggers
- structural flow boundaries

These logs become stable reference points across builds, making regressions easier to detect.

### 4. Debugging as a Last Resort

Traditional debugging tools still matter:

- breakpoints
- step execution
- memory inspection

But they should not be the primary way a system is understood.

Most issues should become visible first through:

- architectural constraints
- deterministic flow
- structural logging

Debugging should remain a last resort.

## Conclusion

Debugging cannot be eliminated completely.

However, strong architecture can dramatically reduce how often debugging is necessary.

In many systems, the best debugging strategy is not becoming better at debugging,  
but **designing software where bugs are harder to create**.
