# File types
this one had so many compression methods piled  on each other,
it wasnt hard,but it is tedious work.
```
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
Flag.pdf  flag.sh
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ sh ./Flag.pdf                 
x - created lock directory _sh00046.
x - extracting flag (text)
./Flag.pdf: 119: uudecode: not found
restore of flag failed
flag: MD5 check failed
x - removed lock directory _sh00046.
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ sh Flag.pdf  
x - created lock directory _sh00046.
x - extracting flag (text)
Flag.pdf: 119: uudecode: not found
restore of flag failed
flag: MD5 check failed
x - removed lock directory _sh00046.
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ sh flag.sh  
x - created lock directory _sh00046.
x - extracting flag (text)
flag.sh: 119: uudecode: not found
restore of flag failed
flag: MD5 check failed
x - removed lock directory _sh00046.
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ sudo rm sharutils             
rm: cannot remove 'sharutils': No such file or directory
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ sudo apt-get update           
Get:1 http://packages.microsoft.com/repos/code stable InRelease [10.4 kB]
Hit:2 https://dl.winehq.org/wine-builds/debian bookworm InRelease                                            
Get:3 https://brave-browser-apt-release.s3.brave.com stable InRelease [7,547 B]                              
Get:5 https://dl.google.com/linux/chrome/deb stable InRelease [1,811 B]                                      
Get:6 https://packages.microsoft.com/repos/ms-teams stable InRelease [17.5 kB]                      
Get:4 http://kali.download/kali kali-rolling InRelease [30.6 kB]
Get:7 http://packages.microsoft.com/repos/code stable/main armhf Packages [135 kB]
Get:8 http://packages.microsoft.com/repos/code stable/main arm64 Packages [135 kB]
Get:9 http://packages.microsoft.com/repos/code stable/main amd64 Packages [134 kB]
Get:10 http://packages.microsoft.com/repos/code stable/main armhf Contents (deb) [56.2 kB]
Get:11 https://brave-browser-apt-release.s3.brave.com stable/main amd64 Packages [4,085 B]
Get:12 http://packages.microsoft.com/repos/code stable/main amd64 Contents (deb) [56.2 kB]
Get:13 https://dl.google.com/linux/chrome/deb stable/main amd64 Packages [1,075 B]            
Get:14 http://packages.microsoft.com/repos/code stable/main arm64 Contents (deb) [56.2 kB]    
Get:15 http://kali.download/kali kali-rolling/non-free Sources [132 kB]                        
Get:16 http://kali.download/kali kali-rolling/main Sources [15.7 MB]                                    
Get:17 http://kali.download/kali kali-rolling/contrib Sources [77.9 kB]                                      
Get:18 http://kali.download/kali kali-rolling/main amd64 Packages [19.5 MB]                                  
Get:19 http://kali.download/kali kali-rolling/main i386 Packages [19.2 MB]                                   
Get:20 http://kali.download/kali kali-rolling/main amd64 Contents (deb) [45.4 MB]                            
Get:21 http://kali.download/kali kali-rolling/main i386 Contents (deb) [43.8 MB]                             
Get:22 http://kali.download/kali kali-rolling/contrib i386 Packages [101 kB]                                 
Get:23 http://kali.download/kali kali-rolling/contrib amd64 Packages [116 kB]                                
Get:24 http://kali.download/kali kali-rolling/contrib amd64 Contents (deb) [172 kB]                          
Get:25 http://kali.download/kali kali-rolling/contrib i386 Contents (deb) [142 kB]                           
Get:26 http://kali.download/kali kali-rolling/non-free i386 Packages [179 kB]                                
Get:27 http://kali.download/kali kali-rolling/non-free amd64 Packages [222 kB]                               
Get:28 http://kali.download/kali kali-rolling/non-free amd64 Contents (deb) [931 kB]                         
Get:29 http://kali.download/kali kali-rolling/non-free i386 Contents (deb) [884 kB]                          
Fetched 147 MB in 2min 28s (993 kB/s)                                                                        
Traceback (most recent call last):
  File "/usr/lib/cnf-update-db", line 27, in <module>
    col.create(db)
  File "/usr/share/command-not-found/CommandNotFound/db/creator.py", line 95, in create
    self._fill_commands(con)
  File "/usr/share/command-not-found/CommandNotFound/db/creator.py", line 143, in _fill_commands
    self._parse_single_contents_file(con, f, fp.stdout)
  File "/usr/share/command-not-found/CommandNotFound/db/creator.py", line 282, in _parse_single_contents_file
    priority = component_priorities[component]
KeyError: 'non-free-firmware'
Reading package lists... Done
E: Problem executing scripts APT::Update::Post-Invoke-Success 'if /usr/bin/test -w /var/lib/command-not-found/ -a -e /usr/lib/cnf-update-db; then /usr/lib/cnf-update-db > /dev/null; fi'
E: Sub-process returned an error code
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ sudo apt install sharutils --fix-missing
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libatk1.0-data linux-image-5.18.0-kali5-amd64 python3-ajpy python3-pysmi python3-pysnmp4
Use 'sudo apt autoremove' to remove them.
Suggested packages:
  bsd-mailx | mailx sharutils-doc
The following NEW packages will be installed:
  sharutils
0 upgraded, 1 newly installed, 0 to remove and 1133 not upgraded.
Need to get 262 kB of archives.
After this operation, 1,449 kB of additional disk space will be used.
Get:1 http://kali.download/kali kali-rolling/main amd64 sharutils amd64 1:4.15.2-9 [262 kB]
Fetched 262 kB in 2s (114 kB/s)                  
Selecting previously unselected package sharutils.
(Reading database ... 439480 files and directories currently installed.)
Preparing to unpack .../sharutils_1%3a4.15.2-9_amd64.deb ...
Unpacking sharutils (1:4.15.2-9) ...
Setting up sharutils (1:4.15.2-9) ...
Processing triggers for man-db (2.11.1-1) ...
Processing triggers for kali-menu (2022.4.1) ...
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ sh flag.sh                              
x - created lock directory _sh00046.
x - extracting flag (text)
x - removed lock directory _sh00046.
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
flag  Flag.pdf  flag.sh
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag    
flag: current ar archive
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cat falg    
cat: falg: No such file or directory
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cat flag    
!<arch>
flag/           0           0     0     644     1024      `
�i����h����ѣ ѣ##'���SG�z�Ѩrш@4�@hb0�C@1F��kϹ=�_@{O}�������ѦM4�M
��"����<M�)h�V��τH�I��W��8�"'f0�D!��xr�_f�Th�4ª~���ѣM�b@4h�#G���@�@S& 

