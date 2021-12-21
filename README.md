# Jie-Li
Additional file 9. The command used to run the software.
#------------------------Delete low quality reads----------------------------------------------------------------

nNs=5
JUNK_FILTER=NNNNN,AAAAAAAAAAA,GGGGGGGGGGGG

#------------------------Delete adapter reads----------------------------------------------------------------

delete_adapter=T
adapter1=GATCGGAAGAGC
adapter2=GATCGGAAGAGC
min_overlap=5
min_len_trim_adapter=100

#------------------------Filter abundance reads--------------------------------------------------------

Abundance_mis=2
Abundance_threads=8
Abundance_sequences_filter=MRCAB
Abundant_file_dir=/mnt/dgfs/database/genome_db_public/homo_sapiens/Ensembl/v101/mRNA/Abundance

#------------------------Reads mapping to genome software hisat2 analyze-----------------------------------------

HISAT2BuildSplice=T
HISAT2_threads=12
min_intron_length=20
max_intron_length=500000
dta=dta


#------------------------Reads mapping to genome software tophat analyze-----------------------------------------

#min_intron_length=50
#max_intron_length=500000
library_type=fr-firststrand

mate_inner_dist=50
mate_std_dev=20
Tophat_threads=4
min_segment_length=70
max_segment_length=40000
mis=2
read_edit_dist=2
tophat_gtf_guide=G
keep_tmp=F



#------------------------Quantify transcripts and genes software stringtie analyze-------------------------------

stringtie_threads=10
stringtie_abundance=1

#------------------------Differential genes software ballgown analyze--------------------------------------------

expression_value=FPKM
remove_low_copy=0

#------------------------Significant conditions------------------------------------------------------------------

DESeq=T
Chi_square=T
FDR=0.05
FDR_app=T
log2fold=1
log2fold_app=T
