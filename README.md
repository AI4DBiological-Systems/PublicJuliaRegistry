# PublicJuliaRegistry
Public package registry for Julia packages that are developed by the National Research Council of Canada, or its collaborators in the AI-4-Design Challenge funding programs.

Automated via [LocalRegistry.jl](https://github.com/GunnarFarneback/LocalRegistry.jl)

# To connect this registry with your Julia installation
The following line connects this registry along with (re-adding just to be safe) the `General` (i.e. the default public) julia registry to your Julia installation. This only needs to be run once for every Julia installation.
```
using Pkg
pkg"registry add General https://github.com/AI4DBiological-Systems/PublicJuliaRegistry"
```

# To install a package from this registry
Make sure this registry is connected to your Julia installation. Then do the typical package installation as if you are installing a package from the main Julia registry. For example, to install `NMRHamiltonian`, do
```
using Pkg
pkg"add NMRHamiltonian"
```

# How it works
For an informal disucssion on how this registry was set up and maintained, see [https://github.com/RoyCCWang/RWPublicJuliaRegistry](https://github.com/RoyCCWang/RWPublicJuliaRegistry).
