# Improving Genome Nexus' Command Line Interface Experience - GSoC 2022 Final Work Submission


## Overview

Genome Nexus [1] is a command line tool for the annotation and interpretation of mutations in cancer. cBioPortal leverages Genome Nexus' API to show how a mutation might change the protein or how often a mutation occurs in healthy populations or patients with cancer. The workflow of how Genome Nexus related to cBioPortal is shown below:

![plot](./workflow.png)

## Goals

Currently there a variety of different tools to help with this including 
  * [genome-nexus-annotation-pipeline](https://github.com/genome-nexus/genome-nexus-annotation-pipeline) for annotation of MAF files,
  * [annotation-tools](https://github.com/genome-nexus/annotation-tools) for annotation of VCF files and
  * [genome-nexus-cli](https://github.com/genome-nexus/genome-nexus-cli) with a redesigned interface for both. 
  
The first goal is to improve the command line experience of Genome Nexus by unifying the current 3 tools into a single recommended command line interface and the second goal is to develop public documentation on how to best annotate a mutation file in MAF and VCF leveraging the new unified interface.

## Approved Pull Requests

Here is the list of approved pull requests and their respective commits:
  * Maf file validation [#196](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/pull/196), [f446339](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/f446339a67f67cb8667914b62225d48d461ebf7a)
  * Replace log4j imports with slf4j [#199](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/pull/199), [3bf2844](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/3bf284469dea1ec2d1d63b66eab5309994d35c8e)
  * Add tests for MutationRecordProcessor [c3b1574](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/c3b15741889b24db71bed12545921c7f0decaf5b)
  * Replace apache.lo4j with slf4j [44288aa](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/44288aa014deced50c3704ac98bfd2b58e5ae1ef)
  * Unwanted logs while file loading PR:[#195](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/pull/195) [44288aa](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/44288aa014deced50c3704ac98bfd2b58e5ae1ef)
    * Excessive logs are removed
  *   [#208](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/pull/208)  [c302523](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/c302523f41d34c6fb9ab66b5bcf213f012ebecde)
  * [#195](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/pull/195)  [8bad1bf](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/8bad1bf90f64f4c9380c2e1849390559bec18213)
  * [#207](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/pull/207)  [e2e8c65](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/e2e8c655fd0203ca34a92540d37e7fe407e3196c)
  * Convert config.yml to unit tests [1a5dd65](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/1a5dd658db4c059d5ba4dca8815e083d6e0d4a23)
  * Remove converted tests from config.yml [71b2d50](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/71b2d508ba441c3a048a0c4cbd09723d35478dea)
  * Delete old batch test [0f857ec](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/0f857ec2564f67c41608b2977f74e811605417ae)
  * [#200](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/pull/200)  [ab7b1b0](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/ab7b1b0f96c4e1d1c388772f5c0355b18f3020be)
  * Add output-format as option and its functionality with an example file [5f30f5b](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/5f30f5b07e803d4f46cac5f4e58b0b76987d18e1)
  * Add output format tcga [b79f777](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/b79f777f672a75af7a566498f1f2b9bdf7187194)
  * Add output format minimal [52d9d77](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/52d9d7760cf314c35e07c7cb41358983db8e35f9)
  * Add subcommands annotate and merge [71116e7](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/71116e7496c1c07098fbcb8796397633342a2a98)
  * add tests for minimal and tcga output formats [5737506](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/573750651d64d3b624946fa3d43db195d5fd0077)
  * add tests for custom output format [50798b1](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/50798b16d0ca2a12a7c96a4e2f0f142b265e2708)
  * Use post method as default [5d24b3f](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/5d24b3f1250c1a83ff3d3370b0fb5eebee4177b0)
  * Fix redundant exception prints [0e7a1f3](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/0e7a1f34c77cad02faf003e80a29832a15985cca)
  * Rename tcga to extended [3965d15](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/3965d1513b6cb1dffe303e242b0af6ec9b6982b4)
  * Document [d51a557](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/d51a5576d2cc050c07ea8be466e4336223e6e26e)
  * Fix custom file formatting [98115a0](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/98115a0153873e4a9d85e7e45130bd3092caf174)
  * Add runtime metrics (avg, total) [#221](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/pull/221) [50953cd](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/50953cdd6326490bb82d4e031ce1ce9604526314)
  * Address Rmadupuri test errors [#224](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/pull/224) [0a95018](https://github.com/genome-nexus/genome-nexus-annotation-pipeline/commit/0a950182fba7a916b810faeb788db242c38e23fc)



[1] de Bruijn I, Li X, Sumer SO, et al. Genome Nexus: A Comprehensive Resource for the Annotation and Interpretation of Genomic Variants in Cancer. JCO Clin Cancer Inform. 2022;6:e2100144. doi:10.1200/CCI.21.00144

