<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Thanks again! Now go create something AMAZING! :D
***
***
***
*** To avoid retyping too much info. Do a search and replace for the following:
*** github_username, repo_name, twitter_handle, email, project_title, project_description
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->




<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/harmeetgill/capstone_project">
    <img src="https://camo.githubusercontent.com/7818eb78e231aedb0e98e27cf1335f1c3093a4c5a5aa7264c355e6b66f255888/687474703a2f2f696d6775722e636f6d2f315a63527972632e706e67" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Prediction of cancer types based on genomic and clinical features</h3>

  <p align="center">In the UK, between 2015 and 2017, there were 357,000 new cases of cancer, which is roughly 1,000 new cases a day (1). In 2018, worldwide there were an estimated 9.6 million deaths associated with cancer (2). Access to clinical data associated with cancer patients presents its own set of challenges, for example, manual data entry and lack of real-time access. Therefore, with this project I wanted to determine whether I could use an open data source for clinical features associated with cancer diagnoses and treatment, as well as genomic data to predict the cancer type.
    <br />
    <a href="https://github.com/harmeetgill/capstone_project"><strong>Explore the docs »</strong></a>
    <br />
    <br />
  </p>
</p>


<!-- ABOUT THE PROJECT -->
## About The Project


### Data collection and cleaning
The data source used was cBioPortal for cancer genomics (3). This is an open source repository for cancer genomes, including the associated clinical data comprising of 303 studies, spanning 869 cancers and nearly 120,000 samples. The data was collected using an API and filtered for features with at least 2000 samples attributed to them. Once cleaned the dataset consisted of 163 cancers, 129 features and nearly 85,000 samples.

### EDA
The 163 cancers were consolidated into 18 groups to maximise the predictive of the classfication models. EDA revealed genomic insights such as lymphomas/leukemias and cancers related to the cardiovascular and immine sustems to contain one of the lowest incidence of copy number alterations, indicating a lower level of genomic instability. However, frequency of mutation counts in lymphomas/leukemias was higher, while cancers of the digestive system displayed the opposite pattern.

Clinical insights include similarities between the average age of cancer patients of different races in for example, prostate and lung cancers. Large differences lies in the age of different races of adrenal, breast and liver cancer patients.

### Modelling and key findings
Models used for this project include logistic regreassion, decision tree classifier and random forest. 
**Logistic regression**<br>
The baseline score was 0.13. Logistic regression achieved a mean cross-validation (cv) score of 0.62 and test score 0f 0.62. In terms of the F1-scores, leukemia/lymphoma-related cancers displayed a score of 0.76, while the bone cancers scored the worst (0.5). The F1-score for adrenal cancers was 0.65 despite the support number being the lowest (train:test - 285:71). Supporting earlier EDA, leukaemias and lymphomas are negatively correlated with fraction genome altered. In addition, agreeing with clincial diagnostics, the direction of correlation of different tumour grades with cancer class prediction reflect tumour progression or lack of progression.

**Decision tree classifier (DTC)**<br>
This model acheived a mean cv score of 0.62 and test score of 0.63.  F1-score for leukemias/lymphomas was 0.79, while bone cancer had a score of 0.3. Therefore, the DTC largely agrees with the logisitic regression model. Perhaps unsurprisingly, the most important features highlighted by the DTC was fraction genome altered and mutation count.

**Random forest**<br>
This model, similarly to DTC, achieved a mean cv score of 0.62 and test score of 0.63. Therefore, only marginally better than the logisitic regression model, however F1-score for leukemias/lymphomas was 0.79, while bone cancer had a score of 0.3. Therefore, the DTC largely agrees with the logisitic regression model. Perhaps unsurprisingly, the most important features highlighted by the DTC was fraction genome altered and mutation count.

### Conclusion
This project was a preliminary investigation into the prediction of cancer types using clinical and genomic features. The models utilised here have successfully predicted cancer types 50% above the baseline score. The best performing model were the single decision tree and random forest models. Features highlighted by each model point to copy number alterations being of less importance in cancers such as leukaemias and lymphomas, which is supported by known literature by [Buccitelli et al](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5378169/#:~:text=Chromosome%20instability%20(CIN)%20is%20a,genomic%20stability%20(Sheltzer%202013).).

### Limitations and future work
One of the limitations of this dataset is that there is limited data available for some of the cancer types resulting in an imbalance between the classes. This is perhaps reflected in the confusion matrices where some cancers are incorrectly predicted as breast. This may be explained by the abundance of breast cancer samples available in this dataset, compared with other cancers. Secondly, there is an inherent bias in feature reporting for solid and non-solid tumours. For example, it is not possible to report tumour size for a non-solid tumour. Therefore, such limitations should be addressed in future work.

### Project contents:
<ul>
  <li><strong>Data collection</strong><br> [1_capstone_notebook_data_collection.ipynb]</li>(https://github.com/harmeetgill/capstone_project/blob/main/1_capstone_notebook_data_collection.ipynb) </li>
<li><strong>EDA</strong><br> [2_capstone_notebook_cleaning_EDA.ipynb]</li>
<li><strong>Modelling 1</strong><br> 3_capstone_notebook_logistic_regression.ipynb</li>
<li><strong>Modelling 2</strong><br> 4_capstone_notebook_modelling_decision_tree.ipynb</li>
<li><strong>Modelling 3</strong><br> 5_capstone_notebook_modelling_random_forest.ipynb</li>
</ul>

#### References
(1) https://www.cancerresearchuk.org/health-professional/cancer-statistics-for-the-uk
<br>
(2) https://www.who.int/news-room/fact-sheets/detail/cancer
<br>
(3) https://www.cbioportal.org/

Project Link: [https://github.com/harmeetgill/capstone_project](https://github.com/harmeetgill/capstone_project)


<!-- CONTACT -->
## Contact

LinkedIn: https://linkedin.com/in/harmeetgill28/ 






<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/harmeetgill/repo.svg?style=for-the-badge
[contributors-url]: https://github.com/harmeetgill/repo/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/harmeetgill/repo.svg?style=for-the-badge
[forks-url]: https://github.com/harmeetgill/repo/network/members
[stars-shield]: https://img.shields.io/github/stars/harmeetgill/repo.svg?style=for-the-badge
[stars-url]: https://github.com/harmeetgill/repo/stargazers
[issues-shield]: https://img.shields.io/github/issues/harmeetgill/repo.svg?style=for-the-badge
[issues-url]: https://github.com/harmeetgill/repo/issues
[license-shield]: https://img.shields.io/github/license/harmeetgill/repo.svg?style=for-the-badge
[license-url]: https://github.com/harmeetgill/repo/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/harmeetgill28

