# Variable management

Intelligent Test supports the definition and management of variables that allow non‑constant values to be passed to the algorithm. These variables enable dynamic behavior based on technology or ILT device, reducing hard‑coded logic and improving reusability across projects.

Variables are supported at multiple levels:

-   **Technology Variables**

    Define values that apply to all ILT devices within a specific technology.

-   **ILT Device Variables**

    Define values specific to an ILT Device Code. These variables can further refine or override technology‑level values for a given device. This layered approach ensures the most specific value is used at runtime, while still allowing shared defaults at technology levels.


-   **[Creating and editing Technology Variables](../id_docs/it_create_variable.md)**  
Only users with the Tester role can create and edit Variables.
-   **[Creating and editing ILT Device Variables](../id_docs/it_create_ilt_variable.md)**  
Only users with the Tester role can create and edit Variables.

**Parent topic:**[Intelligent Test](../id_docs/intelligent_test_intro.md)

