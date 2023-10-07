# PublicJuliaRegistry
Public package registry for Julia packages that are developed by the National Research Council of Canada (NRC), or its collaborators in the *AI for design of biological systems* master project from the NRC Artificial Intelligence for Design Challenge program.

Automated via [LocalRegistry.jl](https://github.com/GunnarFarneback/LocalRegistry.jl)

# To connect this registry with your Julia installation
The following line connects this registry along with (re-adding just to be safe) the `General` (i.e. the default public) julia registry to your Julia installation. This only needs to be run once for every Julia installation.

HTTPS:
```
using Pkg
pkg"registry add General https://github.com/AI4DBiological-Systems/PublicJuliaRegistry"
```

SSH (use this if you have write access to this registry):
```
using Pkg
pkg"registry add git@github.com:AI4DBiological-Systems/PublicJuliaRegistry.git"
```

# To install a package from this registry
Make sure this registry is connected to your Julia installation. Then do the typical package installation as if you are installing a package from the main Julia registry. For example, to install `NMRHamiltonian`, do
```
using Pkg
pkg"add NMRHamiltonian"
```

# How it works
For an informal disucssion on how this registry was set up and maintained, see [https://github.com/RoyCCWang/RWPublicJuliaRegistry](https://github.com/RoyCCWang/RWPublicJuliaRegistry).

# Troubleshoot
If you see 
```
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:AI4DBiological-Systems/PublicJuliaRegistry.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
while registering/updating a package, it could mean your Julia installation has an older version of this registry. Do the following, then try registering/updating again:
```
import Pkg
Pkg.Registry.update()
```
