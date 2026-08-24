# Support for \(Sweeps\) Arrays of input values and results

This feature supports the ability to define parameter sweeps within a single Test Definition, eliminating the need to manually create multiple test cases. This functionality enables automation to dynamically generate a series of test instances based on input value variations.

Single Test Definition drives the generation of multiple test cases. Input parameters can be swept across a defined range or assigned multiple discrete values.

To support this capability, the you must use curly brackets \{\} to denote variable expansion logic:

-   Elements inside \{\} are separated by semicolons ;.
-   A sweep is defined using colon-separated values \(:\) in the format:
-   \{start:step:end\} – User wants to expand the test definition for this input from start value to end value at a particular step
-   \{val1;val2;val3\} – User wants to expand the test definition for this input with this given values
-   \{start:step:end; val1;val2;val3\} - User wants to expand the test definition for this input from start value to end value at a particular step and then expand with the other values \(combining both actions\).

Each generated test must have a unique output name, which the user must account for in the output formatting.

**Parent topic:**[Test Definition](../id_docs/it_test_definition.md)

