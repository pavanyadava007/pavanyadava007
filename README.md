# Hi, I'm Pavan

M.Sc. student at FAU Erlangen-Nürnberg, specializing in AI in autonomous driving, based in Germany. I have hands-on ADAS experience from Continental (radar test automation, camera functions in C++) and AUMOVIO (explainable AI for an end-to-end driving model).

I am most interested in vehicle motion prediction and state estimation, sensor fusion and real-time C++.

In my own projects I use public real-world data where I can (nuScenes, RadioML, real cell test data), let scripts write every number, and put the limits next to the results: what was simulated, what ran only on x86, what did not work.

**Tech:** Python (NumPy, PyTorch), C++17, C, Bazel/CMake, Linux, Docker, TensorRT, CAN/IMU/radar/camera data.

## Selected projects

Every number below is taken from the project's own README, where the scripts and data behind it are described.

| Project | What it is | Measured result | Links |
|---|---|---|---|
| **drive-replay** | Replay tooling for an ADAS stack plus vehicle dynamics and ego motion prediction on real nuScenes CAN data (Python, C++17) | Yaw-rate RMSE 0.357 deg/s with the dynamic single-track model vs 0.458 deg/s kinematic (192 test scenes) | [Code](https://github.com/pavanyadava007/drive-replay) / [Demo](https://huggingface.co/spaces/pavanyadava07/drive-replay) |
| **motor-led-mw** | C99 motor + LED middleware on Zephyr with TrustZone (QEMU), an agent that writes on-target unit tests, and a BMS module with an EKF SoC estimator | EKF SoC RMSE 0.57 to 0.86 % on held-out drive cycles at 25 degC from a 20 % initial error, where Coulomb counting stays at about 20 % | [Code](https://github.com/pavanyadava007/motor-led-mw) / [Demo](https://huggingface.co/spaces/pavanyadava007/motor-led-mw) |
| **offroad-bevfusion** | Camera + LiDAR + radar BEV perception (3D detection, BEV segmentation, occupancy) with TensorRT, a C++ runner and ROS 2 | 30 Hz C++ TensorRT loop under CPU load: p99 46.65 ms and 2229 missed deadlines without mitigation, 19.47 ms and 0 with SCHED_FIFO (6000 iterations) | [Code](https://github.com/pavanyadava007/offroad-bevfusion) / [Demo](https://huggingface.co/spaces/pavanyadava07/offroad-bevfusion) |
| **sigint-fusion** | Signal analysis platform: Kafka ingest, ONNX modulation classifier, Kalman/Hungarian emitter fusion, LangGraph analyst agent | 75.7 % val top-1 on 21-class modulation classification (real DeepSig RadioML, 1024 samples) | [Code](https://github.com/pavanyadava007/sigint-fusion) / [Demo](https://huggingface.co/spaces/pavanyadava07/sigint-fusion) |
| **langgrasp** | Language-guided pick-and-place on a simulated SO-101 arm (Grounding DINO, YOLO11-seg, depth fusion, ACT, PPO, safety monitor) | Modular language pipeline placed 115/120 (95.8 %) in MuJoCo | [Code](https://github.com/pavanyadava007/langgrasp) / [Demo](https://huggingface.co/spaces/pavanyadava07/langgrasp) |
| **assembly-lab** | Learned insertion with 1 mm clearance on a simulated Franka Panda with a wrist force-torque sensor | Behavior cloning 179/200 (89.5 %) nominal, 156/200 without the F/T input (McNemar p = 1.4e-3) | [Code](https://github.com/pavanyadava007/assembly-lab) / [Demo](https://huggingface.co/spaces/pavanyadava07/assembly-lab) |

## Contact

[LinkedIn](https://linkedin.com/in/pavan-yadav-annappa-840538161) / pavanyadava07@gmail.com
