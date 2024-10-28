**Contributors:** Babatunde OWOLOYE, Kanu Calista, Emmanuel Owoeye

EGFR Visualization in Computational Biology: Harnessing Homology Modeling and AlphaFold for Protein Modeling in Cancer Research

**Introduction**

The Epidermal Growth Factor Receptor (EGFR) plays a critical role in regulating cell growth, survival, and differentiation, making it a key focus in cancer research. Mutations and overexpression of EGFR are linked to various cancers, including lung, breast, and colorectal cancer. Visualizing the structure and dynamics of EGFR is crucial for understanding its biological functions and designing targeted therapies.

**Report**

We chose EGFR as our protein (Protein ID: 3poz) and ensured it is a protein present in the protein data bank. The 3D crystal protein structure was dowloaded from RCSB  (<https://www.rcsb.org/>) in pdb and fasta formats (for further modeling)

**Perform Homology Modeling**

We perform homology modeling using SWISS MODEL, with the fasta format of protein gotten from RCSB PDB.  Base on the EGFR template, and dowloaded the result in pdb format.

Again we run AlphaFold modeling on AlphaFold server with the EGFR fasta file gotten from the RCSB, saved result in pdb format

**Visualize the protein**

With the help of pymol, the protein were visualized successsfully.

**Analyze the protein structure**

**\*EGFR Binding and Active Sites\***

In the Epidermal Growth Factor Receptor (EGFR), with UniProt ID P00533, several critical sites are involved in its functionality:

**Binding Sites for ATP:**

- 718-726: This region is involved in binding ATP, which is essential for the receptor's kinase activity.

- 745: Another ATP binding site crucial for the enzymatic function of EGFR.

- 790-791: These residues also participate in ATP binding, facilitating the transfer of phosphate groups.

- 855: This site contributes to ATP binding, supporting the phosphorylation activity of the kinase domain.

  **Active Sites:**

- 837: This residue acts as a proton acceptor, playing a key role in the enzymatic mechanism of the kinase domain.

**Domains:**

The main domain of the Epidermal Growth Factor Receptor (EGFR) is the \*tyrosine kinase domain\*. EGFR is a receptor tyrosine kinase, and its primary function involves the activation of tyrosine kinase activity, which plays a crucial role in signaling pathways that regulate cell growth, differentiation, and survival. The main domain of the Epidermal Growth Factor Receptor (EGFR) is the \*tyrosine kinase domain\*. EGFR is a receptor tyrosine kinase, and its primary function involves the activation of tyrosine kinase activity, which plays a crucial role in signaling pathways that regulate cell growth, differentiation, and survival.
**




**Other cancer-related mutations.**

**Lung cancer (LNCR)**

The gene represented in this entry is involved in disease pathogenesis

**Description**

A common malignancy affecting tissues of the lung. The most common form of lung cancer is non-small cell lung cancer (NSCLC) that can be divided into 3 major histologic subtypes: squamous cell carcinoma, adenocarcinoma, and large cell lung cancer. NSCLC is often diagnosed at an advanced stage and has a poor prognosis.

MIM:[**211980**](https://www.omim.org/entry/211980) 


**Inflamatory skin and bowel disease, neinatal, 2 (NISBD2)**

The disease is caused by variants affecting the gene represented in this entry

**Description**

A disorder characterized by inflammatory features with neonatal onset, involving the skin, hair, and gut. The skin lesions involve perioral and perianal erythema, psoriasiform erythroderma, with flares of erythema, scaling, and widespread pustules. Gastrointestinal symptoms include malabsorptive diarrhea that is exacerbated by intercurrent gastrointestinal infections. The hair is short or broken, and the eyelashes and eyebrows are wiry and disorganized.

MIM:[**616069**](https://www.omim.org/entry/616069)


**Compare the structures obtained from homology modeling and AlphaFold, noting any significant differences or similarities**

Homology modeling and AlphaFold are both methods used to predict the 3D structure of a protein.

**Similarities**

- Both methods predit a similar overall fold for EGFR
- Both methods agree on the secondary structure elements (alpha helices and beta sheets)
- Both methods predict a similar organization of the domains

**Significant differences**

\-  Active site conformation: AlphaFold may predict a more open or closed conformation of the active site, depending on the ligand or context.

\-  Extracellular domain structure: AlphaFold can predict a more detailed structure for the extracellular domain, including disulfide bonds and glycosylation sites.

**Evaluate the Protein Modelling Techniques**

EGFR (Epidermal Growth Factor Receptor). It is a protein that plays an important role in cell growth, division and survival. It is a member of the ErbB family of receptor tyrosine kinases, which also includes ErbB2 (HER2), ErbB3 (HER3), and ErbB4 (HER4). Uniprot ID (P00533)

**Functions**

EGFR binds to epidermal growth factor (EGF) and other ligands, triggering a signaling cascade that regulates cell prolieration, differentiation and survival.

1\. Cell proliferation and growth: EGFR activation stimulates cell division and growth.

2\. Cell differentiation: EGFR regulates cell fate decisions and differentiation.

3\. Cell survival and apoptosis: EGFR promotes cell survival and inhibits apoptosis (programmed cell death).

4\. Cell migration and adhesion: EGFR regulates cell movement and adhesion to the extracellular matrix.

Receptor tyrosine kinase binding ligands of the EGF family and activating several signaling cascades to convert extracellular cues into appropriate cellular responses (PubMed:[**10805725**](https://www.uniprot.org/citations/10805725), PubMed:[**27153536**](https://www.uniprot.org/citations/27153536), PubMed:[**2790960**](https://www.uniprot.org/citations/2790960), PubMed:[**35538033**](https://www.uniprot.org/citations/35538033)).

Ligand binding triggers receptor homo- and/or heterodimerization and autophosphorylation on key cytoplasmic residues.

Isoform [**2**](https://www.uniprot.org/#Isoform_2) may act as an antagonist of EGFR action.


**Role in cancer**

` `EGFR is often overexpressed or mutated in certain types of cancer (NSCLC), breast cancer and glioblastoma. Which can lead uncontrolled  cell growth and tumor formation.

**Evaluate the two modeling techniques (homology modeling vs. AlphaFold)**

**Homology SWISS modeling**

Template:  **[3poz.1.A](https://swissmodel.expasy.org/templates/3poz.1)** Epidermal growth factor receptor
*EGFR Kinase domain complexed with tak-285*

Identity: 100.00

Similaty: 0.62

Ligards : 1 x 03P	

Method : X-ray 1.50A

Oligo state : monomer

![Aspose Words 1438e956-551e-427f-b498-3b431062a568 001](https://github.com/user-attachments/assets/68d0426f-7d2f-4219-baf9-d15537cb1f01)




**AlphaFold Modeling**

- Blue: Very high (plDDT > 90)
- Sky blue: Confident (90 > plDDT > 70)
- Yellow: Low (70 > plDDT > 50)
- Orange: Very low (plDDT < 50)

  ipTM = -pTM = 0.88 

  ![Aspose Words 1438e956-551e-427f-b498-3b431062a568 002](https://github.com/user-attachments/assets/3bea49d8-f8cf-4c2b-8e93-5ab9aad12f28)

![Aspose Words 1438e956-551e-427f-b498-3b431062a568 003](https://github.com/user-attachments/assets/06a59f14-f8c3-4338-851e-e7a56e068135)


  **Compared to the crystal structures on the PDB**

  (using align and RMSD measurements on pymol)

  We calculated the RMSD value on pymol with the help of this commands : 

  *align molecule1, molecule2, cycles=0, transform=0*

  where;

  ` `RMSD value of AlphaFold align with PDB (Apo)

  = 3.194 Å

  RMSD value of AlphaFold align with Homology SWISS modeling 

  = 3.795 Å

  ` `RMSD value of Homology SWISS modeling align with PDB (Apo)

  = 0.372  Å

  **Techniques that is more durable**

  The more accurate techniques for our protein is “Homology SWISS modeling”.

  Aligning and calclulating RMSD value of Homology SWISS model and RCSB gives  of “0.372  Å” which is “<2” shows a great similarities of the alignmemts.

  While the one of AlphaFold and RCSB or  AlphaFold and SWISS gives a result that is “>2” shows  dissimilarities in the alignments

  **Reference**

  1\. \*Kobayashi, S., & Mitsudomi, T. (2016). "EGFR Mutations and Erlotinib Resistance in Non-Small Cell Lung Cancer." \*Nature Reviews Clinical Oncology, 13(6), 297-307.\*\*

  `   `- This review provides insights into the role of EGFR mutations in cancer and the challenges of resistance to targeted therapies.

  2\. \*Jumper, J., Evans, R., Pritzel, A., et al. (2021). "Highly Accurate Protein Structure Prediction with AlphaFold." \*Nature, 596(7873), 583-589.\*\*

  `   `- This paper introduces AlphaFold and demonstrates its effectiveness in predicting protein structures with high accuracy.

  3\. \*Miller, B. L., & Ghosh, A. K. (2019). "Homology Modeling of Protein Structures: An Overview." \*Methods in Molecular Biology, 2025, 1-20.\*\*

  `   `- A comprehensive overview of homology modeling techniques and their applications in protein structure prediction.

  4\. \*Liu, H., & Scheraga, H. A. (2020). "The Role of Computational Methods in Protein Structure Prediction and Drug Discovery." \*International Journal of Molecular Sciences, 21(11), 3944.\*\*

  `   `- This article discusses the role of computational methods in understanding protein structures and their implications for drug discovery.

  5\. \*Yang, H., & Xu, X. (2017). "Structural Insights into EGFR Inhibitor Binding: A Homology Modeling Approach." \*Journal of Structural Biology, 197(1), 1-10.\*\*

  `   `- This paper explores EGFR structure and inhibitor interactions using homology modeling.

  6\. \*Tsuchiya, Y., & Nakamura, H. (2022). "Advances in Cancer Research: EGFR Targeted Therapies and Computational Approaches." \*Frontiers in Oncology, 12, 839745.\*\*
