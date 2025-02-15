<!--

SPDX-FileCopyrightText: © 2024—2025 David Bliss

SPDX-License-Identifier: MIT
-->

# flac2lossy

`flac2lossy.sh` recursively encodes a directory of FLAC format files to Opus or MP3,
recreating the same directory structure in the output directory. It makes use
of all CPU cores (or as many as you would like). The tool does partial updates,
so that only new or modified files are (re-)encoded. Encodes are removed if the
original no longer exists. Album art is copied to the encoded directory if its
name matches {cover,folder}.{jpg,png}.

## Usage

```shell
Usage:
    ./flac2lossy.sh [options] <FLAC_DIR> <LOSSY_DIR>

Options:
    -h          Print this help page
    -b <kbit/s> Set which bitrate to encode to
    -f          Rename cover images to folder.{png,jpg}.
    -j <jobs>   Run up to <jobs> encoder processes in parallel.
    -t [opus|mp3] Lossy output type. Default 'opus'.
```

## Dependencies

Flac, opus-tools, bash.
