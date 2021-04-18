### Preprocessing Dnase file
Preprocessing of DNase-Seq datasets:
Dataset	Assay	Link

`HEK293T DNA accessibility	DNase-Seq	wgEncodeOpenChromDnaseHek293tPk `


unzip file using:

    gunzip w wgEncodeOpenChromDnaseAdultcd4th1Pk.narrowPeak.gz

compress file

    bgzip -c w wgEncodeOpenChromDnaseAdultcd4th1Pk.narrowPeak > wgEncodeOpenChromDnaseAdultcd4th1Pk.narrowPeak.gz

Indexing using:

    tabix -p bed w wgEncodeOpenChromDnaseAdultcd4th1Pk.narrowPeak.gz

Preprocessing of the crisper targets file turning it to tsv format.
Calculation of intersection
Go over each target in targets file and query it using tabix:

    tabix wgEncodeOpenChromDnaseAdultcd4th1Pk.narrowPeak.gz chr1:713835-714424
save results to new csv file with intersection results 

### Preprocessing targets file

### Narrow peak
                    
**chrom **|**chromStart **|**chromEnd **|**name **|**score **|**strand **|**upstream **|**protospacer **|**PAM **|**downstream **|**signal\_value\_dnase**
:chr1:|:100:|:200:|:.:|:0:|:.:|:180:|:5.0945  :|:-1:|:50:|:-----:
