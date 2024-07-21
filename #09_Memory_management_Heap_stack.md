# Overview

Memory management is useful to be sure we are not using moer memory than necessary or duplicating datas for no reason.

In Rust it is managed automatically but if we want we can have control on this, so it is cool to know the idea.

In Java, we have the garbage collector that delete variables when they are not used later on in the script.


# Rust Ram Managment
2 sections in RAM
## Stack
**LIFO** : Last in, First out
**FILO**: First in Last out.
Super fast, prioritise when possible because fast.

In stack we have the adress, the name and the value of the variable.






## Heap
Heap is mapping the value to an adress(pointer). To retrieve the value we need to know the adress of the pointer. It is slower than the stack.
