# Project Charter

## Project title

`MCU Based Environmental Sensor Node with Long-Range Wireless Communication `

## Problem and motivation

`[What problem or opportunity does this project address, and why does it matter?]`
The goal of this project is to investigate how embedded devices can communicate with each other to perform a task despite being separated by a large distance. This is important for applications where environmental data must be collected from places that are dangerous or difficult for humans to access.

This project will focus on collecting environmental data at a remote sensing node and reliably transmit that data to a base station to display.

## Intended users and stakeholders

`[Identify the people affected by or interested in the system.]`

Potential users of this system is anyone who needs to remotely monitor environmental conditions in locations where human access is dangerous or difficult to access. Possible applications include monitoring hazardous environments.

## Baseline system or starting point

`[Describe existing hardware, software, prior project, or reference design.]`
The current baseline system consists of two TM4C123 microcontrollers, and TMP36 temperature sensor, and an Analog to Digital Converter driver written in C. The existing software lets the TM4C123 to sample analog sensor data.

## Proposed research and development extension

`[Explain what will be added, changed, or investigated.]`
A long range wireless communication system will be researched and integrated with the two TM4C123 microcontrollers.
One microcontroller will operate as a remote sensing node that gathers environmental data and transmits it wirelessly. The second microcontroller will operate as a base station that receives, validates and displays the transmitted data.

Additional environmental sensors, and their corresponding software drivers will also be developed and integrated as hardware becomes available.

The completed system will be tested at different distances to determine the reliability and practical range of the wireless communication link.


 
## Primary research question

`[Write one focused question that can be answered with evidence.]`
To what extent can a TM4C123 based environmental sensor node reliably transmit usable sensor data to a remote base station over a long range wireless communication link.

## Supporting questions

- `[Question 1]`
 What hardware and communication method are best for transmitting and receiving sensor data over a large distance?
  
- `[Question 2]`
How can the system determine whether data received by the base station is correct and has not been corrupted during transmission?

## Scope and boundaries

### Included

- `[Minimum capability]`
- Microcontroller 1 will operate as the remote sensor node.
- The sensor node will collect environmental data.
- Environmental data will be sent wirelessly.
- Microcontroller 2 will operate as the base station.
- The base station will receive and interpret transmitted data.
- The system will include a method for detecting invalid or corrupted data.
- Received sensor data will be formatted and displayed to a terminal.
- Communication reliability will be tested at multiple distances.
  
### Excluded or stretch goals

- `[Item intentionally outside the minimum scope]`
- Multiple remote sensing nodes.
- Internet or cloud connections.
- Battery optimization.

## Constraints and risks

| Constraint or risk | Likely effect | Planned response |
|---|---|---|
| `[Item]` | `[Effect]` | `[Response]` |
| `Wireless interference & obstacles` | `Packet loss or corrupted data` | `Examine received data` |
| `Data corruption` | `Incorrect sensor values could be interpreted as valid` | `Implement and error detection method` |
| `Sensor and ADC noise` | `Sensor reading fluctuate` | `Get a baseline of sensor measurements before wireless test` |
| `Hardware/Software Integration` | `Individual components may work separately but fail when integrated` | `Develop and test each system incrementally` |
## Preliminary success criteria

| Criterion | Target | Evidence |
|---|---:|---|
| `[Measurable outcome]` | `[Value]` | `[Test or artifact]` |
| `Environmental Sensing` | `1 Environmental sensor sampled successfully` | `Sensor reading & Code` |
| `Wireless Communication` | `Successful wireless data transfer between the 2 MCUs` | `Terminal Output and system demo` |
| `Data Integrity` | `System can identify invalid packets` | `Error detection testing` |

