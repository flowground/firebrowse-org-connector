# ![LOGO](logo.png) FireBrowse Beta API **flow**ground Connector

## Description

A generated **flow**ground connector for the FireBrowse Beta API API (version 1.1.38 (2018-02-26 11:01:29 484103261f6ef681a05cf163)).

Generated from: https://api.apis.guru/v2/specs/firebrowse.org/1.1.38/swagger.json<br/>
Generated at: 2019-05-07T17:40:44+03:00

## API Description

A simple and elegant way to explore cancer data

## Authorization

This API does not require authorization.

## Actions

### Retrieve all data by genes Gistic2 results.

> This service provides access to the Gistic2 all_data_by_genes.txt output data. This data is a gene-level table of copy number values for all samples. The returned copy number values are in units (copy number - 2) so that no amplification or deletion is 0, genes with amplifications have positive values, and genes with deletions are negative values. The data are converted from marker level to gene level using the extreme method: a gene is assigned the greatest amplification or the least deletion value among the markers it covers. Results may be filtered by cohort, gene, or barcode, but at least one gene or barcode must be supplied.

*Tags:* `Analyses`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `gene` - _optional_ - Comma separated list of gene name(s).
* `tcga_participant_barcode` - _optional_ - Comma separated list of TCGA participant barcodes (e.g. TCGA-GF-A4EO).
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: tcga_participant_barcode, cohort, gene.

### Retrieve Gistic2 significantly amplified genes results.

> This service provides access to the Gistic2 amp_genes.conf_99.txt output data.  At least 1 gene or cohort must be supplied.

*Tags:* `Analyses`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `gene` - _optional_ - Comma separated list of gene name(s).
* `q` - _optional_ - Only return results with Q-value <= given threshold.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: q, cohort, gene.

### Retrieve Gistic2 significantly deleted genes results.

> This service provides access to the Gistic2 del_genes.conf_99.txt output data.  At least 1 gene or cohort must be supplied.

*Tags:* `Analyses`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `gene` - _optional_ - Comma separated list of gene name(s).
* `q` - _optional_ - Only return results with Q-value <= given threshold.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: q, cohort, gene.

### Retrieve focal data by genes Gistic2 results.

> This service provides access to the Gistic2 focal_data_by_genes.txt output data. This output is similar to the all_data_by_genes.txt output, but using only focal events with lengths greater than the  focal length cutoff. This data is a gene-level table of copy number values for all samples. The returned copy number values are in units (copy number - 2) so that no amplification or deletion is 0, genes with amplifications have positive values, and genes with deletions are negative values. The data are converted from marker level to gene level using the extreme method: a gene is assigned the greatest amplification or the least deletion value among the markers it covers. Results may be filtered by cohort, gene, and/or barcode, but at least one gene or barcode must be supplied.

*Tags:* `Analyses`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `gene` - _optional_ - Comma separated list of gene name(s).
* `tcga_participant_barcode` - _optional_ - Comma separated list of TCGA participant barcodes (e.g. TCGA-GF-A4EO).
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: tcga_participant_barcode, cohort, gene.

### Retrieve all thresholded by genes Gistic2 results.

> This service provides access to the Gistic2 all_thresholded_by_genes.txt output data. A gene-level table of discrete amplification and deletion indicators for all samples. A table value of 0 means no amplification or deletion above the threshold. Amplifications are positive numbers: 1 means amplification above the amplification threshold; 2 means amplifications larger to the arm level amplifications observed for the sample. Deletions are represented by negative table values: -1 represents deletion beyond the threshold; -2 means deletions greater than the minimum arm-level deletion observed for the sample. Results maybe filtered by cohort, gene or barcode, but at least one gene or barcode must be supplied.

*Tags:* `Analyses`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `gene` - _optional_ - Comma separated list of gene name(s).
* `tcga_participant_barcode` - _optional_ - Comma separated list of TCGA participant barcodes (e.g. TCGA-GF-A4EO).
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: tcga_participant_barcode, cohort, gene.

### Retrieve aggregated analysis features table.

> This service returns part or all of the so-called <strong>feature table</strong>; which aggregates the most important findings across ALL pipelines in the GDAC Firehose analysis workflow into a single table for simple access.  One feature table is created per disease cohort.  Results may be filtered by date or cohort, but at least 1 cohort must be specified here. For more details please visit the <a href=https://confluence.broadinstitute.org/display/GDAC/Documentation\#Documentation-FeatureTable>online documentation</a>.  Please note that the service is still undergoing experimental evaluation and does not return JSON format.

