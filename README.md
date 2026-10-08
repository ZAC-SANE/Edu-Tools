# edu-tools 🎓

`edu-tools` is an open-source library of interactive, step-by-step engineering and scientific solvers designed for modern classrooms and web platforms. 

Unlike standard "black-box" calculators that only provide a final answer, **edu-tools mirrors handwritten academic solutions**. It displays every intermediate step, formula structure, unit conversion, and numerical substitution in real-time, making it the perfect companion for students verifying homework and teachers generating instant exam keys.

Live implementation featured on: **[groomsti.com](https://groomsti.com)**

---

## ✨ Features

- **Step-by-Step Transparency:** Shows the exact path from raw input variables to the final answer (\(Formula \rightarrow Substitution \rightarrow Output\)).
- **Instant Reactive Updates:** Powered by React hooks—change a slider or numeric input, and the entire derivation updates instantly.
- **Beautiful Mathematical Typography:** Renders high-quality academic notation (\(\sigma, \tau, \Delta, \int\)) using ultra-fast KaTeX rendering.
- **Modular & Scalable Architecture:** Structured as individual, plug-and-play components that can be embedded into any web environment.

---

## 🛠️ Repository Structure

The tools are organized logically by engineering domain to allow easy scaling into new topics:

```text
edu-tools/
├── README.md               # Project overview & documentation
├── package.json            # Project dependencies
└── src/
    ├── components/         # Reusable UI layouts (styled inputs, wrapper blocks)
    └── solvers/            # Core calculation modules
        ├── ResistanceOfMaterials/
        │   ├── AxialStressSolver.jsx
        │   ├── BeamBendingSolver.jsx
        │   └── TorsionSolver.jsx
        ├── Mathematics/
        └── FluidMechanics/
```

---

## 🚀 Getting Started

### Prerequisites
Make sure you have [Node.js](https://nodejs.org) installed on your machine.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com
   cd edu-tools
   ```

2. Install the necessary dependencies (including KaTeX for math rendering):
   ```bash
   npm install
   ```

3. Import global KaTeX CSS into your main entry point file (e.g., `src/main.js` or `src/App.js`):
   ```javascript
   import 'katex/dist/katex.min.css';
   ```

### Usage Example
To use a component like the `AxialStressSolver` inside your React application:

```jsx
import React from 'react';
import AxialStressSolver from './src/solvers/ResistanceOfMaterials/AxialStressSolver';

function App() {
  return (
    <div className="container">
      <h1>Engineering Dashboard</h1>
      <AxialStressSolver />
    </div>
  );
}

export default App;
```

---

## 🤝 Contributing

Contributions are welcome! If you want to add a solver for a new topic (e.g., Thermodynamics, Electrical Circuits, or Dynamics), please follow these guidelines:
1. Fork the repository.
2. Create a new branch for your feature (`git checkout -b feature/new-solver`).
3. Keep pure math calculation logic separate from UI layout for easier unit testing.
4. Open a Pull Request detailing your mathematical formulas and use cases.

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details. This means you are free to use, modify, and distribute this software for educational, commercial, or personal use.
