
# Git Repo accompanying "A Comparison of Programming Languages in Economics" by Jesus Fernandez-Villaverde and S. Boragan Aruoba

Notice that this repo is (for now) run without knowledge or approval of the authors. I just set this up to better tweek the code. 


## My results

I focused on typing the Julia code. I saw that the REPL spends a lot of time inferring types. 

* I achieve a speedup of 18% by typing the model before executing the computation function. 
* I obtain a speedup of 24% with respect to the original code by using linear indices and by switching off bounds checking.

In order to run my code execute line by line `RBC_codes/julia/main.jl`



# Here is their original readme file:


Files:

1) RBC_CPP.cpp: C++ code. 
2) RBC_F90.f90: Fortran code.
3) RBC_F90i.f90: Fortran code, intel compiler (time function does not work with intel)
3) RBC_Julia.jl: Julia code, to run RBC_Julia; @time main() you may want to warm up the JIT before testing for speed.
4) RBC_Matlab.m: Matlab code.
5) RBC_Python.py: Python code.
7) RBC_R.R: R code.
8) RBC_R_Compiler.R: R code compiled.
9) RBC_Mathematica: Mathematica code.

Compilation flags

1) GCC compiler (Mac): g++ -o testc -O3 RBC_CPP.cpp
2) GCC compiler (Windows): g++ -Wl,--stack,4000000, -o testc -O3 RBC_CPP.cpp 
3) Clang compiler: clang++ -o testclang -O3 RBC_CPP.cpp
4) Intel compiler: icpc -o testc -O3 RBC_CPP.cpp
5) Visual C: cl /F 4000000 /o testvcpp /O2 RBC_CPP.cpp 
6) GCC compiler: gfortran -o testf -O3 RBC_F90.f90
7) Intel compiler: ifortran -o testf -O3 RBC_F90.f90
8) javac RBC_Java.java and run as java RBC_Java -XX:+AggressiveOpts