*Tags:* `Analyses`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `date` - _optional_ - Select one or more date stamps.
* `column` - _optional_ - Comma separated list of which data columns/fields to return.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.

### Retrieve MutSig final analysis MAF.

> This service returns columns from the MAF generated by MutSig. Results may be filtered by gene, cohort, tool, or barcode, but at least one gene OR barcode OR cohort must be given.  By default a subset consisting of the most commonly used columns will be returned, but that can be modified with the column parameter. Specifying 'all' in this parameter is a convenient way to return every column of the respective MAF, and has precedence over any any other column selection expression.  The complete list of column names that may be specified is <a href='http://firebrowse.org/api-docs/#!/Metadata/MAFColNames'>given here</a>.  For more information on the mutation data, and how it is processed by Firehose, please consult the <a href="https://confluence.broadinstitute.org/display/GDAC/Documentation#Documentation-MutationPipelines">pipeline documentation</a>.

*Tags:* `Analyses`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `tool` - _optional_ - Narrow search to include only data/results produced by the selected Firehose tool.
* `gene` - _optional_ - Comma separated list of gene name(s).
* `tcga_participant_barcode` - _optional_ - Comma separated list of TCGA participant barcodes (e.g. TCGA-GF-A4EO).
* `column` - _optional_ - Comma separated list of which data columns/fields to return.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: tcga_participant_barcode, cohort, tool, gene.

### Retrieve Significantly Mutated Genes (SMG).

> This service provides a list of significantly mutated genes, as scored by MutSig.  It may be filtered by cohort, rank, gene, tool and/or Q-value threshold, but at least one cohort or gene must be supplied.

*Tags:* `Analyses`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `tool` - _optional_ - Narrow search to include only data/results produced by the selected Firehose tool.
* `rank` - _optional_ - Number of significant genes to return.
* `gene` - _optional_ - Comma separated list of gene name(s).
* `q` - _optional_ - Only return results with Q-value <= given threshold.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: q, cohort, tool, gene, rank.

### Retrieve links to summary reports from Firehose analysis runs.

> This service returns URLs to the analysis result reports for runs of the Broad Institute GDAC Firehose analysis pipeline. At least one year of run reports are maintained in the database, but the reports from the latest run will be returned by default. The set of <a href="https://confluence.broadinstitute.org/display/GDAC/Nozzle">Nozzle</a> reports returned may be filtered by disease cohort, report type and report name.

*Tags:* `Analyses`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `date` - _optional_ - Select one or more date stamps.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `name` - _optional_ - Narrow search to one or more report names.
* `type` - _optional_ - Narrow search to one or more report types.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: date, cohort, type, name.

### Returns RNASeq expression quartiles, e.g. suitable for drawing a boxplot.

> For a given gene compute quartiles and extrema, suitable e.g. for drawing a boxplot (Tukey 1977).  Results may be filtered by cohort, sample type, patient barcode  or characterization protocol, and are returned sorted by cohort.  Note that samples for which no expression value was recorded (e.g. <a href="http://firebrowse.org/api/v1/Samples/mRNASeq?&gene=egfr&cohort=SKCM&tcga_participant_barcode=TCGA-GN-A262">the melanoma sample TCGA-GN-262</a>) are removed prior to calculation.

*Tags:* `Analyses`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `gene` - _required_ - Enter a single gene name.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `protocol` - _optional_ - Narrow search to one or more sample characterization protocols from the scrollable list.
* `sample_type` - _optional_ - For which type of sample(s) should quartiles be computed?
* `Exclude` - _optional_ - Comma separated list of TCGA participants, identified by barcodes such as TCGA-GF-A4EO, denoting samples to exclude from computation.

### Retrieve standard data archives.

> This service returns the archive URLs for our Firehose standard data runs, providing a RESTful interface similar in spirit to the command line <a href="https://confluence.broadinstitute.org/display/GDAC/Download">firehose_get</a> tool. The archives can be filtered based on date, cohort, data type, platform, center, data level, and protocol.

*Tags:* `Archives`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `date` - _optional_ - Select one or more date stamps.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `data_type` - _optional_ - Narrow search to one or more TCGA data types from the scrollable list.
* `tool` - _optional_ - Narrow search to include only data/results produced by the selected Firehose tool.
* `platform` - _optional_ - Narrow search to one or more TCGA data generation platforms from the scrollable list.
* `center` - _optional_ - Narrow search to one or more TCGA centers from the scrollable list.
* `level` - _optional_ - Narrow search to one or more TCGA data levels.
* `protocol` - _optional_ - Narrow search to one or more sample characterization protocols from the scrollable list.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: cohort, protocol, center, data_type, level, tool, platform, date.

