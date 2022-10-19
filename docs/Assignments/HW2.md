# Homework 2

Homework can be submitted via the github link which will create a repository for you with basic template of files you can edit to solve the homework. See the the table for homework submission links which will help you create a github repository in the class team.

[https://piazza.com/ucr/fall2022/gen220/resources](https://piazza.com/ucr/fall2022/gen220/resources)

1. Submit the homework by creating a repository through github classroom [Homework 2](https://classroom.github.com/a/xqKvPWCc)
2. Write a shell script called `count_fires.sh` which does all of the following.
   * Download a comma delimited datasets from https://data.cnra.ca.gov/  which are listing of fires in several decades larger than 5000+. search for "Recent Large Fire Perimiters" in the search box. Click on the dataset it should take you to [this page](https://data.cnra.ca.gov/dataset/recent-large-fire-perimeters-5000-acres). Download the [CSV file](https://gis.data.cnra.ca.gov/datasets/CALFIRE-Forestry::recent-large-fire-perimeters-5000-acres.csv). (hint use `curl`).
   * Print out the range of years that occur in this file (hint cut out the column you want, sort and get either the smallest or largest number)
     * you'll notice there are 2 weird numbers in there "48088" and "6901" - can you tell why? You will need to go into the file and correct something (this is reminder that data are not always clean!) to avoid this problem.
   * Print out the number of fires in the database
     * (hint use `wc`, remove the header or subtract out the rows )
   * Print out the number of fires that occur each year
     * (hint use `cut`, `sort` and `uniq -c`)
   * Print out the name and year of largest fire
     * (hint use `sort`) - use the `GIS_ACRES` column - name is in the column FIRE_NAME
   * Print out the total acreage burned in each year.
     * _hint_ you can simply the file by using cut
     `cut -d, -f2,13 ...` to get the columns you need
     * awk to accumulate `awk -F',' '{sum+=$2;} END{print sum;}'`
     * Can you [filter out](https://www.tim-dennis.com/data/tech/2016/08/09/using-awk-filter-rows.html) just the rows for a given year and add up the numbers for it?
