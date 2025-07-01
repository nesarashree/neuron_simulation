# Leaky Integrate and Fire Neurons
In biological neurons, the electrical action potential initiated in the cell body travels along a presynaptic cell axon & jumps to a postsynaptic cell (synapse). Spikes are the emergence of action potentials. To visualize these spikes, I ran a simulation graphing membrane potential wrt time. Neuron behavior is mathematically modeled by the Leaky Integrate-and-Fire (LIF) with the following parameters:
* resting potential
* reset voltage
* firing threshold
* membrane resistance
* membrane time-scale
* absolute refractory period
LIF artificially reconstructs how neurons fire across a membrane threshold, creating spikes (or action potentials) that then serve as neural (network!) signals.

## 1D LIF SIMULATION
1D LIF simulation:
* V = membrane potential
* tau = time constant (how quickly the neuron integrates inputs)
* t0, t1, t2: = spike times
* w = synaptic weight (neuron receives a spike, V increases by w)
* Vt = firing threshold
[ADD IMAGE]
General model: if voltage is greater than the firing threshold, fire a spike, reset

[ADD IMAGE]
snnTorch’s recursive representation of the LIF neuron.
