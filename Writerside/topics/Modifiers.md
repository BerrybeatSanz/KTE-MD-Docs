# Statuses, Modifiers, and Math (oh no)

## Status: Abstract

A "status" is just something afflicting an entity, whether good or bad.
Many of them exist to hurt, though.

Most commonly, they appear as a random chance from an ability or something else.
For example, I was hoping to have Clef's bugle give somewhere in the ballpark of a 30% chance to give Confusion to any enemy, it runs the chance for every enemy.

## Ideas

Here's the list of some I have in mind:

<tabs>
<tab id="bad" title="Bad">

Confusion
: Gives the target a *base* 15% chance to use a random ability. Only applies when using a non-physical attack. In a battle with 3 or more entities present total, the target is random excluding the target.

Dizzy
: Gives the target a *base* 20% chance to miss upon a physical attack action. That's it. When triggered with more attacks after it, it will cease all further actions. Does not apply to any defense actions.

Slow (Turn-Based)
: Has a *base* 10% chance to skip a target's attack action that turn. Unaffected by resistance modifiers. Cancelled out by Fast.

Slow (Not Turn-Based)
: Has a *base* 15% chance to force the target to perform generally less actions in their set. Unaffected by resistance modifiers. Cancelled out by Fast.

</tab>
<tab id="good" title="Good">

Fast (Turn-Based)
: Allows for the target to perform a second attack action in their turn. Unaffected by modifiers. Cancelled out by Slow.

Fast (Non Turn-Based)
: Allows for the target to perform generally more actions in their set. Unaffected by modifiers. Cancelled out by Slow.

</tab>
</tabs>