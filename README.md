# AI Capital Curve Calculator — Deep Tech

A simple, browser-only tool for visualizing how AI can compress the **bootstrap → Series A** capital curve in **Biopharma**, **Biomed Devices**, and **Digital Health** startups.

Built in collaboration with ChatGPT to explore a trend highlighted by [Axios Pro Rata](https://www.axios.com/2025/08/07/ai-venture-capital-math-jon-mcneill):
> “AI agents can now get application startups to Series A with **80% less seed capital**.” — Jon McNeill, DVx

## 🌐 Live Demo
**[View on GitHub Pages](https://arysky001.github.io/capital-curve)**  
_No downloads. No logins. Runs entirely in your browser._

---

## 🚀 Features
- **Sector selection** — Biopharma, Biomed Device, Digital Health
- **AI leverage sliders** — Adjust AI impact for:
  - Literature & Landscaping
  - In-silico Modeling/Simulation
  - Data Ops & Analysis
  - Regulatory Drafting
  - Prototype Automation
- **Dynamic charting** — See pre-AI vs. AI-adjusted curves update in real time
- **Shareable states** — Copy a link with your sector and slider settings

---

## 🧠 About the Model
The calculator uses a **task-weighted tensor model** to estimate cost compression:

- **3D tensor**: `weights[sector, milestone, task]` — how much each task contributes to cost at each milestone for each sector
- **Vector**: `ai_leverage[task]` — AI automation factor (0.0 to 1.0) per task
- **Tensor dot product** → % reduction in cost for each sector × milestone
- **Floors**: Non-compressible costs for wet-lab, fabrication, and regulatory work  
- **Adjusted cost** = `max(floor, base_cost * (1 - reduction))`

The model is intentionally simplified — it’s a starting point for discussion and refinement, not a precise forecast.

---

## 📦 How to Run Locally
1. Clone the repo:
   ```bash
   git clone https://github.com/arysky001/capital-curve.git
   cd capital-curve
