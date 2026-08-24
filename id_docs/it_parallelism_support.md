# Parallelism support in Test Plans

This feature introduces parallelism support within Test Plans, specifically targeting the P9000 Test System Synchronous \(Sequence-based\) Parallelism. It allows test engineers to specify which device-test combinations can be executed simultaneously during a macro by assigning a matching parallelism label.

To define parallelism within a macro, Intelligent Test uses a set of rules that prevent certain terminal\(s\) from being shared across devices. These rules are specified via an aspect in the test definition called `testGroupRule`. This aspect explicitly identifies which terminals must remain unique per device to ensure safe and valid parallel execution.

Parallel execution is controlled by:

-   A labeling convention: `PNP_GrpName_TestDefSequence`, to uniquely identify the parallel group.
-   A test group rule aspect, which defines terminals that must not be shared between devices to avoid conflicts.

**Parent topic:**[Test Plan](../id_docs/it_test_plan_intro.md)

