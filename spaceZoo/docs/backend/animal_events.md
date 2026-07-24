Illness
```mermaid
flowchart TD
id1(Animal catches illness)-->
id2(Warning -> Icon for illness)--Animal is healed-->
id3(Icon disappears)

id2--While not healed-->
id4(Health gradually drops)

id1--If in same enclosure as others-->
id5(Chance of illness spreading)-->
id1
```
---
Animal ages
```mermaid
flowchart TD
id1(New day)-->
DB1@{ shape: cyl, label: "Check if it's someone's birthday" }--It is!-->
id2@{ shape: rect, label: "Make a list" }--For each bd-animal:-->
DB2@{ shape: cyl, label: "Check age and lifecycle" }-->
id3@{ shape: rect, label: "Increase age by 1" }--Start of new life stage-->
id4(Transformation!!!)

id3--Maximum age-->
id5(Animal moves to a beautiful farm far away)
```
---
Animal dies
```mermaid
flowchart TD
id1(Animal dies)-->
id2(Message with name to make player feel guilty as they should)-->
DB1@{ shape: cyl, label: "Remove from memory" }-->
id3(Free up space in enclosure)
```
---
Animal is born
```mermaid
flowchart TD
id1(New day)-->
DB1@{ shape: cyl, label: "Increase all eggs' ages by 1" }--If ready to hatch-->
id2(Message: A baby hatched)-->
DB2@{ shape: cyl, label: "Check for free enclosures of the correct type" }--Enough free space in enclosures-->
id3@{ shape: rect, label: "Choose whether to keep animal" }--Keep them-->
id4@{ shape: rect, label: "Name the baby and choose an enclosure" }-->
DB3@{ shape: cyl, label: "Store animal with full stats and age 0" }

id3--Don't keep them-->
id5(Animal is removed)

DB2--Not enough space-->
id6(New message two days later)--Enough free space-->
id3
id6--Not enough space-->
id5
```