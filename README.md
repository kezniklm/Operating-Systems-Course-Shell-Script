# Operating Systems Course - Project 1 - Shell Script

## Implementation of Shell script for analyzing records of individuals with confirmed cases of COVID-19 in the Czech Republic
Evaluation: 11/15 points

## Assignment
#### [Assignment link](https://github.com/kezniklm/IOS_project1/blob/master/Assignment.pdf)
## Description
The goal of this task is to create a shell script for analyzing records of individuals with confirmed COVID-19 infection in the Czech Republic. The script will filter the records and provide basic statistics based on user input.

## Script Interface Specification
* NAME
* corona - analyzer for records of individuals with confirmed COVID-19 infection
## USAGE

* corona [-h] [FILTERS] [COMMAND] [LOG [LOG2 [...]]]
    * OPTIONS
        * COMMAND can be one of the following:
            * infected: counts the number of infected individuals.
            * merge: merges multiple record files into one while preserving the original order (header will appear only once).
            * gender: displays the number of infected individuals by gender.
            * age: displays statistics on the number of infected individuals by age (details below).
            * daily: displays statistics on infected individuals for each day.
            * monthly: displays statistics on infected individuals for each month.
            * yearly: displays statistics on infected individuals for each year.
            * countries: displays statistics on infected individuals for each country of infection (excluding CZ, the country code for the Czech Republic).
            * districts: displays statistics on infected individuals for each district.
            * regions: displays statistics on infected individuals for each region.
            * FILTERS can be a combination of the following (each used at most once):

        * -a DATETIME: filters records to include only those after this date (including the date). DATETIME should be in the format YYYY-MM-DD.
        * -b DATETIME: filters records to include only those before this date (including the date).
        * -g GENDER: filters records to include only those of the specified gender. GENDER can be M (male) or F (female).
        * -s [WIDTH]: for the gender, age, daily, monthly, yearly, countries, districts, and regions commands, displays data graphically as histograms instead of numerical values. The optional parameter WIDTH sets the width of the histograms, i.e., the length of the longest row, to WIDTH. WIDTH must be a positive integer. If WIDTH is not provided, the width of the rows follows the requirements specified below.
        * -h: displays the help message with a brief description of each command and option.
