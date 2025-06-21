# Statuses and Modifiers

This is the big one, really.
I've been working on a Status system for a while, and there's quite a lot to it, so nothing better to do than get to it.

## Statuses

A status is a special little effect that an OC can have, providing a bad, neutral, or good change to the style to shake up battling.
Each quality of statuses are below, and the letter in parentheses is the variable associated with them.
These variables may be used whenever needed, to allow for a lot of choice.
Math is heavily involved with statuses, however usually I will be there to run calculations.
A bot will be coming soon to be handling these checks as opposed to myself.

> You are not required to use statuses. However, providing the option to be there in the first place is the major goal.
{style=note}

<tabs>
<tab title="Count (C)" id="count">

A status has a Count, which is a very specific way of keeping track of Cycles.
Cycles and Counts are technically different but will always remain the same value, yet serve different purposes depending on status’ effect description.
This mechanic is pulled directly from *Slay The Spire*, of which I will use an example from that game to demonstrate this concept.

The game has a status, Frail, which reduces Dexterity by that count.
Say it’s applied at 3 cycles in this case.
The Count and Cycles are both 3, reducing Dexterity by 3.
However, next cycle, Cycles and Count are at 2, meaning Dexterity is only reduced by 2 now.
This can be used for a sort of bleed-esque effect, or a diminishing effect over time.

In the case that Counts are not used in an ability's description, then don't bother.
</tab>
<tab title="Augmentation (A)" id="augmentation">

Augmentation is where the math part of the Status game becomes much more apparent.
**Burn II** is **Burn** with an augment of 2.
If a status’ effect doesn’t account for A, augmentation is functionally useless.
Get ready for something in the future to speed up calculations MUCH quicker.

Assume that the default status name when used in combat is an augment of 1.
Also, negative numbers for augments do not exist, nor can they be 0.

This sort of concept can work in two major ways.
Either in the effect with some sort of scalable thing to show how weaker or stronger statuses can work, or in Default Trigger Rate (DTR), which can be buffed / nerfed depending on the augmentation.

</tab>
<tab title="Stacking" id="stacking">

The concept of Stacking can go in two ways.
Firstly, multiple statuses can be on top of one another, but statuses without a stackable attribute cannot be layered on themselves.
So, an OC can have **Confusion** and **Dizzy**, but not two **Dizzy** counts at the same time.
If an effect that is non-stackable is applied to itself, the prior effect is overwritten with the new one.
So, a **Dizzy III** can be replaced by a **Dizzy II** and there’s nothing to do about it, priority doesn’t exist in these cases. 

</tab>
</tabs>

### The Lists

Here's one massive list, whether they're good or bad is up to you.

| Status    | Default Affliction Rate    | Effect                                                                                                                 |
|-----------|----------------------------|------------------------------------------------------------------------------------------------------------------------|
| Burn      | 3 Cycles, 100% Trigger     | Causes lingering burns to plague the affected, rebounding slight damage per physical hit dished out.                   |
| Confusion | 3 Cycles, $10+2A$% Trigger | Will choose a random ability within scope to use upon trigger. Does not activate with physical attacks.                |
| Dizzy     | 3 Cycles, $10+A$% Trigger  | Will have a set chance for a physical attack to miss. Future attacks in a chain will not be executed, new chains will. |

New will be added in the future, or whenever I finish a current set.

### Partner Effects

While the main list isn't complete, that isn't to say that there aren't more in the works.
Some of these are what's known as Partner Effects, replacements.

For an example, take an entity made of fire.
Not one that primarily uses fire, one that *is* fire.
It would be weird to have them with a **Burn** status, so **Uncontrolled** is used in lieu.

These partner effects must be specified per-oc; as each one will react differently.
One of my boys, Nuclide, has the partner to **Irradiated** as **Decay** or **Rapid Decay**, each of which will be their own section on his pages soon.

## Modifiers

Now, it wouldn't be a system if there weren't more needlessly complicated things in the workings, so here are Modifers.
Modifiers are per-oc, and change how the OC reacts to statuses.
Each status should have their own modifiers; and you don't need to include all of them.

It requires thinking about your oc's strengths and weaknesses, susceptibilities and balancing.

As an example, Clef is fairly resistant to sound, so maybe a -15% affliction chance to Confusion.
But, once it's applied, it could have a +10% trigger chance, as he's still pretty weak-willed and isn't the most mentally resilient.

There are 5 main modifiers to consider:

<tabs>
<tab title="Cycle" id="cycle">

A cycle modifier is a flat addition or subtraction to an effect’s added cycles.
For example, an OC with a -1 cycle modifier against Dizzy will have one less cycle of Dizzy from ALL sources.
Do note that cycle modifiers cannot be used to bring a cycle count below 1.

</tab>
<tab title="Affliction Chance" id="ac">

An affliction chance modifier is as it says on the tin;
if a status from an ability has a 50% chance of enabling the status onto the opponent, that will go down to 40% if the affliction chance modifier for that status is -10%.

If the number goes above 100%, then the chance is always 100% plus the overhead to add 1 to the augment.
As an example, a 120% chance for **Burn** to afflict will be a 100% chance for **Burn I**, so just a 20% chance for **Burn II**.

</tab>
<tab title="Trigger Chance" id="tc">

As the name implies, this is if the status is applied, it will have a fixed increase or decrease for it to trigger.
This is not the same as affliction chance.

If the number goes over 100%, then the chance is always 100% to trigger once, overhead to trigger twice.
Continue that sort of pattern for higher numbers.

</tab>
<tab title="Effect Severity" id="es">

Effect Severity is how much the effect will do to the target.
This is a little more abstract, as this is pulled from general weaknesses and resistances.

While I don't have a concrete system (yet), I'm thinking about a static multiplier.

</tab>
<tab title="Augment Shift" id="as">

Augment shift is as the name implies.
If a status is applied, it is treated as if the argument was modified.

As an example, **Burn I** on an OC with an Augment Shift on Burn of +1 will be treated as **Burn II** functionally.

</tab>
</tabs>

## Conclusion

Statuses and Modifiers are entirely optional, bottom line.
But, be sure to know them in case an opponent uses them.

The option is here, and that's all that matters.
If you do want to use it, use it.