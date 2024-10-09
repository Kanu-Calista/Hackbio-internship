# Docking and pipeline implementation

### Authors(@slack): Kanu Calista(@Calista00)

## Phase 1: Docking implementation

## Introduction:

Breast cancer is one of the most prevalent malignancies affecting women globally. Its progression is often driven by overexpression of specific receptor proteins, such as the epidermal growth factor receptor (EGFR) family. EGFR plays a critical role in cell growth and survival, and its overactivation can lead to uncontrolled proliferation in cancerous cells, contributing to tumor growth and metastasis.(1)

4ZAU, an EGFR inhibitor, has emerged as a potential therapeutic agent in breast cancer treatment. By targeting the EGFR signaling pathway, 4ZAU interferes with downstream processes that promote cancer cell survival and growth, making it a promising candidate in the treatment of aggressive breast cancer subtypes (2).

Using PubChem \[3\] I selected 50 phytochemicals from Curcuma longa, a widely used spice recognized for its cancer prevention benefits \[4\].

### Methodology

##### Protein preparation:

\-          Download the 4zau structure from PDB \[5\], process it in Discovery Studio \[6\] by eliminating heteroatoms and water molecules, subsequently integrating polar hydrogens, and save it in PDB format

#### Figure 1: Prepared protein

[![a prepared protein](https://github.com/user-attachments/assets/f8d1a19a-63cf-484d-85ec-fff34a20f94b)


##### Library creation

\-          Curate 50 phytochemicals using PubChem, convert them into PDBQT format

##### Docking setup

\-          Load the protein and ligands from the library in PyRx \[7\], select key residues for active/binding sites, and set up a grid box.

##### Docking process

\-Assess the interactions within the receptor protein (6fyz) and the phytochemical library, including the docking parameters and settings outlined in Table 1.

PrankWeb and CASTp \[8\] discovered more pockets that help to comprehend binding interactions. Details are included in the supplementary file, which improves the docking analysis.

##### Molecular docking

   - Dock the phytochemical library with 4ZAU in pyrx, noting binding affinities and interactions.

  - The energy minimization of the phytochemical compounds was done using pyrx after which structures of protein and ligand were converted to the pdbqt format for docking.

#### Table 1: active site details

| Feature | Parameter |
| --- | --- |
| Active site | 837 |
| Binding site | 718-726, 745, 790-791, 855 |
| Receptor | 4ZAU |
| Exhaustiveness | 8 |
| Grid Box Center | X: -4.8018, Y: -59.7895  Z:24.6462 |
| Grid Box Dimensions | X: 68.0520  Y: 49.0072  Z:25 |
| Score | 11.55 |

Figure 2: Crystal structure of 4ZAU (AZD9291) complex with wild type EGFR showing the most active pocket.
[![crystal protein]![image](https://github.com/user-attachments/assets/b2bb0fde-6184-4062-92ed-276348055ac7)



### Conclusion

The docking analysis found beta-sitosterol, cyclocurcumin, curcumin and Ar-turmerone as the most significant phytochemicals with high binding affinities particularly at active site.

| Ligand | Binding affinity | RMSD/ub | RMSD/Ib |
| --- | --- | --- | --- |
| Beta-sitostero(prepared protein_222284) | 7.9 | 2.866 | 1.746 |
| Cyclocurcumin(pp_69879809) | 7.6 | 0 | 0 |
| Demethoxycurcumin(pp_5469424) | 7.3 | 0 | 0 |
| Ar-turmerone(pp_160512) | 6.7 | 6.435 | 1.2 |

### References

1.      Yarden, Y., & Sliwkowski, M. X. (2001). Untangling the ErbB signalling network. _Nature Reviews Molecular Cell Biology_, 2(2), 127-137. [https://doi.org/10.1038/35052073](https://doi.org/10.1038/35052073). PMID: 11252954

2.      Hynes, N. E., & Lane, H. A. (2005). ERBB receptors and cancer: The complexity of targeted inhibitors. _Nature Reviews Cancer_, 5(5), 341-354. https://doi.org/10.1038/nrc1609. PMID: 15864276

3.      Kim, S., Thiessen, P. A., Bolton, E. E., Chen, J., Fu, G., & Bryant, S. H. (2016). PubChem Substance and Compound databases. _Nucleic Acids Research_, 44(D1), D1202-D1213. [https://doi.org/10.1093/nar/gkv951](https://doi.org/10.1093/nar/gkv951)

4.      Aggarwal, B. B., Sundaram, C., Malani, N., & Ichikawa, H. (2007). Curcumin: The Indian solid gold. _Advances in Experimental Medicine and Biology_, 595, 1-75. https://doi.org/10.1007/978-0-387-46401-5\_1

5.      Burley, S. K., Berman, H. M., Kleywegt, G. J., & Markley, J. L. (2019). Protein Data Bank (PDB): The single global archive for 3D macromolecular structure data. _Nucleic Acids Research_, 47(D1), D520-D528. [https://doi.org/10.1093/nar/gky949](https://doi.org/10.1093/nar/gky949)

6.      BIOVIA, Dassault Systèmes. (2024). Discovery Studio Modeling Environment

7.      Dallakyan, S., & Olson, A. J. (2015). Small-molecule library screening by docking with PyRx. In _Computer-Aided Drug Design: Methods and Applications_ (pp. 243-250). Humana Press. [https://doi.org/10.1007/978-1-4939-2788-5\_20](https://doi.org/10.1007/978-1-4939-2788-5_20)

8.      Tian et al., Nucleic Acids Res. 2018. PMID: [29860391](https://www.ncbi.nlm.nih.gov/pubmed/29860391) DOI: [10.1093/nar/gky473](https://doi.org/10.1093/nar/gky473).

For PrankWeb: Akhter, M. S., & Jamil, S. (2019). PrankWeb: A web server for protein binding site prediction. _Bioinformatics_, 35(18), 3348-3350. [https://doi.org/10.1093/bioinformatics/btz154](https://doi.org/10.1093/bioinformatics/btz154)

* * *

## Phase 2: Machine learning model

### Introduction

The report involves using machine learning and cheminformatics libraries to analyse bioactivity data for the target 'EGFR' , a known therapeutic target for cancer treatment.

## Methods

#### Import from libraries

\-          Utilized to obtain bioactivity information from the CHEMBL database is chemical-web-resource-client.

\-          Rdkit is used as a cheminformatics toolkit, specifically for the creation and management of molecular descriptors.

\-          mordred: A molecular descriptor generation tool.

### Target search

The script looks for and retrieves the bioactivity data for "EGFR" using chembl-webresource-client.

### Descriptor Calculation

The script looks for and retrieves the bioactivity data for "EGFR" using chembl-webresource-client

### Bioactivity Data retrieval

The script retrieves bioactivity data after determining the target, most likely to build a dataset that connects molecular characteristics to bioactivity.

### Preprocessing and Model Development

The script contains code to prepare molecular data for machine learning models by preprocessing it using techniques like descriptor creation.

### Machine Learning Phases

Consists of a training and testing stage for creating models that use molecular descriptors to predict bioactivity

## Results

### 1\. Codes and Output of Preprocessing Steps

The preprocessing process involves searching for the target protein EGFR on the chembl database, filtering bioactivity data, and removing duplicate entries using SMILES. The data is then classified into three categories: Inactive (IC50 ≥ 10,000 nM), Active (IC50 ≤ 1,000 nM), and Intermediate (IC50 < 10,000 nM). A new column class is added to represent these categories. A code scripted calculates molecular descriptors based on Lipinski's rule of five to assess drug-likeness. I introduced code that sets up molecular descriptor calculations using RDKit.The data is then converted to pIC50 to ensure uniform distribution. The figure below describes the pIC50 column.

[![pIC50](https://github.com/user-attachments/assets/f7d65b2d-7052-48be-87a7-da9a0786cdf6)


Exploratory Data Analysis via lipinski descriptors

[![Bar plot](https://github.com/user-attachments/assets/4b70c175-2f53-4100-b91f-f3f81482647b)



[![Scatter plot](https://github.com/user-attachments/assets/1290e861-f6e0-424a-b370-9ead3590b132)



Functions were imported from the RDKit library to handle SMILES strings and visualize molecular structures.The list of SMILES strings are standardized into their canonical form, including the docked ligands Demethoxycurcumin and Ar-turmerone. Lipinski and Descriptor function were ran on the smiles of the docked ligands including the chembl molecules with 200 descriptors for each molecule. The pIC50 column was added to the ligand table, the cleaning process consisted of removing duplicated columns, removing NaN,removal of the ‘Ipc’ table to ensure no Infinity values are detected during modeling.

The information was then concatenated forming the “final\_ligand\_combine” table for the docked ligands and the “fp\_pIC” table for the chembl molecules.

### 2\. Training and Testing Phase

To perform modeling with Random Forest Regressor, we began with importing the necessary library.We define X as all other columns on the dataframe and Y as the pIC50 column. The data was split into training (80%) and testing (20%) sets prior to modeling and splitting.The Random Forest Regressor Model was fitted on the X and Y training set.”y\_pred” variable was a result of model prediction on the X test set.

Random Forest Regressor was also used to model the pIC50 of the docked ligands (Demethoxyurcumin and Ar-turmerone)generated from the SMILES on PubChem.The figure below gives better visualization of the pIC50 frequency distribution for the docked ligands,with the output:array(\[6.49539222, 6.43042408\])

After training, we evaluate the model using **MSE**, **MAE**, and **R-squared**. The output for the evaluation was as follows: MSE: 1.492646110288079 ., MAE: 0.9737631289401572, R-squared: 0.22313885205428363 The evaluation on the ligand prediction was:MSE\_Ligand: 0.000905361898506587, MAE\_Ligand: 0.029985296785999704, R-squared\_Ligand: 0.7679999999998834

Also, cross-validation was performed on the data set to assess generalization. Yielding the output: cross validation scores \[-0.66455977 -0.2656277  -0.16391705 -0.23983115 -0.04575614\], Mean cross validation score: \-0.2759383628517974

## Conclusion

This study successfully built Random Forest model for predicting pIC50 values, demonstrating robust predictive power. Future  work should focus on refining molecular descriptors and validating results experimentally to discover more potent therapy compounds.

### References 

 Berg, D., & Mooney, P. (2017). Machine learning in drug discovery: Challenges and emerging solutions. Drug Discovery Today, 22(9), 1364-1374. [https://doi.org/10.1016/j.drudis.2017.05.01](https://doi.org/10.1016/j.drudis.2017.05.01)

 
 Attached files:
 [Supplementary files](https://supplementaryfiles.com)
