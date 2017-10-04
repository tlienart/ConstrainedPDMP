# Constrained PDMP

In this repository, two notebooks are available:

* `ConstrainedLogReg-demo.ipynb`: shows how to declare a model using the PDMP library, it is similar though more specialised than the examples found in the documentation of [PDMP.jl](https://github.com/alan-turing-institute/PDMP.jl).
* `ConstrainedLogReg-exps.ipynb`: which reproduces the experiment results presented in the paper *Piecewise Deterministic Markov Processes for Scalable Monte Carlo on Restricted Domains* by Bierkens et al.

Executing the second notebook completely may take a significant amount of time for all the experiments to be computed.

## Installation and Requirements

### For the demo

* [Julia 0.6](https://julialang.org/downloads/) (Julia 0.5 will also work)

In a Julia REPL:

```julia
Pkg.update()
Pkg.add("IJulia")
```

This demo uses the package [PDMP.jl](https://github.com/alan-turing-institute/PDMP.jl) which you can install by doing

```julia
Pkg.clone("https://github.com/alan-turing-institute/PDMP.jl")
Pkg.build("PDMP")
```

Next,

* quit Julia
* start Jupyter `jupyter notebook`
* open the notebook `*-demo.ipynb` and go through it.

**Note**: when using Julia 0.6, you may get warning boxes. This is because the package relies on `Klara.jl`, an external package that does not yet meet the new syntax requirements. If you'd like to not see such warnings, run this in a Julia REPL:

```
using IJulia
IJulia.installkernel("Julia nodeps", "--depwarn=no")
```

then restart the notebook and change the kernel to `Julia nodeps`.

### For the experiments

* To display figures, you will need the `PyPlot` package.
