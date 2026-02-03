# EGT-POMDP-Adaptive-Honeypot-Deployment-Deception-Framework
This Python script is a cybersecurity simulation framework designed to model and optimize honeypot deployment strategies in SDN environments. It combines Evolutionary Game Theory and Partially Observable Markov Decision Processes (POMDP) to simulate the dynamic interactions between network attackers and defenders.
# EGT-POMDP: Adaptive Honeypot Deployment Framework
## 📋 Project Overview
This project simulates an advanced Cyber Deception Defense mechanism using **Evolutionary Game Theory (EGT)** and **Partially Observable Markov Decision Processes (POMDP)**. 
The framework models the interaction between a sophisticated attacker and an adaptive defender in an SDN-like environment. The goal is to dynamically optimize the deployment of **Honeypots (Honey-baits)**—fake vulnerabilities designed to lure attackers—thereby protecting real assets (CVEs) and exhausting attacker resources.
## ✨ Key Features
### 1. Multi-Layer Decision Engine
* **Short-term Adaptation:** Uses **Replicator Dynamics** to adjust defense strategies based on immediate attacker behavior.
* **Long-term Planning:** Implements a **Bellman Optimal Equation** loop to solve POMDPs, allowing the defender to make non-myopic deployment decisions (Horizon planning).
### 2. Realistic Vulnerability Management (`CVEManager`)
* Simulates real-world vulnerabilities (CVE-2018-XXXX, etc.).
* Calculates **Similarity Scores** between Real Assets and Honeypots using attributes like Port, CVSS score, and Response Signatures.
* Includes "Deception Effect" logic where honeypot believability decays over time if deployed statically.
### 3. Bayesian Attacker Model
* The attacker is not static; they maintain a "Belief" state about the network.
* Uses **Bayesian Inference** to update the probability of a target being a honeypot based on interaction feedback.
### 4. Comprehensive Analysis & Visualization
* **Ablation Studies:** Built-in comparison engine to test Dynamic vs. Static vs. Random deployment strategies.
* **Metrics:** Tracks Defense Success Rate, Attacker/Defender Utility, Trap Efficiency, and Link Crossover Rounds.
* **Visuals:** Generates evolution curves, radar charts, and stack plots for academic reporting.
## 🛠️ Requirements
The simulation requires Python 3.8+ and the following libraries:
```bash
pip install numpy pandas matplotlib scipy sympy torch
