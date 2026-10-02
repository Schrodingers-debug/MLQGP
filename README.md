# MLQGP

This work uses a small neural network to describe the quark-gluon plasma, the hot matter made of quarks and gluons. The network is trained on lattice results for pressure, energy, and related quantities, and it learns how the effective quark and gluon masses depend on temperature and density. Those masses are then used to calculate how the plasma conducts electricity and heat, including the Seebeck and Thomson coefficients. Separate fits to the upper and lower lattice bands give a range around the central result.

MLQGPS.ipynb trains the central model on Thermo_data_central.csv and writes mlqgps_model.
MLQGPS_uplow.ipynb is the same training on the high and low tables. Upper weights go to mlqgps_model_upper, lower weights to mlqgps_model_lower.
MLQGPS_fit_plots.ipynb loads the central weights and plots the loss, the lattice fit, and the masses.
seebeck_og.ipynb loads the central weights and computes conductivity, Seebeck, and Thomson.
MLQGPS_band.ipynb loads central, upper, and lower and plots each set, then the band between them.
