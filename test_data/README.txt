wig file was created using: 

/mnt/work1/users/home2/quever/git/hmmcopy_utils/bin/readCounter --window 1000000 --quality 20 \
--chromosome "chr1,chr2,chr3,chr4,chr5,chr6,chr7,chr8,chr9,chr10,chr11,chr12,chr13,chr14,chr15,chr16,chr17,chr18,chr19,chr20,chr21,chr22,chrX,chrY" \
/mnt/work1/users/pughlab/projects/LGSA/swgs/ichor_cna/input/LGSA-001-195344_S3.cocleaned.bam |\
 sed "s/chrom=chr/chrom=/" >  /mnt/work1/users/pughlab/projects/LGSA/swgs/ichor_cna/output/wig/LGSA-001-195344_S3.wig


Parameters were run using:

Rscript /mnt/work1/users/home2/quever/git/ichorCNA/scripts/runIchorCNA.R \
  --id LGSA-001-195344_S3 \
  --WIG /mnt/work1/users/pughlab/projects/LGSA/swgs/ichor_cna/output/wig/LGSA-001-195344_S3.wig \
  --ploidy "c(2,3)" \
  --normal "c(0.2, 0.3, 0.4, 0.5,0.6,0.7,0.8,0.9)" \
  --maxCN 5 \
  --gcWig /mnt/work1/users/home2/quever/git/ichorCNA"/inst/extdata/gc_hg19_1000kb.wig" \
  --mapWig /mnt/work1/users/home2/quever/git/ichorCNA"/inst/extdata/map_hg19_1000kb.wig" \
  --centromere /mnt/work1/users/home2/quever/git/ichorCNA"/inst/extdata/GRCh37.p13_centromere_UCSC-gapTable.txt" \
  --normalPanel /mnt/work1/users/home2/quever/git/ichorCNA"/inst/extdata/HD_ULP_PoN_1Mb_median_normAutosome_mapScoreFiltered_median.rds" \
  --includeHOMD False --chrs "c(1:22, \"X\")" --chrTrain "c(1:22)" \
  --estimateNormal True --estimatePloidy True --estimateScPrevalence True \
  --scStates "c(1,3)" --txnE 0.9999 --txnStrength 10000 --outDir /mnt/work1/users/pughlab/projects/LGSA/swgs/ichor_cna/output/


