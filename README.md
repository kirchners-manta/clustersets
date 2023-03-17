# Cluster sets for QCE calculations using Peacemaker

This repository contains cluster sets that can be employed to perform Quantum Cluster Equilibrium (QCE) calculations with the [Peacemaker software package](https://github.com/kirchners-manta/peacemaker3). The collection of cluster sets is continuously growing and will be updated regularly. There is no warranty that the cluster sets are complete, i.e. that they contain all possible clusters for a given system.

## Structure 

The clustersets are stored in different directories, depending on whether it is a pure, binary or multi-component system. For every system, the necessary *flist* and *xyz* files are stored in separate folders. A sketch of the directory structure is shown below.

```
Clustersets
│   README.md
│   LICENSE
|    
└───│──────────────────────────────│───────────────────────────────────│
    │                              │                                   │
pure_systems                    binary_systems                      ternary_systems
    │                              │                                ...
    └───system_1                   └───system_1
    │   └───xyz                    │   └───component_a
    │   │   │   a1-1.xyz           │   │     │
    │   │   │   a2-2.xyz           │   │     └───xyz
    │   │   │   ...                │   │     │   │   a1-1.xyz 
    │   │                          │   │     │   │   a2-2.xyz
    │   └───flist                  │   │     │   │   ... 
    │       │   a1-1.flist         │   │     │
    │       │   a2-2.flist         │   │     └───flist
    │       │   ...                │   │         │   a1-1.flist
    │                              │   │         │   a2-2.flist 
    └───system_2                   │   │         │   ...
        ...                        │   │
                                   │   └───component_b
                                   │   │     │  
                                   │   │     └───xyz
                                   │   │     │   │   b1-1.xyz
                                   │   │     │   │   b2-2.xyz
                                   │   │     │   │   ...
                                   │   │     │
                                   │   │     └───flist
                                   │   │         │   b1-1.flist
                                   │   │         │   b2-2.flist
                                   │   │         │   ...
                                   │   │
                                   │   └───mixture_ab
                                   │         │  
                                   │         └───xyz
                                   │         │   │   a1b1-1.xyz
                                   │         │   │   a1b1-2.xyz
                                   │         │   │   ...
                                   │         │
                                   │         └───flist
                                   │             │   a1b1-1.flist
                                   │             │   a1b1-2.flist
                                   │             │   ...
                                   │
                                   └───system_2
                                       ...

```

## Problems:
- HCL: no hessian for heptamer-6cyc-1 