### Obtain identities of TCGA consortium member centers.

> By default this function returns a table of all consortium members in TCGA, aka centers; it provides both the HTTP domain and full organizational name of each center.  A subset of this table may be obtained by explicitly specifying one or more domain names.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `center` - _optional_ - Narrow search to one or more TCGA centers from the scrollable list.

### Retrieve names of all TCGA clinical data elements (CDEs).

> Retrieve names of all patient-level clinical data elements (CDES) available in TCGA, unioned across all disease cohorts. A CDE will be listed here only when it has a value other than NA for at least 1 patient case in any disease cohort. For more information on how these CDEs are processed see our <a href="https://confluence.broadinstitute.org/display/GDAC/Documentation">pipeline documentation</a>.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.

### Retrieve names of CDEs normalized by Firehose and selected for analyses.

> This service returns the names of patient-level clinical data elements (CDEs) that have been normalized by Firehose for use in analyses, unioned across all disease cohorts. For more information on how these CDEs are processed, see our <a href="https://confluence.broadinstitute.org/display/GDAC/Documentation">pipeline documentation</a>.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.

### Translate TCGA cohort abbreviations to full disease names.

> By default this function returns a table containing all TCGA cohort abbreviations and their corresponding disease names.  A subset of that table may be obtained by explicitly specifying one or more cohort abbreviations.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.

### Retrieve sample counts.

> Returns the aliquot counts for each disease cohort, per sample<br/>
> type and data type.  The sample type designation of "Tumor"<br/>
> may be used to aggregate the count of all tumor aliquots into<br/>
> a single number per disease and data type. See the SampleTypes<br/>
> function for a complete description of sample types.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `date` - _optional_ - Select one or more date stamps.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `sample_type` - _optional_ - Narrow search to one or more TCGA sample types from the scrollable list.
* `data_type` - _optional_ - Narrow search to one or more TCGA data types from the scrollable list.
* `totals` - _optional_ - Output an entry providing the totals for each data type.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: cohort.

### Retrieve dates of all GDAC Firehose stddata & analyses runs that have been ingested into FireBrowse.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.

### Simple way to discern whether API server is up and running

> Returns a message to indicate that API (server) is up and running, or times out if not.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.

### Retrieve names of all columns in the mutation annotation files (MAFs) served by FireBrowse.

> Retrieve the names of all columns in the mutation annotation files (MAFs) hosted by FireBrowse.  For more information on the mutation data, and how it is processed by Firehose, please consult the <a href="https://confluence.broadinstitute.org/display/GDAC/Documentation#Documentation-MutationPipelines">pipeline documentation</a>.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.

### Retrieve list of all TCGA patients.

> This service returns a list of all TCGA patient barcodes in FireBrowse, optionally filtered by disease cohort.  The barcodes are obtained directy from the clinical data.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: cohort.

### Translate TCGA platform codes to full platform names.

> By default this function returns a table of all of the technology platforms used to sequence or characterize samples in TCGA--both their short platform codes and full names.  A subset of this table may be obtained by explicitly specifying one or more platform codes.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `platform` - _optional_ - Narrow search to one or more TCGA data generation platforms from the scrollable list.

### Given a TCGA barcode, return its short letter sample type code.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `TCGA_Barcode` - _required_ - Enter a single TCGA barcode, of any form: e.g. TCGA-GF-A4EO-06 or TCGA-EL-A3D5-01A-22D-A202-08

### Translate from numeric to symbolic TCGA sample codes.

> Convert a TCGA numeric sample type code (e.g. 01, 02) to its corresponding symbolic (short letter) code (e.g. TP, TR).

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `code` - _required_ - Narrow search to one or more TCGA sample type codes.

### Translate from symbolic to numeric TCGA sample codes.

> Convert a TCGA sample type code in symbolic form (or 'short letter code' like TP, TR) to its corresponding numeric form (e.g. 01, 02).

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `short_letter_code` - _required_ - TCGA sample type short letter code(s) (e.g. TP, NB, etc.). 

### Return all TCGA sample type codes, both numeric and symbolic.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.

### Obtain identities of tissue source sites in TCGA.

