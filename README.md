#![NucleotidesAreJustHumanBytes](https://i.imgur.com/pjgoejH.png)
# dna


## Why `dna` when we have `protobuf` and `cap'n-proto`
They're great; probably better than this implementation, but protobuf isn't worth learning because they don't document enough for me, and cap'n proto specifies this on thier documentation:

> Any change not listed above should be assumed NOT to be safe. In particular:<br>
> 
> You cannot change a field, method, or enumerant’s number.<br>
> You cannot change a field or method parameter’s type or default value.<br>
> You cannot change a type’s ID.<br>
> You cannot change the name of a type that doesn’t have an explicit ID, as the implicit ID is generated based in part on the type name.<br>
> You cannot move a type to a different scope or file unless it has an explicit ID, as the implicit ID is based in part on the scope’s ID.<br>
> You cannot move an existing field into or out of an existing union, nor can you form a new union containing more than one existing field. <br>

## Why call it `dna`?

<s>I have the undergraduate prereqs to apply for med school, but I love software more</s>

This design combines a "proto-protocol" inspired by mechanisms in both DNA transcription and simple bootloaders.

## Okay, but again, why `dna` when we have `protobuf` and `cap'n-proto`?
If you step back and think about this for a second -- DNA, something even fewer primitives than the ones we have in systems programming, manages to encode a self-describing protocol that supports changing "fields", "default values", "ID's", and DNA Helicase does this with only a small number of "algorithms", yet somehow we can't seem to support this on pure-math machines? (Mm.. I'm not so sure.)

Cellular biology contains some of nature's most fascinating infrastructure. The human DNA protocol "supports" mutations, transactions, cloning, and even transmission. We can borrow the principles as abstractions and apply them to software. If nature-inspired designs work in A.I., then it should also be true that we can borrow nature-inspired designs to work for IO protocol conception.

## What does `dna` do?
`dna`'s best employee, "`Heli`", a cartoonishly-shaped protein with a clipboard, initializes a queue and reads an input source. It reads this stream, walking along to visit every sequential slot to ask for the value held there.<br> 
<br>
"`0x00000008`", says the oldest resident.<br>

`Heli` never looks up. <br>
"Uh-huh", recording their response.<br>

It advances in this fashion, never looking up from the clipboard — failing to notice how the age on the responders grows younger and younger.
Every so often, there's a blank slot. `Heli` doesn't care, though. Just records what they saw.<br>
Sometimes, there's a random younger resident near the front, but for the most part `Heli` only ever sees the most senior attendees at the start.<br>

Near the end, however, `Heli` gets annoyed. The answers start becoming obnoxiously repetitive.<br>
"`0x00000000`", "`0x00000000`", "`0x00000000`", "`0x00000000`",<br>
"`0x00000000`", "`0x00000000`", "`0x00000000`", "`0x00000000`",<br>
"`0xFFFFFFFF`", "`0xFFFFFFFF`", "`0xFFFFFFFF`", "`0xFFFFFFFF`",<br>
"`0xFFFFFFFF`", "`0xFFFFFFFF`", "`0xFFFFFFFF`", "`0xFFFFFFFF`",<br>
"`...`"<br>
"`0x00000000`", "`0x00000000`", "`0x00000000`", "`0x00000000`",<br>
"`0x00000000`", "`0x00000000`", "`0x00000000`", "`0x00000000`",<br>
"`0xFFFFFFFF`", "`0xFFFFFFFF`", "`0xFFFFFFFF`", "`0xFFFFFFFF`",<br>
"`0xFFFFFFFF`", "`0xFFFFFFFF`", "`0xFFFFFFFF`", "`0xFFFFFFFF`",<br>

`Heli` clenches up and snaps their pen. "What the helicase is going on he-"<br>
They look up.<br>
"Oh!", `Heli` chuckles. "Looks like we're done."

Next, they read over their notes, flip the page upside-down, and walk over to the address with the last thing that wasn't part of that obnoxious `0x00` `0xFF` business.

