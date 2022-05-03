# CPGME Genome Analysis Workshop

### May 4, 2022

*Egon A. Ozer, MD PhD (<e-ozer@northwestern.edu>)*  

# Microbial Sequence Assembly & Alignment
---

# Section 2 - Basic command line usage

This section is to introduce you to basic operations in the command line. These commands may or may not be specific to Mac and Linux operating environments. To use a Linux environment in Windows, follow these instructions to install Windows Subsystem for Linux (WSL): <https://docs.microsoft.com/en-us/windows/wsl/install> 

## Section 2.1 `ls`

The `ls` command is used to list the contents of a directory. If you use the `ls -l` command, you'll get a lot more information about the contents such as whether an item is a file or directory and how big the file is, etc.


## Section 2.2 `cd`

The `cd` command is used to change directories. 

* If you type `cd <directory name>` you'll move into that directory
* You can use `cd ..` (two periods) to move back up one directory
* You can move down multiple directories by listing the path you'd like to take. For example:`cd directory1/directory2/directory3` 
* Most terminal programs will allow you to drag a file or folder into the terminal. So if you'd like to cd into a folder in your Finder window, for example, you can type `cd ` (followed by a space) in your terminal, then use your mouse to drag the folder into the Terminal window and hit Enter. 

## Section 2.3 `pwd`

The `pwd` command will tell you your present working directory. Helps keep you from getting lost sometimes.  

## Section 2.4 `mkdir`

The `mkdir` command will create a new directory. For example, if you want to create a directory called "output" in your current directory, just type `mkdir output`

## Section 2.5 `cat`

The `cat` command is short for "concatenate", but it's mostly used for displaying a text-based file to your terminal window. Careful, this command dumps the entire contents of the file to your Terminal so if it's a large file (like a genome sequence file, for example), it could take a while to print everything. Unless the file you are looking at is very short, you may be better off using `less` (described below).

## Section 2.6 `less`

The `less` command allows you to look at the contents of a file in your Terminal without printing the whole thing at once.

* You can either use `less` and the name of the file (i.e. `less genome.fasta`) or you can pipe the output of another command to `less` using the **pipe character** "|" to explore it in a controlled way (i.e. `cat genome.fasta | less`)
* Use the **arrow keys** to scroll up or down one line at a time or use the **space bar** to scroll down several lines at a time 
* To exit the `less` screen, hit the `q` key (without shift)

## Section 2.7 Redirection, or `>`

If you want to direct the output of a command that usually prints to the screen to a file instead, just use the redirect character `>` at the end of the command and type a file name to direct the file to.

* Example: `cat genome.fasta > new_file.fasta`
* **WARNING**: If you redirect to an existing file, it will be overwritten by the new file. The overwritten data will not be able to be recovered. 

## Section 2.8 `gzip`

Gzip compression software is not necessarily a standard program, but is so widely distributed that it's more likely than not that it is part of your distribution. It comes standard on Mac and almost all flavors of Linux. Gzip is used to compress files to save space and decompress them when needed.

* Gzipped files usually end with the `.gz` suffix
* Sequence read files are almost always gzipped and it's best to leave them this way. Most software that uses sequencing reads can automatically decompress them as needed.
* To gzip file, just use the command `gzip <file>` The output file will be named the same as the input file, but with a `.gz` suffix
* To take a quick peek at a gzipped file, you can string a few commands together. For a read file named "reads_1.fastq.gz" you use this command: `gzip -cd reads_1.fastq.gz | less`. The `-cd` setting is actually two settings together, `-d` to decompress (rather than the default compress) and `-c` tells the program to output the decompressed file to the Terminal. You can then pipe that output to `less` 

There are lots more commands we don't have time to go through at this point (like the necessary, but potentially very dangerous `rm` command), but the more you work in this space, the more you'll pick these commands up.

---

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.