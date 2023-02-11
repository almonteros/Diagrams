# Diagrams

A work in progress. I am writing code in Rust to draw and analyze Feynman diagrams. The starting point is a more basic (while still interesting) situation that uses Feynman diagrams. The basic idea is to input a Hamiltonian with a free and intereacting part. Then output the Feynman diagrams to the desired order, analyzed and sorted. Finally, (if working in the Matsubara formulation) solve simple Matsubara Summations symbolically. The output is the (Matsubara) Green's function also sometimes known as the correlator or propagator. Finally I would like to wrap it all up as a Python library. 

This is project is partially a labor of love and partially for my own edification.

This work is based off of previous work I did in Python. The purpose of this project is three fold.

- To become better acquanted with the Rust programming language
- To leverage Rust's speed advantage (over Python)
- To parallelize processes safetly

The general approach is as follows.

1) Define Operators

   i) Create operators struct
  
   ii) Overload operations
  
   iii) Define commutation relations
  
  iv) Impliment Wick's theorem
  
2) Define Diagrams

   i) Choose between an adjacency matric or adjacency list, previous choice was the matrix
   
   ii) Create routines to analyze diagrams (e.g. DFT, permutation)
   
   iii) Impliment Fourier Transform
   
3) Matsubara Summation

   i) Impliment a method to solve the Matsubara Summations
   
4) Pythonize
   
   i) Create a Python package 
