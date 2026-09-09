# Inferring lung cancer under limited learning data through gate-based and annealing-based quantum techniques

## Overview

Early diagnosis of lung cancer and reliable decision support are crucial steps since
this is a leading cause of cancer-related mortality worldwide. This research aims
to build an approach using quantum-assisted capacity that can infer lung cancer
from a limited amount of patient data. To do so, this research starts with a dataset
containing 309 patient records, which is augmented and balanced to 540 patient
records. This dataset has 16 attributes of symptom and risk-based lung cancer
factors. Following preprocessing on the dataset, this study uses a quantum method
named quadratic unconstrained binary optimization (QUBO) to select the relevant
features of the dataset. Three classifiers, quantum support vector machine (QSVM),
quantum k-nearest neighbor (QKNN), and quantum boosting (QBoost), are then
trained and tested on the processed dataset to identify lung cancer. These classifiers
are examined using different frameworks of circuit and annealing-based quantum
techniques. Only 108 balance samples are used during training the classifiers
to ensure the learning capability of the quantum method from limited data. To
safeguard against overfitting and underfitting due to a lack of data, the remaining
432 samples are evaluated to estimate prediction error. All experiments are done
using cross-validation. The final results demonstrate that the QSVM by D-Wave
framework achieves the best performance with an accuracy of 94.31% in simulation
and 91.90% in a real D-Wave quantum computer. The findings of this work show a
path for applying quantum computing to support healthcare decision-making when
data availability is often limited.

Discover Quantum Science
https://doi.org/10.1007/s44464-026-00038-4
---

## Project Structure

```text
Inferring Lung/
│
├── pennylane simulation/
│   └── pennylane_lung_svm_compare_80_test_432.ipynb
│
├── cirq Simulation/
│   └── cirq_lung_svm_compare_80_test_432.ipynb
│
├── openjij Simulation/
│   └── openjij_lung_svm_compare_80_test_432.ipynb
│
├── Qiskit_Simulation/
│   └── qiskit_lung_svm_compare_80_test_432.ipynb
│
├── Dwave simulation/
│   └── d_wave_lung_svm_compare_80_test_432.ipynb
│
├── Qwave QPU & HYBRID Solver/
│   └── qpu & h_solver.ipynb
│
├── IBM QPU & D-Wave QPU/
│   ├── ibm_QPU_svm_for_50_samples.ipynb
│   └── adv2_system_for_50samples.ipynb
│
└── README.md
```

---

## Objectives

The main objectives of this project are:

* Apply quantum machine learning techniques for lung classification.
* Compare quantum algorithms across multiple quantum frameworks.
* Evaluate quantum SVM performance using different quantum backends.
* Investigate real quantum hardware execution.
* Compare simulator, QPU, and hybrid solver performance.
* Analyze the potential advantages and limitations of quantum approaches for healthcare machine learning applications.

---

## Platforms and Technologies

### Quantum Computing Platforms

| Platform         | Type                                    |
| ---------------- | --------------------------------------- |
| PennyLane        | Quantum simulation framework            |
| Cirq             | Quantum circuit simulation framework    |
| Qiskit           | Quantum computing simulation framework  |
| OpenJij          | Quantum-inspired optimization framework |
| D-Wave Simulator | Quantum annealing simulation            |
| D-Wave QPU       | Real quantum annealing hardware         |
| IBM QPU          | Real gate-based quantum hardware        |
| Hybrid Solver    | Quantum-classical hybrid optimization   |

---

## Machine Learning Methods

The project uses:

* Support Vector Machine (SVM)
* Quantum Kernel SVM
* Quantum feature mapping
* Kernel-based classification
* Quantum optimization methods
* Hybrid quantum-classical learning workflows

---

## Methodology

The experimental workflow consists of:

1. Data preprocessing and preparation.
2. Feature selection and transformation.
3. Quantum feature encoding.
4. Quantum kernel construction.
5. SVM model training.
6. Testing and evaluation.
7. Performance comparison between:

   * Classical simulation
   * Quantum simulation
   * D-Wave QPU
   * IBM QPU
   * Hybrid quantum solvers

---

## Experiments

The project contains experiments using different quantum computing environments.

### Quantum Simulators

* PennyLane simulator
* Cirq simulator
* Qiskit simulator
* OpenJij simulator
* D-Wave quantum annealing simulator

### Quantum Hardware

* **D-Wave QPU**

  * Real quantum annealing processor.
  * Used for optimization-based classification experiments.

* **IBM QPU**

  * Real gate-based quantum processor.
  * Used for quantum circuit execution and classification experiments.

### Hybrid Quantum-Classical Solvers

Hybrid workflows combine classical optimization with quantum processing to improve scalability and practical performance.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/Inferring-Lung.git
cd Inferring-Lung
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate the environment:

Linux/macOS:

```bash
source venv/bin/activate
```

Windows:

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Required Libraries

Main dependencies include:

```text
numpy
pandas
scikit-learn
matplotlib
jupyter
pennylane
qiskit
cirq
openjij
dwave-ocean-sdk
```

---

## Running Experiments

Start Jupyter Notebook:

```bash
jupyter notebook
```

Navigate to the desired experiment folder and run the corresponding notebook.

Example:

```text
pennylane simulation/
    pennylane_lung_svm_compare_80_test_432.ipynb
```

For D-Wave experiments:

```text
Dwave simulation/
    d_wave_lung_svm_compare_80_test_432.ipynb
```

For real quantum hardware experiments:

```text
IBM QPU & D-Wave QPU/
    ibm_QPU_svm_for_50_samples.ipynb
    adv2_system_for_50samples.ipynb
```

---

## Evaluation Metrics

The experiments evaluate:

* Classification accuracy
* Prediction performance
* Quantum kernel effectiveness
* Execution time
* Simulator vs hardware performance
* Optimization efficiency

---

## Results

The project provides comparative analysis between:

| Approach           | Evaluation                              |
| ------------------ | --------------------------------------- |
| Classical SVM      | Baseline performance                    |
| Quantum Kernel SVM | Quantum-enhanced classification         |
| D-Wave Simulator   | Annealing simulation performance        |
| D-Wave QPU         | Real quantum annealing performance      |
| IBM QPU            | Real quantum circuit performance        |
| Hybrid Solver      | Combined quantum-classical optimization |

Detailed numerical results and plots are available inside the experiment notebooks.

---

## Future Work

Future improvements may include:

* Larger medical imaging datasets.
* Quantum neural network approaches.
* Improved quantum error mitigation.
* More advanced feature encoding methods.
* Larger-scale execution on quantum hardware.
* Comparison with classical deep learning models.

---

## Citation

If you use this project in academic research, please cite:

```text
Inferring Lung: Quantum Machine Learning Approaches for Lung Classification.
```

---

## License

This project is released under the MIT License unless otherwise specified.
