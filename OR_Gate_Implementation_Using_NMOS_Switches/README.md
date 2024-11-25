# OR Gate Implementation Using NMOS Switches

This project provides an in-depth explanation of the OR gate implementation using NMOS switches. It includes the circuit design, simulation setup, analysis, and verification of results. This project validates the behavior of an OR gate through schematics and plotted graphs.


## 1. Setup

### Components Used
- **NMOS Transistors (M1, M2):** Function as switches.
- **Voltage Sources:**
  - **V1:** Pulse source representing input signal 1.
  - **V2:** Pulse source representing input signal 2.
  - **V3:** Constant 1.8V supply.
- **Ground (GND):** Common reference point for the circuit.

### Circuit Functionality
- When either or both inputs (V1 or V2) are `HIGH`, the output is `HIGH` (logic 1).
- When both inputs are `LOW`, the output is `LOW` (logic 0).

The circuit is designed to replicate the behavior of a logical OR gate using NMOS switches.


## 2. Simulation

### Simulation Parameters
- **Voltage Source V1 (Input 1):**
  - `PULSE(0 1.8 20ms 1ns 1ns 20ms 50ms)`
  - Initial Voltage: 0V
  - Peak Voltage: 1.8V
  - Delay: 20ms
  - Rise/Fall Time: 1ns
  - ON Time: 20ms
  - Period: 50ms
- **Voltage Source V2 (Input 2):**
  - `PULSE(0 1.8 0 5ns 5ns 20ms 50ms)`
  - Initial Voltage: 0V
  - Peak Voltage: 1.8V
  - Delay: 0ms
  - Rise/Fall Time: 5ns
  - ON Time: 20ms
  - Period: 50ms
- **Supply Voltage V3:**
  - Constant Voltage: 1.8V.
- **Simulation Command:**
  - `.tran 1s`: Transient analysis run for 1 second.


## 3. Analysis

### Key Observations
- **NMOS Transistors:** Conduct current when their gate voltage (V1 or V2) is `HIGH`.
- **Output Voltage:** Matches the OR gate truth table:
  - **HIGH (1.8V):** When either or both inputs are `HIGH`.
  - **LOW (0V):** When both inputs are `LOW`.

### Waveforms Plotted
- **Current Through NMOS Transistors (M1 and M2):**
  - X-Axis: Time (seconds).
  - Y-Axis: Current (microamperes).
  - Displays the conduction behavior of each transistor when the respective input is active.
- **Output Voltage Response:**
  - X-Axis: Time (seconds).
  - Y-Axis: Output voltage (volts).
  - Confirms the logical behavior of the circuit as an OR gate.


## 4. Plotting

### Graph 1: Current Through M1 and M2
- Captures the conduction of NMOS transistors as input pulses activate them.
- Spikes indicate the flow of current when the gate voltage of either M1 or M2 is `HIGH`.

### Graph 2: Output Voltage Response
- Demonstrates the circuit's OR gate behavior.
- The output voltage is plotted, showing a `HIGH` state whenever one or both inputs are `HIGH`.


## 5. Interpretation

### Key Insights
- The NMOS transistors function correctly as switches, enabling the circuit to replicate an OR gate.
- The plotted graphs validate that the output voltage rises to 1.8V when any input is `HIGH`, as expected for an OR gate.

### Logical Validation
The simulation results match the OR gate truth table:

| **V1** | **V2** | **Output (V3)** |
|--------|--------|----------------|
| 0      | 0      | 0              |
| 0      | 1      | 1              |
| 1      | 0      | 1              |
| 1      | 1      | 1              |


## 6. Verification

- The results were cross-verified by observing the output behavior across multiple input pulse combinations.
- The circuit was simulated under transient conditions for 1 second to ensure consistency.


## 7. Final Adjustments

- The rise and fall times of the pulses were adjusted to ensure smooth transitions during simulation.
- The supply voltage was fixed at 1.8V to align with the transistor threshold voltage requirements.


## 8. Conclusion

- The NMOS-based circuit successfully replicates the behavior of an OR gate.
- The simulation results confirm the expected logical behavior, demonstrating that the circuit is operational and valid.
- This implementation provides a practical example of how digital logic gates can be constructed using analog components such as NMOS transistors.

### 9. Practical Applications

- Understanding how NMOS transistors can be used to design basic logic gates.
- Provides insights into transient analysis for digital logic simulation.

### 10. Future Enhancements

- Extend the circuit design to implement other logic gates (e.g., AND, XOR).
- Optimize transistor sizing for real-world applications.
