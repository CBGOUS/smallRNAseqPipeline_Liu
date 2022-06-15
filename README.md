Pipeline to implement a basic NGS analysis (small RNAseq and RNAseq).
This allows the stepwise analysis of an NGS dataset. Output from one step serves as input to the subsequent step, 
so the analysis needs to follow a logical order. 
For example, mapping must come before read counting, and adapter trimming must precede mapping.

Basic command line execution is as follows:

java -jar -Dlog4j.configurationFile=file:log4j2.xml  NGSsmallRNA.jar -r configuration.yaml -p pipeline.json -d ngsdata.tsv

where the yaml file contains parameters for each step, the json file specifies which steps should be performed, 
and the tsv file specifies the data to be analyzed.

The reference files folder contain the yaml, json and tsv files used in the small RNAseq analysis for the lung cells (A549 and BEAS2B). 

In lungcells_miRNA_hsu.yaml file, NEBNext.fa contains the 3' adaptor sequence for adaptor trimming: AGATCGGAAGAGCACACGTCT# small RNAseq Pipeline
