# Bakhit Adam | Mechanical Design Portfolio

Mechanical design learner focused on **mechanisms**, **CAD modeling**, and **engineering software tools**.

## 👨‍🔧 Profile
I design and study mechanical systems with a focus on practical mechanism performance:
- Kinematic analysis
- Motion simulation
- Parametric CAD design
- Engineering calculation tools

## 🧰 Core Skills
- **Mechanical Design:** Linkages, shafts, gears, cam-follower systems, tolerance basics
- **Analysis:** Kinematics, force estimation, design calculations
- **CAD & Tools:** SolidWorks, Fusion 360, AutoCAD
- **Programming:** Python, NumPy, Matplotlib, basic HTML/CSS/JavaScript

## 📁 Featured Mechanical Design Projects

### 1) Four-Bar Linkage Design & Analysis
**Goal:** Design a four-bar mechanism for controlled rocker output.

**Work completed:**
- Selected link lengths based on motion requirements.
- Calculated transmission angle across crank rotation.
- Identified toggle/near-singularity positions.
- Built CAD concept and 2D motion visualization.

**Deliverables:**
- Link parameter table
- Angle vs crank-position plots
- Design notes with assumptions

---

### 2) Slider-Crank Mechanism Study
**Goal:** Evaluate piston displacement and motion quality.

**Work completed:**
- Computed piston position vs crank angle.
- Estimated velocity/acceleration trends.
- Compared multiple rod-length ratios.
- Suggested dimensions for smoother operation.

**Deliverables:**
- Calculation sheet / Python script
- Plots of displacement, velocity, acceleration
- Design recommendation summary

---

### 3) Cam-Follower Profile Prototype
**Goal:** Create a cam profile from displacement law.

**Work completed:**
- Defined follower motion segments (rise, dwell, return).
- Generated cam profile points.
- Checked pressure angle and curvature limits.
- Proposed manufacturable profile update.

**Deliverables:**
- Cam profile chart
- Motion law documentation
- Risk/constraint notes

## 🧪 Example Calculation Snippet (Slider-Crank)
```python
import math

def piston_position(r, l, theta_deg):
    theta = math.radians(theta_deg)
    return r * math.cos(theta) + math.sqrt(l**2 - (r * math.sin(theta))**2)

print(piston_position(50, 140, 30))
```

## 🎯 Portfolio Direction (Next 3 Steps)
1. Publish CAD screenshots/animations for each project.
2. Add one validation case comparing hand-calculation vs code output.
3. Build a small web app to input mechanism parameters and visualize motion.

## 📬 Contact
- Email: your-email@example.com
- LinkedIn: https://linkedin.com/in/your-profile
- GitHub: https://github.com/bakhitadam
