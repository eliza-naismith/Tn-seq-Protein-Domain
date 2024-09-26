# JBrowse2 visualisation setup

![image](https://github.com/user-attachments/assets/0ed09119-7c6e-4f68-ba8e-24e9cdce836e)

1. Feature track of gene positions, labelled with the gene names or locus tags (if unnamed);
2. Feature track for UniProtKB domain positions, labelled with the domain or region names;
3. Feature track for Pfam domain positions, labelled with the short-domain names and descriptions;
4. XY-track of Tn-sequencing insertion coordinates on a logarithmic scale;
5. XY-track for all TA-site coordinates, with each site represented as a count of 1;
6. Feature track for essentiality state positions, if available, using different colours based on essentiality state type and labelled accordingly.

### Steps to recreating the visualisation setup

JBrowse2 desktop application is available from: https://jbrowse.org/jb2/download/  
Diesh, C., Stevens, G.J., Xie, P. et al. JBrowse 2: a modular genome browser with views of synteny and structural variation. Genome Biol. 2023;24(74)

Using the _M. tuberculosis_ JSON file set-up, the visualisation can be recreated for _M. tuberculosis_ or _M. bovis_:
1. Download the GitHub repository to local computer.
2. Launch a new session in JBrowse2 and open the corresponding reference fasta file as a FastaAdapter.
   * Assembly name & assembly display name should be set to: __M. tuberculosis__ or __M. bovis__

![image](https://github.com/user-attachments/assets/ce6e939f-8c18-42c9-aa6c-701de4da64c7)

3. Launch linear genome view, and open corresponding assembly.
4. Open the track selector -> Select three horizontal lines -> Select Add track...
5. Change from default add track workflow to __Add track JSON__
6. One at a time, copy and paste the contents of each JSON file into the text box and submit. Check the track is displayed as expected.
   * You __must__ change the localPath within each JSON file to match the path in which your repository is saved. For ease, change /yourpath/ to the GitHub project folder path.
   * If using _M. bovis_ instead of _M. tuberculosis_, the __assemblyNames__ must be adjusted accordingly.

![image](https://github.com/user-attachments/assets/9d237845-77e7-48a7-b3b8-7425a46c67b2)
