# PLC Based Medication Dispensing System
### This project presents a fault-tolerant PLC-based medication dispensing system designed to improve safety, reliability, and uptime in medical environments. By applying Reliability-Centered Maintenance (RCM) principles and integrating fault-handling logic into Siemens PLC, this system ensures continuous operation and precise medication delivery even under fault conditions.

## Features
Custom logic implemented in Siemens TIA Portal to detect, isolate, and recover from common faults.

Failure Modes and Effects Analysis and Reliability Block Diagrams used to model system reliability and optimize control strategies.

Stress testing and redesign reduced system downtime by identifying and mitigating high-risk failure points.

Simulated extreme operational scenarios to validate system robustness.

Intelligent fallback routines for critical modules such as dosage counters, actuator control, and input sensors.

## System Architecture


<img width="545" alt="Screenshot 2025-05-19 195457" src="https://github.com/user-attachments/assets/30ba638b-37e7-4246-937a-6cc6ef14ef2d" />


## PLC Environment
Platform: Siemens TIA Portal (v16 or higher)

PLC Used: Siemens S7-1200

Programming Language: Ladder Logic (LD) with support blocks in Function Block Diagram (FBD)

## Key Modules
Main_Logic: Core dispensing process with state transitions

Fault_Handler: Detects sensor/actuator failures, triggers alarms or fallback actions

Redundant_Sensors: Cross-verification of critical sensor readings

Data_Logger: Logs fault events, operational cycles, and system state transitions

Emergency_Mode:	Reduced-functionality mode ensuring safe minimal dispensing during failure

## Reliability Engineering Approach

### Failure Modes and Effects Analysis (FMEA)
Identified failure modes for input interfaces, sensor misreads, mechanical jamming, power failure

Prioritized risks using Risk Priority Number (RPN)

Mitigation strategies integrated into control logic

### Reliability Block Diagrams (RBD)
Modeled critical paths in dispensing sequence

Redesigned system to introduce redundancy and reduce single points of failure

### Stress Testing Protocol
Simulated over 1000 operational cycles under variable load and power conditions

Injected faults to validate fallback and logging mechanisms

## Results
Reduced Failure Rate by eliminating critical single points of failure.

Increased Uptime by 22% compared to baseline dispensing system.

Improved Safety through real-time fault isolation and graceful degradation of services.

## How to Run:
Open Siemens TIA Portal and load the project from the PLC_Project/ folder.

Connect to a Siemens S7-1200 PLC or simulate using TIA's built-in PLC simulator.

Monitor variable states, alarm outputs, and cycle logging during test execution.

## Future Improvements
Integration with HMI for better fault visibility

Real-time network logging to hospital management system

Automated fault classification using machine learning
