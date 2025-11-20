# PROTEIN-LIGAND-DOCKING-7L0D-SARS-CoV-2-Main-Protease-Mpro-in-Complex-with-ML188-
PROTEIN LIGAND DOCKING 7L0D = SARS-CoV-2 Main Protease (Mpro) in Complex with ML188 
Protein-Ligand Docking Simulation: SARS-CoV-2 Mpro and Inhibitor 0EN 🦠💻

Overview

This repository contains the complete input, configuration, and result files for a Protein-Ligand Docking simulation using AutoDock Vina. The objective was to predict the most stable binding pose and affinity of the small molecule inhibitor 0EN within the active site of the SARS-CoV-2 Main Protease (Mpro).

Mpro is a critical enzyme necessary for viral replication, making it a key drug target in COVID-19 research. This simulation provides computational evidence of the predicted interaction strength and binding geometry.

Target System Details

    Protein Target (Receptor): SARS-CoV-2 Main Protease (Mpro), based on PDB ID 7L0D.

    Ligand (Inhibitor): Compound 0EN.

    Software Used: AutoDock Vina.

    Goal: Predict the binding affinity and conformation of the 0EN inhibitor to Mpro.

Simulation Results and Configuration

1. Best Binding Affinity

The simulation successfully predicted multiple binding modes. The top predicted affinity score indicates the predicted strength of the interaction.
Mode	Affinity (kcal/mol)
1 (Best Pose)	-5.8

A lower (more negative) binding affinity score suggests a more favorable and stable binding interaction.

2. Docking Grid Parameters

The search space for the docking run was defined by the coordinates in the config.txt file, encompassing the suspected binding pocket:
Parameter	Value (Angstroms)
center_x	11.958
center_y	-9.895
center_z	8.418
size_x	108
size_y	126
size_z	126

Repository Files

File Name	Description	Category
SARS_PROTEIN.pdb	Original PDB structure of the Mpro receptor.	Input
SARS_PROTEIN.pdbqt	Receptor file prepared for AutoDock Vina (includes charges and atom types).	Input
0EN.pdb	Original PDB structure of the 0EN ligand.	Input
Lig.pdbqt	Ligand file prepared for AutoDock Vina.	Input
config.txt	Configuration file specifying the grid box coordinates and input/output names.	Input/Config
out.pdbqt	Docking results file containing all predicted poses and their affinity scores.	Output
out.pdb	PDB format of the best predicted binding pose (Mode 1).	Output
log.txt	AutoDock Vina log file, detailing the execution summary and affinity scores table.	Output/Log
COMMAND PROMPT RESULTS.txt	Raw console output from the Vina execution.	Output/Log
7l0d.cif	Crystallographic Information File (CIF) for the reference PDB structure.	Context

Setup and Visualization

To visualize the predicted protein-ligand complex and analyze the molecular interactions:

    Dependencies: Install a molecular visualization tool such as PyMOL or ChimeraX.

    Load Structures:

        Load the prepared receptor structure: SARS_PROTEIN.pdb.

        Load the docking result file: out.pdbqt. (The viewer will display all binding poses; focus on Mode 1.)

    Analysis: Inspect the best pose (out.pdb) to identify key molecular interactions (e.g., hydrogen bonds, hydrophobic contacts) between the 0EN ligand and the amino acid residues in the Mpro active site.
