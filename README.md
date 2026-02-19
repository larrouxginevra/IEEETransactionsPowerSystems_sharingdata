# IEEETransactionsPowerSystems_sharingdata

This repository provides the input data required to reproduce the simulation results presented in the manuscript **"Enhancing Power Systems Transmission Adequacy via Optimal BESS Siting and Sizing Using Benders Decomposition with Feasibility Cuts"**, submitted to *IEEE Transactions on Power Systems*.

## Power-flow inputs (`PF_input/`)

The following files are used as inputs to the power-flow computations.

**Note:** `P_input` matches the dataset published on IEEE DataPort (linked below). `Q_input` is reconstructed as described in the paper.  
IEEE DataPort reference: https://ieee-dataport.org/documents/time-series-data-load-generation-and-power-flow-ieee-bus-systems

- `P_input.npy` — nodal active power injections  
- `Q_input.npy` — nodal reactive power injections  
- `V_input.npy` — nodal voltage magnitudes  
- `Q_limits_l.npy` — lower limit on nodal reactive power  
- `Q_limits_u.npy` — upper limit on nodal reactive power  

## Power-flow outputs (`PF_output/`)

The following files are outputs of the power-flow computations and serve as inputs to the optimization problem described in the paper.

**Note:** at buses with generators, the generators’ reactive power (a decision variable in the optimization problem) is subtracted from `Q_PF`.

- `P_PF.npy` — nodal active power injections  
- `Q_PF.npy` — nodal reactive power injections  


