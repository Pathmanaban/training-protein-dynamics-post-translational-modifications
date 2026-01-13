In this final chapter, we summarize the main steps and concepts covered throughout the training. The course combined biophysical predictions, sequence analysis, structural context, and post-translational modification data to explore a biologically relevant protein in a reproducible and practical way.

The workflow presented in this training is intended as a template that can be adapted to other proteins and research questions. Participants are encouraged to reuse and extend the presented approaches in their own projects.

---

## 6.1 Lessons learnt

Throughout this training, we highlighted several practical and conceptual lessons, including:

- How biophysical predictions complement both sequence and structural based analyses  
- The value of multiple sequence alignments for identifying conserved and variable regions  
- The importance of structural and biophysical context when interpreting PTMs  
- The benefits and limitations of prediction-based approaches  

These lessons aim to support more informed and critical use of computational tools in biological research.

## 6.2 Take-home messages

The key messages of this training can be summarized as follows:

- Biophysical profiles provide insight beyond primary sequence information  
- Integrating multiple data sources leads to more robust biological interpretation  
- Prediction tools are powerful but must be used with awareness of their assumptions  
- Reproducible workflows enable reuse and extension of analyses  

These points are intended to guide future analyses and encourage thoughtful tool usage.

## 6.3 Discussion and open questions

This section is intended as a space for reflection, discussion, and feedback.

!!! question "Questions for you"

    1. What parts of the course content were most useful or most challenging?
    2. Which steps or concepts would benefit from additional explanation or examples?
    3. How could this training be improved to better support your research needs?
    4. Do you have feedback on the usability, clarity, or limitations of the tools presented in this course?

## 6.4 Files structure

During this training the following files have been created and used:

```shell
./training-data-directory
│─── P07949.fasta # Canonical protein sequence of P07949
│─── P07949.90-similar.fasta # 90%-similarity sequences of P07949
│─── P07949.90-similar.msa.fasta # Clustal-Omega MSA of 90%-similarity sequences
│─── P07949.90-similar.msa.kinase.fasta # Clustal-Omega MSA of Kinase domain
│─── P07949_s909p_y928p_y981p.fasta # Mutated canonical protein sequence with 3 mut.
│─── AF-P07949-F1-model_v6.cif # AlphaFold model for P07949 in mmCIF format (optional)
│─── AF-P07949-F1-model_v6.pdb # AlphaFold model for P07949 in PDB format
│─── 6nja.cif # Experimental structure for 6NJA in mmCIF format (optional)
│─── 6nja.pdb # Experimental structure for 6NJA in PDB format
│─── 2ivs.cif # Experimental structure for 2IVS in mmCIF format (optional)
│─── 2ivs.pdb # Experimental structure for 2IVS in PDB format
│─── fold_p07949_modifications_model_0.cif # AlphaFold server prediction for phospho
│─── fold_p07949_modifications_model_0.pdb # AlphaFold server prediction for phospho
│─── fold_p07949_s909p_y928p_y981p.cif # AlphaFold server prediction for mutations
└─── fold_p07949_s909p_y928p_y981p.pdb # AlphaFold server prediction for mutations
```

---

!!! note "To follow up: : Go to next page"
    [Follow up page](/../../follow_up_training) explains how to apply the same workflow to proteins of your own interest.
