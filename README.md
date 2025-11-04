# Quantum Oracle for Shor's Algorithm

This repository contains a rudimentary QROM Builder that takes a function, defined according to its truth table via a Python dictionary, and encodes it in a quantum circuit.

## Description

This notebook walks through the develop of a QROM function; a Qiskit function that, in essence, takes a boolean function f 
and outputs an associated quantum circuit U. 

We will do one of the `straightforward' implementation of the task, by creating a function 'build_qrom' that takes in the function input as a dictionary, effectively describing the truth table of the function, and then translating this information into an equivalent quantum circuit. 

Obviously, this is computationally intensive to say the least, but it gets the job done for our current purposes (and the fact that I don't have as much time right now as for the last mini progject).

I plan on eventually updating this code so that it is compatible with the lamba calculus, taking such a function and ``deconstructing" it into indecomposable logical operations, and then including the equivalent quantum gate to the circuit, effectively acting as a "quantum compiler" (if that is the correct way of thinking of such an operation). 
I believe this would get such a function to be closer to a state-of-the-art functino to complete the given task. 

### Technical Requirements

This project requires Python 3 and the following Python libraries:
* Qiskit
* MatPlotLib
* NumPy

## Usage

The main implementation and verification for the oracle are contained within the `QROMBuilder.ipynb' notebook. 

## References

[Nag25] Nagy, A. (2025), *Course Notes: Erdos Institute Fall 2025 Quantum Computing Bootcamp*

[Ngu24] Nguyen, H. (2024), *Implement the Deutsch-Jozsa Algorithm in Qiskit and IBM Quantum*, Medium. Available at: https://hoaio.medium.com/implement-the-deutsch-jozsa-algorithm-in-qiskit-and-ibm-quantum-98d7c12e87f6.

[NC10] Nielsen, M. A., & Chuang, I. L. (2010), *Quantum Computation and Quantum Information: 10th Anniversary Edition*, Cambridge University Press.

[Qis25] Qiskit contributors (2025), Learn Quantum Computation using Qiskit, https://qiskit.org/learn

## Statement on use of AI 
Google's Gemini 3 LLM was used in the development of this project. Specifically, I used it to explain the use of the MCX gate and go through simple examples
which substantially increased my understanding of the mathematics of the gate ( I understood how it could be used in this algorithm, but wanted to understand
the underlying operators). It was also used to quickly debug cells in the Jupyter notebook and generate tests to ensure that my code was working as intended. 
I also used it to quickly calculate the Boolean values for the modular function used as the last example in the notebook, and generate the corresponding
Python dictionary. 
