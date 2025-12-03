# scs

A breakdown of our algorithm 
Basic Local Alignment Search Tool (BLAST)

Algorithm steps:

Protein Word List (Neighborhood words)

Keep words that meet or exceed a certain threshold value, discard all others
Scanning for word "hits":

For each word, create a lookup table (hash table) where each word is mapped to all occurrences of that word in the database sequence (by index)
Scanning the database part is done using the KMP exact pattern matching algorithm (from the lecture)
Extending "hits" based on score obtained from scoring matrix

Extension process is terminated in one direction when the segment pair score (between query database sequences) falls a certain distance below the best score found for shorter extensions

May need to access NCBI protein database for meaningful tests



Random protein sequence generator (for testing purposes): https://www.bioinformatics.org/sms2/random_protein.html

Protein sequence is fetched from the NCBI protein database using the python biopython module: To run this program locally, install the biopython module using 'pip install biopython'
We have also shown extensive testing of our methods and the outputs can be seen in the python notebook file. 

Chain-B insulin-like receptor, Drosophila melanogaster (fruit fly) https://www.ncbi.nlm.nih.gov/protein/9EF4_B

Research papers on this topic we reviewed 

Stephen F Altschul, Warren Gish, Webb Miller, Eugene W Myers, and David J Lipman. Basic local alignment search tool. Journal of molecular biology, 215(3):403– 410, 1990.

https://www.biostat.wisc.edu/bmi576/papers/blast.pdf

Samuel Karlin and Stephen F Altschul. Methods for assessing the statistical significance of molecular sequence features by using general scoring schemes. Proceedings of the National Academy of Sciences, 87(6):2264–2268, 1990.

https://web.stanford.edu/class/sbio228/public/readings/Bioinformatics_I_Lecture6/Karlin_PNAS_90_Statistical_significance_alignment.pdf

Additional BLAST paper:

https://link.springer.com/article/10.1186/gb-2001-2-10-reviews2002
