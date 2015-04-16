# Introduction #
This page contains many work-arounds and tips and tricks.

# NCBIGet and NCBISearch commands #
Sometimes when using the -ef (ncbiget) command you will get an error (mostly due to networking problems). This can be quite annoying with large datasets however there is a solution.

When you do a -es search, the log file contains the gi numbers. If you take those gi numbers and put them in a plain text file -- call it "rbcL\_gi.txt", you can write a simple python script wrapping phyutility to them retrieve the sequences:

### python script get.py ###
```
import os, sys
final = "rbcL_gb.fasta"
handle = open("rbcL_gi.txt", "rU")
for line in handle:
	line = line.strip()
	cmd = "/Users/smitty/bin/phyutility -ef -term "+line+" -ll 3000 -log log.txt -out out.fasta"
	print cmd
	os.system(cmd)
	cmd= "cat out.fasta "+final+" > temp.fasta"
	os.system(cmd)
	cmd="mv temp.fasta "+final
	os.system(cmd)
```

The code is run simply by typing python get.py in the terminal.

Obviously change the files in the script to reflect yours and the location of phyutility to reflect yours. This assumes you can run "cat" which is a unix command (so linux and mac users need not worry, windows users will probably need to check or maybe install cygwin),