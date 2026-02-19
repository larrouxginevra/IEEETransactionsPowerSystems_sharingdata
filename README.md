# IEEETransactionsPowerSystems_sharingdata

This repository provides the data required to reproduce the simulation results presented in the manuscript **“Enhancing Power Systems Transmission Adequacy via Optimal BESS Siting and Sizing Using Benders Decomposition with Feasibility Cuts”**, submitted to *IEEE Transactions on Power Systems*.

## Power flow inputs (`PF_input/`)

The following files are used as inputs to the power-flow computations.

**Note:** nodal active power injections are not included in this repository, as they are taken from the IEEE DataPort dataset linked below. `Q_input` is reconstructed as described in the paper and includes load _only_ (i.e., not generator) reactive power. `Q_min` and `Q_max` are obtained by combining generators’ reactive power limits with fixed load contributions.

IEEE DataPort reference: https://ieee-dataport.org/documents/time-series-data-load-generation-and-power-flow-ieee-bus-systems

- `Q_input.npy` — nodal reactive power injections (load only)
- `V_input.npy` — nodal voltage magnitudes
- `Q_min.npy` — lower bound on nodal reactive power
- `Q_max.npy` — upper bound on nodal reactive power

## Power flow outputs (`PF_output/`)

The following files are outputs of the power flow computations and serve as inputs to the optimization problem described in the paper.

**Note:** generator reactive power is treated as a decision variable in the optimization problem; therefore, at buses with generators, the reactive power injections used are taken from `Q_input`.

- `S_PF.npy` — nodal apparent power injections (complex)
- `V_PF.npy` — nodal voltage phasors (complex)


