# GeneName2EntrezIDMusMusculus

This is combined bash/R script that will use a file with **mouse** gene symbols in **a first column** of a file and preppend a ENREZ ID to it, while keeping the structure of the file from  other columns. Script sets its host to ensembl.org thus it could be especially useful when biomaRt site is down.


# Dependencies
Rscript, BiomaRt

# Usage
chmod 775 GeneName2EntrezIDMusMusculus.sh

./GeneName2EntrezIDMusMusculus.sh file.txt

# Example

<pre>
head file.txt
Tcf21	1
Ahr	4
Gapdh	5

chmod 775 GeneName2EntrezIDMusMusculus.sh
./GeneName2EntrezIDMusMusculus.sh file.txt


head file.txt.genename

21412 Tcf21	1
11622 Ahr	4
101056341 Gapdh	5

Note that **only lines with mathces in the Biomart database** are present in the output , those without a match are not in the output file.


