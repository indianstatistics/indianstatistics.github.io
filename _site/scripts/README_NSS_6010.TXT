These scripts have been written to be run on GNU/linux and require awk
and MySQL (which can be on the same computer or on another computer
accessible over network). Both awk and mysql are cross-platform and
with simple modifications to these scripts, it should be possible to
use them on other operating systems.

These scripts read unit-level data from the 60th round of NSS Survey
of Employment and Unemployment, generate csv files for all the levels,
create a mysql database, and load the data into it. The csv files are
deleted in the end. With trivial modification of nss60_10.sh, you can
retain the csv files or skip creation of MySQL database altogether.

The scripts read following data files:

./Data/AHQ1.TXT
./Data/AHQ2.TXT
./Data/AHQ3.TXT
./Data/AHQ4.TXT
./Data/AHQ5.TXT
./Data/AHQ6.TXT
./Data/AHQ7.TXT
./Data/AHQ8.TXT

These correspond to one block each.

To run these scripts, you need to do the following.

1. Put the entire contents of the CD containing NSS 60th Round
Schedule 10 data in a directory. Please put all the original data files 
in a sub-directory called "Data". Please check the data files. 
If they are named differently, either rename the data files or 
modify the script. If data files are compressed using some
compression utility (zip or rar), uncompress them.

2. Uncompress the script files. Uncompressing the script files will
give a directory called scripts. Move this to the directory which has
the contents of the CD.

3. cd to scripts directory from the terminal and give the following
command: ./nss60_10.sh

Please note that the script creates a new database called NSS_60_10.
If there is already a database with this name, it will be deleted. You
have been warned.

Level 03 includes an extra variable 'ID' as an additional primary key, 
since the primary keys specified in the readme file provided for the NSS Data 
did not uniquely identify all the records due to missing Person Serial Numbers 
for 2 households.

The script may take a lot of time to read the data. The actual time
taken will depend on the processing power of the computer on which the
script is run. If you want to interrupt the process in the middle, you
can do that using CTRL-C.



