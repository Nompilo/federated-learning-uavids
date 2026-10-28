# federated-learning-uavids

This repository contains the official codebase for the paper: "Adversarial Robustness of Federated Learning for UAV Intrusion Detection in Satellite-Terrestrial Integrated Networks."

This repository offers a fully reproducible pipeline to assess the robustness of Federated Learning (FL) models against adversarial attacks. Using the UAVIDS-2025 dataset, we benchmark four lightweight architectures (MLP, 1D-CNN, GRU, and Autoencoder) against data poisoning (label flipping), model poisoning (weight scaling), backdoor, and Sybil attacks. We also evaluate the performance of Byzantine-robust aggregation algorithms (Krum, Multi-Krum, Trimmed Mean, Median) compared to standard FedAvg and FedDWM.

Key Findings:

* Standard supervised models (MLP, 1D-CNN, GRU) are highly vulnerable to model poisoning and collapse into degenerate states (AUC = 0.500).
* The unsupervised Autoencoder is inherently resilient to data poisoning.
* Distance-based robust aggregators (Krum, Multi-Krum) preserve non-trivial signal detection (AUC up to 0.886) even when supervised models collapse
