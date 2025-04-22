# 🌀 2D Lid-Driven Cavity Flow Simulation

A Python-based interactive simulation of the classic **lid-driven cavity flow** problem using the **vorticity–streamfunction formulation** of the incompressible Navier–Stokes equations.

This app leverages **Gradio** to provide a real-time, visual interface for experimenting with flow behavior under different Reynolds numbers, wall velocities, and grid resolutions.

## 🚀 Features

- 🧪 Interactive sliders for real-time flow simulations
- 🎨 U-Velocity contours and streamlines
- 📈 Centerline velocity profiles
- 💨 Divergence plots for incompressibility checks
- 🔁 Reynolds number–based viscosity calculation
- 📐 Dynamic computation of any one of the four parameters: `ρ`, `μ`, `U`, `Re` when the other three are specified
- 💻 Simple, intuitive Gradio interface

---

## 📊 Governing Equations

The simulation uses the **streamfunction–vorticity** formulation of the 2D incompressible Navier–Stokes equations:

- **Vorticity Transport Equation:**

  ∂ω/∂t + **V** · ∇ω = ν∇²ω

- **Poisson Equation for Streamfunction:**

  ∇²ψ = –ω

- **Velocity Field:**

  u = ∂ψ/∂y, v = –∂ψ/∂x


---

## 🧮 Parameters

| Parameter        | Description                                  |
|------------------|----------------------------------------------|
| `Nx`             | Grid size in X and Y directions (Nx × Nx)    |
| `Wall Velocity`  | Velocity of the moving top wall              |
| `ρ`              | Fluid density                                |
| `μ`              | Dynamic viscosity                            |
| `dt`             | Time step size                               |
| `Re`             | Reynolds number                              |

When any **3 of `ρ`, `μ`, `U`, `Re`** are provided, the 4th is computed automatically.

---

