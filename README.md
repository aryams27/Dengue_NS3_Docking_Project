# Dengue_NS3_Docking_Project
In Silico Analysis of Antiviral Compounds Against Dengue Virus NS3 Protein

## Objective
Perform molecular docking of antiviral compounds (Asunaprevir and Simeprevir) against the dengue virus NS3 protein, starting from homology modeling and analyzing interactions using Discovery Studio.

## Tools Used
- **Discovery Studio** – Visualization of protein-ligand interactions
- **AutoDock Vina** – Molecular docking
- **Python** – Programming-based binding affinity calculation
- **Open Babel** – Used for file format conversion
- **Cygwin** – Used to run AutoDock and obtain docking result files (.dlg).
- **PyMOL** – Used for validation of the homology model by superimposing structures and calculating RMSD values to assess structural accuracy.

## Workflow
1. **Homology Modeling of NS3 Protein**  
   - Generated NS3 protein structure using comparative modeling in Modeller.  
   - Validated the model using DOPE profile and RMSD report.

2. **Programming-based Binding Affinity Calculation**  
   - Used Python scripts to compute binding affinity for two ligands.  
   - **Results:**  
     - Ligand 1 (Asunaprevir):  -7.291  kcal/mol  
     - Ligand 2 (Simeprevir): -10.803  kcal/mol  
   - These values provided initial insight but were **approximate estimates**.

3. **Molecular Docking Using AutoDock Vina**  
   - Prepared protein and ligands for docking.  
   - Set docking grids.  
   - Docking results showed **improved binding affinities**:  
     - Ligand 1: -11.65 kcal/mol  
     - Ligand 2: -11.46 kcal/mol  

4. **Visualization in Discovery Studio**  
   - Best docking poses were visualized to examine ligand-protein interactions.  
   - Generated interaction diagrams for reporting.

---

## Results

| Ligand           | Binding Affinity (Programming) | Binding Affinity (Docking) | Visualization |
|-----------------|-------------------------------|----------------------------|---------------|
| Asunaprevir      | -7.291 kcal/mol                | -11.65 kcal/mol           | ![Ligand1](Docking_ligand1/run2_interaction.png) |
| Simeprevir       | -10.803 kcal/mol               | -11.46 kcal/mol           | ![Ligand2](Docking_ligand2/run4_interaction.png) |

**Note:** Binding affinities from docking are generally more accurate than initial programming estimates, which explains the variation in values.

**Modelling Figures:**  
- NS3 protein model: ![NS3_model](Modelling/NS3_model.png)
- Superimposed NS3 model: ![NS3_superimposed](Modelling/NS3_superimposed.png)  
- DOPE profile: ![DOPE_profile](Modelling/DOPE_profile.png)  
- RMSD validation report included in `Modelling/RMSD_report.txt`.
---

## Folder Structure
Dengue_NS3_Docking_Project/
│
├── Data/                  # Original raw files
│   ├── Asunaprevir.sdf
│   ├── Simeprevir.sdf
│   ├── NS3_model.pdb
│   └── NS3_sequence.txt
│
├── Docking_ligand1/       # Docking results for ligand 1
│   ├── ligand1.pdbqt
│   ├── run2.png
│   └── run2_interaction.png
│
├── Docking_ligand2/       # Docking results for ligand 2
│   ├── ligand2.pdbqt
│   ├── run4.png
│   └── run4_interaction.png
│
├── Modelling/             # Homology modeling results
│   ├── NS3_model.pdb
│   ├── NS3_model.png
│   ├── NS3_superimposed.pdb
│   ├── NS3_superimposed.png
│   ├── DOPE_profile.png
│   └── RMSD_report.txt
│
├── Progdock/              # Programming-based docking & analysis
│   ├── Docking_Binding_Affinity.ipynb
│   ├── docking_binding_affinity.py
│   ├── NS3_model.pdbqt
│   ├── docked_ligand_1.pdbqt
│   └── docked_ligand_2.pdbqt
│
└── README.md              # Project overview


