# HumVarCalCPGR
Human Variant Calling Pipeline

This pipeline consists of three phases in accordance with the GATK Best practices

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
