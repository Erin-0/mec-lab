# 🧪 Labo3D — Interactive 3D Mechanics Physics Laboratory

An interactive 3D browser-based physics laboratory built with **Three.js**, designed to simulate three classic university mechanics experiments (**TP1, TP2, and TP3**) with real-time physics, automated data logging, dynamic tables, and live plotted curves.

---

## 🎯 Experiments Included

### 🎡 TP1 — Gyroscope (U52006)
- **Horizontal Balancing:** Adjust the large (`1400 g`) and small (`80 g`) counterweights plus the fine-adjustment screw to reach `0.0°`.
- **Part 1 (Proper Rotation):** Insert the stabilization rod into the base socket, attach the `50 g` hooked mass to the spindle cord, release it, and automatically record `4` revolutions (`t_φ`, `T`, `ω`).
- **Part 2 (3D Precession):** Remove the stabilization rod, mount `50 g` and `100 g` precession masses at `d = 32 cm`, spin the flywheel, and automatically measure `t_R` (10 turns) and `t_P` (1 precession turn) to verify `t_R · t_P ≈ Cte`.
- **3D Vector Visualization:** Toggleable angular momentum ($\vec{L}$) and torque ($\vec{\tau}$) vectors.

### 🕰️ TP2 — Compound Pendulum (*Pendule Pesant*)
- **Precision Mass Positioning:** Slide the cylindrical mass (`1231.91 g`) from `5 cm` to `90 cm` with a real-time **magnifier ruler loupe** and quick target chips.
- **Small-Angle Release Zone:** Drag the graduated rod (`L = 100 cm`) into the green safe zone (`4°–15°`) and release.
- **Automated Photogate:** Counts `3` complete oscillations (`t_exp`, `T_exp = t/3`) and compares against theoretical models ($T_{th}$ and simple pendulum $T_0$).
- **Live Graph & Export:** Plots $T^2$ and $T_0^2 = f(r)$ with intersection detection and **CSV export**.

### ⚙️ TP3 — Rotational Dynamics (*Dynamique de Rotation*)
- **Moment of Inertia & Huygens' Theorem:** Position the `260 g` brass masselottes at `r₁ = 20 cm` and `r₂ = 10 cm` (or drag freely/asymmetrically).
- **Matelco Electronic Clock:** Simulates the `18°` ($\pi/10\text{ rad}$) shutter vane occultation with working **M/A**, **AUTO/MAN**, **EFF**, and **RAZ** controls.
- **Data & Curves:** Automatically logs `6` turns (`n = 1..6`), computes slopes and experimental inertia $J_{\text{exp}}$, and plots $\Omega^2 = f(n)$.
- **Dry Friction & Clutch:** Measures friction work ($W_{fr}$) and power ($P_{fr}$) during free coasting, plus a working **clutch lever** to engage the lower solid mid-rotation ($J_1 \Omega_1 = (J_1 + J_2)\Omega_2$).

---

## 🎮 Controls

| Key / Action | Function |
| :--- | :--- |
| `W` `A` `S` `D` or Arrow Keys | Move around the laboratory (`Shift` to sprint) |
| **Left-Click** (on background) | Lock pointer for FPS camera look (`ESC` to unlock) |
| **Right-Click + Drag** | Rotate camera freely without pointer lock |
| **Left-Click / Drag** (on apparatus) | Interact, slide weights, wind cords, or spin the rotor |
| `Z` (Hold) | Optical zoom |
| `C` | Toggle crouch |
| `Q` | Drop / put down held item (TP1) |
| `N` | Open / close measurement tables & graphs |

---

## 📁 Project Structure

```text
labmecanique/
├── index.html
├── README.md
└── images/
    ├── Christiaan Huygens (1629–1695).webp
    ├── Leonhard Euler (1707–1783).jpg
    ├── Léon Foucault (Jean Bernard Léon Foucault, 1819–1868).jpg
    └── متزلج.jfif
```

---

## 🚀 How to Run Locally

> ⚠️ **Important:** Because the 3D scene loads local image textures into WebGL, opening `index.html` directly via `file://` will be blocked by browser CORS security policies. Always run it through a local HTTP server.

### Option 1 — Python (Quickest)
```bash
cd path/to/labmecanique
python -m http.server 8000
```
Then open **`http://localhost:8000`** in your browser.

### Option 2 — VS Code Live Server
1. Open the project folder in **VS Code**.
2. Install the **Live Server** extension.
3. Click **Go Live** at the bottom-right corner.

---

## 🛠️ Built With
- [Three.js (r128)](https://threejs.org/) — 3D WebGL rendering, lighting, and shadows
- **HTML5 Canvas** — Procedural lab textures, handwritten whiteboards, digital clock displays, and live physics graphs
- **Vanilla JavaScript & CSS3** — Zero-dependency single-page application
```
