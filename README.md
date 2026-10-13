# NEB Configuration Generation for NiH and PdH

## Overview

This repository contains Fortran 90 programs and LAMMPS input files for automated Nudged Elastic Band (NEB) calculations involving nickel hydride (NiH) and palladium hydride (PdH).

The workflow uses occupation vectors to define configurations, LAMMPS to relax initial and final structures, and Fortran and Bash scripts to automate configuration processing and NEB calculations.

## Repository Structure
NEB-Million-Configurations/
├── README.md
├── Ni/
│   ├── NEB_OCCUP1.txt
│   ├── NiAlH_jea.eam.alloy
│   ├── excute1_4000Nih.f90
│   ├── in_NIH_initial.eam
│   ├── in_NIH_initial1.eam
│   ├── input_NEB
│   ├── occupation_in_1NNN1.txt
│   ├── print_occupation_4000_files_final.f90
│   └── resultP1.sh
└── Pd/
    ├── NEB_OCCUP1.txt
    ├── PdAgH_HybridPd3Ag.eam.alloy
    ├── excute1_4000PdH.f90
    ├── in_PdH_initial.eam
    ├── in_PdH_initial1.eam
    ├── input_NEB
    ├── occupation_in_1NNN1.txt
    ├── print_occupation_4000_files_final.f90
    └── resultP1.sh

## Nickel Hydride (NiH)

The `Ni/` directory contains the files used for the NiH workflow.

(i) NiAlH_jea.eam.alloy`: EAM/alloy potential file used for the NiH system.
(ii) NEB_OCCUP1.txt`: Occupation-vector data used in configuration generation.
(iii) occupation_in_1NNN1.txt`: Occupation-related input data.
(iv) in_NIH_initial.eam`: LAMMPS input for initial-structure relaxation.
(v) in_NIH_initial1.eam`: LAMMPS input for final-structure relaxation.
(vi) input_NEB`: LAMMPS input for NEB calculations.
(vii) print_occupation_4000_files_final.f90`: Fortran 90 program for reading and processing occupation vectors.
(viii) excute1_4000Nih.f90`: Main Fortran 90 program for automating the NiH NEB workflow.
(ix) resultP1.sh`: Bash script for automated execution.

## Palladium Hydride (PdH)

The `Pd/` directory contains the corresponding files for the PdH workflow.

(i) PdAgH_HybridPd3Ag.eam.alloy`: EAM/alloy potential file used for the PdH system.
(ii) NEB_OCCUP1.txt`: Occupation-vector data used in configuration generation.
(iii) occupation_in_1NNN1.txt`: Occupation-related input data.
(iv) in_PdH_initial.eam`: LAMMPS input for initial-structure relaxation.
(v) in_PdH_initial1.eam`: LAMMPS input for final-structure relaxation.
(vi) input_NEB`: LAMMPS input for NEB calculations.
(vii) print_occupation_4000_files_final.f90`: Fortran 90 program for reading and processing occupation vectors.
(viii) excute1_4000PdH.f90`: Main Fortran 90 program for automating the PdH NEB workflow.
(ix) resultP1.sh`: Bash script for automated execution.

## Software Requirements

- Fortran 90-compatible compiler, such as GNU Fortran (`gfortran`).
- LAMMPS with the required NEB and potential support.
- Bash shell and a compatible Linux environment.
- Input structures and occupation-vector files required by the workflow.

## Workflow

1. Read occupation-vector data.
2. Generate or process the required atomic configurations using the Fortran programs.
3. Relax the initial and final structures using LAMMPS.
4. Execute NEB calculations using the `input_NEB` file.
5. Automate the workflow using `resultP1.sh`.

The exact commands and required settings depend on the source code and simulation environment.

## Usage

Run each material's workflow from its corresponding directory after checking the input paths, potential settings, executable names, and LAMMPS configuration.
Here for Ni and Pd case x=0.001 shown, for other x values change in the excute1_4000PdH.f90 and excute1_4000Nih.f90 files.
Before running the scripts, verify that the required input files and LAMMPS executables are available.

## Reproducibility

Document the compiler version, LAMMPS version, potential provenance, system size, and configuration-generation parameters when sharing results.

## License and Potential Files

The source code and potential files may have different licensing or redistribution requirements. Confirm the relevant permissions before redistributing potential files or selecting a repository license.
