---
theme: seriph
background: https://cover.sli.dev
title: From Numerical Methods to SHYFEM
info: |
  ## From Numerical Methods to SHYFEM
  A progressive learning and teaching module on conservation laws,
  shallow-water equations, and finite-element hydrodynamic modeling.
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 45min
---

<RestartOnEnter><LorenzBackground /></RestartOnEnter>

# From Numerical Methods to SHYFEM

### Conservation Laws, Shallow-Water Equations, and Finite Elements

<div class="mt-8 text-sm opacity-70">
Enrico Baglione
</div>

---

# Purpose of This Module
## Learning and teaching through the same workflow

<div class="grid grid-cols-2 gap-10 mt-10">

<div v-click class="bg-blue-50 border border-blue-200 rounded-lg px-6 py-5 text-left">

### Learning objective

Understand the physical and numerical foundations required to configure, run, and evaluate SHYFEM.

</div>

<div v-click class="bg-teal-50 border border-teal-200 rounded-lg px-6 py-5 text-left">

### Teaching objective

Transform each verified learning step into reusable material for a Numerical Modeling course.

</div>

</div>

---

# Starting Point
## Concepts already covered in the Numerical Modeling course

<div class="grid grid-cols-2 gap-8 mt-6 text-left">

<div>

- Time discretization
- Explicit and implicit methods
- Runge-Kutta methods
- Linear multistep and BDF methods
- Space-time discretization

</div>

<div>

- Transport equation
- Numerical advection schemes
- Dissipation and dispersion
- Von Neumann stability analysis
- CFL and boundary conditions

</div>

</div>

<div v-click class="mt-8 px-5 py-3 rounded-lg bg-gray-100 border border-gray-300">

The next step is the transition from discrete operators on regular grids to conservation laws and unstructured finite-element meshes.

</div>

---
layout: section
---

<RestartOnEnter>
  <SpirographBackground :speed="50" :trailLength="11000" />
</RestartOnEnter>

# Learning Roadmap

From governing equations to a working hydrodynamic model

---

# Course Roadmap
## Progressive modules

<div class="flex flex-col gap-2 mt-4 text-left text-sm">

<div class="px-4 py-2 rounded-lg bg-blue-50 border border-blue-200 text-blue-900">
<span class="font-bold mr-2">1.</span> Conservation Laws and Integral Balances
</div>

<div class="px-4 py-2 rounded-lg bg-blue-50 border border-blue-200 text-blue-900">
<span class="font-bold mr-2">2.</span> From Navier-Stokes to the Shallow-Water Equations
</div>

<div class="px-4 py-2 rounded-lg bg-teal-50 border border-teal-200 text-teal-900">
<span class="font-bold mr-2">3.</span> Finite Differences, Finite Volumes, and Finite Elements
</div>

<div class="px-4 py-2 rounded-lg bg-teal-50 border border-teal-200 text-teal-900">
<span class="font-bold mr-2">4.</span> Weak Formulation and Linear Finite Elements
</div>

<div class="px-4 py-2 rounded-lg bg-yellow-50 border border-yellow-200 text-yellow-900">
<span class="font-bold mr-2">5.</span> Triangular Elements and Unstructured Meshes
</div>

<div class="px-4 py-2 rounded-lg bg-yellow-50 border border-yellow-200 text-yellow-900">
<span class="font-bold mr-2">6.</span> Semi-Implicit Hydrodynamic Schemes
</div>

<div class="px-4 py-2 rounded-lg bg-purple-50 border border-purple-200 text-purple-900">
<span class="font-bold mr-2">7.</span> SHYFEM Workflow, Verification, and Validation
</div>

</div>

---

# From Physics to Model Output
## The complete workflow

<div class="mt-10 grid grid-cols-4 gap-3 text-sm">

<div v-click="1" class="rounded-lg border border-blue-200 bg-blue-50 p-4">
<div class="font-bold">Physical system</div>
<div class="mt-2 opacity-70">Scales and processes</div>
</div>

<div v-click="2" class="rounded-lg border border-blue-200 bg-blue-50 p-4">
<div class="font-bold">Governing equations</div>
<div class="mt-2 opacity-70">Mass and momentum</div>
</div>

