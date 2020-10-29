# Medical AI Challenge

# Subject
Aims to develop decision-making AI that selects data-driven optimal treatment.

# Background
The effectiveness of medication depends on the individual patient characteristics. Until now, treatment is based on average effectiveness, but in fact, it is not effective in certain patients or causes fatal side effects.Since medical big data can provide a large amount of information on such treatment results, it is expected that customized treatment according to the characteristics of individual patients will be possible if using this.However, it is very difficult to find the effect of treatment, or causal relationship, using the variables of various patients and biased historical data. This challenge uses past data to differentiate between patients who were suitable for treatment and those who were not, and creates a decision aid AI that can find people whose progress will improve when treatment is progressed in the future and recommend them to doctors. Will.

# Model 

For our feature engineering, our stratgy was tyring to build and apply suvival analysis model instead of using classification and not focus on getting right labels. We also tried and applied many different threshold but the threshold as 0.24 was the best results. The model wasn't good enought to get correct result and we had 6th placed out of 22 teams.


# Training Data - These are just for your understanding what we worked on during hackaton. I won't include train and test files. 

### trainX.csv
-	It is continuous data between 0 and 1, and expresses the patient's condition.
-	Columns from X0 to X16, composed of 17 variables, reflect the patient's individual status.
-	Some of these exist as confounding variables, affecting treatment while at the same time affecting the patient's final survival (Y).
-	The treatment (T) performed in this data was randomly performed by the medical staff, and several variables were considered at the time of treatment, but it is not necessarily the best treatment.

### trainY.csv
-	It represents the final survival period of each patient, and there are two columns, time and event.
-	The final survival period is the ultimate goal of this treatment of interest to the healthcare practitioner, and may prolong survival if treated with appropriate patients, but for some patients this treatment shortens survival.
-	Time is continuous data, not negative, and is the patient's survival time.
-	Event is binary data, 1 is the patient's event occurrence, 0 is censored. (In this data, there is no censored data for convenience of analysis.)	

### trainA.csv
-	It is binary data, meaning treatment (T), that is, treatment.
-	Express how you have been treated in the past. This does not mean the correct answer. In some cases, it has been healed well, and in other cases, survival has been reduced because of a failure.
-	1 means executing treatment to the patient, 0 means no execution.

### Test Data
-	The format of trainX.csv is the same test data.

# Goal
-The best way to prolong survival in the test patient population is the answer. (It could be T=1 or T=0.)
-Please indicate the submitted value as (1/0) with or without treatment for each patient.

# Result of the Hackathon
According the score board before the last day of Hackaton, we were scored 260 correct data set out of 268 which was the 6th place out of 22 teams. Since they give award only top 4, we didn't get awarded. It was great opportunity to learn about not just statistical models and feature engineerings but also teamwork and time management in short period of time to finish the work.   
