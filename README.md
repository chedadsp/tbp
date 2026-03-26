# Three-Body Problem Simulation

### **[Launch the Simulation](https://chedadsp.github.io/tbp/)**

---

Three celestial bodies. One shared gravitational field. No analytical solution.

This is an interactive, real-time simulation of one of the most famous unsolved problems in classical mechanics — the **three-body problem**. Watch as three masses dance through space in trajectories that are perpetually unpredictable, occasionally breathtaking, and never the same twice.

![Three-Body Problem](https://img.shields.io/badge/physics-three--body%20problem-blue?style=for-the-badge)
![Zero Dependencies](https://img.shields.io/badge/dependencies-zero-brightgreen?style=for-the-badge)
![MIT License](https://img.shields.io/badge/license-MIT-yellow?style=for-the-badge)

---

## Why This Exists

In 1687, Newton solved the two-body problem. In the centuries since, the three-body problem has humbled every mathematician who tried to do the same for just *one more mass*. Henri Poincare proved it has no general closed-form solution — and in doing so, accidentally invented chaos theory.

This simulation lets you **feel** that chaos. Watch stable orbits dissolve into wild ejections. See two bodies lock into a temporary binary while the third swings past. Drag a body just slightly off course and witness an entirely different future unfold.

## Features

- **Real-time gravitational simulation** powered by Velocity Verlet integration for accurate, energy-preserving physics
- **Force visualization** — velocity vectors, gravitational force arrows, and net acceleration rendered live
- **Orbital trails** that paint each body's path through space
- **Drag interaction** — click and reposition any body to reshape the system
- **Adjustable gravity and time scale** to explore parameter space
- **Energy tracking** — kinetic, potential, and total energy displayed in real time
- **Auto-reset** — if all bodies escape the viewport, the system gracefully restarts
- **Zero dependencies** — a single HTML file, no build step, no frameworks

## Controls

| Control | Action |
|---|---|
| **Speed slider** | Adjust simulation speed (0.1x – 50x) |
| **Gravity slider** | Scale gravitational constant (0.1 – 10) |
| **Randomize** / `R` | Generate a fresh configuration |
| **Pause** / `Space` | Freeze time |
| **Click & drag** | Reposition any body |

## The Physics

The simulation computes pairwise gravitational attraction between all three bodies using Newton's law of universal gravitation:

$$F = G \frac{m_1 \cdot m_2}{r^2}$$

Integration uses the **Velocity Verlet** method — a symplectic integrator that conserves energy far better than naive Euler methods, making the simulation stable over long time horizons. A softening parameter prevents numerical singularities during close encounters.

Each randomized configuration is carefully constructed: bodies are placed with orbital-scale velocities and zero net momentum, giving the system a fighting chance at producing the kind of intricate, quasi-stable orbits that make the three-body problem so mesmerizing.

## Run It Locally

```bash
git clone https://github.com/chedadsp/tbp.git
cd tbp
open index.html
```

That's it. No `npm install`. No build step. Just one HTML file and the laws of physics.

## License

[MIT](LICENSE)

---

*"The three-body problem is to the rest of mechanics what Fermat's Last Theorem is to the rest of mathematics."*
