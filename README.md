# !IAPlus
SPSS Macro code for Item Analysis

About !IAPlus

!IAPlus is an SPSS macro that has the functionality of processing test or questionnaire response data and compute a variety of classical test theory statistics. It should be used primarily to evaluate the quality of the response data. As such, SPSS is required to execute the instructions generated by !IAPlus, and !IAPlus is called from, and run from within an SPSS syntax window.

In addition to using SPSS, !IAPlus has the option of calculating IRT related statistics. It calculates IRT statistics using the TAM package in R. When using TAM, !IAPlus provides the option to use marginal maximum likelihood estimation for the Rasch, 2 parameter logistic model, or the generalized partial credit model.
Summary item statistics are calculated and presented overall, or by groups specified by the user. When IRT is used, the Equated P+ statistic is computed for each group.

Requirements

!IAPlus requires a working copy of SPSS installed in the computer where the analysis is conducted. If the optional IRT statistics are requested, the R programming language also needs to be installed in the computer. Within R, it requires the TAM package. !IAPlus installs the TAM package when needed.
In addition to the macro, a working version of SPSS, and R (optional), !IAPlus requires an SPSS system file with response data to a survey or a test. The responses must be stored in numeric format. Responses stored as SPSS system missing values (SYSMIS) will be treated as not administered and will be excluded from the analysis. Using numeric values, the responses can be coded as valid responses, or as one of several missing type response possibilities. As such, the macro allows for differential treatment of omitted, not reached, not administered or other missing type responses. 

For the calculation of classical test theory statistics, values for the responses do not need to be sequential and can be one or more digits. But for the calculation of IRT based statistics, scored responses need to be sequential, and starting at 1 or 0. When responses start at 1, the program provides the option to down-code the response data. More details are presented later in this manual in the parameter section. 

In addition to the response data, !IAPlus can accept one or more ID variables for each response record, and one or more grouping variables used for the analysis. There are two types of grouping variables, classification variables (CLASSVARS) and group comparison variables (BYVARS). These are explained later in the syntax reference section, but when these are specified, the analysis is carried out for each of the groups defined by the grouping variables. Unlike the response data, which must be numeric, the grouping and ID variables can be string, numeric or a combination.  There is no restriction of the number of digits, and the categories for the grouping variables do not need to be sequential.
