# Glossary of terms

-   **Aspects**

    Key value pairs that contain the details of the design of an element \(can be ALN/INT/Datetime/Enumeration/Complex types\).

-   **Attachments**

    Documents that are assigned to an entity to provide further details of is design \(Word/Excel/PPT\).

-   **BASIS**

    The Basis captures all the parameters that are identified during report configuration. Report parameters identify the variables that you want to track during the semiconductor manufacturing process. For example, you might want to track specific Lot IDs and their status, wafers within a Lot, and the equipment \(tools\) used to manufacture the wafer during wafer manufacturing.

-   **DFD**

    DFD stands for Data Flow Diagram. A DFD is a flow diagram that represents how new and updated data flows into the Rapids Information Center \(IC\) during the ETL process.

-   **Dataset**

    Abstraction of a query on a data source. A dataset contains both the metadata and the data values. A dataset can use physical, virtual, and custom resolvers to access the data.

-   **Data View**

    A view of a data table that can be customized to present a subset of data from a data table. It contains metadata and instructions for receiving data but it does not store the data values.

-   **Device**

    Within a Macro layout, the Device is the core technology area. Macros can have one to fifty Devices depending on area and wiring. Devices represent the DUT \(Device Under Test\) from a layout and contain a parametric specification if designed through automation. If the DUT is being electrically tested, Devices are mapped to specific pad assignments.

-   **Design Rule Checker \(DRC\)**

    A program supported through an eDiscovery Analyzer \(EDA\) vendor software that contains a deck of the ground rules in the design manual that is being used for the testsite. The DRC deck is checked against the CAD layout design for a Macro to flag violations of any of the rules, for example, minimal space dimensions between elements.

    DCR is also known as the **Design Rule Check** that represents a verification check that ensures that a macro layout is complete.

-   **Gate**

    Gate is the terminal of a MOSFET device. Gate voltage is the voltage that is measured or applied by the Gate.

-   **GPIB**

    GPIB is an abbreviation for General-Purpose Interface Bus, a short-range digital communication 8-bit parallel multi-master interface defined by the IEEE 488 standard. Commands on this bus consist of a single mnemonic and is preceded by an asterisk **\*** and some commands have a query form that adds a **?** after the command. For example, some instruments on the bus are recognized through an **IDN?** query.

    **Note:** Not all instruments respond to an **IDN?** query.

-   **KERF**

    Kerf refers to the area in a silicone wafer that is used to separate individual dies at the end of wafer processing.

    Kerf can also be referred to as the width of material removed from a silicon wafer.

    A Kerf can also be defined as a scribe line \(also known as a Kerf or frame\) in an area in a silicone wafer. This area also contains features that help the manufacturing process but are not present in a final product.


-   **Layout path**

    A **layout path** is the file system or repository path where the macro’s physical layout data resides. This path is required so the verification system knows where to fetch the layout files to run the selected checks.


-   **Macro**

    Macros are areas on a chip that is being designed/produced. Each tests site can support hundreds to thousands of Macros. See test site.

-   **Pad**

    A metal area with its own design that contacts a probe during electrical testing. Padsets contain a set number of pads within a padset, usually twenty-five. Padsets can have multiple designs. The arrangement and permutations of pads within a padset require unique padset names. Only Project Administrators can create pads and pad assignments.

-   **PadAssignments**

    Each Device has a set of Pad Assignments if it is being electrically tested. The assignment data has a two-fold purpose:

    1.  It defines the metal wiring that must exist between a Device and the pads and padsets for them to be physically connected in hardware. Automated wiring scripts pull this definition into the code to draw the Computer-Aided Design \(CAD\) wiring.
    2.  It matches a convention set by the electrical test team on how the electrical tests need to be coded for the appropriate electrical signal passing. If the wiring \(1\) does not align to a strategy the electrical test team can support \(2\), then the Device might not be valid for electrical testing and learning.
    3.  Project Managers assign PadAssignments to Projects and Macros. Projects and Macros can use only Assigned PadAssignments.
-   **PCell**

    In design eDiscovery Analyzer software, a pcell is a body of code that takes parameters for dimensions and design elements as inputs. The Pcell then produces a CAD semiconductor layout design for a specific Device as an output. In Intelligent Design, the pcell represents the name of that design code and entry options for all the input parameters that must be specified to generate the design. A Device uses one \(or multiple nested\) pcells that is specified in the ID tool, and a Macro might contain designs = generated by multiple pcells.

