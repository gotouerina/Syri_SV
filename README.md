# Genome SV detection

## 01.syri
syri : https://github.com/schneebergerlab/syri

To install syri , type

    conda create -n syri_env -c bioconda syri
    conda activate syri_env
or

    conda install -c bioconda syri

You can also try to build from the source code

It is recommanded to do syri after mummer alignment

I have write an instruction about it ,see

https://github.com/gotouerina/Colinear_mummer_NGenomeSyn

It is also recommanded to split genome into chr to perform syri , there I provide a perl script split.pl , Usage:

        perl split.pl <_.fasta>
 
The result of syri can be visualized by plotsr : https://github.com/schneebergerlab/plotsr

you can install it by typing 

        conda install -c bioconda plotsr 

and you can check the example in the plotsr dictionary

##   02.Assemblytics

Upload file on http://assemblytics.com

or dowanload source code on https://github.com/marianattestad/assemblytics

##   03.SVIM-ASM

snakemake pipeline : svimasmhap.py 

#    SV annotation

vcfanno is recommanded to annotate the SV VCFformat file. Git : https://github.com/brentp/vcfanno

        wget https://github.com/brentp/vcfanno/releases/download/v0.3.5/vcfanno_linux64
        vcfanno_linux64 config.toml $vcf > $annotated.vcf

example config.toml are provided in foleder config.

#    SV filter and Go

use gff file

        perl grep.pl $file $output $gff;
        perl svfilter $input $output;

You may need use convertid2name.pl ,it is in https://github.com/gotouerina/Comparative-genomics-script/blob/main/PERLscripts/convertid2name.pl

Go : metascape

