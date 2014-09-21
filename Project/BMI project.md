BMI for Adult 
========================================================

### A Project Presentation for Developing Data Product Course 

- author: Linghuan Zeng
- date: 9/20/2014


Contents
========================================================

- What's BMI?

- How to calculate BMI for adult?

- How to interprete BMI result?

BMI and BMI Formula (for Adult) 
========================================================
* *Body Mass Index (BMI)* is a number calculated from a person's weight and height
* Calculation: 
  +  Formular 1 :  Weight (kg) / [Height (meter)]^2   
  or 
  + Formular 2 :  Weight (lb) / [Height (inch)]^2 * 703 

 
BMI (for Adult) Interpretation
========================================================
* BMI can be considered an reliable alternative for direct measures of body fat. 
* BMI is an inexpensive and easy-to-perform method of screening for weight categories that may lead to health problems.  
* Below is the relationship between BMI and Weight Status 

BMI   | Weight Status
------------- | -------------
Below 18.5   |  Underweight
18.5 – 24.9  | Normal
25.0 – 29.9  |	Overweight
30.0 and Above | Obese


R Code and Example (Using Formula 1)
========================================================   

```r
BMI <- function(w,h){round(w / (h)^2,2)}
weightstatus <- function(w, h) { BMI <- round(w / (h)^2,2)
        if ( BMI < 18.50) {wstatus <- 'Underweight'}
        else if ( BMI < 25.00 ) {wstatus <- 'Normal'}
        else if ( BMI < 30.00) {wstatus <- 'Overweight'}
        else {wstatus <- 'Obese'}
        return(wstatus) }
BMI(68,1.65);weightstatus(68, 165) #Example: Weight=68 kg, Height=1.65 m
```

```
[1] 24.98
```

```
[1] "Underweight"
```
