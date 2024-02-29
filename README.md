**BoreWell Smart Contract**

**Introduction:**
BoreWell is a Solidity smart contract designed to facilitate decisions related to pump selection, pipe count, and pipe size for bore wells. It offers functionalities to determine suitable pumps, validate the number of pipes, and assess pipe sizes based on given parameters.

**Contract Functions:**

1. **SelectPump(uint256 depth)**
   - **Purpose:** This function assists in selecting an appropriate pump based on the depth of the bore well.
   - **Parameters:**
     - `depth`: The depth of the bore well in meters.
   - **Returns:** A string indicating the recommended pump (`Pump_A` or `Pump_B`).
   - **Behavior:** If the depth is less than or equal to 100 meters, it suggests using `Pump_A`; otherwise, it recommends using `Pump_B`.

2. **NoOfPipes(uint256 numberOfPipes)**
   - **Purpose:** This function verifies the number of pipes used in the bore well.
   - **Parameters:**
     - `numberOfPipes`: The count of pipes installed in the bore well.
   - **Behavior:** It verifies that the number of pipes matches a predetermined value of 10. If not, it raises an assertion error.

3. **SizeOfPipe(uint256 pipeSize)**
   - **Purpose:** This function evaluates the size of pipes used in the bore well.
   - **Parameters:**
     - `pipeSize`: The size of the pipe in millimeters.
   - **Behavior:** It checks if the provided pipe size is recommended. If the size is less than 10mm, it reverts the transaction with an error message indicating that the pipe size is not suitable.



**Author:**

Nishanth Chandrashekar

