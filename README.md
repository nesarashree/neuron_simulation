# Leaky Integrate and Fire (LIF) Neurons

<p align="center">
  <img src="images/unnamed.png" alt="Spike image" width="500px" />
</p>

In biological neurons, the electrical action potential initiated in the cell body travels along a presynaptic cell axon & jumps to a postsynaptic cell (synapse). Spikes are the emergence of action potentials. To visualize these spikes, I ran a simulation graphing membrane potential wrt time. Neuron behavior is mathematically modeled by the Leaky Integrate-and-Fire (LIF) with the following parameters:

* resting potential
* reset voltage
* firing threshold
* membrane resistance
* membrane time-scale
* absolute refractory period

LIF artificially reconstructs how neurons fire across a membrane threshold, creating spikes (or action potentials) that then serve as neural (network!) signals.

## 1D LIF SIMULATION
Models a single neuron’s membrane potential V over time. If voltage V is greater than the firing threshold Vt, fire a spike, and reset.
<p>
  <img src="images/spike.png" alt="Spike image" width="350px" />
</p>

* V = membrane potential
* tau = time constant (how quickly the neuron integrates inputs)
* t0, t1, t2: = spike times
* w = synaptic weight (neuron receives a spike, V increases by w)
* Vt = firing threshold
<p align="center">
  <img src="images/1d_simulation.png" alt="1D simulation snapshot" width="300px">
</p>

## 2D LIF SIMULATION
Models neurons arranged in a two-dimensional grid. At each time step, if `V i,j > Vt i,j` then `neuron (i, j)` fires a spike, resets its membrane potential, and updates its threshold dynamically. Membrane potentials also decay exponentially and integrate inputs from neighbors.

* V i,j = membrane potential of neuron at position (i, j)
* tau = time constant
* input spikes = external inputs to neurons, possibly different for each neuron
* w = synaptic weights (influence from neighboring neurons’ spikes)
* Vt i,j = dynamic firing threshold
<p align="center">
  <img src="images/2D.png" alt="1D simulation snapshot" width="350px">
</p>
