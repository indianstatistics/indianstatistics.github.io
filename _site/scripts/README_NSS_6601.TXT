These scripts have been written to be run on GNU/linux and require awk
and MySQL (which can be on the same computer or on another computer
accessible over network). Both awk and mysql are cross-platform and
with simple modifications to these scripts, it should be possible to
use them on other operating systems.

These scripts read unit-level data from the 66th round of NSS Survey
of Consumer Expenditure Type 1, generate csv files for all the levels,
create a mysql database, and load the data into it. The csv files are
deleted in the end. With trivial modification of nss66_1_1.sh, you can
retain the csv files or skip creation of MySQL database altogether.

The scripts read following data files:

./Data/LVL66S011.01.TXT
./Data/LVL66S011.02.TXT
./Data/LVL66S011.03.TXT
./Data/LVL66S011.04.TXT
./Data/LVL66S011.05.TXT
./Data/LVL66S011.06.TXT
./Data/LVL66S011.07.TXT
./Data/LVL66S011.08.TXT
./Data/LVL66S011.09.TXT
./Data/LVL66S011.10.TXT

These correspond to one level each.

To run these scripts, you need to do the following.

1. Put the entire contents of the CD containing NSS 66th Round
Schedule 1, Type 1 data in a directory. The actual data files are in a
sub-directory called "Data". Leave that as it is. Please check the
data files. If they are named differently, either rename the data
files or modify the script. If data files are compressed using some
compression utility (zip or rar), uncompress them.

2. Uncompress the script files. Uncompressing the script files will
give a directory called nss661_scripts. Move this to the directory which has
the contents of the CD.

3. cd to scripts directory from the terminal and give the following
command: ./nss66_1_1.sh

Please note that the script creates a new database called NSS_66_1_Type1.
If there is already a database with this name, it will be deleted. You
have been warned.

The script may take a lot of time to read the data. The actual time
taken will depend on the processing power of the computer on which the
script is run. If you want to interrupt the process in the middle, you
can do that using CTRL-C.



