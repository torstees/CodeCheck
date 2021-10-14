# CodeCheck
This is a small code exercise intended to allow us some insight into your ability to address a coding task. 
We are interested in seeing a clearly documented method as well as be able to view or run the final results.

## Environment Expectations
Before we get to the challenge itself, we have a few high-level expectations we require out of any response.

### 1. Programming Language
You are free to use whatever language you wish. 

### 2. Executing code / demonstrating work
Given the importance of being able to see your work, the solution provided should include both the code and
a reproducible way for us to view the results. This might be anything from a docker compose file to an
R Shiny application. 

### 3.  Code Style / Format Standards
While we do not have a specific code format / style standard we wish for you to adhere to, you are require to adhere
to _some_ standard.  This must be clearly described in your final pull request.

The _only_ exception to the above is if the language you are either requested to use or chose to use provides a
formatter as a 1st class citizen of the language, e.g. [Golang](https://golang.org/)'s 
[gofmt](https://golang.org/cmd/gofmt/) tool.  In these situations, you _must_ use the language's provided formatter.

## The Challenge
The high level objective is to provide a "Variable report" viewer that shows the information in the included JSON object.

1. The included JSON file contains a series of "Observations" that each have a set of "Components" describing features of a dataset, 
such as the minimum and maximum observed values.
   * The outer container is a [FHIR Bundle](https://www.hl7.org/fhir/bundle.html#resource)
   * This Bundle's "entry" is an array of [FHIR Observations](https://www.hl7.org/fhir/observation.html#resource)
   * The Observation has a "valueCodeableConcet" which names the variable being described.
   * The Observation has an array of "component" which describe the features of that variable, for example the count of individuals with the race indicated.
   * Note that the above FHIR documentation is complex and covers substantially more depth than is necessary here, but is provided for reference.
1. Create a simple application that allows for searching and display of these variables and their attributes.
    * May be a web application or local application
1. Create a `RESPONSE_README.md` file with the following:
    1. Explanation of coding standards used
    1. Explanation of how to run the program
    1. Description of basic workflow of program
    1. Answers to the following questions derived from the data:
        1. How many Observations are present here?
        2. How many individuals have "Phenotype Present" for "Abnormal leukocyte morphology"?
        3. List the five variables with the highest number of total observations.

## Instructions
Please  provide us with a link to a github (or similar) repo that contains your code and documentation.
