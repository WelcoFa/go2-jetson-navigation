# Jetson and Go2 setup checklist

This checklist defines planned work. Unchecked items have not been verified by this repository.

## 1. Record the hardware

| Item | Current record |
| --- | --- |
| Robot | Unitree Go2 EDU; exact configuration to confirm |
| Research computer | NVIDIA Jetson Orin NX planned; installed module and memory to confirm |
| Carrier board / expansion dock | To confirm |
| Standalone or robot-mounted Jetson | To confirm |
| Power supply / harness | To confirm |
| Storage | To confirm |
| Sensors available to research software | To confirm |
| Ubuntu / JetPack versions | To confirm |
| Robot firmware / SDK versions | To confirm |

- [ ] Confirm the robot variant, Jetson module, carrier board, and physical connections.
- [ ] Record the existing operating system and installed software.
- [ ] Preserve any vendor configuration and identify a backup/recovery procedure before changing the installation.
- [ ] Verify the power, mounting, and cooling requirements against documentation for the actual hardware.

## 2. Establish communication

- [ ] Identify the robot-facing Ethernet interface and existing network configuration.
- [ ] Record the robot and Jetson addresses after verification; do not assume example addresses apply.
- [ ] Establish access to the Jetson and verify communication with the robot.
- [ ] Select the applicable Unitree SDK/ROS 2 setup instructions and record exact versions.
- [ ] Validate read-only robot telemetry before enabling motion commands.

## 3. Review SEA-NAV requirements

- [ ] Record the upstream SEA-NAV commit being evaluated.
- [ ] Identify its deployment entry points and required model/checkpoint files.
- [ ] Confirm policy observations, action outputs, update rates, and configuration files.
- [ ] Confirm required sensors, coordinate frames, and localization inputs.
- [ ] Confirm the boundary between navigation and locomotion.
- [ ] Confirm whether deployment uses high-level velocity commands or low-level joint commands.
- [ ] Verify the proposed ROS 2 / SDK2 Python split against the code.
- [ ] Record software compatibility and upstream license requirements.

## 4. Validate the integration in stages

- [ ] Check sensor data and localization independently.
- [ ] Run policy inference without publishing motion commands.
- [ ] Define the motion-command owner, stop procedure, stale-data behavior, and test area before robot trials.
- [ ] Follow the applicable Unitree procedure for the confirmed control mode.
- [ ] Complete an initial supervised trial and record observations.
- [ ] Document a repeatable startup and shutdown sequence.

## 5. Define experiments

- [ ] Agree on the research question and baseline.
- [ ] Choose tasks, environments, and evaluation metrics.
- [ ] Define how trials, configurations, and results will be recorded.
- [ ] Record failures and limitations alongside successful trials.

For each completed milestone, add the date, relevant versions/configuration, and evidence rather than only checking the box.
