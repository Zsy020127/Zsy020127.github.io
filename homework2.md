# 上机练习 
## 2）Linux命令练习中的结果
### step0.准备: 解压缩.gtf的文件
    
    cd linux
    gunzip 1.gtf.gz
    ls
输出：

    1.gtf  file
### step1.查看文件基本信息
命令1

    cat 1.gtf | head

输出：

    #!genome-build R64-1-1
    #!genome-version R64-1-1
    #!genome-date 2011-09
    #!genome-build-accession :GCA_000146045.2
    #!genebuild-last-updated 2011-12
    IV      ensembl gene    1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding";
    IV      ensembl transcript      1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding";
    IV      ensembl exon    1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding"; exon_id "YDL248W.1"; exon_version "1";
    IV      ensembl CDS     1802    2950    .       +       0       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YDL248W"; protein_version "1";
    IV      ensembl start_codon     1802    1804    .       +       0       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding";
命令2

    cat 1.gtf | tail

输出：

    Mito    ensembl exon    85035   85112   .       +       .       gene_id "tM(CAU)Q2"; gene_version "1"; transcript_id "tM(CAU)Q2"; transcript_version "1"; exon_number "1"; gene_source "ensembl"; gene_biotype "tRNA"; transcript_name "tM(CAU)Q2"; transcript_source "ensembl"; transcript_biotype "tRNA"; exon_id "tM(CAU)Q2.1"; exon_version "1";
    Mito    ensembl gene    85295   85777   .       +       .       gene_id "RPM1"; gene_version "1"; gene_source "ensembl"; gene_biotype "ncRNA";
    Mito    ensembl transcript      85295   85777   .       +       .       gene_id "RPM1"; gene_version "1"; transcript_id "RPM1"; transcript_version "1"; gene_source "ensembl"; gene_biotype "ncRNA"; transcript_name "RPM1"; transcript_source "ensembl"; transcript_biotype "ncRNA";
    Mito    ensembl exon    85295   85777   .       +       .       gene_id "RPM1"; gene_version "1"; transcript_id "RPM1"; transcript_version "1"; exon_number "1"; gene_source "ensembl"; gene_biotype "ncRNA"; transcript_name "RPM1"; transcript_source "ensembl"; transcript_biotype "ncRNA"; exon_id "RPM1.1"; exon_version "1";
    Mito    ensembl gene    85554   85709   .       +       .       gene_id "Q0297"; gene_version "1"; gene_source "ensembl"; gene_biotype "protein_coding";
    Mito    ensembl transcript      85554   85709   .       +       .       gene_id "Q0297"; gene_version "1"; transcript_id "Q0297"; transcript_version "1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "Q0297"; transcript_source "ensembl"; transcript_biotype "protein_coding";
    Mito    ensembl exon    85554   85709   .       +       .       gene_id "Q0297"; gene_version "1"; transcript_id "Q0297"; transcript_version "1"; exon_number "1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "Q0297"; transcript_source "ensembl"; transcript_biotype "protein_coding"; exon_id "Q0297.1"; exon_version "1";
    Mito    ensembl CDS     85554   85706   .       +       0       gene_id "Q0297"; gene_version "1"; transcript_id "Q0297"; transcript_version "1"; exon_number "1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "Q0297"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "Q0297"; protein_version "1";
    Mito    ensembl start_codon     85554   85556   .       +       0       gene_id "Q0297"; gene_version "1"; transcript_id "Q0297"; transcript_version "1"; exon_number "1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "Q0297"; transcript_source "ensembl"; transcript_biotype "protein_coding";
    Mito    ensembl stop_codon      85707   85709   .       +       0       gene_id "Q0297"; gene_version "1"; transcript_id "Q0297"; transcript_version "1"; exon_number "1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "Q0297"; transcript_source "ensembl"; transcript_biotype "protein_coding";  
命令3

    cat 1.gtf | head -15
输出：

    #!genome-build R64-1-1
    #!genome-version R64-1-1
    #!genome-date 2011-09
    #!genome-build-accession :GCA_000146045.2
    #!genebuild-last-updated 2011-12
    IV      ensembl gene    1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding";
    IV      ensembl transcript      1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding";
    IV      ensembl exon    1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding"; exon_id "YDL248W.1"; exon_version "1";
    IV      ensembl CDS     1802    2950    .       +       0       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YDL248W"; protein_version "1";
    IV      ensembl start_codon     1802    1804    .       +       0       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding";
    IV      ensembl stop_codon      2951    2953    .       +       0       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding";
    IV      ensembl gene    3762    3836    .       +       .       gene_id "YDL247W-A"; gene_version "1"; gene_source "ensembl"; gene_biotype "protein_coding";
    IV      ensembl transcript      3762    3836    .       +       .       gene_id "YDL247W-A"; gene_version "1"; transcript_id "YDL247W-A"; transcript_version "1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "YDL247W-A"; transcript_source "ensembl"; transcript_biotype "protein_coding";
    IV      ensembl exon    3762    3836    .       +       .       gene_id "YDL247W-A"; gene_version "1"; transcript_id "YDL247W-A"; transcript_version "1"; exon_number "1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "YDL247W-A"; transcript_source "ensembl"; transcript_biotype "protein_coding"; exon_id "YDL247W-A.1"; exon_version "1";
    IV      ensembl CDS     3762    3833    .       +       0       gene_id "YDL247W-A"; gene_version "1"; transcript_id "YDL247W-A"; transcript_version "1"; exon_number "1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "YDL247W-A"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YDL247W-A"; protein_version "1";
