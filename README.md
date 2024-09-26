# Tn-seq-Protein-Domain

__This analysis contains the scripts to analyse Tn-seq insertion data at the protein domain level.__

This includes:
* Curating GFF3 files of domains which map to the corresponding genomic coordinates
  * UniProtKB domains and regions
  * NCBI Pfam dataset CD-search domains and conserved family regions
* Calculating 'unannotated regions' of genes which don't contain any domains (this allows individual domain essentiality to be compared to other regions within the gene)
* Generating a GFF3 file of all genetic features to use with the TRANSIT HMM model (DeJesus et al. 2013)
* Generating a GFF3 file of the essentiality of different regions from the TRANSIT HMM model (DeJesus et al. 2013) model output

The output files are designed to be used in __JBrowse2__ (Diesh et al. 2023) to visualise transposon insertions on the protein domain level.
An example of this is below:

![image](https://github.com/user-attachments/assets/6d546bb9-fd5a-4d45-a05d-dbd5ba2efe13)

1. Feature track of gene positions, labelled with the gene names or locus tags (if unnamed);
2. Feature track for UniProtKB domain positions, labelled with the domain or region names;
3. Feature track for Pfam domain positions, labelled with the short-domain names and descriptions;
4. XY-track of Tn-sequencing insertion coordinates on a logarithmic scale;
5. XY-track for all TA site coordinates, with each site represented as a count of 1;
6. Feature track for essentiality state positions, if available, using different colours based on essentiality state type and labelled accordingly.

### Case studies
The data from __two__ case studies are used to validate the analysis and visualisation set-up:
1. _M. tuberculosis_ Tn-seq dataset from DeJesus et al. (2017)
2. _M. bovis_ Tn-seq dataset provided by Jennifer Stiens, School of Natural Sciences, Birkbeck College, University of London
_Note_: As the _M. tuberculosis_ and _M. bovis_ dataset formats available and requirements are slightly different, two additional processing scripts exist to recreate the _M. tubeculosis_ analysis.

### References
DeJesus MA, Gerrick ER, Xu W, Park SW, Long JE, Boutte CC, Rubin EJ, Schnappinger D, Ehrt S, Fortune SM, Sassetti CM, Ioerger TR. Comprehensive Essentiality Analysis of the Mycobacterium tuberculosis Genome via Saturating Transposon Mutagenesis. mBio. 2017;8(1):e02133-16.  

DeJesus, M.A., Ioerger, T.R. A Hidden Markov Model for identifying essential and growth-defect regions in bacterial genomes from transposon insertion sequencing data. BMC Bioinformatics. 2013;14(303)  

Diesh, C., Stevens, G.J., Xie, P. et al. JBrowse 2: a modular genome browser with views of synteny and structural variation. Genome Biol. 2023;24(74)
