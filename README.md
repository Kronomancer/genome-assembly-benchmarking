# CSC448 Final Project – Genome Assembly and Evaluation

## Overview
This project implements a comparative genome assembly pipeline for Honeybee and Carpenter Bee sequencing data. It covers data acquisition, quality control, preprocessing, assembly with multiple assemblers, and assembly evaluation against reference genomes.

The workflow is designed to run in Google Colab using micromamba for environment management.

## Data Sources
- Honeybee reads: SRR36076821
- Carpenter Bee reads: SRR24955310
- Bacterial dataset: SRR3924617
- Honeybee reference genome: RefSeq GCF_003254395.2
- Carpenter Bee reference genome: NCBI accession GCA_049004755.1

## Tools and Software
- Google Colab
- micromamba (Python 3.10)
- SRA Toolkit (fasterq-dump)
- FastQC
- Trimmomatic
- SPAdes
- MEGAHIT
- QUAST
- NCBI Datasets CLI

## Directory Structure
BioinformaticsProject/
├── Reads/
│   ├── Honeybee/
│   │   ├── new_reads/
│   │   ├── result_spades/
│   │   └── result_megahit/
│   └── CarpenterBee/
│       ├── new_reads/
│       ├── result_spades/
│       └── megahit_carpenterbee/

## Pipeline Steps
1. Environment setup with micromamba
2. Read download using fasterq-dump
3. Quality control with FastQC
4. Read trimming with Trimmomatic
5. Genome assembly with SPAdes and MEGAHIT
6. Assembly evaluation with QUAST against reference genomes

## Outputs
- Assembled contigs (FASTA)
- FastQC reports
- QUAST evaluation reports

## Notes
- Resource usage is configurable per run.
- Some cells clear the Colab workspace to conserve storage.
- File paths may require adjustment depending on Drive layout.
