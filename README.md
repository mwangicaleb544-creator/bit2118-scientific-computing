# Scientific Computing (Unit Code 2118) – Group 18 Work.

**Department:** Computing and Informatics
**Unit:** Scientific Computing (BIT 2118)
**Year, Semester:** 2026, Sept/Dec
**Repository owner:** Caleb Mwangi (BSCCS/2024/74201)

> The tasks were discussed and solved as a group (Group 18).

---

## 1. Group members.

| No. | Name | Reg. No. |
|---|---|---|
| 1 | Natasha Wanjiru | BSCCS/2024/53895 |
| 2 | Alice Nzomo | BSCCS/2024/73556 |
| 3 | Scarlet Patience | BSCCS/2024/54567 |
| 4 | Maureen Wanjiku | BSCCS/2024/73963 |
| 5 | Morris Maina | BSCCS/2024/55176 |
| 6 | Juakim Njuguna | BSCCS/2024/54733 |
| 7 | Brian Japan | BSCCS/2024/74678 |
| 8 | Levi Omare | BSCCS/2024/56230 |
| 9 | Gideon Chebet | BSCCS/2024/73487 |
| 10 | Caleb Mwangi | BSCCS/2024/74201 |

## 2. About this repository.

This repository contains the solutions to Tasks 2–20 of the Scientific Computing group work, using Python with NumPy, SciPy and Matplotlib. For every task we:

1. Identified the **input values** and the **mathematical operation** performed by the program.
2. **Changed at least one input or parameter** and explained how the result changed.
3. Explained the **meaning of the output** in words, and interpreted the graph where there was one.
4. **Modified the program to solve a different but related real-world case**, and documented its assumptions, input data, output and interpretation.

The Prerequisite (Data Science Essentials with Python, self-paced) was completed before starting these tasks.

## 3. Tools and libraries.

| Library | Use in this project |
|---|---|
| NumPy | Arrays, vectorization, matrix operations, linear algebra, random numbers |
| SciPy | LU decomposition, root finding, nonlinear systems, interpolation, curve fitting, integration, ODE solvers, optimization |
| Matplotlib | Graphs of convergence, fitted curves, interpolation, ODE solutions and simulations |
| timeit | Comparing a Python loop with vectorized NumPy code |

Python 3.10 or newer is recommended. **NumPy 2.0 or newer is required**, because Task 16 uses `np.trapezoid`.

## 4. Repository structure.

```text
.
├── README.md
├── requirements.txt
├── .gitignore
├── code/        Original and modified programs for Tasks 2–20
├── outputs/     Console output of each program run
├── images/      Saved graphs (PNG)
└── docs/        Group 18 written documentation
```

Each task has two programs in `code/`: the original (for example `Task_02_numpy_arrays.py`) and the modified version for a related real-world case (for example `Task_02_numpy_arrays_modified.py`).

## 5. How to run.

```bash
# 1. Clone the repository
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY

# 2. Create and activate a virtual environment
python -m venv .venv
.venv\Scripts\activate            # Mac/Linux: source .venv/bin/activate

# 3. Install the libraries
pip install -r requirements.txt

# 4. Run a program (always from the repository root)
python code/Task_02_numpy_arrays.py
python code/Task_02_numpy_arrays_modified.py
```

To save a program's printed output to a file:

```bash
python code/Task_02_numpy_arrays.py > outputs/Task_02_output.txt
```

Programs that draw graphs open a Matplotlib window (close it to let the program finish) and save a PNG in `images/`, which the program creates if it does not exist.

## 6. Tasks and modified real-world cases.

| Task | Topic | Original problem | Modified case | Modified program |
|---|---|---|---|---|
| 2 | NumPy arrays | Weather-station temperatures | Greenhouse sensor in the Nairobi highlands | `Task_02_numpy_arrays_modified.py` |
| 3 | Vectorization | Network latency conversion | Internet bandwidth (Mbps to MB/s) | `Task_03_vectorization_modified.py` |
| 4 | Floating-point errors | 0.1 + 0.2 and unstable formula | Banking accumulation error | `Task_04_numerical_errors_modified.py` |
| 5 | Matrix algebra | Rotating and scaling a square | Robot arm waypoints | `Task_05_matrix_algebra_modified.py` |
| 6 | Linear systems | Counting active servers | Two-loop circuit currents | `Task_06_linear_systems_modified.py` |
| 7 | Gaussian elimination and LU | One matrix, many measurement sets | Four-node structure under load | `Task_07_gaussian_lu_modified.py` |
| 8 | Iterative methods | Five-point temperature grid | Metal rod with seven points | `Task_08_iterative_linear_modified.py` |
| 9 | Eigenvalues | Node importance in a 4-node network | Five-person friend network | `Task_09_eigenvalues_modified.py` |
| 10 | Bisection and fixed point | Equilibrium temperature | Break-even production | `Task_10_root_finding_modified.py` |
| 11 | Newton and secant | IRR of a cash-flow series | IRR of a 50,000 project or loan | `Task_11_irr_modified.py` |
| 12 | Nonlinear equations | Circle and parabola | Overlapping cell-tower coverage | `Task_12_nonlinear_modified.py` |
| 13 | Interpolation | Hourly temperature to 10-minute values | Cumulative rainfall | `Task_13_interpolation_modified.py` |
| 14 | Curve fitting | Server response time vs users | Phone battery drain | `Task_14_curve_fitting_modified.py` |
| 15 | Numerical differentiation | Speed from GPS positions | Acceleration from velocity | `Task_15_differentiation_modified.py` |
| 16 | Numerical integration | Energy from smart-meter power | Distance from bus speed | `Task_16_integration_modified.py` |
| 17 | Euler method | Newton's law of cooling | Drug concentration in the blood | `Task_17_euler_modified.py` |
| 18 | ODEs with SciPy | RC circuit charging | SIR epidemic model | `Task_18_scipy_ode_modified.py` |
| 19 | Optimization | Cheapest server mix | Cheapest fertilizer mix | `Task_19_optimization_modified.py` |
| 20 | Monte Carlo | Server overload probability | Project deadline risk | `Task_20_monte_carlo_modified.py` |

