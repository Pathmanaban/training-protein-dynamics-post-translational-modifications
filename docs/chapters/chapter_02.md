This chapter moves from theory to practice by predicting the “anatomy” of the protein at the level of its biophysical properties. Using the **B2BTools** suite, we will explore how different regions of the protein behave in terms of dynamics, structure, and flexibility.

!!! question "Chapter questions"

    1. How to use the B2BTools online platform to predict biophysical profiles for protein sequences ?
    2. How to find biophysical patterns using the platform ? 
    3. 

## 2.1 Biophysical profiles

As mentioned earlier, the **B2BTools** suite provides several predictors to analyse protein biophysical properties:

- Backbone and side-chain dynamics (via **DynaMine**)
- Intrinsically disordered residues (via **DisoMine**)
- Early folding regions (via **EFoldMine**)
- Beta-aggregation-prone regions (via **AgMata**)

## 2.1 Extracting the protein sequence

The first step is to download the protein sequence in FASTA format.

!!! example "Hands-on: P07949 sequence"

    Download the canonical protein sequence from UniProtKB. Visit the official UniProtKB website, locate the protein entry, and download the FASTA sequence.

    ??? success "Solution"

        The following FASTA sequence corresponds to the protein of interest and was retrieved from:
        https://rest.uniprot.org/uniprotkb/P07949.fasta

        ```
        >sp|P07949|RET_HUMAN Proto-oncogene tyrosine-protein kinase receptor Ret OS=Homo sapiens OX=9606 GN=RET PE=1 SV=3
        MAKATSGAAGLRLLLLLLLPLLGKVALGLYFSRDAYWEKLYVDQAAGTPLLYVHALRDAP
        EEVPSFRLGQHLYGTYRTRLHENNWICIQEDTGLLYLNRSLDHSSWEKLSVRNRGFPLLT
        ...
        DGTNTGFPRYPNDSVYANWMLSPSAAKLMDTFDS
        ```

        You should now have the file `P07949.fasta` available in your working environment.

## 2.2 Analysing single sequences (standalone)

The Bio2Byte lab provides an online platform to run the biophysical predictions described above for proteins of interest. The platform is available at:
https://bio2byte.be/online_predictors/ (this resource is still under active development, and user feedback is highly appreciated. A previous version of the platform is available at: https://bio2byte.be/b2btools).

!!! warning "Required token"
    First of all, write down in your notes a personal alphanumeric **TOKEN** to enable job submission and later retrieval of results.
    
