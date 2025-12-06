# Chapter 7 — Hardware & Lab Setup

Physical AI requires **specialized hardware** to bridge the gap between simulation and real-world deployment.  
This chapter explains **workstations, edge devices, sensors, and robot labs** necessary to run the course successfully.

---

## 🌐 Why Hardware Matters

- Physics simulation and AI perception are **computationally intensive**  
- Realistic humanoid deployment requires **low-latency processing**  
- Edge computing demonstrates **resource constraints** compared to cloud workstations  

---

## 🖥️ Digital Twin Workstation (Required per Student)

A high-performance workstation is critical for simulation, rendering, and AI training.

### Recommended Specs:
| Component | Minimum | Recommended |
|-----------|---------|-------------|
| GPU | RTX 4070 Ti (12GB VRAM) | RTX 3090 / 4090 (24GB VRAM) |
| CPU | Intel Core i7 / AMD Ryzen 9 | Intel Core i9 / AMD Ryzen 9 7950X |
| RAM | 32 GB DDR5 | 64 GB DDR5 |
| OS | Ubuntu 22.04 LTS | Ubuntu 22.04 LTS |

**Notes:**  
- GPU handles **simulation and Vision-Language-Action models**  
- CPU performs **rigid body physics and Gazebo calculations**  
- Ubuntu preferred for ROS 2 native compatibility  

---

## 🧠 Physical AI Edge Kit

Edge devices allow **deployment of AI nodes on low-power hardware**, demonstrating real-world constraints.

### Components:
| Component | Model | Notes |
|-----------|-------|------|
| Brain | NVIDIA Jetson Orin Nano (8GB) / Orin NX (16GB) | Runs ROS 2 inference stack |
| Vision | Intel RealSense D435i / D455 | RGB + Depth + IMU sensors |
| Balance | BNO055 IMU (USB) | Often integrated in RealSense |
| Voice Interface | ReSpeaker USB Mic Array v2.0 | For Whisper voice commands |
| Storage & Power | SD Card (128GB) + Jumper Wires | Required for OS and edge connectivity |

**Cost:** ~\$700 per student kit  

---

## 🤖 Robot Lab Options

Depending on budget and goals, three approaches are possible:

### Option A — Proxy Robot (Budget-Friendly)
- Robot: Unitree Go2 Edu (~\$1,800–\$3,000)  
- Pros: Durable, ROS 2 compatible, affordable  
- Cons: Quadruped (not humanoid)  
- Use: Kinematics, perception, AI deployment practice  

### Option B — Miniature Humanoid
- Robot: Hiwonder TonyPi Pro (~\$600), Robotis OP3 (~\$12k)  
- Pros: Humanoid form factor for locomotion and manipulation  
- Cons: Limited processing; cannot run Isaac ROS efficiently  
- Use: Walking and grasping simulations, edge AI nodes  

### Option C — Premium Humanoid
- Robot: Unitree G1 Humanoid (~\$16k)  
- Pros: Full humanoid with dynamic walking, open SDK  
- Use: Sim-to-Real capstone deployment  

---

## ☁️ Cloud-Based Lab (Optional / High OpEx)

For students without RTX machines, cloud instances can host simulations:

- AWS G5/G6 instances (~\$1.50/hour) with 24GB GPU  
- Isaac Sim Omniverse Cloud for simulation  
- Edge kits required for real-world deployment  
- Latency is a concern; models must be trained in cloud, then flashed to Jetson  

---

## ⚡ Summary of Architecture

| Component | Hardware | Function |
|-----------|---------|---------|
| Sim Rig | PC with RTX GPU + Ubuntu 22.04 | Runs Isaac Sim, Gazebo, Unity, AI training |
| Edge Brain | Jetson Orin Nano | Runs inference stack for AI control |
| Sensors | RealSense Camera + LiDAR | Feeds real-world data to AI |
| Actuator | Unitree Go2 / G1 | Executes motion and manipulation commands |

---

## 🔧 Key Takeaways

- High-performance **workstation required** for simulation  
- Edge devices demonstrate **resource-constrained deployment**  
- Robot lab depends on budget: proxy, miniature humanoid, or premium  
- Cloud lab is viable but introduces **latency and cost challenges**  
- Capstone project integrates **simulation, AI, edge deployment, and hardware**  

---

**This concludes the main chapters of your textbook.**  

---

If you want, I can now **compile all 7 chapters in order with final `.md` filenames and sidebar ready**, so you can **drop them into Docusaurus and have a fully functional book** without any missing chapters.  

Do you want me to do that next?
