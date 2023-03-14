# Clustersets

**This repository contains clustersets.** <p>
**The aim is to provide peacemaker users with a choice of cluster sets.**

## Structure 

- The clustersets are stored in different folders depending on whether it is a pure, binary or ternary system.
- For every system *flist* and *xyz* files are stored in separate folders.

```
Clustersets
│   README.md
│    
└───│──────────────────────────────│───────────────────────────────────│
    │                              │                                   │
pure_systems                    binary_systems                      ternary_systems
    │                              │                                ...
    └───system_1                   └───system_1
    │   └───xyz                    │   └───component_a
    │   │    │   a1-1.xyz          │   │      │
    │   │    │   a2-2.xyz          │   │      └───xyz
    │   │    │   ...               │   │      │    │   a1-1.xyz 
    │   │                          │   │      │    │   a2-2.xyz
    │   └───flist                  │   │      │    │   ... 
    │       │   a1-1.flist         │   │      │
    │       │   a2-2.flist         │   │      └───flist
    │       │   ...                │   │          │   a1-1.flist
    │                              │   │          │   a2-2.flist 
    └───system_2                   │   │                  │   ...
        ...                        │   │
                                   │   └───component_b
                                   │   │     │  
                                   │   │     └───xyz
                                   │   │     │    │   b1-1.xyz
                                   │   │     │    │   b2-2.xyz
                                   │   │     │    │   ...
                                   │   │     │
                                   │   │     └───flist
                                   │   │         │   b1-1.flist
                                   │   │         │   b2-2.flist
                                   │   │         │   ...
                                   │   │
                                   │   └───mixture_ab
                                   │        │  
                                   │        └───xyz
                                   │        │    │   a1b1-1.xyz
                                   │        │    │   a1b1-2.xyz
                                   │        │    │   ...
                                   │        │
                                   │        └───flist
                                   │            │   a1b1-1.flist
                                   │            │   a1b1-2.flist
                                   │            │   ...
                                   │
                                   └───system_2
                                       ...

```