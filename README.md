# SISEC MUS 2018 Preview Generator

This repository aims to generate 30s excerpts from both the
[MUSDB18](https://sigsep.github.io/musdb.html) music data set and the estimated
sources submitted by participants of [SiSEC MUS 2018](https://sisec.inria.fr/).

Previews are generated from a pre-defined cut-list, such as those created using
[sigsep-mus-previews](sigsep-mus-previews).

## Usage

1. Install python3.6 requirements using `pip install -r requirements.txt`

2. Trim the reference MUSDB18 using
    ```
    python trim.py --musdb /path/to/musdb --previews 30s_previews.csv -o previews_output_dir
    ```
    where `30s_previews.csv` is the cut-list.

3. Trim the estimated wav files (for example) using:
    ```
    python trim.py --musdb /path/to/my_estimations --previews 30s_previews.csv -o previews_output_dir --iswav
    ```