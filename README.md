# gatk3-4-rnaseq-germline-snps-indels
 Workflows for processing RNA data for germline short variant discovery with GATK (v3+v4) and related tools 

### Requirements/expectations :
 - BAM (test was done by bam file which was created by hisat2 and picard tools add group:
 java -jar ~/software/picard/build/libs/picard.jar AddOrReplaceReadGroups I=S3D_5day_RMrRNA.bam O=S3D_5day_RMrRNA.new.bam RGID=4 RGLB=lib1 RGPL=illumina RGPU=unit1  RGSM=20 >>logs 2>&1 & )

### Output :
 - A BAM file and its index.
 - A VCF file and its index. 
 - A Filtered VCF file and its index. 

 Runtime parameters are optimized for Broad's Google Cloud Platform implementation.
 For program versions, see docker containers.

### Important Note :
- The workflow allows users to opt to use GATK4 for all tools instead of the default combination between 
GATK3 and GATK4, but note the workflow has not been validated to run using all GATK4 tools. 
- Runtime parameters are optimized for Broad's Google Cloud Platform implementation. 
- For help running workflows on the Google Cloud Platform or locally please
view the following tutorial [(How to) Execute Workflows from the gatk-workflows Git Organization](https://software.broadinstitute.org/gatk/documentation/article?id=12521)

### LICENSING :
 This script is released under the WDL source code license (BSD-3) (see LICENSE in
 https://github.com/broadinstitute/wdl). Note however that the programs it calls may
 be subject to different licenses. Users are responsible for checking that they are
 authorized to run all programs before running this script. Please see the docker
 page at https://hub.docker.com/r/broadinstitute/genomes-in-the-cloud/ for detailed
 licensing information pertaining to the included programs. 
