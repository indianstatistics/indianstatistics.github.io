These scripts have been written to be run on GNU/linux and require awk
and MySQL (which can be on the same computer or on another computer
accessible over network). Both awk and mysql are cross-platform and
with simple modifications to these scripts, it should be possible to
use them on other operating systems.

These scripts read unit-level data from the 61st round of NSS Survey
of Employment and Unemployment, generate csv files for all the levels,
create a mysql database, and load the data into it. The csv files are
deleted in the end. With trivial modification of nss61_10.sh, you can
retain the csv files or skip creation of MySQL database altogether.

The scripts read following data files:

./Data/ah12.txt
./Data/ah22.txt
./Data/ah32.txt
./Data/ah42.txt
./Data/ah52.txt
./Data/ah62.txt
./Data/ah72.txt
./Data/ah82.txt

These correspond to data for different states.

To run these scripts, you need to do the following.

1. Put the entire contents of the CD containing NSS 61st Round
Schedule 10 data in a directory. Please put all the original data files 
in a sub-directory called "Data". Please check the data files. 
If they are named differently, either rename the data files or 
modify the script. If data files are compressed using some
compression utility (zip or rar), uncompress them.

2. Uncompress the script files. Uncompressing the script files will
give a directory called scripts. Move this to the directory which has
the contents of the CD.

3. cd to scripts directory from the terminal and give the following
command: ./nss61_10.sh

Please note that the script creates a new database called NSS_61_10.
If there is already a database with this name, it will be deleted. You
have been warned.

Levels 08, 09 and 10 include an extra variable 'Autoid' as an 
additional primary key for these levels, since the primary keys specified 
in the readme file provided for the NSS Data did not uniquely identify 
all the records.

The script may take a lot of time to read the data. The actual time
taken will depend on the processing power of the computer on which the
script is run. If you want to interrupt the process in the middle, you
can do that using CTRL-C.



