# MonteCarlo Whiteboard Pricer 🖋📈
**Sketch any payoff.  Price it with Monte Carlo—instantly.**

Turn a Jupyter/Colab notebook into a mini-trading desk:  
draw a curve, hit “Run Monte Carlo,” and get full payoff analytics in seconds.

---

## 🎯 Key Features
| What you get | Details |
|--------------|---------|
| **Interactive whiteboard** | Built with `ipycanvas`; click-and-drag to sketch any payoff shape (calls, straddles, digital exotics, your own inventions). |
| **Sketch-to-function engine** | Mouse points → price/payoff pairs → **linear interpolation** via `scipy.interpolate`. Values outside the drawn range default to zero. |
| **Vectorised Monte Carlo** | 10 000 geometric-Brownian paths (NumPy) evaluate your payoff under risk-neutral drift. |
| **Instant risk metrics** | Expected payoff, standard deviation, and **left-tail 95 % VaR** (5th-percentile) printed and plotted. |
| **Clean dual-panel plot** | Top: your payoff curve.  Bottom: histogram of simulated outcomes with mean & VaR markers. |
| **Self-contained notebook** | Works out-of-the-box in Colab—no local GUI setup. |

---

## 🚀 Quick Start
| Method | Steps |
|--------|-------|
| **Colab (fastest)** | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yourusername/montecarlo-whiteboard-pricer/blob/main/whiteboard_pricer.ipynb) |
| **Local Jupyter** | ```bash
git clone https://github.com/yourusername/montecarlo-whiteboard-pricer.git
cd montecarlo-whiteboard-pricer
pip install -r requirements.txt
jupyter notebook whiteboard_pricer.ipynb
``` |

---

## ⚙️ Model & Parameters
* **GBM formula:** \( S_T = S_0 \exp\bigl((\mu - \tfrac12\sigma^2)T + \sigma\sqrt{T}Z \bigr) \) with \( Z \sim \mathcal{N}(0,1) \).  
* **Defaults:**  
  &nbsp;&nbsp;`S0 = 1.0`, `MU = 0`, `SIGMA = 0.20`, `T = 1.0`, `N_PATHS = 10_000`  
* **Customisation:** Edit those constants at the top of the notebook to run different scenarios or increase path count.

---

## 🛠 Tech Stack
Python 3 • NumPy • SciPy • Matplotlib • ipycanvas • ipywidgets • Jupyter/Colab

---

## 🧭 Roadmap
- [ ] CLI wrapper & modular packaging (`src/` directory, pytest)  
- [ ] Control-variate & antithetic variance reduction  
- [ ] Pathwise/bump Greeks (Δ, Γ)  
- [ ] Real-market vol calibration (Yahoo Finance)  
- [ ] GPU acceleration via Numba/JAX  

---

## 📄 License
MIT

---

## 🙋‍♂️ Author
**Min Heo** — triple major (Physics • Pure Math • English) & aspiring quant.  
[LinkedIn](https://www.linkedin.com/in/yourprofile)

> *From sketch to price—no spreadsheets, no boilerplate, just quant insight.*
