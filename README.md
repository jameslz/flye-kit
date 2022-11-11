#### flye-kit: long reads assembly with Flye and Pilon
<br>

#### 1. dependence

`flye`, `pilon`


#### 2. CLI API

```
Program: flye-kit: long reads assembly with Flye and Pilon.
Version: 0.0.1
Contact: ZHANG LEI <zhanglei@logictek.cn>

Usage:   flye-kit  [options]

Options:
         -1 STR  FASTQ file of first short reads in each pair.  (required)
         -2 STR  FASTQ file of second short reads in each pair. (required)
         -l STR  FASTQ or FASTA file of long reads.  (required)
         -q STR  long reads quality: pacbio-raw | pacbio-corr | pacbio-hifi |
                                     nano-raw | nano-corr | nano-hq (required)
         -n STR  strain name for sequence label.  (required)
         -g STR  estimated genome size (for example, 5m or 2.6g), (required)
         -o STR  Output directory (required)
         -p STR  Other Flye parametes. default: [""]
         -t INT  CPU number, default: [40]
         -r INT  rounds for pilon polish, default: [2]
```

#### 3. examples

CMD:

```sh
flye-kit -1 illumina/L_1.clean.fq.gz -2 illumina/L_2.clean.fq.gz  -l nanopre/L.fq.gz  -q nano-raw -n L -g 13m -o L
```