## 7. Key results.

| Task | Main result of the original program | Result of the modified case |
|---|---|---|
| 2 | Mean 23.12 °C, min 17.50 °C, max 29.40 °C | 7 hours above 25 °C, hottest hour 12 |
| 3 | Vectorized code far faster than a loop (about 45–57× on our machines; varies by computer) | RMS speed 7.64 MB/s |
| 4 | `0.1 + 0.2 == 0.3` is False; unstable formula loses accuracy at x = 1e-12 | float32 sum of 0.01 × 100,000 gives about 1000.665 |
| 5 | Determinant 3 = area scale factor 2 × 1.5 | Rectangle rotated 30° and moved by (3, 2) |
| 6 | 3 Type A and 4 Type B servers | I1 = 0.4364 A, I2 = 0.0545 A |
| 7 | x = [5, 5, 5] for the first measurement set | Load [10,0,0,5] gives [3.909, 1.727, 1.273, 2.091] |
| 8 | T = [86.67, 73.33, 60, 46.67, 33.33]; Jacobi 150 and Gauss-Seidel 75 iterations | Rod: Jacobi 263 and Gauss-Seidel 132 iterations |
| 9 | Dominant eigenvalue 2.5616; B and C most important | λ = 2.2143; person C most central |
| 10 | Equilibrium 27.525211 °C (bisection 38 steps, fixed point 13) | Break-even at 68.218 units |
| 11 | IRR 11.542461% | IRR 15.2382% |
| 12 | Two real intersections at (±1.5175, 1.3028) | Towers' edges meet at (3.75, ±3.3072) |
| 13 | At 10:30: linear 23.25 °C, cubic 23.36 °C | At hour 10: linear 9.50 mm, cubic 9.71 mm |
| 14 | Quadratic fit RMSE 1.55 ms; 377.86 ms at 400 users | Battery half-life 7.57 h; 20% at about 17.6 h |
| 15 | Speeds rise from 4.80 to 8.00 m/s | Acceleration falls from 3.20 to 2.10 m/s² |
| 16 | Trapezoid 15.700 kWh, Simpson 15.800 kWh | Distance 310.0 m (trapezoid), 316.7 m (Simpson) |
| 17 | Euler 26.40 °C vs exact 26.78 °C (error 0.372) | h = 12 h is unstable (11.5778 instead of 0.1573) |
| 18 | Capacitor at 4.9663 V after 5 s, error about 9.3e-10 V | β = 0.4 peaks at 40.6% on day 19.4; β = 0.2 at 15.8% on day 43.8 |
| 19 | Best mix 5.882 Type B (cost 105.88); whole servers: 6 Type B (cost 108) | 1 bag F1 + 0.4 bag F2 (cost 46); whole bags cost 60 |
| 20 | Overload probability 10.616% | 68.1% chance of exceeding 20 weeks; 90th percentile 24.7 weeks |

## 8. Documentation.

- `docs/` – the Group 18 documentation with the full explanations for each task (input and operation, parameter change, output meaning and the modified case).
- `outputs/` – saved console output for each program.
- `images/` – saved graphs for the tasks that plot results.

## 9. Assumptions and notes.

- The data in the modified programs is assumed or invented for the exercise, not taken from real measurements.
- Random simulations use fixed seeds, so results are repeatable. Other seeds give slightly different values.
- Timings in Task 3 depend on the computer and change from run to run.
- Where a graph is produced, its interpretation is given in the documentation.
- The modified cases use simplified models (for example, constant rates in the drug-concentration and SIR cases, and evenly spaced data in the interpolation and integration cases). Real data would be noisier, so the numbers should be read as illustrations of the methods, not as predictions.
- Numerical methods trade accuracy against effort. For example, Euler's method became unstable when the step size was too large (Task 17), and Gauss-Seidel needed about half the iterations of Jacobi (Task 8), while Simpson's and the trapezoid rule gave slightly different answers on the same data (Task 16).
- Comparing an approximate answer with an exact or library answer (as in Tasks 17 and 18) is a useful habit: it shows how much error the method introduces, instead of just trusting the output.
- Some results depend on the environment, such as the NumPy version (2.0 or newer for `np.trapezoid`) and the timings in Task 3, so the outputs in `outputs/` may differ slightly on another machine.
- Possible improvements: add unit tests that check each program's key results, replace the invented data with real datasets, and add error estimates to the integration and differentiation tasks.

## 10. References.

- NumPy documentation: https://numpy.org/doc/
- SciPy documentation: https://docs.scipy.org/doc/scipy/
- Matplotlib documentation: https://matplotlib.org/stable/
- BIT 2118 Scientific Computing Group Work handout

## 11. Academic integrity.

The task discussions were done as a group, but this repository is my own individual submission, as required by the unit instructions.