命令4

    ls -lh 1.gtf
输出：

    -rw-rw-r-- 1 test test 12M Sep 11  2018 1.gtf
命令5

    wc -l 1.gtf
输出：

    42252 1.gtf
命令6

    grep -v "^#" 1.gtf | grep -v '^$' | wc -l
输出：

    42247
命令7

    cat 1.gtf | awk '$0!~/^\s*$/{print}' | head -10
输出：

    #!genome-build R64-1-1
    #!genome-version R64-1-1
    #!genome-date 2011-09
    #!genome-build-accession :GCA_000146045.2
    #!genebuild-last-updated 2011-12
    IV      ensembl gene    1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding";
    IV      ensembl transcript      1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding";
    IV      ensembl exon    1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding"; exon_id "YDL248W.1"; exon_version "1";
    IV      ensembl CDS     1802    2950    .       +       0       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YDL248W"; protein_version "1";
    IV      ensembl start_codon     1802    1804    .       +       0       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding";  
命令8

    grep -v '^\s*$' 1.gtf | head -10
输出：

    #!genome-build R64-1-1
    #!genome-version R64-1-1
    #!genome-date 2011-09
    #!genome-build-accession :GCA_000146045.2
    #!genebuild-last-updated 2011-12
    IV      ensembl gene    1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding";
    IV      ensembl transcript      1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding";
    IV      ensembl exon    1802    2953    .       +       .       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding"; exon_id "YDL248W.1"; exon_version "1";
    IV      ensembl CDS     1802    2950    .       +       0       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YDL248W"; protein_version "1";
    IV      ensembl start_codon     1802    1804    .       +       0       gene_id "YDL248W"; gene_version "1"; transcript_id "YDL248W"; transcript_version "1"; exon_number "1"; gene_name "COS7"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "COS7"; transcript_source "ensembl"; transcript_biotype "protein_coding";
### step2.数据提取
#### step2.1 筛选特定的列
命令1

    cat 1.gtf | awk ' { print $1, $2, $3 } ' | head
输出：

    #!genome-build R64-1-1
    #!genome-version R64-1-1
    #!genome-date 2011-09
    #!genome-build-accession :GCA_000146045.2
    #!genebuild-last-updated 2011-12
    IV ensembl gene
    IV ensembl transcript
    IV ensembl exon
    IV ensembl CDS
    IV ensembl start_codon
命令2

    cat 1.gtf | cut -f 1,2,3 | head
输出：

    #!genome-build R64-1-1
    #!genome-version R64-1-1
    #!genome-date 2011-09
    #!genome-build-accession :GCA_000146045.2
    #!genebuild-last-updated 2011-12
    IV      ensembl gene
    IV      ensembl transcript
    IV      ensembl exon
    IV      ensembl CDS
    IV      ensembl start_codon
命令3

    cut -f 1,3,4,5 1.gtf | head
输出：

    #!genome-build R64-1-1
    #!genome-version R64-1-1
    #!genome-date 2011-09
    #!genome-build-accession :GCA_000146045.2
    #!genebuild-last-updated 2011-12
    IV      gene    1802    2953
    IV      transcript      1802    2953
    IV      exon    1802    2953
    IV      CDS     1802    2950
    IV      start_codon     1802    1804
#### step2.2 筛选特定的行
命令

    cat 1.gtf | awk '$3 =="gene" { print $1, $3, $9 } ' | head
输出：

    IV gene gene_id
    IV gene gene_id
    IV gene gene_id
    IV gene gene_id
    IV gene gene_id
    IV gene gene_id
    IV gene gene_id
    IV gene gene_id
    IV gene gene_id
    IV gene gene_id
### step3.提取和计算特定的feature
#### step3.1 提取并统计featrue类型
命令

    grep -v '^#' 1.gtf |awk '{print $3}'| sort | uniq -c
输出：

    7050 CDS
    7553 exon
    7126 gene
    6700 start_codon
    6692 stop_codon
    7126 transcript
#### step3.2 计算特定feature特征长度
命令1

    cat 1.gtf | awk ' { print $3, $5-$4 + 1 } ' | head
输出：

    1
    1
    1
    1
    1
    gene 1152
    transcript 1152
    exon 1152
    CDS 1149
    start_codon 3
命令2

    cat 1.gtf | awk 'BEGIN{size=0;}$3 =="CDS"{ len=$5-$4 + 1; size += len; print "Size:", size } ' | tail -n 1
输出：

    Size: 9030648
命令3

    cat 1.gtf | awk 'BEGIN{L=0;}$3 =="CDS"{L+=$5-$4 + 1;}END{print L;}'
输出：

    9030648
