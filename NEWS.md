# did 2.0.1
  * Compute critical value for simultaneous confidence bands even when some standard error is zero (set these to NA)
  
  * Improved codes for unbalanced panel data: faster and more memory efficient
  
  * Correct estimates of P(G=g|Eventually treated) with unbalanced panel data. This affects **aggte** objects with unbalanced panel data
  
  * Bug fixes for summary **aggte** objects
  
  * Allow clustering for unbalanced panel data
  
  * Fixed error in calendar-type aggregation within **aggte** function (point estimates were not being weighted by group-size; now they are).
  
  * Additional error handling
  
  
# did 2.0.0
  * Big improvement on code base / functionality / testing
  
  * Deprecated **mp.spatt** function and replaced it with **att_gt** function

  * Calling **att_gt** is similar to calling **mp.spatt**; instead of formula for outcome of the form `y~treat`, now just pass the name of the outcome variable

  * Deprecated **mp.spatt** function and replaced it with **conditional_did_pretest** function

  * New **est_method** parameter.  Can call any function for 2x2 DID in the **DRDID** package (default is now doubly robust estimation, but inverse probability weights and regression estimators are also supported) as well as provide custom 2x2 DID estimators

  * Bug fixes for including groups that are *already treated* in the first period

  * Allow for user to select control group -- either *never treated* or *not yet treated*

  * Add functionality for uniform confidence bands for all aggregated treatment effect parameters

  * Introduced dynamic effects in pre-treatment periods.  These allow for users to report event study plots that are common that include pre-treatment periods and are common in applied work.  The event study plots in the **did** package are robust to selective treatment timing (unlike standard regression event study plots)

  * Support for using repeated cross sections data instead of panel data is much improved

  * Support for using sampling weights is much improved

  * Big improvement to website, vignettes, and code documentation
  
  * Code for dealing with unbalanced panels
  
  * Allow for event studies to be computed over subsets of event times
  
  * Allow for treatment anticipation via *anticipation* argument
  
# did 1.2.3
  * Corrected check problems

# did 1.2.2

  * Improved ways to summarize aggregated treatment effect parameters

  * Fixed bug related to needing new version of BMisc

  * Fixed bug related to plotting with no pre-treatment periods

  * Improved ways to easily plot aggregated treatment effect parameters
  
# did 1.2.1

  * Added some error handling for some cases with small group sizes, and fixed some cryptic error messages

  * Fixes handling for data being in format besides *data.frame* (e.g. *tibble*)

  * Add warnings about small group sizes which are a very common source of trouble

# did 1.2.0

  * Updates for handling repeated cross sections data, both estimation and inference

# did 1.1.2

  * bug fixes for testing without covariates, allowed to pass NULL in addition to ~1

# did 1.1.1

  * fixed issues between BMisc and formula.tools

  * added point estimates for repeated cross sections data

# did 1.1.0

  * bug fixes for the case without any covariates

# did 1.0.0

  * first version of package, functions for computing group-time average treatment effects, combining them into a smaller number of parameters, and pre-testing the common trends assumption



