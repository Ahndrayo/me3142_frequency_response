# 📈 Transfer Function Identification from Bode Plot Data

This project demonstrates how to estimate a transfer function from experimental frequency response data using Python.

## 📊 Overview

Given frequency response data:
- Frequency: `ω` (rad/s)
- Gain: `|H(jω)|` in dB
- Phase: `∠H(jω)` in degrees

We aim to identify a transfer function of the system.


---

## ⚙️ What This Notebook Does

### 1. Load Experimental Data
- Reads data from an Excel file
- Extracts:
  - Frequency (`omega`)
  - Gain (`gain_dB`)
  - Phase (`phase_deg`)

---

### 2. Estimate Poles from Bode Plot
- Break frequencies (`ω₁`, `ω₂`) are manually identified from asymptotic plots
- These define the structure of the transfer function
---

### 3. Fit System Gain (K)
- Uses `scipy.optimize.curve_fit`
- Fits complex frequency response:
  
\[
H(j\omega) = \frac{K}{(1 + j\omega/\omega_1)(1 + j\omega/\omega_2)}
\]

---

### 4. Validate Transfer Function
- Reconstructs full Bode plots:
  - Gain vs frequency
  - Phase vs frequency

- Overlays:
  - Experimental data
  - Model prediction

---

## 
---

## ▶️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/Ahndrayo/me3142_frequency_response.git
```

### 2. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate      # Mac/Linux
venv\Scripts\activate         # Windows
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Run Jupyter Notebook


