# Go2 Jetson Navigation

Research workspace for deploying the **SEA-NAV reinforcement-learning navigation policy** on a **Unitree Go2 EDU quadruped**, using an **NVIDIA Jetson Orin NX** as the onboard research computer.

## Project status

This repository is in the planning and hardware setup stage. It currently contains documentation only: no robot-control code, trained policies, or validated deployment configuration.

The immediate milestone is to identify the available hardware, establish Jetson–Go2 communication, and verify access to robot state and required sensors before integrating navigation software.

## Planned scope

- Set up the Jetson Orin NX and its connection to the Go2 EDU.
- Establish a reproducible software environment and record hardware-specific configuration.
- Evaluate and integrate the [SEA-NAV policy and deployment code](https://github.com/11chens/SEA-Nav-Code).
- Validate perception, localization, navigation, and the robot-control interface in stages.
- Record experiments, results, and deployment procedures so collaborators can reproduce them.

The exact research question, evaluation metrics, and experimental protocol remain to be defined.

## Proposed system

The project notes describe the following candidate architecture:

```text
Sensors -> ROS 2 perception/localization -> SEA-NAV policy stack
                                              |
                                  Unitree SDK2 Python interface
                                              |
                                           Go2 EDU
```

**This is a proposal, not a verified implementation.** The Notion page identifies its deployment flowchart as GPT-generated and requiring a check against the SEA-NAV repository. The policy inputs and outputs, sensor requirements, control mode, and division between navigation and locomotion must be confirmed from the upstream code.

The preferred interfaces in the project notes are `unitree_ros2` and/or `unitree_sdk2_python`. Their exact responsibilities will be documented after that review.

## Start here

1. Work through the [hardware and software setup checklist](docs/setup-checklist.md).
2. Review the [project references and open questions](docs/research-notes.md).
3. Record actual hardware and software details before selecting installation or deployment instructions.

## Documentation

| File | Purpose |
| --- | --- |
| [Setup checklist](docs/setup-checklist.md) | Bring-up milestones and hardware inventory |
| [Research notes](docs/research-notes.md) | Sources, assumptions, and unresolved design decisions |
| [.gitignore](.gitignore) | Keep local environments, credentials, recordings, and large model artifacts out of Git |

## Collaboration

Keep setup instructions tied to the hardware and versions actually tested. For experiments, record the code revision, policy source, configuration, and results. Link large datasets and model artifacts instead of committing them directly.

This repository documents our integration work. Refer to each upstream project for its own license and reuse conditions before incorporating its code or models.

## Source of these notes

Initial documentation was prepared on **2026-10-22** from the team's [Unitree GO2 quadruped Notion page](https://app.notion.com/p/Unitree-GO2-quadruped-3dbe4fdd9add80f19abaf9b2e86ce5e7), which may require workspace access. Linked deployment instructions have not yet been validated on our hardware.
