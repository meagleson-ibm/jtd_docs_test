# Configure a TSP

The process of configuring a TSP test to be run via TestBench

For the Generic Keithley TSP to interface correctly with user defined TSP files the script header and stored values must follow the following conventions. The default location for storing TSP scripts is in the TSP folder. TSP scripts are ASCII files with “tsp” extension names.

1.  The function name and filename must match. For example, the file with the name HCI.tsp, it should follow the format `HCI = function(….)`.

2.  Input parameters to be passed into the function must be placed between `Input Start` and `Input Stop` and follow the format of `<variable_name>, <variable_type>, <unit>, <default_value>, <min_value>, <max_value>, <comment>` where:

    -   **`<variable_name>`**

        The name of the input parameter.

    -   **`variable_type>`**

        The type of input parameter. Allows values are double or int.

    -   **`<unit>`**

        Any string to help the user know the units associated with the input parameter.

    -   **`<default_value>`**

        The default value to use. The user can change this value inside of TestBench.

    -   **`<min_value>`**

        The minimum allowed value the user can enter.

    -   **`<max_value>`**

        The maximum allowed value the user can enter.

    -   **`<comment>`**

        Short description of what the variable does to display to the user.

3.  Output parameters to be passed into the function must be placed between `Output Start` and `Output Stop` and follow the format of `<variable_name>, <list or scalar>, <variable_type>, <comment>` where:

    -   **`<variable_name>`**

        The name of the output parameter. This will be stored as a test property or column depending on if the output parameter is a list or scalar \(see next description\).

    -   **`<list or scalar>`**

        One of two possible values,

        -   **List**

            A Lua array. The array is defined as follows: `<array_name>={}` At the end of the test TestBench retrieves the values stored in the array.

        -   **Scalar**

            A single value stored as a test property. Scalars should be initialized at the beginning of the TSP function to be retrieved at the end of the test.

    -   **`variable_type>`**

        The type of variable. All list output parameters should be double. Scalar output parameters can be double, int, or string.

    -   **`<comment>`**

        Short description of what the variable does to display to the user.


The following is an example header file demonstrating the function definition, input parameter definition, and output parameter definition.

```
-- clear up memory
collectgarbage()

--Function Name:HCI

-- Define Input Parameters
--variable_name,type,unit,default_value,low_value,max_value,comment

--Input Start
--pre_VgStart,double,V,0,-2,2,Pre-stress Gate Voltage Start Value
--pre_VgStop,double,V,1,-2,2,Pre-stress Gate Voltage Stop Value
--pre_VgStep,double,V,0.02,-0.2,0.2,Pre-stress Gate Voltage Step Value
--Vdlin,double,V,0.05,-2,2,Drain Linear Voltage
--Vdsat,double,V,0.7,-2,2,Drain Saturation Voltage
--Vg_stress,double,V,0.35,-5,5,Gate Stress Voltage does not include overdrive
--Vd_stress,double,V,0.7,-5,5,Drain Stress Voltage
--StressTime,double,sec,100,1,1e6,Stress Time
--ppd,double,n/a,5,1,100,Points per decade to make sense measurement
--InitialSenseTime,double,sec,10e-3,5e-3,1e3,How long to wait for the 1st sense measurement
--maxSenseDelay,double,sec,1000,1,1e5,Max time to wait before making a sense measurement
--Ith_target,double,A,1e-6,1e-10,1,Idrain at Vth usually 100nA*W/L
--Vth_target,double,V,0,-2,2,Target Vth. Will calculate an Overdrive for Vg for stress and sense measurements; 0 = disable
--Ioff_target,double,A,0,-0.1,0.1,Target Ioff. Will calculate an Overdrive for Vg for stress and sense measurements; 0 = disable
--MeasDelay,double,sec,0.2,0,100,Delay Before measurement post voltage change
--Input Stop

-- Define Output Parameters
--variable_name,list or scalar,type,comment

--Output Start
--pre_Vg,list,double,Pre-stress Gate Voltage
--pre_Iglin,list,double,Pre-stress Linear Region Gate Current
--pre_Idlin,list,double,Pre-stress Linear Region Drain Current
--abspre_Idlin,list,double,Pre-stress Linear Region ABS Drain Current
--pre_Igsat,list,double,Pre-stress Linear Region Gate Current
--pre_Idsat,list,double,Pre-stress Linear Region Drain Current
--abspre_Idsat,list,double,Pre-stress Linear Region ABS Drain Current
--Time_stress,list,double,Stress time
--Igsat_stress,list,double,Saturation Gate Current (includes Vg Overdrive)
--Idsat_stress,list,double,Saturation Drain Current (includes Vg Overdrive)
--Iglin_stress,list,double,Linear Gate Current (includes Vg Overdrive)
--Idlin_stress,list,double,Linear Drain Current (includes Vg Overdrive)
--Ieff_stress,list,double,Ieffective (includes Vg Overdrive)
--Ioff_stress,list,double,Ioff (includes Vg Overdrive)
--Ireflin_stress,list,double, Iref for Vtlin calc measured at Vtlin0
--DeltaVtlin_stress,list,double, Vtlin shift
--Irefsat_stress,list,double, Iref for Vtlin calc measured at Vtsat0
--DeltaVtsat_stress,list,double, Vtsat shift
--IdStress,list,double,Id Stress
--Vtlin0,scalar,double,Linear Threshold Voltage
--Vtsat0,scalar,double,Saturation Threshold Voltage
--Ieff0,scalar,double,Effective Drive Current
--Ioff0,scalar,double,Off-state leakage current
--Overdrive,scalar,double,Overdrive voltage used
--ExitReason,scalar,string,Test Exit Reason
--Output Stop

HCI = function(pre_VgStart,pre_VgStop,pre_VgStep,Vdlin,Vdsat,Vg_stress,Vd_stress,StressTime,ppd,InitialSenseTime,maxSenseDelay,Ith_target,Vth_target,Ioff_target,MeasDelay)
	-- Initialize output parameters
	pre_Vg = {}
	pre_Idlin = {}
	pre_Iglin = {}
	abspre_Idlin = {} -- for determining Vtlin shifts
	pre_Idsat = {}
	pre_Igsat = {}
	abspre_Idsat = {} -- for determining Vtsat shifts
	
	Time_stress = {}
	Igsat_stress = {}
	Idsat_stress = {}
	Iglin_stress = {}
	Idlin_stress = {}
	Ieff_stress = {}
	Ioff_stress = {}
	Ireflin_stress = {}
	DeltaVtlin_stress = {}
	Irefsat_stress = {}
	DeltaVtsat_stress = {}
	IdStress = {}
	
	Vtlin0 = -1e10
	Vtsat0 = -1e10
	Ieff0 = -1e10
	Ioff0 = -1e10
	Overdrive = 0
	
	ExitReason = "Error"
...

```

**Parent topic:**[Keithley TSP](../../id_docs/testbench/keithley_tsp.md)

