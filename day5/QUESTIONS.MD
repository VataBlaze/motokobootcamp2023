Q1: True or False: we can prevent the heap being erased during upgrades by using a stable heap.

A1: False. By utilizing the functions 'preupgrade' & 'postupgrade' the heap memory can be stored safely during an upgrade.

Q2: A.call() -> B.call() -> C How much time (or rounds of consensus) do we need to wait for an answer?

A2: 4 seconds (2 rounds of consensus).

Q3: Is possible to realize an intercanister call in query mode?

A3: No, this would result in a compile-time error.