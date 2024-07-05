![SRA Downloader](https://raw.githubusercontent.com/s-andrews/sradownloader/master/logo/sradownloader.png)

This repository is a fork of [sradownloader](https://github.com/s-andrews/sradownloader). Enhancements include the ability to download samples from the ENA database utilizing [Axel](https://github.com/axel-download-accelerator/axel), a command-line download accelerator. Additionally, users now have the flexibility to choose between FTP or wget for downloads. These modifications were motivated by the need to accelerate sample downloads and to provide an alternative due to FTP downloads being blocked on our HPC cluster.

### New options:

```bash
usage: sradownloader [-h] [--quiet] [--version] [--outdir OUTDIR] [--threads THREADS] [--retries RETRIES] [--force FORCE] [--fqdump FQDUMP] [--axel-connections AXEL_NUM_CONNECTIONS] [--ftp] [--wget] [--axel] [--nogeo] [--noena] [--noncbi] runtable

Download data from the SRA

positional arguments:
  runtable              The SraRunTable.txt file from the SRA run selector

options:
  -h, --help            show this help message and exit
  --quiet               Supress all but essential messages
  --version             show program's version number and exit
  --outdir OUTDIR       Folder to save data to (default .)
  --threads THREADS     Number of threads (default 1)
  --retries RETRIES     Number of times we'll retry a download before giving up (default 5)
  --force FORCE         Overwrite output files even if they exist
  --fqdump FQDUMP       Path to the fastq dump program (default fasterq-dump)
  --axel-connections AXEL_NUM_CONNECTIONS
                        Number of connections to use with axel (default 5)
  --ftp                 Use FTP to download from ENA (default)
  --wget                Use wget to download from ENA
  --axel                Use axel to download from ENA
  --nogeo               Disable sample name lookup from GEO
  --noena               Don't try downloading from ENA
  --noncbi              Don't try downloading from NBCI
```

# Acknowledgements

All credit goes to [s-andrews](https://github.com/s-andrews) for creating this invaluable tool.
