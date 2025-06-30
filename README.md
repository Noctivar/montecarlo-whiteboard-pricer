# MonteCarlo Whiteboard Pricer 🖋📈

| **Description** | **Sketch any payoff. Price it with Monte Carlo.** |
|-----------------|--------------------------------------------------------------|
| **Purpose** | Turn a Jupyter/Colab notebook into a mini-trading desk |
| **Workflow** | Draw a curve, hit "Run Monte Carlo," and get full payoff analytics in seconds |

---

## 🚀 Key Features

| Feature | Description | Technology |
|---------|-------------|------------|
| **Interactive Whiteboard** | Click-and-drag to sketch any payoff shape (calls, straddles, digital exotics, your own inventions) | `ipycanvas` |
| **Sketch-to-Function Engine** | Mouse points → price/payoff pairs → linear interpolation (values outside drawn range default to zero) | `scipy.interpolate` |
| **Vectorised Monte Carlo** | 10,000 geometric-Brownian paths evaluate your payoff under risk-neutral drift | NumPy |
| **Instant Risk Metrics** | Expected payoff, standard deviation, and left-tail 95% VaR (5th-percentile) | Real-time calculation |
| **Clean Dual-Panel Plot** | Top: your payoff curve / Bottom: histogram of simulated outcomes with mean & VaR markers | Matplotlib |
| **Self-Contained Notebook** | Works out-of-the-box in Colab—no local GUI setup required | Jupyter/Colab |

---

# ⚡ Quick Start

| Method | Instructions |
|--------|--------------|
| **🌐 Colab (Fastest)** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1gDPQcb8aNJiNRojrRzR0R1Yz6iklP0kM?usp=sharing) |
| **💻 Local Jupyter** | `git clone https://github.com/yourusername/montecarlo-whiteboard-pricer.git`<br>`cd montecarlo-whiteboard-pricer`<br>`pip install -r requirements.txt`<br>`jupyter notebook whiteboard_pricer.ipynb` |

---

## ⚙️ Model & Parameters

| Symbol | Description | Default Value | Notes |
|--------|-------------|---------------|-------|
| `S0` | Initial stock price | `1.0` | Starting point for simulation |
| `MU` | Drift (risk-neutral) | `0.0` | Risk-neutral measure |
| `SIGMA` | Volatility | `0.20` | Annual volatility (20%) |
| `T` | Time to expiry (years) | `1.0` | One year to maturity |
| `N_PATHS` | Monte Carlo paths | `10,000` | Simulation accuracy |

### 📊 GBM Process

| Component | Formula |
|-----------|---------|
| **Geometric Brownian Motion** | S<sub>T</sub> = S<sub>0</sub> exp[(μ - ½σ²)T + σ√T·Z] |
| **Random Component** | Z ~ N(0,1) |

> **💡 Customization:** All parameters are defined at the top of the notebook—edit them to explore new scenarios or scale path counts.

---

## 🛠️ Tech Stack

| Category | Technologies |
|----------|-------------|
| **Core Language** | Python 3 |
| **Numerical Computing** | NumPy, SciPy |
| **Visualization** | Matplotlib |
| **Interactive Components** | ipycanvas, ipywidgets |
| **Environment** | Jupyter, Google Colab |

---

## 🧭 Development Roadmap

| Priority | Feature | Status |
|----------|---------|--------|
| 🔧 | Modular `src/` package + CLI wrapper (pytest, ruff, CI) | ⏳ Planned |
| 📈 | Antithetic & control-variate variance reduction | ⏳ Planned |
| 🔢 | Pathwise / bump Greeks (Δ, Γ) | ⏳ Planned |
| 📊 | Implied-vol calibration (Yahoo Finance) | ⏳ Planned |
| ⚡ | GPU acceleration (Numba / JAX) | ⏳ Planned |

---

## 📄 License

| License Type | Details |
|--------------|---------|
| **MIT License** | Open source, free to use and modify |

---

