# 092812 #
Added amino acids to the concatenation. This corrects a bug where previously phyutility would concatenate amino acid datasets without complaining but would convert to DNA (making symbols ambiguous that are only found in amino acids). Now phyutility will concatenate amino acids correctly when the -aa option is added. This would mean that it would work like phyutility -concat -aa -in infile1 infile2 infile3 -out outfile
# 070912 #
Added amino acids to the cleaning with a -aa option. So works like
phyutility -clean 0.1 -aa -in infile -out outfile
Other amino acid options will be added in the new future.
# 012912 #
BACK! After a bit of a hiatus on other code projects, I am back to editing and adding features to phyutility. Please stay tuned for more updates.
# 070409 #
Uploaded new .jar file for phyutility. Please download this and replace your existing phyutility.jar file (of course, if yours is named Phyutility.jar, change the name of the new file to reflect that). If you haven't downloaded phyutility package before, please download both and replace the .jar in the folder with the new one. More features soon!
# 022808 #
We now have a publication that can be cited when using phyutility: Smith, S. A. and Dunn, C. W. (2008) Phyutility: a phyloinformatics tool for trees, alignments, and molecular data. Bioinformatics. 24: 715-716. The paper can be found [here](http://bioinformatics.oxfordjournals.org/cgi/content/abstract/24/5/715).

# 112007 #
Release 2.2 has been uploaded with many bug fixes.

# 111307 #
SVN has been updated with source code. Instructions will appear in the WIKI for downloading and using with Eclipse.

# 101607 #

Sources for the new release have been posted. I will have updates to the sources in the SVN repository soon enough, but until then the source package has everything.

# 100907 #

A new release which includes database functionality has been uploaded (2.1). Please report problems in the Issues section. Also, info will be added in the Wiki to accompany the manual (HOWTOs).

# 081607 #

An alpha download has been posted in the downloads section. **Use with great caution.** Also be sure to post any issues in the issues section.

# 081607 #

A second alpha download has been posted in the downloads section. **Use with great caution.** Also be sure to post any issues in the issues section. This second alpha includes NCBI functions, including searching and fetching from nucleotide databases.