<div v-click="3" class="rounded-lg border border-teal-200 bg-teal-50 p-4">
<div class="font-bold">Discretization</div>
<div class="mt-2 opacity-70">Space and time</div>
</div>

<div v-click="4" class="rounded-lg border border-purple-200 bg-purple-50 p-4">
<div class="font-bold">Model output</div>
<div class="mt-2 opacity-70">Verification and validation</div>
</div>

</div>

<div v-click="5" class="mt-10 text-xl">

$$
\text{Physics}
\rightarrow
\text{Mathematical model}
\rightarrow
\text{Numerical model}
\rightarrow
\text{Scientific interpretation}
$$

</div>

---

# Development Rule
## Content grows together with understanding

<div class="grid grid-cols-4 gap-4 mt-10 text-sm">

<div class="rounded-lg bg-gray-100 border border-gray-300 p-4">
<div class="font-bold">PLANNED</div>
<div class="mt-2">Structure defined</div>
</div>

<div class="rounded-lg bg-yellow-50 border border-yellow-300 p-4">
<div class="font-bold">DRAFT</div>
<div class="mt-2">Initial explanation</div>
</div>

<div class="rounded-lg bg-blue-50 border border-blue-300 p-4">
<div class="font-bold">VERIFIED</div>
<div class="mt-2">Physics and equations checked</div>
</div>

<div class="rounded-lg bg-teal-50 border border-teal-300 p-4">
<div class="font-bold">TEACHING-READY</div>
<div class="mt-2">Classroom review completed</div>
</div>

</div>

<div v-click class="mt-10 italic opacity-75">
No topic is presented as consolidated knowledge before its assumptions and limits are understood.
</div>

---
layout: section
---

<RestartOnEnter>
  <WaveBackground :speed="0.012" />
</RestartOnEnter>

# Module 1

Conservation Laws and Integral Balances

---

# Module 1 — Learning Questions
## Status: PLANNED

<div class="text-left mt-8">

1. What does it mean for a physical quantity to be conserved?
2. How is a balance written over a control volume?
3. What is the relation between integral and differential forms?
4. What do flux and source terms represent?
5. How does mass conservation lead to the continuity equation?
6. Which parts of this structure are inherited by the shallow-water equations?

</div>

<div v-click class="mt-8 px-5 py-3 rounded-lg bg-blue-50 border border-blue-200">

The first worked example will be added after the integral balance and the divergence theorem have been reviewed.

</div>

---

# Reusable Structure for Each Topic
## From definition to SHYFEM

<div class="grid grid-cols-3 gap-4 mt-8 text-sm">

<div class="rounded-lg border border-blue-200 bg-blue-50 p-4">
<div class="font-bold">1. Definition</div>
<div class="mt-2">What is the concept?</div>
</div>

<div class="rounded-lg border border-blue-200 bg-blue-50 p-4">
<div class="font-bold">2. Physical meaning</div>
<div class="mt-2">Which process does it describe?</div>
</div>

<div class="rounded-lg border border-teal-200 bg-teal-50 p-4">
<div class="font-bold">3. Formulation</div>
<div class="mt-2">How is it written mathematically?</div>
</div>

<div class="rounded-lg border border-teal-200 bg-teal-50 p-4">
<div class="font-bold">4. Discretization</div>
<div class="mt-2">How is it represented numerically?</div>
</div>

<div class="rounded-lg border border-yellow-200 bg-yellow-50 p-4">
<div class="font-bold">5. Minimal example</div>
<div class="mt-2">Can the behavior be reproduced?</div>
</div>

<div class="rounded-lg border border-purple-200 bg-purple-50 p-4">
<div class="font-bold">6. SHYFEM link</div>
<div class="mt-2">Where does it appear in the model?</div>
</div>

</div>

---

# Next Learning Step
## Conservation over a control volume

<div class="mt-12 text-2xl">

$$
\text{Rate of accumulation}
=
\text{Inflow}
-
\text{Outflow}
+
\text{Sources}
-
\text{Sinks}
$$

</div>

<div v-click class="mt-12 text-sm opacity-70">

This statement will become the starting point for the continuity equation and the finite-volume comparison.

</div>

