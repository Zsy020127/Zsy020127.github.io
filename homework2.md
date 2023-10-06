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

    
