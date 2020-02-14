# sbx-centrifuge

[Sunbeam](https://github.com/sunbeam-labs/sunbeam) extension for running [centrifuge](https://github.com/infphilo/centrifuge)

A short-read classifer of bacterial taxa from metagenomic samples.

Takes decontaminated reads as input (regular part of the sunbeam pipeline)

## Installation

1. git clone https://github.com/sunbeam-labs/sbx_centrifuge

2. cp sbx_centrifuge $SUNBEAM_DIR/extensions/

3. cat sunbeam/extensions/sbx_centrifuge/config.yml >> sunbeam_config.yml (the config.yml that your are using for your given project)

4. Download your desired database of bacteria, etc. from the centrifuge website above

5. Edit sunbeam_config.yml to have desired parameters (important: "index" points to your downloaded centrifuge index)

## Running

sunbeam run --configfile ./sunbeam_config.yml all_centrifuge --use-conda {rest of parameters}

- If you have trouble running with "--use-conda" it may be best just to install the needed packages into the sunbeam environment (e.g. `conda activate sunbeam && conda install --file sbx_centrifuge_env.yml`)

## References

Sunbeam: https://github.com/sunbeam-labs/sunbeam
Centrifuge: https://github.com/infphilo/centrifuge
isolated Conda environment: http://snakemake.readthedocs.io/en/stable/snakefiles/deployment.html#integrated-package-management
