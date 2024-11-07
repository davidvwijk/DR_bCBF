# Disturbance-Robust Backup Control Barrier Functions (DR-bCBF)

_Abstract_ - Obtaining a controlled invariant set is crucial for safety-critical control with control barrier functions (CBFs) but is non-trivial for complex nonlinear systems and constraints. Backup control barrier functions allow such sets to be constructed online in a computationally tractable manner by examining the evolution (or flow) of the system under a known backup control law. However, for systems with unmodeled disturbances, this flow cannot be directly computed, making the current methods inadequate for assuring safety in these scenarios. To address this gap, we leverage bounds on the nominal and disturbed flow to compute a forward invariant set online by ensuring safety of an expanding norm ball tube centered around the nominal system evolution. We prove that this set results in robust control constraints which guarantee safety of the disturbed system via our Disturbance-Robust Backup Control Barrier Function (DR-BCBF) solution. Additionally, the efficacy of the proposed framework is demonstrated in simulation, applied to a double integrator problem and a rigid body spacecraft rotation problem with rate constraints.

D. van Wijk, S. Coogan, T. G. Molnar, M. Majji, and K. L. Hobbs, "Disturbance-Robust Backup Control Barrier Functions: Safety Under Uncertain Dynamics", Submitted to IEEE Control Systems Letters (L-CSS) with ACC option. 2024. Preprint: [[link]](https://arxiv.org/abs/2409.07700#)

Code release case number: AFRL-2024-6238

## Supplemental Video: Spacecraft Rotation Example
The objective is to keep the angular velocity trajectory within the red sphere (safe region). Our approach obeys the norm constraint on the angular velocity in the presence of unknown time-varying disturbances, while the standard bCBF approach does not, violating safety multiple times. Click the thumbnail below to watch!

[![Spacecraft Rotation Supplemental Video](https://github.com/davidvwijk/DR-bCBF/blob/main/thumbnail_cropped.jpg)](https://www.youtube.com/watch?v=kJRBKPcA4dk)

## Running the code

1. Install the necessary packages using pip install -r requirements.txt
2. Call main_sim.py for either the spacecraft rotation example or the double integrator example.

To re-create Figure 2 in the paper (phase space visualization of double integrator for multiple backup horizons), call sampleCI.py.
