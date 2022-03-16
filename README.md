# CMOS-Implementation-of-8bit-Wallace-Tree-Multiplier
This repository presents the design of 8bit Wallace Tree Multiplier using Synopsys Custom Compiler on 28nm CMOS Technology.
# Table of Content
- [Abstract]()
- [Detailed Explanation]()
- [Reference Circuit]()
- [Tools Used]()
- [CMOS NOT Gate]()
- [CMOS AND Gate]()
- [CMOS OR Gate]()
- [CMOS Ex-OR Gate]()
- [Half Adder Module]()
- [Full Adder Module]()
- [CMOS 8X1 Multiplier]()
- [Design Approach]()
- [LAYER1-Group 1 Reduction]()
- [LAYER1-Group 2 Reduction]()
- [LAYER1-Group 3 Reduction]()
- [LAYER2-Group 4 Reduction]()
- [LAYER3-Group 5 Reduction]()
- [LAYER3-Group 6 Reduction]()
- [Ripple Carry Adder]()
- [Layer4 Reduction]()
- [Wallace tree Symbol]()
- [DC Analysis Testbench]()
- [Simulation Result]()
- [Netlist]()
- [Author]()
- [Acknowledgements]()
- [References]()

# Abstract
A Wallace multiplier is a hardware implementation of a binary multiplier, a digital circuit that multiplies two integers. It uses a selection of full and half adders (the Wallace tree or Wallace reduction) to sum partial products in stages until two numbers are left. Wallace multipliers reduce as much as possible on each layer.
Wallace multipliers were devised by the Australian computer scientist Chris Wallace in 1964.

The Wallace tree has three steps:
1. Multiply each bit of one of the arguments, by each bit of the other.
2. Reduce the number of partial products to two by layers of full and half adders.
3. Group the wires in two numbers, and add them with a conventional adder.

# Introduction
The Wallace tree is a variant of long multiplication.
- The first step is to multiply each digit (each bit) of one factor by each digit of the other. Each of this partial products has weight equal to the product of its factors. The final product is calculated by the weighted sum of all these partial products.
- In the second step, the resulting bits are reduced to two numbers; this is accomplished as follows: As long as there are three or more wires with the same weight add a following layer:-
1. Take any three wires with the same weights and input them into a full adder. The result will be an output wire of the same weight and an output wire with a higher weight for each three input wires.
2. If there are two wires of the same weight left, input them into a half adder.
3. If there is just one wire left, connect it to the next layer.
- In the third and final step, the two resulting numbers are fed to an adder, obtaining the final product.

