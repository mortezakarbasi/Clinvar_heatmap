## How to draw Heatmap for data from clinvar 
first get and clean data with  tool from follwoing link :
[clinvar perl github](https://github.com/dlal-group/clinvar-perl)
also the video which is learn how to use clinvar-perl [youtube link](https://www.youtube.com/watch?v=ivuM2d9B4yI)
for running the program need to install and with the following code:
``` bash
sudo apt-get update
sudo apt-get install liblist-moreutils-perl
sudo apt-get install libsort-fields-perl
```
download the clinvar data from ftp of Clinvar in NCBI
variant_summary.txt.gz 
decompressed the file 
``` bash
gzip -d variant_summary.txt.gz
```
after that using that using see the video and the clean file for your gene
``` bash
perl clinvar-viewer.pl summary gene <gene name>
```
example 
``` bash
perl clinvar-viewer.pl summary gene IGHMBP2
```
after getting the ighmbp2 clean file 
open jupyter note book example for IGHMBP2 and change the ighmbp2
also you can see the video from following [link](https://www.youtube.com/watch?v=0U9cs2V-Mqc) for learning how to draw heatmap

