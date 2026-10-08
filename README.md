**AI4OS: Online Operating-System Tuning**

Investigating AI-assisted runtime configuration of operating systems for cloud workloads.

**This is the project homepage. Currently its only purpose is to apply for a CloudLab account.**

AI4OS is an academic research project on online operating-system tuning. Its goal is to understand how learning-based methods can improve the performance and resource efficiency of cloud servers as workloads change. This page provides a high-level overview of the planned research and its experimental requirements.

Linux exposes configurable parameters across multiple subsystems. Their effects depend on the workload, hardware, and configuration of other subsystems. We plan to study runtime adjustment of these parameters using system telemetry and application-level performance feedback.

The experimental scope includes CPU scheduling, memory management, storage I/O, networking, interrupt handling, and CPU power management. We will examine throughput, tail latency, adaptation time, and tuning overhead under controlled workloads.

Initial work will reproduce selected experiments from existing research and establish comparable baselines. Candidate references include MLOS for automated experimentation and conventional optimization, OPPerTune for post-deployment online configuration tuning, and TuxBot for LLM-guided OS tuning. Where necessary, methods will be adapted to a common workload and parameter interface.
CloudLab's bare-metal access is needed to control host-level settings and observe their effects with predictable performance isolation. Conventional cloud VMs may hide or restrict physical CPU power controls, interrupt configuration, and other host-level interfaces. Experiments may also require rebuilding or modifying the Linux kernel to enable instrumentation or expose experimental controls on allocated nodes.

We plan to begin with small, time-bounded experiments using public benchmarks and synthetic data. Resources will be released when experiments finish, and CloudLab's management, monitoring, and access mechanisms will be preserved. The project is intended for non-commercial academic research, with findings to be disseminated through scholarly publications or research reports.

## Selected reference systems

**MLOS**  
[MLOS in Action: Bridging the Gap Between Experimentation and Auto-Tuning in the Cloud](https://www.vldb.org/pvldb/vol17/p4269-kroth.pdf). PVLDB, 2024. An experimentation and autotuning framework with pluggable optimizers. [Source code](https://github.com/microsoft/MLOS).

**OPPerTune**  
[OPPerTune: Post-Deployment Configuration Tuning of Services Made Easy](https://www.usenix.org/conference/nsdi24/presentation/somashekar). NSDI, 2024. Online configuration tuning using reinforcement learning. [Source code](https://github.com/microsoft/OPPerTune).

**TuxBot**  
[TuxBot: Semantic-Aware Online OS Tuning with Large Language Models](https://github.com/Columbia-DAP-Lab/TuxBot). An LLM-guided Linux tuning system.
