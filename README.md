# Cortical-Model-Gamma-Oscillations
Parametric computation and persistent gamma in a cortical model (Chambers et al. 2012)

These are the source files to generate the data in Figs 4-6 of the paper:

"Parametric computation predicts a multiplicative interaction between synaptic
strength parameters that control gamma oscillations" by Jordan D. Chambers,
Blair Bethwaite, Neil T. Diamond, Tom Peachey, David Abramson,
Steve Petrou1 and Evan A. Thomas. 
Frontiers in Computational Neuroscience (2012) 6:1

1) Build the neuron load library from the command line
nrnivmodl mod

2) The python script des2runs.py reads the design file created by Nimrod,
creates a PBS run file which passes the parameters to neuron model and 
submits the run to the PBS queueing system.

3) The matlab script EFPgen.m reads the output files and generates local 
field traces in matlab format (EFP.mat)

4) The matlab script EFP2PSD.m reads the EPF data and creates power spectra
in matlab format (PSD.mat)

5) The matlab script singleoutput.m reads the PSD file and generates the
output used in figs 4, 5 and 6 of the paper.

You will almost certainly need to modify these scripts to work in your
environment.
