# Turn-Based Introduction

It sounds silly to have an introduction for something as ubiquitous as turn-based combat, but it's essential for documentation.
Turn-based combat is as it is on the tin - two people taking turns, dealing and defending attacks.

## The Process
This isn't concrete, but here's a plan.
Each turn you get is two phases: defending and attacking.
You get one message each, unless you need more than the character cap (for some reason).

A turn is per-person, but a cycle is when both people have gone and it's returned to the person who originally went first, cooldowns are often represented with cycles in mind.

> It's preferred you *don't* shove a bunch of linking attacks together, three max for good combat.
This is because some abilities can interrupt further actions, or some statuses can too, which means writing 20 different attacks is just wasting your time and making yourself more vulnerable.
Besides, to even do that many, you'll need **Fast**, or its equivalents.
**Fast** is defined later in the pages.
{style="note"}

## Music
The battle music is of the person of whom is being attacked, similar how it would work in some other implementations.
Except for some key differences, like support intrusions or special forms, but those are per-OC and must be specified when they do occur.

