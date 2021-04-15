#!/bin/bash



file=$1
while read line;do
 echo ${line} | awk '{if($0 !~ /^[0-9]+$/) print $0;}' >> no_num.txt

done < ${file}
