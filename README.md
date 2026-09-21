# Vertical Circular Motion, String Tension & Projectile Slackening Lab

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178c6.svg?logo=typescript)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-19.0-61dafb.svg?logo=react)](https://react.dev/)
[![Vite](https://img.shields.io/badge/Vite-6.2-646cff.svg?logo=vite)](https://vitejs.dev/)
[![Author: Shamsuddin Piash](https://img.shields.io/badge/Author-Shamsuddin%20Piash-0ea5e9.svg)](https://piashoverflow.github.io)
[![BUET ME](https://img.shields.io/badge/Institution-BUET%20'25-10b981.svg)](https://buet.ac.bd)

> **Interactive Computational Physics Simulator & Educational Workbench**  
> Developed by **Shamsuddin Piash** | Department of Mechanical Engineering, Bangladesh University of Engineering and Technology (BUET).

---

## 🔬 Overview & Conceptual Motivation

Interactive physics simulation modeling non-linear vertical circular pendulum motion, string tension dynamics, and slackening parabolic arcs.

Designed from **first-principles physics and numerical mechanics**, this simulation bridges textbook analytical theory and real-time computation. It enables students, researchers, and competitive engineering candidates to visualize dynamic force interactions, observe parametric trends, and verify conservation laws interactively.

---

## 📐 Mathematical Formulation & Physics Derivations

### Governing Dynamic Equations

For a mass $m$ attached to a light inextensible string of length $L$ executing vertical circular motion at angle $\theta$ from the vertical:

$$T(\theta) - m g \cos\theta = \frac{m v(\theta)^2}{L} \implies T(\theta) = m \left(g \cos\theta + \frac{v(\theta)^2}{L}\right)$$

By conservation of mechanical energy between bottom point ($v_0$) and angle $\theta$:

$$\frac{1}{2} m v_0^2 = \frac{1}{2} m v(\theta)^2 + m g L (1 - \cos\theta) \implies v(\theta)^2 = v_0^2 - 2 g L (1 - \cos\theta)$$

Critical velocity conditions:
1. **Full Loop Completion**: $v_{bottom} \ge \sqrt{5 g L}$, with top velocity $v_{top} \ge \sqrt{g L}$ and $T_{top} \ge 0$.
2. **Oscillation Regime**: $v_{bottom} \le \sqrt{2 g L}$ (bob never exceeds horizontal position).
3. **String Slackening & Projectile Transition**: $\sqrt{2 g L} < v_{bottom} < \sqrt{5 g L}$, string tension drops to zero ($T=0$) in upper half, transitioning the mass into a parabolic projectile trajectory.

---

## ✨ Key Features & Interactive Workbench

- **Real-Time Phase Space Visualization**: Live angle $	heta(t)$, angular velocity $\omega(t)$, and tension $T(t)$ plots.
- **String Slackening Projectile Engine**: Seamlessly transitions into free-flight projectile physics when tension vanishes.
- **Energy Conservation Gauge**: Real-time bar indicators verifying $E = K + U$ conservation.
- **Interactive Speed Injector**: Trigger arbitrary initial impulse velocities to test looping vs oscillating boundaries.

---

## 🔒 Confidentiality, Security & Academic Integrity

This repository adheres strictly to professional security standards, privacy guidelines, and academic integrity policies:

- **Proprietary & Institutional Protection**: Underlying academic curricula, institutional questions, and confidential research data are sanitized and protected under institutional agreements.
- **Environment & Secrets Hygiene**: No private keys, passwords, or personal credentials are hardcoded. API tokens (e.g., Gemini AI or cloud compute) must be supplied via local `.env` files or secure CI/CD secrets.
- **Vulnerability Reporting**: Please refer to [SECURITY.md](SECURITY.md) for instructions on confidential disclosure.

---

## 🛠️ Project Structure & Architecture

```
.
├── src/
│   ├── components/       # UI panels, canvas renderer, sliders & controls
│   ├── utils/            # Physics solvers, RK4 ODE integration, vector math
│   ├── types.ts          # Strongly typed simulation interfaces
│   ├── App.tsx           # Primary application workbench
│   └── main.tsx          # Application root
├── public/               # Static assets & icons
├── metadata.json         # Simulator metadata & capabilities
├── package.json          # Dependencies & build scripts
├── tsconfig.json         # TypeScript compiler configuration
├── vite.config.ts        # Vite bundle & dev server configuration
├── SECURITY.md           # Confidentiality & vulnerability disclosure policy
└── LICENSE               # MIT License
```

---

## 🚀 Quickstart & Local Setup

### Prerequisites
- **Node.js**: `v18.0.0` or higher
- **npm** or **bun** / **pnpm**

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/piashoverflow/Vertical-Circular-Motion.git
cd Vertical-Circular-Motion

# 2. Install dependencies
npm install

# 3. Configure environment variables (if applicable)
cp .env.example .env

# 4. Launch the local development server
npm run dev
```

Visit `http://localhost:3000` in your browser to interact with the simulation.

### Production Build

```bash
npm run build
npm run preview
```

---

## 👤 Author & Academic Affiliation

**Shamsuddin Piash**  
*B.Sc. in Mechanical Engineering (Graduated March 2025)*  
**Bangladesh University of Engineering and Technology (BUET)**  
Dhaka, Bangladesh

- **Portfolio Website**: [piashoverflow.github.io](https://piashoverflow.github.io)
- **GitHub**: [@piashoverflow](https://github.com/piashoverflow)
- **LinkedIn**: [linkedin.com/in/shamsuddin-piash](https://linkedin.com/in/shamsuddin-piash)
- **Email**: [mohammadshamsuddinpiash0722@gmail.com](mailto:mohammadshamsuddinpiash0722@gmail.com)

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for complete details.
