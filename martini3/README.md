Martini 3 Phosphoinositide Parameters
======================================================================

These parameters have been developed to take full advantage of the Martini 3
improved interaction matrix. The parameterization procedure is detailed in the
ChemRxiv preprint manuscript:
  * L. Borges-Araújo, P.C.T. Souza, F. Fernandes and M.N. Melo, _Improved
Parameterization of Phosphatidylinositide Lipid Headgroups for the Martini 3
Coarse-Grain Force Field_, J. Chem. Theory Comput., 2021
[doi:10.1021/acs.jctc.1c00615](https://doi.org/10.1021/acs.jctc.1c00615)

When using these parameters, please cite this reference.

The `CHANGELOG.old.md` document details the development prior to version
control under git.

Finally, be sure to check back for any parameter updates!

The following `insane.py` entry can be used to prepare lipid membranes
with these phosphoinositide parameters.
```
moltype = "INOSITOLLIPIDS"
lipidsx[moltype] = (   .5,  .5,   0,  .25,   0,   0, .5,  1,  0,   .5,   0,   0,   0,   0,   0,   0,   1,   1,   1,   1,   1,   1)
lipidsy[moltype] = (    0,   0,   0,    0,   0,   0,  0,  0,  0,    0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0)
lipidsz[moltype] = (    8,   9,   9,  8.5,   7,  10, 10, 10,  6,    6,   5,   4,   3,   2,   1,   0,   5,   4,   3,   2,   1,   0)
lipidsa.update({       # 1    2    3    4    5     6   7   8  9    10   11   12   13   14   15    16   17   18   19   20   21   22
    "POPI": (moltype, " C1   C2   C3   C4   PO4   -   -   -  GL1  GL2  C1A  D2A  C3A  C4A   -     -   C1B  C2B  C3B  C4B   -    -"),
    "POP1": (moltype, " C1   C2   C3   C4   PO4  P3   -   -  GL1  GL2  C1A  D2A  C3A  C4A   -     -   C1B  C2B  C3B  C4B   -    -"),  # POP1_3
    "POP4": (moltype, " C1   C2   C3   C4   PO4   -  P4   -  GL1  GL2  C1A  D2A  C3A  C4A   -     -   C1B  C2B  C3B  C4B   -    -"),  # POP1_4
    "POP5": (moltype, " C1   C2   C3   C4   PO4   -   -  P5  GL1  GL2  C1A  D2A  C3A  C4A   -     -   C1B  C2B  C3B  C4B   -    -"),  # POP1_5
    "POP2": (moltype, " C1   C2   C3   C4   PO4  P3  P4   -  GL1  GL2  C1A  D2A  C3A  C4A   -     -   C1B  C2B  C3B  C4B   -    -"),  # POP2_34
    "POP7": (moltype, " C1   C2   C3   C4   PO4  P3   -  P5  GL1  GL2  C1A  D2A  C3A  C4A   -     -   C1B  C2B  C3B  C4B   -    -"),  # POP2_35
    "POP6": (moltype, " C1   C2   C3   C4   PO4   -  P4  P5  GL1  GL2  C1A  D2A  C3A  C4A   -     -   C1B  C2B  C3B  C4B   -    -"),  # POP2_45
    "POP3": (moltype, " C1   C2   C3   C4   PO4  P3  P4  P5  GL1  GL2  C1A  D2A  C3A  C4A   -     -   C1B  C2B  C3B  C4B   -    -"),  # POP3_345
    "SAPI": (moltype, " C1   C2   C3   C4   PO4   -   -   -  GL1  GL2  C1A  D2A  D3A  D4A  C5A    -   C1B  C2B  C3B  C4B   -    -"),
    "SAP1": (moltype, " C1   C2   C3   C4   PO4  P3   -   -  GL1  GL2  C1A  D2A  D3A  D4A  C5A    -   C1B  C2B  C3B  C4B   -    -"),  # SAP1_3
    "SAP4": (moltype, " C1   C2   C3   C4   PO4   -  P4   -  GL1  GL2  C1A  D2A  D3A  D4A  C5A    -   C1B  C2B  C3B  C4B   -    -"),  # SAP1_4
    "SAP5": (moltype, " C1   C2   C3   C4   PO4   -   -  P5  GL1  GL2  C1A  D2A  D3A  D4A  C5A    -   C1B  C2B  C3B  C4B   -    -"),  # SAP1_5
    "SAP2": (moltype, " C1   C2   C3   C4   PO4  P3  P4   -  GL1  GL2  C1A  D2A  D3A  D4A  C5A    -   C1B  C2B  C3B  C4B   -    -"),  # SAP2_34
    "SAP7": (moltype, " C1   C2   C3   C4   PO4  P3   -  P5  GL1  GL2  C1A  D2A  D3A  D4A  C5A    -   C1B  C2B  C3B  C4B   -    -"),  # SAP2_35
    "SAP6": (moltype, " C1   C2   C3   C4   PO4   -  P4  P5  GL1  GL2  C1A  D2A  D3A  D4A  C5A    -   C1B  C2B  C3B  C4B   -    -"),  # SAP2_45
    "SAP3": (moltype, " C1   C2   C3   C4   PO4  P3  P4  P5  GL1  GL2  C1A  D2A  D3A  D4A  C5A    -   C1B  C2B  C3B  C4B   -    -"),  # SAP3_345
    "PLPI": (moltype, " C1   C2   C3   C4   PO4   -   -   -  GL1  GL2  C1A  D2A  D3A  C4A   -     -   C1B  C2B  C3B  C4B   -    -"),
    "SDPI": (moltype, " C1   C2   C3   C4   PO4   -   -   -  GL1  GL2  D1A  D2A  D3A  D4A  D5A    -   C1B  C2B  C3B  C4B   -    -"),
})
```
