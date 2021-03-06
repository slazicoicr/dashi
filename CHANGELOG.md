# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.4.0] - 2019-10-11

### Changed
* Split up the Shiny-like app from `rnaseqc.over_time` into its own modules
* Fixed `pooling_qc_sample` gsi-qc-etl imports to conform to v0.5.0

### Added
* BamQC app that mirrors the Shiny-like look of `rnaseqc.over_time`
* `ShinyMimic` class that encapsulates app logic independent of input DataFrame

## [0.3.0] - 2019-10-03

### Changed
* Updated all modules to work with gsi-qc-etl 0.5.0 (which uses versioned
DataFrames)
* Columns defined within a module are proper constants

### Removed
* `aq` module from runreport (dead code)
* `histograms` module from runscanner (did not work as a visualization)

### Added
* Cache location needs to be specified by environmental variable

## [0.2.0] - 2019-09-05

### RNASeQC
#### Added
* User can select shape and colour of plotted data
* Exportable Data Table that matches currently visible plotted data
* Plots can match Data Table sorting

#### Changes
* Updated to Dash 1.2.0
* Proper naming and capitalization of variables
* Improved function documentation
* Data is pulled from Pinery Samples Provenance instead of Pinery Samples


## [0.1.0] - 2019-08-02
Belated start of a Changelog

### Added
* `setup.py` file for easy installation
* `index.py` as the Dashi home screen
* Support for `Dash 1.0`
* `bamqc.gbovertime` module for visualizing GB production over time
* `bcl2fastq.index_summary` module for pooling visualization
* `poolqc.pooling_qc_sample` module for RNA-Seq QC data after Pooling Run
* `rnaseqc.over_time` module for visualizing RNASeQC metrics
* `runreport.proj_hist` module to show project coverage of a run compared to
previous runs
* `runscanner.yield_over_time` module to show machine yield over time