命令4

    cat 1.gtf | awk '$3 =="CDS"{L+=$5-$4 + 1;}END{print L;}'
输出：

    9030648
命令5

    awk 'BEGIN  {s = 0;line = 0;}$3 =="CDS" && $1 =="I"{ s += $5-$4+1;line += 1}END {print "mean="s/line}' 1.gtf
输出：

    mean=1239.52
#### step3.3 分离并提取基因名字
命令

    cat 1.gtf | awk '$3 == "gene"{split($10,x,";");name = x[1];gsub("\"", "", name);print name,$5-$4+1}' | head
输出：

    YDL248W 1152
    YDL247W-A 75
    YDL247W 1830
    YDL246C 1074
    YDL245C 1704
    YDL244W 1023
    YDL243C 990
    YDL242W 354
    YDL241W 372
### step4.提取数据并存入新文件
#### step4.1 提取数据存入txt文件示范
命令

    grep exon 1.gtf | awk '{print $5-$4+1}' | sort -n | tail -3 > 1.txt
    less 1.txt
输出：

    12279
    14730
    14733

# 作业
### 1. 
命令

    cat 1.gtf | awk '$3 =="CDS" && $1 =="XI" ' | sort -k 5 | tail
输出：

    XI      ensembl CDS     82947   82998   .       +       0       gene_id "YKL190W"; gene_version "1"; transcript_id "YKL190W"; transcript_version "1"; exon_number "1"; gene_name "CNB1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "CNB1"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YKL190W"; protein_version "1";
    XI      ensembl CDS     83075   83547   .       +       1       gene_id "YKL190W"; gene_version "1"; transcript_id "YKL190W"; transcript_version "1"; exon_number "2"; gene_name "CNB1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "CNB1"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YKL190W"; protein_version "1";
    XI      ensembl CDS     84704   85900   .       +       0       gene_id "YKL189W"; gene_version "1"; transcript_id "YKL189W"; transcript_version "1"; exon_number "1"; gene_name "HYM1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "HYM1"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YKL189W"; protein_version "1";
    XI      ensembl CDS     86228   88786   .       -       0       gene_id "YKL188C"; gene_version "1"; transcript_id "YKL188C"; transcript_version "1"; exon_number "1"; gene_name "PXA2"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "PXA2"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YKL188C"; protein_version "1";
    XI      ensembl CDS     89287   91536   .       -       0       gene_id "YKL187C"; gene_version "1"; transcript_id "YKL187C"; transcript_version "1"; exon_number "1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "YKL187C"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YKL187C"; protein_version "1";
    XI      ensembl CDS     92747   93298   .       -       0       gene_id "YKL186C"; gene_version "1"; transcript_id "YKL186C"; transcript_version "1"; exon_number "1"; gene_name "MTR2"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "MTR2"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YKL186C"; protein_version "1";
    XI      ensembl CDS     94499   96262   .       +       0       gene_id "YKL185W"; gene_version "1"; transcript_id "YKL185W"; transcript_version "1"; exon_number "1"; gene_name "ASH1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "ASH1"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YKL185W"; protein_version "1";
    XI      ensembl CDS     96757   98154   .       +       0       gene_id "YKL184W"; gene_version "1"; transcript_id "YKL184W"; transcript_version "1"; exon_number "1"; gene_name "SPE1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "SPE1"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YKL184W"; protein_version "1";
    XI      ensembl CDS     98398   98607   .       -       0       gene_id "YKL183C-A"; gene_version "1"; transcript_id "YKL183C-A"; transcript_version "1"; exon_number "1"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "YKL183C-A"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YKL183C-A"; protein_version "1";
    XI      ensembl CDS     98721   99638   .       +       0       gene_id "YKL183W"; gene_version "1"; transcript_id "YKL183W"; transcript_version "1"; exon_number "1"; gene_name "LOT5"; gene_source "ensembl"; gene_biotype "protein_coding"; transcript_name "LOT5"; transcript_source "ensembl"; transcript_biotype "protein_coding"; protein_id "YKL183W"; protein_version "1";
### 2. 
命令

    grep -v '^#' 1.gtf |awk '$1 =="IV" {print $2,$3}' | sort | uniq -c | sort -k 1
输出：

    853 ensembl start_codon
    853 ensembl stop_codon
    886 ensembl gene
    886 ensembl transcript
    895 ensembl CDS
    933 ensembl exon
### 3. 
命令

    awk '$3 =="CDS" && $1 !="IV" && $7 =="-"{print $5-$4+1}' 1.gtf | sort -k 1 -n | tail -2
输出：

    12276
    14730
### 4. 
命令

    awk '$1 == "XV"{print $5-$4+1,$9}' 1.gtf | sort -k 1 -n | tail -5
输出：

    5391 gene_id
    9237 gene_id
    9240 gene_id
    9240 gene_id
    9240 gene_id
### 5.
思路是排除空白行及开头结尾几行后，对每行提取第n列，如果第n列非空白，则n=n+1，继续提取$n，直至提取$n时提取值为空白，print n-1
每一行如上操作后分别输出n，进行sort，升序排列，取最后一行的数值n即为文件列数
具体如何实现还没有想法
