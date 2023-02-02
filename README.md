# Minimap2

Minimap2 is fast aligment program to map DNA and mRNA sequences against reference genome. Minimap2 can be used for mapping short reads( Illumina) and also long reads such as pacbio and Oxford nanopore reads.

# Installation via Conda

conda install -c bioconda minimap2

# Usuage

short read mapping command line ;

time minimap2 -ax sr ref.fasta sample1_R1.fastq.gz  sample2_R2.fastq.gz  > sample.sam 

--time command is used to keep track of the run time of minimap.

# Samtools
(Samtools can be used to convert sam to bam files and then sort/index the bam file)
         

#convert the sam to bam format

samtools view sample.sam > sample.bam 

#sort the bam files

samtools sort sample.bam > sample_sorted.bam


#index the bam files

samtools index sample_sorted.bam 

After Alignment to reference genome, the sorted bam will used for variant calling process as input file for analysis such as  Whole genome sequencing(WGS) or Whole Exome sequencing(WES)


