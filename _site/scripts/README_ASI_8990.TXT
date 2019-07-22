These scripts have been written to be run on GNU/linux and require awk
and MySQL (which can be on the same computer or on another computer
accessible over network). Both awk and mysql are cross-platform and
with simple modifications to these scripts, it should be possible to
use them on other operating systems.

These scripts read unit-level data from the 1989-90 round of ASI Survey,
generate csv files for all the levels, create a mysql database, 
and load the data into it. The csv files are deleted in the end. 
With trivial modification of asi89_90.sh, you can retain the csv files
or skip creation of MySQL database altogether.

The scripts read following data files:

./Data/ASID8990.TXT

To run these scripts, you need to do the following.

1. Put the entire contents of the CD containing ASI 1989-90 data 
in a directory. Please put the original data file in a sub-directory
called "Data". If the data file is named differently, either rename 
the data file or modify the script. If the data file is compressed
using some compression utility (zip or rar), uncompress it.

2. Uncompress the script files. Uncompressing the script files will
give a directory called asi8990_scripts. Move this to the directory which has
the contents of the CD.

3. cd to scripts directory from the terminal and give the following
command: ./asi89_90.sh

Please note that the script creates a new database called ASI_89_90.
If there is already a database with this name, it will be deleted. You
have been warned.

The script may take a lot of time to read the data. The actual time
taken will depend on the processing power of the computer on which the
script is run. If you want to interrupt the process in the middle, you
can do that using CTRL-C.
