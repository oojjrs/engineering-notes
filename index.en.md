---
layout: page
title: "Designing Systems That Rarely Need Debugging"
permalink: /en/
---

[🇰🇷 한국어](../)

# Designing Systems That Rarely Need Debugging

Most debugging happens because systems allow too many invalid states.

Instead of improving debugging techniques, I try to design systems where debugging becomes rare.

I informally call this approach **debuggingless development**.

---

Debugging is usually treated as a normal part of software development.

Write code.  
Run the program.  
Find a bug.  
Debug it.  
Patch it.  
Repeat.

Over time I started wondering whether this cycle itself was the real problem.

> If a system requires frequent debugging, the architecture is probably wrong.

For most of my work as a game developer, I’ve tried to follow an approach I informally call **debuggingless development**.

The term itself is not an established concept.  
It’s simply a name I use to describe a development style focused on reducing the need for debugging through architecture, deterministic execution, and structural logging.

The goal is not to eliminate debugging entirely, but to design systems where debugging becomes rare.

---

## Why debugging becomes difficult

As systems grow larger, debugging becomes harder for reasons that often have little to do with the bug itself.

Large software systems tend to accumulate:

- implicit state  
- unpredictable execution order  
- hidden dependencies  
- fragile interactions between systems  

When this happens, debugging becomes less about fixing a mistake and more about reconstructing what the system is doing.

Often the real issue is not the bug itself, but the structure that allowed it.

---

## Architecture first

The first goal is making **invalid states difficult or impossible to represent**.

This means designing systems with:

- explicit ownership of data  
- clear lifecycle boundaries  
- controlled mutation points  
- explicit state transitions  

Good architecture eliminates entire classes of bugs before they appear.

---

## Deterministic execution

Core systems should execute in a predictable order.

When execution is deterministic:

- behavior becomes easier to reason about  
- bugs become reproducible  
- regression detection becomes easier  

This is particularly important in game systems where multiple subsystems interact every frame.

---

## Structural logging

Logging is often treated as temporary debugging output.

In this approach, logging becomes **part of the architecture itself**.

Important events always produce logs:

- initialization  
- system boundaries  
- entity lifecycle  
- gameplay triggers  
- state transitions  

These logs remain permanently in the codebase.

Because of this, execution flows can be compared across builds.

Many problems reveal themselves simply by comparing logs between versions.

---

## Debugging as a last resort

Debuggers still exist.

Breakpoints, stepping through code, inspecting memory — they remain useful tools.

But they should not be the primary way to understand the system.

In practice, most issues become visible through:

- architecture constraints  
- deterministic behavior  
- structural logs  

Actual debugging sessions tend to happen rarely.

In my experience, it is often **once or twice per year**.

Interestingly, those rare cases are frequently engine-level issues rather than application logic.

---

## A different debugging workflow

Instead of stepping through code, the workflow often looks like this:

1. Logs reveal unexpected behavior  
2. Execution flows are compared across builds  
3. The architectural boundary where behavior diverges becomes obvious  

This often resolves the problem without interactive debugging.

---

## Conclusion

Debugging will always exist.

But the **frequency of debugging** is strongly influenced by system architecture.

Systems that rely heavily on debugging often allow too many invalid states and unpredictable behaviors.

Systems designed with strong constraints tend to reveal problems much earlier.

In many cases, the best debugging strategy is simply:

> design systems where bugs are harder to create.

---

## Open question

I’m curious how common this development style is.

Many teams rely heavily on debugging tools and iterative patching.

But in my experience, architecture quality has a much larger impact on debugging frequency than the tools themselves.

Do others design systems specifically to reduce the need for debugging?

Or is heavy debugging simply unavoidable in most real-world codebases?
