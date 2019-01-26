# prostate_cancer_analysis
The goal of this project is to model seminal vesicle invasion, a prognostic indicator of prostate cancer, based on prostate-specific antigen levels collected through minimally-invasive procedures. 

Data on prostate-specific antigen (PSA) levels can be collected through a simple blood test. If health care professionals could determine the severity of a patient's prostate cancer using a blood test, rather than through an invasive biopsy, the doctor and patient could more easily and comfortably decide on a treatment plan. 

Seminal vesicle invasion (SVI), which occurs when the tumor enters the seminal vesicles outside the prostate, is a poor prognostic indicator of the disease. To learn more about the disease, data on 97 men with prostate cancer were collected before and after radical prostatectomies. The pre-operative PSA level was recorded, and after the radical prostatectomies were performed the presence or absence of SVI was documented. Other variables such as the tumor weight were also measured.

I modeled the SVI indicator based on PSA levels using logistic regression in R. I achieved an overall accuracy rate of 75%, approximately, but the accuracy rate for classification is only about 50% when the patient actually does have seminal vesicle invasion. As a result, I conclude that better minimally-invasive measures for determining the severity of prostate cancer need to be developed, and that more research should be done to find a better model of SVI.
