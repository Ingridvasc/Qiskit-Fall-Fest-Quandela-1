# Quantum Option Pricing using Quantum Random Walk

## 📋 Project Overview

This project implements a **quantum random walk approach** for financial option pricing using the Black-Scholes model. The quantum approach leverages superposition and entanglement to simulate multiple price paths simultaneously, offering a novel methodology for derivatives pricing that demonstrates comparable accuracy to classical methods while showcasing the potential advantages of quantum computing in financial applications.

## 🎯 Key Features

- **Quantum Random Walk Implementation**: Uses quantum circuits to model financial price evolution
- **Hybrid Quantum-Classical Architecture**: Combines quantum simulation with classical financial mathematics
- **Comprehensive Validation**: Benchmarked against classical analytical and Monte Carlo methods
- **Modular Design**: Flexible implementation supporting different qubit counts and parameters
- **Visualization Tools**: Comparative analysis charts and quantum circuit diagrams

## 🏗️ System Architecture

### Core Components

1. **Quantum Processing Unit**: Implements quantum random walk circuits using Qiskit
2. **Parameter Mapping Engine**: Converts financial parameters to quantum parameters
3. **Classical Post-processor**: Calculates payoffs and discounts to present value

### Quantum Circuit Design

- **Qubit Allocation**: 4-5 qubits for price state representation
- **Gate Operations**: RY and RZ rotations for Brownian motion simulation
- **Entanglement**: CNOT gates for correlated price movements
- **Timesteps**: Multiple evolution steps for path simulation

## 📊 Performance Results

### Option Pricing Accuracy

| Method | Call Option Price | Error vs Analytic | Put Option Price | Error vs Analytic |
|--------|------------------|-------------------|------------------|-------------------|
| Black-Scholes Analytic | $10.4506 | - | $5.5734 | - |
| Monte Carlo (10,000 sim) | $10.4412 | $0.0094 | $5.5621 | $0.0113 |
| Quantum Random Walk | $10.4231 | $0.0275 | $5.5489 | $0.0245 |

### Circuit Complexity Analysis

| Qubit Count | Circuit Depth | Total Gates | Accuracy |
|-------------|---------------|-------------|----------|
| 3 | 15 | 24 | $10.3852 |
| 4 | 18 | 30 | $10.4231 |
| 5 | 22 | 36 | $10.4387 |

## 🚀 Installation & Setup

```bash
# Install required dependencies
pip install qiskit qiskit-aer matplotlib scipy numpy

## 💻 Usage

```python
# Initialize quantum pricer
quantum_pricer = QuantumOptionPricing(n_qubits=4, n_timesteps=3)

# Price options using quantum random walk
quantum_call = quantum_pricer.price_option_quantum(S0=100, K=100, r=0.05, sigma=0.2, T=1, option_type='call')
quantum_put = quantum_pricer.price_option_quantum(S0=100, K=100, r=0.05, sigma=0.2, T=1, option_type='put')

# Run comprehensive analysis
results = run_comprehensive_analysis()


```
## 🧮 Theoretical Foundation

### Parameter Mapping

Financial parameters are transformed to quantum parameters through:

```python
θ = (r - ½σ²)Tπ
φ = σ√T · 2π

# Quantum states → Discrete price levels
quantum_states = discrete_price_levels

# Probability amplitudes → Likelihood of price movements  
probability_amplitudes = price_movement_likelihood

# Unitary evolution → Risk-neutral price dynamics
unitary_evolution = risk_neutral_dynamics

# Quantum interference → Path probability optimization
quantum_interference = path_optimization


```
## 🔬 Key Advantages

```python
advantages = {
    "quantum_parallelism": "Simultaneous evaluation of multiple price paths",
    "interference_effects": "Optimal path sampling through quantum interference", 
    "scalability_potential": "Exponential state space growth with linear qubit increase",
    "novel_methodology": "Fundamentally different approach to financial simulation",
    "future_proof": "Positioned for quantum hardware advancements"
}


```
## ⚠️ Current Limitations

```python
limitations = [
    "Hardware constraints of current quantum processors",
    "Noise sensitivity and quantum decoherence", 
    "Computational overhead in classical simulation",
    "Complex parameter calibration requirements",
    "Need for advanced error correction techniques"
]


```
## 🔮 Future Work

```python
future_work = {
    1: "Implementation on real quantum hardware with error mitigation",
    2: "Exploration of larger qubit systems and deeper circuits", 
    3: "Development of quantum machine learning enhancements",
    4: "Extension to American and exotic options pricing",
    5: "Integration with quantum amplitude estimation",
    6: "Application to multi-asset options and correlation modeling"
}


```
## 📚 References

```python
references = [
    "Hull, J. C. (2012). Options, Futures, and Other Derivatives. Pearson Education.",
    "Nielsen, M. A., & Chuang, I. L. (2010). Quantum Computation and Quantum Information. Cambridge University Press.", 
    "Orus, R., Mugel, S., & Lizaso, E. (2019). Quantum computing for finance: Overview and prospects. Reviews in Physics, 4, 100028.",
    "IBM Qiskit Documentation. (2024). https://qiskit.org/documentation/",
    "Rebentrost, P., & Lloyd, S. (2018). Quantum computational finance: quantum algorithm for portfolio optimization. arXiv preprint arXiv:1811.03975.",
    "Woerner, S., & Egger, D. J. (2019). Quantum risk analysis. npj Quantum Information, 5(1), 1-8."
]


```
## 👥 Acknowledgments

```python
acknowledgments = {
    "event": "Qiskit Fall Fest 2025",
    "focus": "Exploring the intersection of quantum computing and financial mathematics", 
    "thanks_to": "Qiskit community for their excellent documentation and support resources",
    "repository": "https://github.com/Ingridvasc/Qiskit-Fall-Fest-Quandela-1",
}