> By default this function returns a table of all sites which contributed source tissue to TCGA, aka TSS's. A subset of this table may be obtained by explicitly specifying one or more sites.

*Tags:* `Metadata`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `tss_code` - _optional_ - Narrow search to one or more TSS codes

### Retrieve TCGA CDEs verbatim, i.e. not normalized by Firehose.

> This service returns patient clinical data from TCGA, verbatim. It differs from the Samples/Clinical_FH method by providing access to all TCGA CDEs in their original form, not merely the subset of CDEs normalized by Firehose for analyses.  Results may be selected by disease cohort, patient barcode or CDE name, but at least one cohort, barcode, or CDE must be provided. When filtering by CDE note that only when a patient record contains one or more of the selected CDEs will it be returned. Visit the Metadata/ClinicalNames api function to see the entire list of TCGA CDEs that may be queried via this method. For more information on how clinical data are processed, see our <a href="https://confluence.broadinstitute.org/display/GDAC/Documentation#Documentation-ClinicalPipeline">pipeline documentation</a>.

*Tags:* `Samples`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `tcga_participant_barcode` - _optional_ - Comma separated list of TCGA participant barcodes (e.g. TCGA-GF-A4EO).
* `cde_name` - _optional_ - Retrieve results only for specified CDEs, per the Metadata/ClinicalNames function
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: tcga_participant_barcode, cohort, cde_name.

### Retrieve CDEs normalized by Firehose and selected for analyses.

> This service returns patient-level clinical data elements (CDEs) that have been normalized by Firehose for use in analyses. Results may be selected by disease cohort, patient barcode or CDE name, but at least one cohort, barcode or CDE must be provided. When filtering by CDE note that only when a  patient record contains one or more of the selected CDEs will it be returned. Visit <a href="http://gdac.broadinstitute.org/runs/info/clinical">this table of CDEs</a> to see what's available for every disase cohort; for more information on how these CDEs are processed see our <a href="https://confluence.broadinstitute.org/display/GDAC/Documentation#Documentation-ClinicalPipeline">pipeline documentation</a>.

*Tags:* `Samples`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `tcga_participant_barcode` - _optional_ - Comma separated list of TCGA participant barcodes (e.g. TCGA-GF-A4EO).
* `fh_cde_name` - _optional_ - Retrieve results only for the CDEs specified from the scrollable list.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: tcga_participant_barcode, cohort, fh_cde_name.

### Retrieve mRNASeq data.

> This service returns sample-level log2 mRNASeq expression values. Results may be filtered by gene, cohort, barcode, sample type or characterization protocol, but at least one gene must be supplied.

*Tags:* `Samples`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `gene` - _optional_ - Comma separated list of gene name(s).
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `tcga_participant_barcode` - _optional_ - Comma separated list of TCGA participant barcodes (e.g. TCGA-GF-A4EO).
* `sample_type` - _optional_ - Narrow search to one or more TCGA sample types from the scrollable list.
* `protocol` - _optional_ - Narrow search to one or more sample characterization protocols from the scrollable list.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: tcga_participant_barcode, cohort, gene, protocol, sample_type.

### Retrieve miRSeq data.

> This service returns sample-level log2 miRSeq expression values. Results may be filtered by miR, cohort, barcode, sample type or Firehose preprocessing tool, but at least one miR must be supplied.

*Tags:* `Samples`

#### Input Parameters
* `format` - _optional_ - Format of result.
    Possible values: json, tsv, csv.
* `mir` - _optional_ - Comma separated list of miR names (e.g. hsa-let-7b-5p,hsa-let-7a-1).
* `cohort` - _optional_ - Narrow search to one or more TCGA disease cohorts from the scrollable list.
* `tcga_participant_barcode` - _optional_ - Comma separated list of TCGA participant barcodes (e.g. TCGA-GF-A4EO).
* `tool` - _optional_ - Narrow search to include only data/results produced by the selected Firehose tool.
* `sample_type` - _optional_ - Narrow search to one or more TCGA sample types from the scrollable list.
* `page` - _optional_ - Which page (slice) of entire results set should be returned. 
* `page_size` - _optional_ - Number of records per page of results.  Max is 2000.
* `sort_by` - _optional_ - Which column in the results should be used for sorting paginated results?
    Possible values: tcga_participant_barcode, cohort, tool, mir, sample_type.

## License

**flow**ground :- Telekom iPaaS / firebrowse-org-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
