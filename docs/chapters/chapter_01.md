Welcome to this VIB training. The authors of this course designed a full teaching day that combines theory with hands-on activities, allowing participants to apply the concepts in practice.

!!! question "Chapter questions"

    1. How can protein biophysical properties help us understand function beyond what is visible from a static structure?
    2. Which regions of a signaling protein, such as a receptor tyrosine kinase, are most likely to be functionally regulated by dynamics or disorder?
    3. How can sequence conservation and divergence across species inform us about essential versus adaptable protein regions?
    4. Why might post-translational modifications preferentially occur in specific biophysical or structural contexts?
    5. How can mutations alter protein behaviour without strongly affecting the overall folded structure?
    6. What are the limitations of studying proteins using a single reference sequence or a single predicted structure?


## 1.1 Introducing the training methodology

The protein of interest for this training is the human **proto-oncogene tyrosine-protein kinase receptor RET**, encoded by the **RET** gene. 

!!! info "Protein sequence"

    Although the UniProt entry describes two isoforms, produced by alternative splicing, this couse is based on the canonical sequence in FASTA format: **P07949-1** ([P07949 · RET_HUMAN](https://www.uniprot.org/uniprotkb/P07949/)).

    ```
    >sp|P07949|RET_HUMAN Proto-oncogene tyrosine-protein kinase receptor Ret OS=Homo sapiens OX=9606 GN=RET PE=1 SV=3
    MAKATSGAAGLRLLLLLLLPLLGKVALGLYFSRDAYWEKLYVDQAAGTPLLYVHALRDAP
    EEVPSFRLGQHLYGTYRTRLHENNWICIQEDTGLLYLNRSLDHSSWEKLSVRNRGFPLLT
    VYLKVFLSPTSLREGECQWPGCARVYFSFFNTSFPACSSLKPRELCFPETRPSFRIRENR
    PPGTFHQFRLLPVQFLCPNISVAYRLLEGEGLPFRCAPDSLEVSTRWALDREQREKYELV
    AVCTVHAGAREEVVMVPFPVTVYDEDDSAPTFPAGVDTASAVVEFKRKEDTVVATLRVFD
    ADVVPASGELVRRYTSTLLPGDTWAQQTFRVEHWPNETSVQANGSFVRATVHDYRLVLNR
    NLSISENRTMQLAVLVNDSDFQGPGAGVLLLHFNVSVLPVSLHLPSTYSLSVSRRARRFA
    QIGKVCVENCQAFSGINVQYKLHSSGANCSTLGVVTSAEDTSGILFVNDTKALRRPKCAE
    LHYMVVATDQQTSRQAQAQLLVTVEGSYVAEEAGCPLSCAVSKRRLECEECGGLGSPTGR
    CEWRQGDGKGITRNFSTCSPSTKTCPDGHCDVVETQDINICPQDCLRGSIVGGHEPGEPR
    GIKAGYGTCNCFPEEEKCFCEPEDIQDPLCDELCRTVIAAAVLFSFIVSVLLSAFCIHCY
    HKFAHKPPISSAEMTFRRPAQAFPVSYSSSGARRPSLDSMENQVSVDAFKILEDPKWEFP
    RKNLVLGKTLGEGEFGKVVKATAFHLKGRAGYTTVAVKMLKENASPSELRDLLSEFNVLK
    QVNHPHVIKLYGACSQDGPLLLIVEYAKYGSLRGFLRESRKVGPGYLGSGGSRNSSSLDH
    PDERALTMGDLISFAWQISQGMQYLAEMKLVHRDLAARNILVAEGRKMKISDFGLSRDVY
    EEDSYVKRSQGRIPVKWMAIESLFDHIYTTQSDVWSFGVLLWEIVTLGGNPYPGIPPERL
    FNLLKTGHRMERPDNCSEEMYRLMLQCWKQEPDKRPVFADISKDLEKMMVKRRDYLDLAA
    STPSDSLIYDDGLSEEETPLVDCNNAPLPRALPSTWIENKLYGMSDPNWPGESPVPLTRA
    DGTNTGFPRYPNDSVYANWMLSPSAAKLMDTFDS
    ```

We will predict biophysical features for this protein using the Bio2Byte online platform, specifically the **B2BTools** suite. To enable a deeper analysis of these biophysical properties, we will generate a multiple sequence alignment (MSA) of sequences sharing at least 90% identity. This alignment will be used to identify conserved and variable patterns across homologous sequences.

The MSA will be created using **Clustal Omega**, and the aligned kinase domain will be extracted using a **Google Colab** notebook.

Post-translational modifications (PTMs) for the protein of interest will be explored using the **Scop3P** online platform, which is directly linked from the B2BTools prediction results. After analyzing the available information on modifications, structures, and experimental evidence, we will follow a more detailed protocol to link biophysical patterns with PTMs.

Finally, the course will address the impact of mutations. We will show how to modify the wild-type sequence and assess the effect of single amino acid substitutions on biophysical profiles and predicted protein structures using **AlphaFold v3**.

## 1.2 Rethinking the protein structure and function 
TBC

### 1.2.1 Proteins are dynamic systems, not static objects
TBC

### 1.2.2 Limitations of deep learning–based structure prediction
TBC

### 1.2.3 Memorization and dominant conformations
TBC

## 1.3 ELIXIR Belgium node services used in this training

Belgium is part of the ELIXIR Europe network as a National Node. The Belgian node, [ELIXIR Belgium](https://www.elixir-belgium.org/), provides both federal-level services and local initiatives, including research infrastructure, domain-specific services, training activities, and workshops.

This course focuses on two bioinformatics tools and resources: **B2BTools**, used to predict and analyse protein biophysical features, and **Scop3P**, used to explore post-translational modifications (PTMs).

### 1.3.1 Introduction to Bio2Byte Tools

**DynaMine** is a predictor specifically designed to estimate protein backbone dynamics. Backbone dynamics are related to, but not the same as, protein disorder. DynaMine was trained using values derived from NMR chemical shift data and therefore captures protein movements in solution. Its training set includes both fully folded proteins and intrinsically disordered proteins.

The **B2BTools** tool suite extends the original DynaMine predictor by including several predictors developed by the Bio2Byte lab.

In addition to backbone dynamics, it provides predictions for side-chain dynamics and conformational preferences (alpha helix, beta sheet, and coil), all derived from NMR data and trained using the same methodology. The platform also includes predictors for early folding regions (**EFoldMine**), beta-sheet aggregation (**AgMata**), and protein disorder (**DisoMine**).

### 1.3.2 Introduction to Scop3P (and Scop3PTM)

Scop3P, developed at Ghent University and available online since June 2019, is a dedicated resource to explore and interpret the impact of phosphorylation sites on human protein structure and function. It supports researchers in analysing individual phosphosites or phosphoproteins within a structural, biophysical, and biological context.

The resource integrates public data from several major international databases, including UniProtKB and the Protein Data Bank (PDB). In addition, it incorporates reprocessed mass spectrometry-based phosphoproteomics data from PRIDE/ProteomeXchange. These datasets are collected worldwide, making Scop3P a strongly international and community-driven resource.

!!! success "About Scop3PTM"
    TBC

## 1.4 The target protein family

This protein has a sequence length of 1114 amino acids. It can be found in UniProtKB under the accession **P07949** or the entry name **RET_HUMAN**.

According to the functional annotation provided by UniProt, this protein plays a central role in several cellular processes:

> This protein is a receptor tyrosine-protein kinase involved in numerous cellular mechanisms including cell proliferation, neuronal navigation, cell migration, and cell differentiation in response to glia cell line-derived growth family factors (GDNF, NRTN, ARTN, PSPN and GDF15). In contrast to most receptor tyrosine kinases, RET requires not only its cognate ligands but also coreceptors, for activation. 

> It acts as a dependence receptor via the GDNF-GFRA1 signaling: in the presence of the ligand GDNF in somatotrophs within pituitary, promotes survival and down regulates growth hormone (GH) production, but triggers apoptosis in absence of GDNF.

> It is required for the molecular mechanisms orchestration during intestine organogenesis via the ARTN-GFRA3 signaling: involved in the development of enteric nervous system and renal organogenesis during embryonic life, and promotes the formation of Peyer's patch-like structures, a major component of the gut-associated lymphoid tissue (By similarity).

> It mediates, through interaction with GDF15-receptor GFRAL, GDF15-induced cell-signaling in the brainstem which triggers an aversive response, characterized by nausea, vomiting, and/or loss of appetite in response to various stresses.

> It modulates cell adhesion via its cleavage by caspase in sympathetic neurons and mediates cell migration in an integrin (e.g. ITGB1 and ITGB3)-dependent manner.

> Also, it is active in the absence of ligand, triggering apoptosis through a mechanism that requires receptor intracellular caspase cleavage.

> It triggers the differentiation of rapidly adapting (RA) mechanoreceptors.

> **It phosphorylates PTK2/FAK1.**

In this training, we will focus on a specific protein domain: the kinase domain, located approximately between positions 724 and 1016 of the protein sequence.

!!! info "Protein Kinase domain sequence"

    Here you can find the domain sequence in FASTA format ([PROSITE-ProRule: PRU00159](https://prosite.expasy.org/rule/PRU00159)).

    ```
    LVLGKTLGEGEFGKVVKATAFHLKGRAGYTTVAVKMLKENASPSELRDLLSEFNVLKQV
    NHPHVIKLYGACSQDGPLLLIVEYAKYGSLRGFLRESRKVGPGYLGSGGSRNSSSLDHP
    DERALTMGDLISFAWQISQGMQYLAEMKLVHRDLAARNILVAEGRKMKISDFGLSRDVY
    EEDSYVKRSQGRIPVKWMAIESLFDHIYTTQSDVWSFGVLLWEIVTLGGNPYPGIPPER
    LFNLLKTGHRMERPDNCSEEMYRLMLQCWKQEPDKRPVFADISKDLEKMMVKRRDYL
    ```

!!! note "Let's get started"
    [Next chapter](/../../chapters/chapter_02) explains how to use this resource.
