# Spatio-Temporal Human Detection and Survivability Prioritization

This capstone project is the work of [Divyansh Kumar](https://github.com/divyansh-1611), [Sarthak Sharma](https://github.com/Sarthak061), and [Raghav Deshwal](https://github.com/rdeshwal731).

## Project Overview

Disaster scenarios often overwhelm manual triage efforts, highlighting the need for intelligent systems to aid in rapid decision-making. This project presents a framework using computer vision and reinforcement learning (RL) to automate human detection and assign survival priority scores from disaster footage. By analyzing complex scenes efficiently, it aims to support emergency response teams in prioritizing aid based on nuanced survival cues.

## Methodology

### Two-Stage Pipeline

1. **Feature Extraction**: Using EfficientNet-B0, a deep learning model, we extract high-dimensional feature vectors (d=1280) from individuals detected in the challenging C2A dataset. These features capture visual cues such as posture, injuries, and environmental threats.

2. **Dynamic Scene Graphs (DSGs)**: Contextual information is captured by constructing DSGs, which represent humans and significant environmental elements as nodes, with edges encoding spatial proximity, potential interactions, and relationships to hazards.

3. **Survival Prioritization**: In the second stage, a Soft Actor-Critic (SAC) reinforcement learning agent processes the extracted features and DSG representations. The SAC agent assigns a continuous survival priority score (0-1) to each individual, optimizing for individuals with a higher likelihood of survival.

### Key Technologies

- **EfficientNet-B0**: A deep learning architecture that balances efficiency and accuracy for extracting features.
- **Dynamic Scene Graphs (DSGs)**: Graph-based representation that models spatial-temporal dependencies and interactions within the disaster scene.
- **Soft Actor-Critic (SAC)**: A reinforcement learning algorithm used to assign survival priority based on the visual and contextual information in the scene.

## Results

The system was trained with a focus on robustness and effective triage decision-making. Reward curves from the training process show clear convergence, indicating stable learning, while policy outputs demonstrate a high level of accuracy in assigning priority scores. This approach successfully integrates visual cues and relational data to emulate complex triage decisions.
