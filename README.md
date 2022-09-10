# Improving Genome Nexus' Command Line Interface Experience - GSoC 2022 Final Work Submission


## Overview

Genome Nexus [1] is a tool for the annotation and interpretation of mutations in cancer. cBioPortal leverages Genome Nexus' API to for instance show how a mutation might change the protein or how often a mutation occurs in healthy populations or patients with cancer. We recently released Genome Nexus as a standalone tool and website. The workflow of how Genome Nexus related to cBioPortal is shown below:

Screen Shot 2022-04-01 at 11 37 17 AM

The annotation of the inputted mutation file happens on the command line. There are several formats of mutation files, the most popular being Mutation Annotation Format and VCF. We want to make it as easy as possible for people to annotate mutation files for import into cBioPortal. Currently there a variety of different tools to help with this including (a) genome-nexus-annotation-pipeline for annotation of MAF files, (b) annotation-tools for annotation of VCF files and (c) genome-nexus-cli with a redesigned interface for both. For this project we can either create a unified command line experience under (b) if the student is familiar with Java or Python or in (c) if they prefer to work in JavaScript.

[1] de Bruijn I, Li X, Sumer SO, et al. Genome Nexus: A Comprehensive Resource for the Annotation and Interpretation of Genomic Variants in Cancer. JCO Clin Cancer Inform. 2022;6:e2100144. doi:10.1200/CCI.21.00144

Goal:

Improve the command line experience of Genome Nexus by unifying the current 3 tools into a single recommended command line interface
Develop public documentation on how to best annotate a mutation file in MAF and VCF leveraging the new unified interface
Approach:

Learn about mutation file formats including MAF and VCF. What does each row represent? What is single nucletiode variant (SNV), what is a deletion, what is an insertion?
Research how to build user friendly command line interfaces
Create a unified user friendly command line interface in either Java, Python or JavaScript
Need skills:

Either Java, Python or JavaScript
