# Manure-Incubation-nrfA-Sequencing-Project <br/><br/>

As part of a funded research project by Dr. Mary Ann Bruns to study bacteria capable of performing dissimilatory nitrate reduction to ammonium (DNRA, functional gene = nrfA) in agricultural soils. Bruns' post-doc, Dr. Arnab Bhowmik, performed an incubation study to assess how the addition of either raw manure or digested manure impacted nrfA communities of soils with previous management histories of either having synthetic fertilizer or broadcast manure additions. 
<br/> Moisture has also been a variable that has been thought to control DNRA rates in soils, as DNRA is a redox reaction that requires an extra 3 electron transfer compared to denitrification. Therefore, two different water-filled pore space (WFPS) %'s were used, 60 and 95. 
<br/> Illumina amplicon sequencing was performed on nrfA communities in the soils, BM and Fert, and manures, Raw and Digested, before incubations. Sequencing was also performed on samples from day 2 and day 16 of the incubations. <br/> <br/>
All raw fastq files have been uploaded to NCBI under the BioProject ID PRJNA613230. All code and metadata is available here to reproduce the results.

<br/><br/> Here is an overview of the sequence processing/analysis that was performed: 
<br/> 1. Dada2 in R was used to filter/trim sequences, determine amplicon sequence variants (ASVs), and remove chimeric sequences 
<br/> 2. Taxonomy was assigned with a custom database for nrfA sequences that was downloaded from FunGene 
<br/> 3. A phylogenetic tree was constructed in R using the msa and phangorn packages 
<br/> 4. Alpha-diversity was calculated for baseline and incubated samples separately from rarefied datasets and ANOVAs were performed 
<br/> 5. Beta-diversity was assesed with weighted UniFrac and PERMANOVAs were performed with the vegan package
<br/> 6. Pairwise permanovas were performed with the RVAideMemoire package
<br/> 7. Mantel tests were performed to determine if weighted UniFrac dissimilarities were correlated with NO3-, NH4+, or nrfA gene copy numbers (which were quantified from the incubated samples at day 2 and day 16)
<br/> 8. Differential abundance analyses were performed on baseline samples and incubated samples to determine if any taxa were differentially abundant across Day, WFPS, amendment type, or soil fertilization history

