# Assign3
## Spring 2018

The purpose of this exercise is to get comfortable creating scripts using vim on a server, while teaching you the remainder of bash scripting you'll need as a foundation for this course. The scripts themselves are not particularly exciting but they are the building blocks you'll need.  You will be asked to create 11 scripts, which all come from http://dtg.usc.edu/tgrn510/index.php/bash-scripting/.  These are to all be placed in your "bin" directory. The results of running these should be put into a forked version of this github. 

The final question is considerably more difficult and requires you to put concepts together you have learned at this point.

 Completion means the scripts work in your home directory and you have put the results in your github where you will replace the placeholder text with the results from running the script. For exampler, you should replace

*REPLACE WITH RESULTS*

with codeblock text using backticks, which show both the program being called in trgn510.pmed.io and the result.  After, it should be:

`
davidcraig@trgn510:~/bin ls | test.sh
TEST.SH
`

### 1
Please create pointless.sh, changing from printing your hostname with $HOSTNAME, to your $USER

` [zhaniyaz@trgn510 bin]$ ./jas_pointless.sh

zhaniyaz
5
6
`


### 2
Please create quotequotes.sh, please add 1 additional lines that prints the process id of the current script using a special variable in a sentence: "The process id for this script is **235**"

` [zhaniyaz@trgn510 bin]$ ./jas_quotequotes.sh
trgn510.pmed.io
VARIABLE
I am on trgn510.pmed.io
I am on $HOSTNAME
I am on $HOSTNAME
The process id for this script is 2136
`

### 3
Please create processes.sh.  Modify it such that it prints the top 5 CPU consuming processes

`[zhaniyaz@trgn510 bin]$ ./jas_processes.py
UID PID PPID C STIME TTY TIME CMD root 1 0 0 Jan19 ? 00:02:41 /usr/lib/systemd/systemd --switched-root --system --deserialize 19 root 2 0 0 Jan19 ? 00:00:00 [kthreadd] root 3 2 0 Jan19 ? 00:00:00 [ksoftirqd/0] root 5 2 0 Jan19 ? 00:00:00 [kworker/0:0H] root 7 2 0 Jan19 ? 00:00:01 [migration/0]`

### 4
Please create makeupper.sh.  Modify it to return lower case results, and change the name to makelower.sh

`[zhaniyaz@trgn510 bin]$ mv jas_makeupper.sh jas_makelower.sh`

`[zhaniyaz@trgn510 bin]$ ./jas_processes.py | ./jas_makelower.sh
uid pid ppid c stime tty time cmd root 1 0 0 jan19 ? 00:02:48 /usr/lib/systemd/systemd --switched-root --system --deserialize 19 root 2 0 0 jan19 ? 00:00:00 [kthreadd] root 3 2 0 jan19 ? 00:00:00 [ksoftirqd/0] root 5 2 0 jan19 ? 00:00:00 [kworker/0:0h] root 7 2 0 jan19 ? 00:00:01 [migration/0] 
`

### 5
Referring to math.sh, create a script called add.sh that takes two inputs and adds them, **add.sh 5 3** would print 8

`
[zhaniyaz@trgn510 bin]$ ./add.sh 9 9
18
`

### 6
Create a program "mb_or_kb.sh", referring to bigornot.sh and useful.sh, create a script called big file that checks to see if the file exists provided as the first argument exists, and if it exists then gets the filesize, storing it as a variable. I have not provided you with a way to get filesize in exercise, and expect you to search web for a way.  The program then checks to see if the size is greater than 1,000,000.  If its less then 1,000,000, it prints the number of kilobytes (divide by 1000) followed by "kB".  If its greater than 1,000,000, then print the number of megabytes followed by "MB".

*REPLACE WITH RESULTS for mb_or_kb.sh ~/.bashrc*

### 7
Create a program "count_by_to.sh", referring to count.sh.  The file should take two arguments, and should count jumping by the first argument until the second argument is reached, starting at 0.  For example, *count.sh 2 10* would print 0 2 4 6 8 10

`
[zhaniyaz@trgn510 bin]$ ./count_by_to.sh 2 10
0  2  4  6  8  10
All done
`

### 9
Please create whatgene.sh.  Please edit such that the function print_gene, prints upper case of the input.

`
[zhaniyaz@trgn510 bin]$ whatgene.sh 
PTEN 
J 
`

### 10
Please create a bash shell called "genotype.sh" that takes a VCF as argument 1, and prints space delimited chromosome, position, reference, alternative, and genotype for all genotypes in VCF.

`
[zhaniyaz@trgn510 bin]$ genotype.sh ~/projects/assign2/HG001_GRCh37_GIAB_highconf_CG-IllFB-IllGATKHC-Ion-10X-SOLID_CHROM1-X_v.3.3.2_highconf_PGandRTGphasetransfer.vcf | head
1	239339	A	G	0/1:0:0,0:0,0:99:0/1:.:.
1	239482	G	T	0/1:403:92,104:0,0:198:0/1:.:.
1	240147	C	T	0/1:291:55,90:0,0:198:0/1:.:.
1	240898	T	G	0/1:343:82,77:0,0:198:0/1:.:.
1	567239	CG	C	1|1:534:0,214:38,252:241:1/1:.:PATMAT
1	568745	C	CCA	0/1:817:255,152:255,152:198:0/1:.:.
1	837214	G	C	0|1:558:122,138:135,166:581:0/1:.:PATMAT
1	838153	CA	C	1|1:404:0,197:0,197:99:1/1:.:PATMAT
1	842825	A	G	1|1:463:0,209:31,240:279:1/1:.:PATMAT
1	845283	G	T	1|1:482:58,269:0,211:353:1/1:.:PATMAT
`
