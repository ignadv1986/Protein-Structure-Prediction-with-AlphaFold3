# Alphafold
Using Alphafold3 to determine the structure of the CRAMP1 protein.

**Note:** This project is not intended to present novel findings. All biological insights described here are based on our previously [published study](https://pmc.ncbi.nlm.nih.gov/articles/PMC12240685/#app2).
The purpose of this repository is to demonstrate practical skills in protein structure prediction using AlphaFold3, structural domain interpretation, and bioinformatics analysis workflows. This includes sequence retrieval, structure visualization, confidence assessment, and domain annotation using established tools.
## Background
Through CRISPR/Cas9-based screening, we identified the previously uncharacterized protein CRAMP1 as a major factor involved in controlling the sensitivity to two functionally different Topoisomerase II inhibitors (TOP2i), ICRF-193 and etoposide, in human cells. Further exploration revealed that CRAMP1 exerts its protection against these compunds by controlling linker histone H1 expression, thereby preventing excessive chromatin decompaction and subsequent TOP2 binding and trapping. Details on this project can be found in [this publication](https://pmc.ncbi.nlm.nih.gov/articles/PMC12240685/#app2).
## Aim of the project
Alphafold3 was used to determine CRAMP1 structure and identify domains that could be involved in its role controlling H1 expresison and/or TOP2i sensitivity.
## Tools
- **Alphafold3:** Protein strucuture was predicted by submitting the CRAMP1 sequence to the [Alphafold server](https://alphafoldserver.com).
- **Uniprot:** Retrieving CRAMP1 aminoacid sequence.
- **[Alphafold-analyser](https://github.com/Orpowell/alphafold-analyser):** Used to visualize the predicted structure and the PAE/pLDDT scores.
- **Python 3:** Required to run Alphafold-analyser scripts.
- **[InterPro](https://www.ebi.ac.uk/interpro/):** For domain annotation based on sequence similarity. 
- **Adobe Illustrator:** Figure processing.
## Workflow
1) The aminoacid sequence of human CRAMP1 was retrieved from Uniprot entry [Q96RY5](https://www.uniprot.org/uniprotkb/Q96RY5/entry) and modelled using Alphafold3 in the Alphafold server.
2) PAE and pLDDT scores were visualized by running the generated .json files though the Alphafold-analyser script mentioned in the tools section.
3) The same script was used to visualize the predicted CRAMP1 structure from the .pdb file.
4) For a clearer visualization, the .png files generated before were processed in Adobe Illustrator.
5) Aminoacid sequence of the predicted domains were inserted in the InterPro website to assess potential sequence similarity to known domains.
## Results
- Alphafold modelling predicted three structured regions within CRAMP1:
  - An N-terminal domain (residues 161-225)
  - A domain composed of a bipartite fold separated by an extended linker:
     - D1: residues 315-427
     - D2: residues 657–740
- Both PAE and pLDDT showed high confidence in these regions, with PAE score below 5 Å and pLDDT above 90.
- A subsequent InterPro identified our predicted N-terminal domain as a SANT domain, which in other proteins allows for DNA and transcription facotr binding.
- No analog domains where detected for CRAMP1 D1 and D2, suggesting that they represent novel or lineage-specific folds.

