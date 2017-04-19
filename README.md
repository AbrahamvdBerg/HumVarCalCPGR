# HumVarCalCPGR
Human Variant Calling Pipeline

This pipeline consists of three phases in accordance with the GATK Best practices.
The tools used for this pipeline are listed under Tools.

Phase 1 - Preprosessing 
Raw reads 
-> Map to reference (BWA MEM) 
-> Mark duplicates (Picard) 
-> Base recallibration 
-> Analysis ready reads

Phase 2 - Variant Discovery (Initial Variant Discovery)
Analysis ready reads
-> Var. Calling (HC -ERC GCVF)
-> Genotype likelihoods

-> Joint Genotyping
-> Raw variants: SNPs; Indels
-> Filter Variants
-> Analysis ready variants: SNPs; Indels

Phase 3 - Callset refinement (Variant Annotation and Priotorization)
Analysis ready variants: SNPs; Indels
-> Refine genotypes
-> Annotate variants
-> Evaluate callset
-> Look good? troubleshoot or use in project

Pipeline framework
Next Flow

Tools
GATK 3.7.0
BWA MEM (Latest version - BWA-0.7.12)
Picard tools (Latest version - 2.9.0)
Oncotator (version 1.9)
GenotypeConcordance (Picard version)

GATK tools:
BaseRecalibrator 
AnalyzeCovariates 
PrintReads
HaplotypeCaller
CombineGVCFs
GenotypeGVCFs
VariantFiltration 
VariantRecalibrator
ApplyRecalibration 
CalculateGenotypePosteriors
VariantAnnotator
SelectVariants
CombineVariants
VariantEval
VariantsToTable



