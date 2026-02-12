# Hi, I'm Bakhit Adam 👋

Mechanical enthusiast focused on **mechanism design**, **simulation**, and **engineering software tools**.

## 🚀 About Me
- 🔧 Interested in: CAD modeling, machine elements, and mechanical mechanism optimization.
- 💻 Building: a portfolio and lightweight engineering apps for mechanism analysis.
- 📚 Learning: Python, MATLAB-style numerical workflows, and web tools for engineers.
- 🤝 Open to collaborate on: mechanical design projects, educational engineering tools, and R&D prototypes.

## 🧰 Skills
- **Mechanical:** Kinematics, statics, dynamics, tolerance analysis, design for manufacturing.
- **Software:** Python, NumPy, Matplotlib, basic web development (HTML/CSS/JS).
- **Tools:** SolidWorks / Fusion 360 / AutoCAD (or your preferred CAD tools).

## 📂 Portfolio Projects (Mechanical Mechanisms)
### 1) Four-Bar Linkage Analyzer
- Input link lengths and crank angle.
- Compute rocker angle, velocity ratio, and transmission angle.
- Visualize mechanism motion in 2D.

### 2) Slider-Crank Simulator
- Piston position, velocity, acceleration.
- Sensitivity analysis versus crank radius and connecting rod length.
- Export plots and design reports.

### 3) Cam-Follower Profile Designer
- Generate cam profile from displacement law.
- Check pressure angle and curvature limits.
- Plot follower displacement/velocity/acceleration.

## ✅ Example You Should Follow (Starter App)
If you want to **start now**, build this exact mini project first.

### Project Structure
```bash
mechanism-studio/
├── backend/
│   ├── main.py
│   ├── mechanism.py
│   └── requirements.txt
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── app.js
└── README.md
```

### Backend Example (`backend/mechanism.py`)
```python
import math

def slider_crank_position(r: float, l: float, theta_deg: float) -> float:
    """Return piston displacement x for slider-crank mechanism."""
    theta = math.radians(theta_deg)
    return r * math.cos(theta) + math.sqrt(l**2 - (r * math.sin(theta))**2)
```

### API Example (`backend/main.py`)
```python
from fastapi import FastAPI
from mechanism import slider_crank_position

app = FastAPI(title="Mechanical Mechanism Studio")

@app.get("/slider-crank")
def get_slider_crank(r: float, l: float, theta: float):
    x = slider_crank_position(r, l, theta)
    return {"r": r, "l": l, "theta": theta, "x": x}
```

### Frontend Example (`frontend/app.js`)
```javascript
async function run() {
  const r = 50, l = 140, theta = 30;
  const res = await fetch(`http://127.0.0.1:8000/slider-crank?r=${r}&l=${l}&theta=${theta}`);
  const data = await res.json();
  document.getElementById("result").textContent = `Piston position x = ${data.x.toFixed(2)} mm`;
}
run();
```

### Run Commands
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```
Then open `frontend/index.html` in browser and display API result.

---

## 🛠️ App Idea: Mechanical Mechanism Studio
A simple app where users can:
- Select a mechanism type (4-bar, slider-crank, cam-follower).
- Enter design parameters.
- Run kinematic calculations.
- View plots and animated motion.
- Export results as PDF/CSV.

### Suggested Tech Stack
- **Frontend:** HTML/CSS/JS (or React).
- **Backend:** Python (FastAPI/Flask).
- **Numerical Engine:** NumPy + SciPy.
- **Visualization:** Matplotlib or Plotly.

## 🗺️ Development Roadmap
1. Define MVP (start with one mechanism: slider-crank).
2. Implement core equations and validation tests.
3. Build UI forms and result charts.
4. Add animation playback and downloadable reports.
5. Expand to more mechanism types.

## 📫 Contact
- LinkedIn: *Add your link*
- Email: *Add your email*
- Portfolio Website: *Add your URL*
