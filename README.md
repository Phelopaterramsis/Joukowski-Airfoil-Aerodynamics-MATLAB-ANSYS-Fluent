# 🛩️ Joukowski Airfoil Aerodynamics – MATLAB & ANSYS Fluent

This folder contains my Aerodynamics project where I analyzed a Joukowski airfoil with 9% thickness-to-chord and 5% camber-to-chord using MATLAB and ANSYS Fluent.

## 📌 Course

- Course: Aerodynamics  
- University: University of Science and Technology – Zewail City  
- Supervisor: Dr. Mohamed Madbouli  
- TA: Eng. Asmaa AlaaElDeen  
- Student: Phelopater Ramsis (202001171)  
- Semester: Fall 2024  

---

## 🧾 Project Overview

The objective of this project was to study the aerodynamic behavior of a **Joukowski airfoil**, including:

- Generating the airfoil numerically using MATLAB  
- Plotting streamlines using the Joukowski transformation  
- Calculating surface velocity distribution  
- Plotting pressure coefficient (Cp) over upper & lower surfaces  
- Studying lift & moment coefficients over angles of attack from –5° to 10°  
- Verifying results with **ANSYS Fluent CFD simulation**

These steps help understand how classical potential-flow theory compares with CFD analysis.  
:contentReference[oaicite:0]{index=0}

---

## ✏️ 1. Airfoil Geometry Generation

MATLAB was used to derive airfoil points from the analytic Joukowski equations.

- Maximum thickness-to-chord: **9%**  
- Maximum camber-to-chord: **5%**  
- Angle of attack used for analysis: **7°**

The code (page 3) computes:
- Airfoil coordinates  
- Chord length  
- Transformation parameters (b, e, β)  
- Final airfoil curve plot  

> See page 3 for the MATLAB script and the airfoil plot.  
:contentReference[oaicite:1]{index=1}

---

## 🌬️ 2. Streamlines Around the Airfoil

Using potential flow elements around a cylinder (vortex + doublet + uniform flow) and the **Joukowski transformation**, streamlines were mapped to the airfoil plane.

MATLAB steps (page 4):

- Compute velocity potential around cylinder  
- Extract stream function Ψ  
- Apply the Joukowski transform  
- Plot streamlines over the airfoil geometry  

This shows how circulation and camber affect flow turning and lift.  
:contentReference[oaicite:2]{index=2}

---

## 💨 3. Surface Velocity Distribution

Velocity was computed separately for:

- Upper surface  
- Lower surface  

Key observations:

- Upper-surface velocity increases significantly due to suction  
- Lower-surface velocity is lower  
- The difference drives lift  

See the plots and MATLAB code on **page 5** of the report.  
:contentReference[oaicite:3]{index=3}

---

## 📉 4. Pressure Coefficient (Cp) Distribution

Cp was computed from the velocity ratio:

- **Cp = 1 − (V / V∞)²**

The plot (page 6) shows:

- Strong suction peak at the leading edge on the upper surface  
- Nearly flat Cp on the lower surface  
- This again confirms positive lift generation  

A screenshot of the Cp plot appears on page 6 of the report.  
:contentReference[oaicite:4]{index=4}

---

## 🪂 5. Lift & Moment Coefficients vs. Angle of Attack

Angles analyzed: **–5° → +10°**

Results (page 7):

- Lift coefficient **Cl increases linearly** with angle of attack (as expected from thin-airfoil theory)  
- Moment coefficient at the leading edge **decreases** with increasing angle  

MATLAB generated two figures:
- Cl vs. AoA  
- Cm_le vs. AoA  

These show the classical aerodynamic behavior of a cambered airfoil.  
:contentReference[oaicite:5]{index=5}

---

## 🖥️ 6. ANSYS Fluent Simulation

ANSYS Fluent was used to validate the MATLAB/potential flow results.

Simulation included:

- Airfoil geometry import  
- Meshing  
- Steady-flow solver  
- Velocity contours  
- Streamline visualization  
- Pressure field comparison  

This confirms the trends predicted by the analytic method.

---

## 🧠 Summary & Insights

From this project, we learned how:

- Joukowski airfoil theory predicts lift using potential flow  
- Surface velocity and Cp distributions indicate lift generation  
- Lift varies linearly with angle for small AoA  
- CFD (ANSYS Fluent) validates the ideal-theory results  
- MATLAB can be used to implement classic aerodynamic transformations  

This project connects classical aerodynamics with modern simulation tools.  

---

## 🗂️ Files in This Folder

- `Aerodynamic-Project-Phelopater-202001171.pdf` — Full report with MATLAB code, figures, and results  
- `README.md` — This summary file  
