# PublicJuliaRegistry
Public package registry for Julia packages that are developed by the National Research Council of Canada, or its collaborators in the AI-4-Design Challenge funding programs.

Automated via [LocalRegistry.jl](https://github.com/GunnarFarneback/LocalRegistry.jl)

# To use a package in this registry
If you want to use one of the packages in this registry, say `NMRHamiltonian`, do:
```
using Pkg
pkg"registry add General https://github.com/AI4DBiological-Systems/PublicJuliaRegistry"
pkg"add NMRHamiltonian"
```

# How it works
For an informal disucssion on how this registry was set up and maintained, see [https://github.com/RoyCCWang/RWPublicJuliaRegistry](https://github.com/RoyCCWang/RWPublicJuliaRegistry).