�1�'�ÅO{�51]�<�T������[�s�-��!Υ��A29��'�͛$:e�P/9����>�}p�Kb&q['
Z3������##Ŏ.�p�!�,��q       EX?AX%�-�Ó�.x�<���G.���%i�"+���vCBx�`I�X�!�v�ۮn�")��4�̏��$>#���B�y���
                     TRAILER!!!                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ sudo apt install subl                   
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package subl
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ man ar              
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ man ar| grep extract
       ar - create, modify, and extract from archives
       The GNU ar program creates, modifies, and extracts from archives.  An archive is a single file
       archive, and can be restored on extraction.
           operation, to request that ar list each name as it extracts it.
           If you do not specify a member, all files in the archive are extracted.
           Files cannot be extracted from a thin archive, and there are restrictions on extracting from
       o   Preserve the original dates of members when extracting them.  If you do not specify this
           modifier, files extracted from the archive are stamped with the time of extraction.
           should be extracted.  If this option is not specified then the current directory will be used.
           Note - although the presence of this option does imply a x extraction operation that option must
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ar xv flag              
x - flag
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
flag  Flag.pdf  flag.sh
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
\flag: cpio archive
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ \man cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cpio flag -i         
cpio: You must specify one of -oipt options.
Try 'cpio --help' or 'cpio --usage' for more information.
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cpio flag --extract
cpio: You must specify one of -oipt options.
Try 'cpio --help' or 'cpio --usage' for more information.
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cpio --file flag --extract
cpio: flag not created: newer or same age version exists
2 blocks
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag flag.cpio   
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cpio --file flag.cpio --extract
2 blocks
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
flag: bzip2 compressed data, block size = 900k
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ bzip2 flag -d               
bzip2: Can't guess original name for flag -- using flag.out
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag flag.bz2 
mv: cannot stat 'flag': No such file or directory
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
flag.cpio  flag.out  Flag.pdf  flag.sh
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag.out flag.bz2
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ bzip2 flag.bz2 -d   
bzip2: flag.bz2 is not a bzip2 file.
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ rm Flag.pdf     
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ rm flag.sh 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
flag.bz2  flag.cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ rm flag.bz2
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cpio --file flag.cpio --extract
2 blocks
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
flag  flag.cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag flag.bz2    
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ bzip2 flag.bz2 -d           
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
flag  flag.cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag\
> 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag 
flag: gzip compressed data, was "flag", last modified: Tue Mar 15 06:50:36 2022, from Unix, original size modulo 2^32 329
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag flag.gz 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ gzip flag.gz -d                                
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
flag: lzip compressed data, version: 1
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ man lzip            
No manual entry for lzip
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ man lzip
No manual entry for lzip
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ sudo apt install lzip
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libatk1.0-data linux-image-5.18.0-kali5-amd64 python3-ajpy python3-pysmi python3-pysnmp4
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  lzip
0 upgraded, 1 newly installed, 0 to remove and 1133 not upgraded.
Need to get 85.9 kB of archives.
After this operation, 175 kB of additional disk space will be used.
Get:1 http://kali.download/kali kali-rolling/main amd64 lzip amd64 1.23-5 [85.9 kB]
Fetched 85.9 kB in 1s (79.5 kB/s)
Selecting previously unselected package lzip.
(Reading database ... 439526 files and directories currently installed.)
Preparing to unpack .../archives/lzip_1.23-5_amd64.deb ...
Unpacking lzip (1.23-5) ...
Setting up lzip (1.23-5) ...
update-alternatives: using /usr/bin/lzip.lzip to provide /usr/bin/lzip (lzip) in auto mode
update-alternatives: using /usr/bin/lzip.lzip to provide /usr/bin/lzip-compressor (lzip-compressor) in auto mo
de
update-alternatives: using /usr/bin/lzip.lzip to provide /usr/bin/lzip-decompressor (lzip-decompressor) in aut
o mode
Processing triggers for man-db (2.11.1-1) ...
Processing triggers for kali-menu (2022.4.1) ...
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag flag.lz
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lzip flag.lz -d\
> 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lzip flag.lz -d 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls             
flag  flag.cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
flag: LZ4 compressed data (v1.4+)
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ man lz         
No manual entry for lz
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lz4             
^CFatal Python error: init_import_site: Failed to import the site module
Python runtime state: initialized
Traceback (most recent call last):
  File "/usr/lib/python3.10/site.py", line 636, in <module>
    main()
  File "/usr/lib/python3.10/site.py", line 623, in main
    known_paths = addsitepackages(known_paths)
  File "/usr/lib/python3.10/site.py", line 406, in addsitepackages
    addsitedir(sitedir, known_paths)
  File "/usr/lib/python3.10/site.py", line 232, in addsitedir
    addpackage(sitedir, name, known_paths)
  File "/usr/lib/python3.10/site.py", line 181, in addpackage
    f = io.TextIOWrapper(io.open_code(fullname), encoding="locale")
KeyboardInterrupt

                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ sudo apt install lz4 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libatk1.0-data linux-image-5.18.0-kali5-amd64 python3-ajpy python3-pysmi python3-pysnmp4
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  lz4
0 upgraded, 1 newly installed, 0 to remove and 1133 not upgraded.
Need to get 92.7 kB of archives.
After this operation, 248 kB of additional disk space will be used.
Get:1 http://kali.download/kali kali-rolling/main amd64 lz4 amd64 1.9.4-1 [92.7 kB]
Fetched 92.7 kB in 1s (62.0 kB/s)
Selecting previously unselected package lz4.
(Reading database ... 439536 files and directories currently installed.)
Preparing to unpack .../archives/lz4_1.9.4-1_amd64.deb ...
Unpacking lz4 (1.9.4-1) ...
Setting up lz4 (1.9.4-1) ...
Processing triggers for man-db (2.11.1-1) ...
Processing triggers for kali-menu (2022.4.1) ...
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lz4 flag -d         
Cannot determine an output filename 
Incorrect parameters
Usage : 
      lz4 [arg] [input] [output] 

input   : a filename 
          with no FILE, or when FILE is - or stdin, read standard input
Arguments : 
 -1     : Fast compression (default) 
 -9     : High compression 
 -d     : decompression (default for .lz4 extension)
 -z     : force compression 
 -D FILE: use FILE as dictionary 
 -f     : overwrite output without prompting 
 -k     : preserve source files(s)  (default) 
--rm    : remove source file(s) after successful de/compression 
 -h/-H  : display help/long help and exit 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lz4 flag -d
Cannot determine an output filename 
Incorrect parameters
Usage : 
      lz4 [arg] [input] [output] 

input   : a filename 
          with no FILE, or when FILE is - or stdin, read standard input
Arguments : 
 -1     : Fast compression (default) 
 -9     : High compression 
 -d     : decompression (default for .lz4 extension)
 -z     : force compression 
 -D FILE: use FILE as dictionary 
 -f     : overwrite output without prompting 
 -k     : preserve source files(s)  (default) 
--rm    : remove source file(s) after successful de/compression 
 -h/-H  : display help/long help and exit 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lz4 -d flag 
Cannot determine an output filename 
Incorrect parameters
Usage : 
      lz4 [arg] [input] [output] 

input   : a filename 
          with no FILE, or when FILE is - or stdin, read standard input
Arguments : 
 -1     : Fast compression (default) 
 -9     : High compression 
 -d     : decompression (default for .lz4 extension)
 -z     : force compression 
 -D FILE: use FILE as dictionary 
 -f     : overwrite output without prompting 
 -k     : preserve source files(s)  (default) 
--rm    : remove source file(s) after successful de/compression 
 -h/-H  : display help/long help and exit 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lz4 -d flag flag
flag already exists; do you want to overwrite (y/N) ? y
flag                 : decoded 0 bytes                                         
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
flag: empty
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls              
flag  flag.cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
flag: empty
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cpio --file flag.cpio --extract
cpio: flag not created: newer or same age version exists
2 blocks
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
flag  flag.cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
flag: empty
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ rm file    
rm: cannot remove 'file': No such file or directory
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ rm flag    
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cpio --file flag.cpio --extract
2 blocks
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
flag  flag.cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
flag: bzip2 compressed data, block size = 900k
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag flag.bz2 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ bzip2 flag.bz2 -d
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
flag  flag.cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag           
flag: gzip compressed data, was "flag", last modified: Tue Mar 15 06:50:36 2022, from Unix, original size modulo 2^32 329
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag flag.gz 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ gzip flag.gz -d
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls
flag  flag.cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
flag: lzip compressed data, version: 1
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lzip flag.gz -d 
lzip: flag.gz: Can't open input file: No such file or directory
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls             
flag  flag.cpio
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lzip flag -d   
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls          
flag.cpio  flag.out
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag.out 
flag.out: LZ4 compressed data (v1.4+)
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lz4 -d flag.out flag
flag.out             : decoded 266 bytes                                       
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag    
flag: LZMA compressed data, non-streamed, size 255
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lzma flag -d        
lzma: flag: Filename has an unknown suffix, skipping
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag           
flag: LZMA compressed data, non-streamed, size 255
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ unlzma flag 
unlzma: flag: Filename has an unknown suffix, skipping
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag flag.lzma
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ unlzma flag.lzma 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
flag: lzop compressed data - version 1.040, LZO1X-1, os: Unix
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lzop        
Command 'lzop' not found, but can be installed with:
sudo apt install lzop
Do you want to install it? (N/y)y
sudo apt install lzop
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following packages were automatically installed and are no longer required:
  libatk1.0-data linux-image-5.18.0-kali5-amd64 python3-ajpy python3-pysmi python3-pysnmp4
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  lzop
0 upgraded, 1 newly installed, 0 to remove and 1133 not upgraded.
Need to get 84.2 kB of archives.
After this operation, 168 kB of additional disk space will be used.
Get:1 http://kali.download/kali kali-rolling/main amd64 lzop amd64 1.04-2 [84.2 kB]
Fetched 84.2 kB in 1s (86.8 kB/s)
Selecting previously unselected package lzop.
(Reading database ... 439547 files and directories currently installed.)
Preparing to unpack .../archives/lzop_1.04-2_amd64.deb ...
Unpacking lzop (1.04-2) ...
Setting up lzop (1.04-2) ...
Processing triggers for man-db (2.11.1-1) ...
Processing triggers for kali-menu (2022.4.1) ...
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lzop flag -d
lzop: flag: unknown suffix -- ignored
skipping flag [flag.raw]
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag flag.lzop
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lzop flag.lzop -d
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls               
flag  flag.cpio  flag.lzop  flag.out
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag
flag: lzip compressed data, version: 1
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag.out
flag.out: LZ4 compressed data (v1.4+)
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lzip flag -d     
lzip: Output file 'flag.out' already exists, skipping.
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ rm flag.out
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ lzip flag -d
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls flag.out 
flag.out
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag.out
flag.out: XZ compressed data, checksum CRC64
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ unxz flag.out   
unxz: flag.out: Filename has an unknown suffix, skipping
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ mv flag.out flag.xz 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ unxz flag.xz 
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ ls         
flag  flag.cpio  flag.lzop
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ file flag    
flag: ASCII text
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cat flag                       
7069636f4354467b66316c656e406d335f6d406e3170756c407431306e5f
6630725f3062326375723137795f33633739633562617d0a
                                                                                                              
┌──(avanish㉿avanish)-[~/Documents/forensics]
└─$ cat flag |xxd -r -p
picoCTF{f1len@m3_m@n1pul@t10n_f0r_0b2cur17y_3c79c5ba}

 
```