-   **Project**

    A Project can be a testsite project or a KERF project. Only Project Administrators can create projects.

-   **PTC**

    The Post Test Calculation system is designed to enrich semiconductor inline electrical test data with a post processor before it is sent to downstream consumers. The enrichment consists of the addition of parameter specification metadata, parameter result categorization, and calculated parameters.

-   **Source**

    Source is a device terminal. If you measure current through the source, it is the Source Current.

-   **Source Measure Unit \(SMU\)**

    An SMU is an instrument that combines a sourcing function and a measurement function on the same pin or connector. It can source voltage or current and simultaneously measure voltage and/or current.

-   **Switch Matrix**

    A switch matrix is used to allow dynamic connections between instrument terminals such as SMUs, PGUs to DUT terminals. Instrument terminals are connected to rows or inputs of the switch matrix and the probe\(s\) or probe card is connected to the columns of the switch matrix.

-   **Technology**

    A Technology is a grouping of Testsite projects and/or Kerf projects

-   **TEF**

    TEF typically refers to **Technology Enablement/Execution Framework** that is the backend framework responsible for running layout verification flows using the provided inputs \(macros, paths, checks\).

-   **Test Assignment**

    **Test Assignments** are created by **Macro Owners** to request specific tests \(test definitions\) to be executed on a given device.

    When there are Test Assignments available, a Test Engineer miight select **Apply** to choose the test assignments are that are automatically preselected on the Test Plan Device configuration screen. This allows **Test Engineers** to easily apply the requested test assignments to devices when creating and configuring a test plan, ensuring the Macro Owner’s testing intent is followed accurately.

    In summary:

    -   Test Assignments are created by Macro Owner.
    -   Then they are sent to Intelligent Test.
    -   Test Engineer can apply them in the creation of a test plan.
-   **TestBench**

    TestBench \(TB\) is a wafer-level semiconductor characterization software control program that is designed to control electrical test equipment such as source-measurement-units, pulse generators, and probers. It is a companion module that accepts IT Standard test plans for execution and gives ID users the capability to configure highly customized test plans. Because of the modular alignment, TB sends test results to IT in real time as test plans execute.

-   **Tester/Prober**

    A physical device used to test the circuits with the Macro/Device by applying electrical pulses to the pads by using probes \(contacts\).

-   **Test Definition**

    The Test Definition defines a specific sequence for a test and the following parameters: the type of device test, the subtype tests, the test equipment, and measurement library to use for the test as well as algorithms used in the test. The test definition also defines input aspects, output aspects, and device parameters. Aspects and parameters are synonymous with specifications. Test definitions are device-specific. Test definitions cannot be edited or copied but they can be used multiple times on a test plan.

    The tester is the only role that can create test definitions.

-   **TestPlan**

    A Test Plan defines a set of parameters and programs for the test and the following parameters: the Technology, the Project, the Macros, and the Devices. The goal of a test plan is to create a TPL file, which can then later be used to test devices.

    Test Plan statuses are Draft and Released. A Draft status is assigned when it is created, and a Release Status is assigned when the Test Plan TPL file is created. Test Plans only in Draft status can be edited. When a TPL file is created and is in Release status, the test plan is no longer editable.

    Tester is the only role that can create test plans.

-   **TestResults**

    The results of test plans when run by Test Devices.

-   **TestSite**

    An item within a technology that represents a chip that is being produced.

-   **Verification Checks**

    Macro verification checks help ensure that macros meet specific criteria before testing. Each verification check provides increasing confidence that the macro is physically valid and ready for future stages.

    -   **Dry Run** Validates configuration, inputs, and set up for a macro and helps identify issues early before running more comprehensive checks.
    -   **Density Check** Validate layout density requirements for compliance and might perform fill operations.
    -   **Final DRC** Validates complete design rule to ensure that the macro complies with all technology and manufacturing rules before proceeding further in the life cycle.
-   **Waivers**

    Requests to allow Macros \(and their specific Devices\) and their specific ground rule violations flagged through DCR to be allowed onto the testsite. Each violation is a waiver request that must be approved and logged in the system for the Macro.


