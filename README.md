# A Robust PPO-optimized Tabular Transformer for Intrusion Detection in Industrial IoT Systems

This repository contains the official implementation of our novel framework for robust intrusion detection on the TON_IoT dataset. It combines the strengths of the Tabular Transformer with Proximal Policy Optimization (PPO) to achieve exceptional classification accuracy, especially on imbalanced and rare classes.

## 🔍 Key Highlights

- 📊 Achieves **98.85% accuracy** on the TON_IoT test set
- 🚨 Excels at detecting rare attack types such as **MITM**
- 🧠 Integrates **reinforcement learning reward shaping**, including:
  - Prediction-based rewards
  - Confidence-adjusted rewards
  - Log-scaled temporal penalty for sequential mistakes

## 📐 Architecture

![Architecture Diagram](./architecture.png)

## 🧪 Experimental Results

| Model Variant         | Accuracy | Macro F1 | MITM F1 |
|----------------------|----------|----------|---------|
| Ours (PPO + TabTF)   | 98.85%   | 97.73%   | 0.8879  |
| TabTF w/o PPO        | 94.0%    | 92.0%    | 0.9000  |
| PPO + MLP            | 96.54%   | 86.67%   | 0.0000  |

## 🏗️ How to Run

```bash
git clone https://github.com/yourusername/ppo-tab-transformer-nids.git
cd ppo-tab-transformer-nids
pip install -r requirements.txt
python train.py
