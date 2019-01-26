**Introduction**

According research conducted by the American Cancer Society, in 2018 around 165,000 men in the United States will be diagnosed with prostate cancer, the most common cancer in men after skin cancer (Key Statistics, 2018). If a patient is diagnosed with prostate cancer, the next step is to determine the prognosis, the likely result of the cancer in the near future. Arriving at an accurate prognosis helps the doctor create a treatment strategy, while also aiding the patient and his family with life planning in light ot the disease.

__Question and Motivation__

Given how common prostate cancer is, a relevant question is whether or not data collected from minimally invasive to non-invasive procedures, such as a blood test, can be used to model prostate cancer severity measures, while also aiding in the prediction of those severity measures. It would be beneficial to the patient if the doctor could determine a prognosis using minimally-invasive or non-invasive procedures, to reduce physical pain and expense. My goal in this paper is to arrive at a model physicians can use to make prostate cancer prognoses, that is only based on data collected from non-invasive to minimally invasive procedures.

__Description of Data Set__

This data set can be used to answer the question of whether data from minimally invasive to non-invasive procedures could be used to build a model of prostate cancer severity, because two variables, the PSA level and the age of the patient, were collected in such a manner. I used these variables to model seminal vesicle invasion, which Potter et al. (2000) demonstrates is an indicator of a poor prognosis if indeed seminal vesicle invasion has occurred. The prognosis would be poor in the case of seminal vesicle invasion, because the cancer would have spread outside the prostate and invaded the seminal vesicle, a different gland.

Modeling the Gleason score may have been a more obvious choice for answering the research question. The reason I did not choose to model the Gleason score was that preliminary results showed that models using the PSA level and age could not predict the Gleason score with a high level of accuracy.

__Exploratory Data Analysis__

To further explore the data, I created box-plots of the seminal vesicle invasion (SVI) variable versus PSA level and age. 

      #read in data
      prostate_cancer = read.table("APPENC05.txt", header = FALSE)
      #set column names
      colnames(prostate_cancer) = c("id", "psa", "volume", "weight", 
                              "age", "hyperplasia", "svi", 
                              "capsular_pen", "gleason")
      par(mfrow = c(1,2))
      #plot of psa versus svi
      plot(as.factor(prostate_cancer$svi), prostate_cancer$psa,
            xlab = "SVI", ylab = "PSA Level", main = "Association of SVI and PSA")
      #plot of age versus svi
      plot(as.factor(prostate_cancer$svi), prostate_cancer$age,
            xlab = "SVI", ylab = "Age", main = "Association of SVI and Age")
     
     
