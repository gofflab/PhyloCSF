<!-- dx-header -->
# PhyloCSF (DNAnexus Platform App)

Phylogenetic analysis of multi-species genome sequence alignments to identify conserved protein-coding regions

This is the source code for an app that runs on the DNAnexus Platform.
For more information about how to run or modify it, see
http://wiki.dnanexus.com/.
<!-- /dx-header -->



<!--
TODO: This app directory was automatically generated by dx-app-wizard;
please edit this Readme.md file to include essential documentation about
your app that would be helpful to users. (Also see the
Readme.developer.md.) Once you're done, you can remove these TODO
comments.

For more info, see http://wiki.dnanexus.com/Developer-Portal.
-->

<!--
TODO: Fill in additional info about how to use each input and output
below.
-->

## Inputs

* **alignments** the ``CrossSpeciesAlignments`` to evaluate, usually generated by the MAF Stitcher app
* **output_name** name of the output table
* **alignments_per_job** controls the degree of parallelization
* **species_set** usually auto-detected for alignments produced by the MAF Stitcher app
* **frames** search over three or six reading frames
* **orf** search over ORFs within each alignment
* **min_codons** minimum length considered in ORF search mode (with ``orf != AsIs``)

## Advanced Inputs

* **strategy** model and parameter optimization strategy
* **all_scores** report all scores computed (with ``frames != 1`` or ``orf != AsIs``)
* **bls** include a Branch Length Score along with PhyloCSF score in output table
* **anc_comp** include an ancestral composition score along with PhyloCSF score in output table
* **dna** include evaluated DNA sequence in output table
* **aa** include evaluated amino acid sequence in output table
* **instance_type** instance type for parallel jobs

## Outputs

* **scores**
* **errors** number of alignments without scores (see job log for details)