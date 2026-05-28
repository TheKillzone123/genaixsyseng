# System Requirements

This document contains the system requirements for the Traffic Light System, derived from the use cases using INCOSE requirements engineering principles.

## Functional Requirements

| Req ID | Requirement Name | Requirement Text | Type | Source | Verify Method |
|--------|------------------|------------------|------|--------|----------------|
| FR-001 | Initialize Traffic Light Cycle | When the system boots, the system shall initialize the traffic light cycle starting with the red LED illuminated. | Functional | UC1, UC6 | Test, Demonstration |
| FR-002 | Display Red Light Phase | The system shall display the red LED during the first phase of the traffic light cycle. | Functional | UC1, UC2 | Test, Inspection |
| FR-003 | Display Green Light Phase | After displaying the red LED, the system shall display the green LED. | Functional | UC1, UC3 | Test, Inspection |
| FR-004 | Display Yellow Light Phase | After displaying the green LED, the system shall display the yellow LED. | Functional | UC1, UC4 | Test, Inspection |
| FR-005 | Cycle Repetition | After displaying the yellow LED, the system shall return to displaying the red LED and continue the cycle indefinitely. | Functional | UC1 | Test, Demonstration |
| FR-006 | Turn Off All Lights on Button Press | When the operator presses the toggle button during an active traffic light cycle, the system shall deactivate all LEDs (red, green, and yellow). | Functional | UC5 | Test, Demonstration |
| FR-007 | Resume Traffic Light Cycle | When the operator presses the toggle button while all LEDs are off, the system shall restart the traffic light cycle, beginning with the red LED. | Functional | UC6 | Test, Demonstration |

## Non-Functional Requirements

| Req ID | Requirement Name | Requirement Text | Type | Source | Verify Method |
|--------|------------------|------------------|------|--------|----------------|
| NFR-001 | Button Response Time | The system shall respond to a button press (toggle on/off) within 100 milliseconds. | Performance | System Design | Test, Analysis |
| NFR-002 | LED Display Duration | Each LED phase (red, green, yellow) shall be displayed for a minimum of 2 seconds and a maximum of 5 seconds. | Performance | System Design | Test, Analysis |
| NFR-003 | Hardware Platform | The system shall be implemented on a Raspberry Pi with GPIO support for digital output and input. | Design Constraint | Project Specification | Inspection |
| NFR-004 | LED Interface | The system shall control exactly three colored LEDs (red, green, yellow) via individual GPIO pins with appropriate current-limiting resistors. | Interface | Project Specification | Inspection, Test |
| NFR-005 | Button Interface | The system shall support a single toggle button for user interaction via a dedicated GPIO pin with debouncing logic. | Interface | System Design | Inspection, Test |
