# Research notes and references

## Established project direction

The team's Notion page identifies the Go2 EDU, an NVIDIA Orin NX computer, and the SEA-NAV RL policy as the intended platform and software direction. It expresses a preference for Unitree's Python and/or ROS 2 interfaces.

The immediate priority is Jetson setup. The page does not establish a completed installation, tested integration, or experimental result.

## References from Notion

| Reference | Intended use |
| --- | --- |
| [Team Notion page](https://app.notion.com/p/Unitree-GO2-quadruped-3dbe4fdd9add80f19abaf9b2e86ce5e7) | Shared project context; access may require sign-in |
| [SEA-NAV code](https://github.com/11chens/SEA-Nav-Code) | Target RL policy and deployment implementation to review |
| [Unitree developer documentation](https://support.unitree.com/home/en/developer/Application_development) | Official development documentation |
| [Unitree SDK2 Python](https://github.com/unitreerobotics/unitree_sdk2_python) | Candidate Python robot interface |
| [Unitree ROS 2](https://github.com/unitreerobotics/unitree_ros2) | Candidate ROS 2 integration |
| [Unitree SDK2 C++](https://github.com/unitreerobotics/unitree_sdk2) | Additional official SDK reference |
| [Go2 user manual](https://marketing.unitree.com/article/en/Go2/User_Manual.html) | Robot operation and hardware reference |
| [Agile But Safe](https://agile-but-safe.github.io/) | Hardware deployment reference to assess for applicability |
| [MiniCPM Go2 deployment](https://github.com/OpenBMB/MiniCPM-Robot/blob/main/MiniCPM-RobotTrack/docs/GO2_DEPLOYMENT.md) | Go2/Jetson setup reference to assess against our hardware |

These links were collected from the project page. Inclusion does not mean that a reference's hardware, dependency versions, wiring, or deployment procedure has been verified for our system.

## Architecture requiring verification

The page proposes ROS 2 for perception/localization and `unitree_sdk2_python` for final Go2 state/control communication. It explicitly says its SEA-NAV deployment flowchart was summarized by GPT and should be double-checked.

Before implementing that diagram, review the upstream code and document:

- Which processes run on the Jetson and which services run on the robot.
- Which sensors, topics, coordinate frames, and policy observations are required.
- How navigation actions reach the locomotion controller.
- Which component owns robot motion commands.
- Whether high-level or low-level control is required and what initialization it needs.
- Which software versions and model artifacts are compatible.

## Open project decisions

- What is the specific research question or hypothesis?
- Are we reproducing SEA-NAV, adapting it, or comparing it with another method?
- What hardware and sensors are already available?
- What environments and tasks will be evaluated?
- What metrics and baselines will define success?
- Where will large recordings, model weights, and experiment outputs be stored?

## Decision log

Add confirmed decisions here as the project progresses. Distinguish a proposal from a decision tested on the robot.

| Date | Decision / observation | Evidence / rationale |
| --- | --- | --- |
| 2026-10-22 | Initialize documentation from the team's Notion page | No implementation or validated deployment configuration exists in this repository yet |