![image](https://user-images.githubusercontent.com/100506744/158533667-cecc8ff5-705c-41f0-9f74-feb3af63b90c.png)
# Tools Used
- **Synopsys Custom Compiler**:  The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. This tool was used to design the circuit on a transistor level.
- **Synopsys Primewave** :  PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform. This tool helped in various types of simulations of the above designed circuit.
- **Synopsys 28nm PDK** :  The Synopsys 28nm Process Design Kit(PDK) was used in creation and simulation of the above designed circuit.
# CMOS NOT gate
![image](https://user-images.githubusercontent.com/100506744/158535775-2efb9fb9-4776-4e3a-8993-b0a46bd58fca.png)

# CMOS AND gate
![image](https://user-images.githubusercontent.com/100506744/158536267-f39048a1-5d05-4716-8c1f-02e86f82c081.png)

# CMOS OR gate
![image](https://user-images.githubusercontent.com/100506744/158536415-a716e915-ee05-41f3-8179-4439b254bb94.png)

# CMOS EX-OR gate
![image](https://user-images.githubusercontent.com/100506744/158536604-854d3d0f-6de7-4ff7-8126-bc0160e82795.png)

# Half Adder
![image](https://user-images.githubusercontent.com/100506744/158536684-d0cbb377-c3fd-4434-89c4-e5e31d5c4c2e.png)

# Full Adder
![image](https://user-images.githubusercontent.com/100506744/158537398-fd6db1f8-1579-43a9-9bac-08ff5f99b96b.png)

# 8X1 Multiplier
![image](https://user-images.githubusercontent.com/100506744/158537510-b20ded4d-b593-4445-98d0-391459d68952.png)

# Design Approach

# layer1 - group 1 Reduction
![image](https://user-images.githubusercontent.com/100506744/158537971-75fd149d-719c-4a96-b55f-f25116d45bb2.png)

# layer1 - group 2 Reduction
![image](https://user-images.githubusercontent.com/100506744/158538092-36bae742-906e-47d8-a4d0-ff1924211a52.png)

# layer1 - group 3 Reduction
![image](https://user-images.githubusercontent.com/100506744/158538204-6604d662-078c-4d7b-8dd0-8d00220d1a26.png)

# layer2 - group 4 Reduction
![image](https://user-images.githubusercontent.com/100506744/158538274-b812a7b5-1a9f-4bbd-b7ce-92c245d269e6.png)

# layer3 - group 5 Reduction
![image](https://user-images.githubusercontent.com/100506744/158538408-3efed4a0-7e3a-4bb0-bb9a-b206a5d5544c.png)

# layer3 - group 6 Reduction
![image](https://user-images.githubusercontent.com/100506744/158538491-ad49f3ab-07d5-45cf-bcc7-f8fa1cdd1c6c.png)

# Ripple carry Adder Reduction
![image](https://user-images.githubusercontent.com/100506744/158538929-9b4e2538-b6a6-4809-899f-efff20aa0110.png)

# layer 4 Reduction
![image](https://user-images.githubusercontent.com/100506744/158539059-28a357ca-7c66-4fef-a7e1-580a484ee77e.png)

# Wallace tree symbol
![image](https://user-images.githubusercontent.com/100506744/158539234-90caf8ca-4fc9-483f-889a-9a0e2ce92bb1.png)

# DC Analysis Testbench
![image](https://user-images.githubusercontent.com/100506744/158539571-6d305388-d01a-4032-a8f6-d9c0cbb4243f.png)

# Simulation Result
![image](https://user-images.githubusercontent.com/100506744/158546209-e9d7ac0a-7adc-45b5-9528-525d6c144743.png)

![image](https://user-images.githubusercontent.com/100506744/158546823-43e9c75e-969d-4d1d-b91b-fd4c0618419a.png)

# Netlist
Refer to the netlist of the circuits here: [Netlist](https://github.com/ashutoshkumar9951/CMOS-Implementation-of-8bit-Wallace-Tree-Multiplier/blob/main/Netlist)

# Author
Ashutosh kumar, Btech in Electronics and Communication Engineering.
J.C. Bose University of Science and Technology, YMCA Faridabad (Haryana)

# Acknowledgements
- [Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
- [Cloud Based Analog IC Design Hackathon](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/')
- [Synopsys India](https://www.synopsys.com/)
- [Sameer Durgoji, NIT Karnataka](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)
- [Chinmay panda, IIT Hyderabad](https://www.iith.ac.in/events/2022/02/15/Cloud-Based-Analog-IC-Design-Hackathon/)

# References
- [1] C.S. Wallace, A suggestion for a fast multiplier, IEEE Trans. Computers, Vol. 13, pp. 14-17, Feb. 1964.
- [2] https://en.wikipedia.org/wiki/Wallace_tree
- [3] K. Prasad and K.K. Parhi, Low-power 4-2 and 5-2 compressors, Proc. of 2001 Asilomar Conf. on Signals, Systems and Computers, Pacific Grove, CA, USA.
- [4] Neil H. Weste and Kamran Eshraghian, Principles of CMOS VLSI design-A Systems Perspective, Pearson Edition Pvt Ltd. 3rd edition.
- [5] N. Sureka ; R. Porselvi ; K. Kumuthapriya, “An Efficient High Speed Wallace Tree Multiplier”, 2013 International Conference on Information Communication and Embedded Systems (ICICES). Technologies







