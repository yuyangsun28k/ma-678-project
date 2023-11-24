# MA-678-project

## Objective

In this project, the goal is to generate an EDA report on a Portuguese banking institution by examining:

-   Any behaviors changes on whether the client has subscribed the term deposit (primary)
-   The distribution of different factors: ages vs. balance
-   Whether a loan affects people's subscription

# Datasets

Data source: <https://archive.ics.uci.edu/dataset/222/bank+marketing>

Literature review: <https://www.sciencedirect.com/science/article/pii/S016792361400061X?via=ihub> <https://www.joiv.org/index.php/joiv/article/view/68/48> <https://www.sciencedirect.com/science/article/pii/S0360835222008622>

# Variables Overview

This document outlines the variables used in the dataset. Each variable is described with its type, description, and additional notes where applicable.

## Variable Descriptions

| Variable      | Type        | Description                                                                                | Additional Notes                                                                                                                                                      |
|---------------|---------------|------------------|------------------------|
| `age`         | Integer     | Age of the client                                                                          | \-                                                                                                                                                                    |
| `job`         | Categorical | Occupation type of the client                                                              | Options: 'admin.', 'blue-collar', 'entrepreneur', 'housemaid', 'management', 'retired', 'self-employed', 'services', 'student', 'technician', 'unemployed', 'unknown' |
| `marital`     | Categorical | Marital status of the client                                                               | Options: 'divorced', 'married', 'single', 'unknown'. Note: 'divorced' means divorced or widowed.                                                                      |
| `education`   | Categorical | Education level of the client                                                              | Options: 'basic.4y', 'basic.6y', 'basic.9y', 'high.school', 'illiterate', 'professional.course', 'university.degree', 'unknown'                                       |
| `default`     | Binary      | Has credit in default?                                                                     | \-                                                                                                                                                                    |
| `balance`     | Euros       | Average yearly balance in euros                                                            | \-                                                                                                                                                                    |
| `housing`     | Binary      | Has housing loan?                                                                          | \-                                                                                                                                                                    |
| `loan`        | Binary      | Has personal loan?                                                                         | \-                                                                                                                                                                    |
| `contact`     | Categorical | Contact communication type                                                                 | Options: 'cellular', 'telephone'. Contains NA                                                                                                                         |
| `day_of_week` | Date        | Last contact day of the week                                                               | \-                                                                                                                                                                    |
| `month`       | Date        | Last contact month of the year                                                             | \-                                                                                                                                                                    |
| `duration`    | Integer     | Last contact duration, in seconds                                                          | This attribute highly affects the output target. Note: should only be included for benchmark purposes.                                                                |
| `campaign`    | Integer     | Number of contacts performed during this campaign and for this client                      | Includes last contact                                                                                                                                                 |
| `pdays`       | Integer     | Number of days that passed by after the client was last contacted from a previous campaign | -1 means the client was not previously contacted. Contains NA                                                                                                         |
| `previous`    | Integer     | Number of contacts performed before this campaign and for this client                      | \-                                                                                                                                                                    |
| `poutcome`    | Categorical | Outcome of the previous marketing campaign                                                 | Options: 'failure', 'nonexistent', 'success'. Contains NA                                                                                                             |
| `y` (Target)  | Binary      | Has the client subscribed to a term deposit?                                               | \-                                                                                                                                                                    |

## Notes

-   The `duration` variable is a critical predictor for the target variable. However, its value is only known after the call is made and should be omitted for a realistic predictive model.
-   Binary variables indicate the presence (`1`) or absence (`0`) of a particular attribute.
-   Categorical variables have specified options and may contain missing values (NA).
