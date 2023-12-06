# Definition
- The first computational model of a neuron was proposed by Warren MuCulloch (neuroscientist) and Walter Pitts (logician) in 1943.
- All weights are **equal**.
- Positive weights are excitatory ad negative are inhibitory.
- Inputs and outputs can be 0 or 1 only means **Boolean only**.
- Excitatory inputs are NOT the ones that will make the neuron fire on their own but they might fire it when combined together.
- M-P neuron is able to conveniently represent the boolean functions which are linearly separable.
- **Linear separability:** (for boolean functions): There exists a line (plane) such that all inputs which produce a 1 lie on one side of the line (plane) and all inputs which produce a 0 lie on other side of the line (plane).

# Architecture
![[Pasted image 20231206172309.png]]

# Limitations
- What about non-boolean (say, real) inputs?
- Do we always need to hand code the threshold?
- Are all inputs equal? What if we want to assign more importance to some inputs?
- What about functions which are not linearly separable? Say XOR function.