!!! example "Hands-on: Predicting the biophysical features"

    Visit the online platform at [https://bio2byte.be/online_predictors](https://bio2byte.be/online_predictors).  
  
    Next, select the **Single Sequence** analysis type and upload your FASTA file.  

    Submitted jobs can be accessed from the **Token results** page:
    [https://bio2byte.be/online_predictors/past-results/](https://bio2byte.be/online_predictors/past-results/).

    Locate your job and open the corresponding results page.
    
    ??? success "Solution"
    
        You will be able to find the results inside the "Single Sequence Predictions" table. Your job will have an action button "View Results" that opens a link like `https://bio2byte.be/online_predictors/results/UUID/`.

### 2.2.1 Understanding the results as biological profiles

#### 2.2.1.1 Exploring intrinsic flexibility and folding propensity

#### 2.2.1.2 Visualization of biophysical profiles

## 2.3 Multiple sequence alignments (MSA)

To fully exploit the predictive power of biophysical tools, it is useful to study the target protein in the context of related proteins. Comparing similar sequences allows the identification of conserved biophysical profiles as well as positions that show divergence across homologs.

### 2.3.1 Working with the aligned kinase domain

UniProtKB provides access to similar proteins directly from the protein entry page, in the **Similar proteins** section.

!!! example "Hands-on: Getting the 90%-identity protein sequences"

    Open the protein entry in UniProtKB and locate the **Similar proteins** table at:
    [https://www.uniprot.org/uniprotkb/P07949/entry#similar_proteins](https://www.uniprot.org/uniprotkb/P07949/entry#similar_proteins).

    Select the entries with 90% sequence identity and choose to view all results in UniProtKB.

    Exclude other human proteins and short sequences to retain proteins with lengths between 1000 and 1120 amino acids.  
    Once the entries are selected, download the canonical sequences using the **Download** option in FASTA format, without compression.

    Before proceeding with the alignment, add the `P07949` sequence at the top of the downloaded FASTA file.

    ??? success "Solution"

        The canonical sequences can be retrieved from the following UniProtKB REST endpoint:
        https://rest.uniprot.org/uniprotkb/stream?download=true&format=fasta&query=accession%3AA0A0D9REZ9+OR+accession%3AA0A2I2ZX13+OR+accession%3AA0A2I3H8C4+OR+accession%3AA0A2I3LXM4+OR+accession%3AA0A2I3TR47+OR+accession%3AA0A2J8IX92+OR+accession%3AA0A2J8IX93+OR+accession%3AA0A2J8XTA5+OR+accession%3AA0A2K5HW95+OR+accession%3AA0A2K5MKU6+OR+accession%3AA0A2K5V8L5+OR+accession%3AA0A2K5YH50+OR+accession%3AA0A2K6CCS4+OR+accession%3AA0A2K6R0I7+OR+accession%3AA0A2R9AWY2+OR+accession%3AA0A2R9B0Q5+OR+accession%3AA0A7N9CS34+OR+accession%3AA0A8C9HBV6+OR+accession%3AA0A8D2EQF8+OR+accession%3AF6S299+OR+accession%3AF6S7W7+OR+accession%3AG1S142+OR+accession%3AG3QLZ3+OR+accession%3AH2NA70+OR+accession%3AH2Q1T9+OR+accession%3AH9ZBZ9+OR+accession%3AH9ZC00.

        The FASTA file contains all the sequences: 
        
        ```
        >tr|A0A0D9REZ9|A0A0D9REZ9_CHLSB Proto-oncogene tyrosine-protein kinase receptor Ret OS=Chlorocebus sabaeus OX=60711 GN=RET PE=3 SV=1
        LTSLLPTVALGLYFSRDAYWEKLYVDQPAGTPLLYVHALRDAPEEVPSFRLGQHLYGTYR
        TRLHENNWICIQEDTGLLYLNRSLDRSSWEKLSGRNRGFPLLTVYLKVFLSPTFLREGEC
        ...
        YANWMLSPSAAKLMDTFDS
        
        >tr|A0A2K5MKU6|A0A2K5MKU6_CERAT Proto-oncogene tyrosine-protein kinase receptor Ret OS=Cercocebus atys OX=9531 GN=RET PE=3 SV=1
        MAKATSGAAGLRLLLLLLLLPLLGKVALGLYFSRDAYWEKLYVDQPAGTPLLYVHALRDS
        PEEVPSFRLGQHLYGTYRTRLHENNWICIQEDTGLLYLNRSLDHSSWEKLSGRNRGFPLL
        ...
        ADGTNTGFPRYANDSVYANWMLSPSAAKLMDTFDS
        ...
        
        >tr|H9ZC00|H9ZC00_MACMU Proto-oncogene tyrosine-protein kinase receptor Ret OS=Macaca mulatta OX=9544 GN=RET PE=2 SV=1
        MAKATSGAAGLRLLLLLLLLPLLGKGALGLYFSRDAYWEKLYVDQPAGTPLLYVHALRDA
        PEEVPSFRLGQHLYGTYRTRLHENNWICIQEDTGLLYLNRSLDRSSWEKLSGRNRGFPLL
        ...
        ASTPSDSLLYDDGLSEEETPLVDCNNAPLPRALPSTWIENKLYGRISHAFTRF
        ```

        Save this FASTA file as `P07949.90-similar.fasta`.

To continue this activity, the multiple sequence alignment (MSA) will be generated using the online **Clustal Omega** server provided by EMBL-EBI.

!!! example "Hands-on: Aligning the sequences"

    Open the Clustal Omega submission form at:
    [https://www.ebi.ac.uk/jdispatcher/msa/clustalo](https://www.ebi.ac.uk/jdispatcher/msa/clustalo).

    Upload the file `P07949.90-similar.fasta` as input.  
    Request the output format as **Pearson/FASTA** and keep the original sequence order by setting the **order** option to *input*.

    Set the job title to `P07949.90-similar.msa`.

    ??? success "Solution"

        After the job has completed on the EMBL-EBI servers, you will be redirected to the results page.  
        This page contains several tabs for exploring the alignment.

        From the **Tool output** tab, download the MSA by clicking the blue **Download** button.

        Example of the aligned P07949 protein sequence:

        ```
        >sp|P07949|RET_HUMAN Proto-oncogene tyrosine-protein kinase receptor Ret OS=Homo sapiens OX=9606 GN=RET PE=1 SV=3
        MAKATSGAAGLRLLLL--LLLPLLGKVALGLYFSRDAYWEKLYVDQAAGTPLLYVHALRD
        ...
        LKQVNHPHVIKLYGACSQD--GPLLLIVEYAKYGSLRGFLRESRKVGPGYLGSGGSRNSS
        ...
        LTRADGTNTGFPRYPNDSVYANWMLSPSAAKLMDTFDS
        ```

        Save this alignment as `P07949.90-similar.msa.fasta`.
        
The next step is to focus the analysis on the kinase domain positions across all aligned sequences. For this purpose, the course provides a Google Colab notebook that runs a Python script to identify and extract the aligned positions corresponding to a defined amino acid range in the original reference sequence.

!!! warning "Google account required"
    You must log in using a Google account to run the code in this notebook. By default, you can use your "@gmail.com" address.

!!! example "Hands-on: Extracting the aligned domain from the MSA"

    Open the Google Colab notebook at:
    https://colab.research.google.com/drive/16GakNh96qJcQFqvl9bUwC_1F5ZpZHGWb?usp=sharing

    The notebook is divided into two main sections.  
    First, run the **four hidden cells** in the section *Dependencies and method definitions* by clicking the **Run** icon. This step loads the required Python libraries and helper functions into memory.

    Next, move to the *Usage* section and execute the cells in order.  
    The first cell will prompt you to upload the alignment file `P07949.90-similar.msa.fasta`.

    After the file is uploaded, fill in the fields in the *Extraction parameters* cell and click the **Run** icon to start the extraction.

    Once the execution is complete, download the output file from the **Files** panel to your local working environment.

    ??? success "Solution"

        Use the following parameters in the *Extraction parameters* cell, based on the kinase domain definition:

        - `uniprot_id`: `P07949`
        - `start_pos`: `724`
        - `end_pos`: `1016`
        - `max_gap_fraction`: `0.4` (40%)
        - `output_filename`: `P07949.90-similar.msa.kinase.fasta`

        After running the cell, a new file will be generated and a summary message similar to the one below will be displayed:

        ```
        Parameters:
        UniProt ID: P07949
        Start Position: 724
        End Position: 1016
        Max Gap Fraction: 0.4
        For sp|P07949|RET_HUMAN: found 0.006779661016949152 as gap fraction (seq len: 295)
        For tr|A0A0D9REZ9|A0A0D9REZ9_CHLSB: found 0.0 as gap fraction (seq len: 295)
        ...
        File P07949.90-similar.msa.kinase.fasta written using alignment columns: 725 and 1020 (295 residues)
        ```

        Save the file `P07949.90-similar.msa.kinase.fasta` in your working environment. To do this, open the **Files** panel from the left navigation bar by clicking the folder icon, locate the file, open the contextual menu, and select **Download**.

        The extracted alignment will start as follows:

        ```
        >sp|P07949|RET_HUMAN Proto-oncogene tyrosine-protein kinase receptor Ret OS=Homo sapiens OX=9606 GN=RET PE=1 SV=3
        LVLGKTLGEGEFGKVVKATAFHLKGRAGYTTVAVKMLKENASPSELRDLLSEFNVLKQVN
        HPHVIKLYGACSQD--GPLLLIVEYAKYGSLRGFLRESRKVGPGYLGSGGSRNSSSLDHP
        ...
        NLLKTGHRMERPDNCSEEMYRLMLQCWKQEPDKRPVFADISKDLEKMMVKRRDYL
        
        >tr|A0A0D9REZ9|A0A0D9REZ9_CHLSB Proto-oncogene tyrosine-protein kinase receptor Ret OS=Chlorocebus sabaeus OX=60711 GN=RET PE=3 SV=1
        LVLGKTLGEGEFGKVVKATAFRLKGRAGYTTVAVKMLKENASPSELRDLLSEFNLLKQVN
        HPHVIKLYGACSQDAPGPLLLIVEYAKYGSLRGFLRESRKVGPGYLGSGGSRNSSSLDHP
        ...
        NLLKTGHRMERPDNCSEEMYRLMLQCWKQEPDKRPVFADISKDLEKMMVKSRDYL
        ```
        
We are now ready to predict the aligned biophysical features using **B2BTools**.

!!! example "Hands-on: Predicting the aligned biophysical features for the kinase domain"

    Open a new browser tab and go to the online platform at:
    https://bio2byte.be/online_predictors

    This time, select **Multiple Sequence Alignment** as the analysis type instead of **Single Sequence**.  
    Upload the file `P07949.90-similar.msa.kinase.fasta` and submit the job.

    After submission, you will be redirected to the **Token results** page.

    ??? success "Solution"

        Once the prediction job has completed, the results will appear in the **MSA Predictions** table. It takes approximately less than two minutes to finish.
        
        Click the **View Results** button to open the results page for the aligned kinase domain.

### 2.3.2 Understanding the results as biological profiles

#### 2.3.2.1 Exploring intrinsic flexibility and folding propensity

#### 2.3.2.2 Visualization of biophysical profiles

TBC

## 2.5 Exporting the results

TBC

## 2.6 Connecting online resources

For a selected protein, a set of "external resources" will be shown in the left navigation bar if the header is recognised as a UniProt entry. For this course, it will be focus on the "PTMs" using Scop3P. 

Clicking on the "Find PTMs on Scop3P" redirects you to the entry page on that resource: [https://iomics.ugent.be/scop3p/index?protein=P07949](https://iomics.ugent.be/scop3p/index?protein=P07949).

!!! note "To be continued..."
    [Next chapter](/../../chapters/chapter_03) explains how to use this resource.
