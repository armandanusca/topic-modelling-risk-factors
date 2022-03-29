# SEC EDGAR Topic Modelling and relevance forecasting of Risk Factors

### Initial Project Statement - Third Year Project - University of Manchester
## Topic modelling of the financial domain

### Background

A large amount of financial information is available through corporate textual disclosures. The volume of data that has become available, however, makes a manual discovery of topics and the interpretation of the texts infeasible. One particular type of information that is of high interest to investors is the corporate disclosure of risk exposures. Using an automated text algorithm could facilitate and speed up the identification of risks that companies are exposed to.

### Description

Companies in the U.S. must disclose their risk factors in a specific section of their annual reports. While identifying this section is relatively easy, the description of the risk factors within this section is unstructured and encompasses several pages. Instead of letting humans read through these sections to identify particular risk factors, the goal of this project is to employ an automated term recognition method to identify the most common risk factors across firms and years. One contribution in this area has been made by Bao and Datta (2014) who employ an LDA model to discover and quantify risk topics. However, individual words that the LDA identifies may not be as meaningful as domain-specific (multi-word) terms. This project will aim to look at how to combine these two approaches.

### Deliverables

The main goal of the project is topic modellig (see (Blei and Lafferty, 2009)) for the financial risk domain. The model will aim to employ a term recognition method (e.g. (Spasic et al. 2013)) to examine whether an accurate automated discovery of risk factors from US firms’ annual report disclosures can be achieved and how it can best be presented. The student will have the opportunity to compare the various approaches to topic discovery, e.g., LDA models and term recognition methods.

### References

Bao, Y., Datta, A., 2014. Simultaneously discovering and quantifying risk types from textual risk disclosures. Management Science 60, 1371–1391.
Blei, David M., and John D. Lafferty, Topic models, Chapter 4 in Srivastava, Ashok N., and Mehran Sahami, eds. Text mining: Classification, clustering, and applications. CRC Press, 2009.
Spasic, Irena et al., 2013, FlexiTerm: a flexible term recognition method, Journal of Biomedical Semantics, 1—15.

##### Supervisor: Goran Nenadic

#### Functionality implemented:

* Extract risk factors section from SEC EDGAR and store them into a MongoDB instance
* Dataset analysis for the extracted documents
* BERTopic model - utilises DTM to generate a view over the evolution of topics throughout time
* Regression model - forecast topic frequency
* Classifier model - evaluate if a topic is going to increase in importance
* Timeseries model - forecast topic frequency (utilising a timeseries model)

### Collab version with models, datasets and pretrained BERTopic can be found [here](https://drive.google.com/drive/folders/1IryUzW8f0Y2pSrlabYnRX-mS_E6lmSya?usp=sharing)

#### User guide:
(It is recommended to be used in a powerful environment comparable to the ones provided by [Google Colab Pro+](https://colab.research.google.com/signup))

Prerequirements:
- Git
- (optional) Git LFS
- Python 3.8
- (optional) MongoDB

1. Create a MongoDB instance locally - or restore the one provided [here](https://drive.google.com/drive/folders/1_zNuddgjzKGUmRq-m8qtTHsqMnJ5aez7?usp=sharing)
2. Clone the repository
3. (optional) Create a virtual environment
4. Get the data - either by running data_gathering.ipynb or by downloading the datasets provided on [Google Drive](https://drive.google.com/drive/folders/1HymSyqCKMx73t9PHm2iGMdD72PWMSIpr?usp=sharing)
5. Run BERTopic_Model (Dynamic Topic Modelling) in order to transform document data into topics based timeseries
6. Run Increasing_Classifier: if you want to determine if a keyword is part of a topic which is going to increase in importance
7. Run Regression_Model: if you want to predict evolution of topics past their limit in the dataset (or on future timestamps)

#### User guide:
The analysis was developed on the following platforms:

* AMD Ryzen 5 4600h | 32GB RAM | NVIDIA GeForce® GTX 1650 4GB GDDR6
  * Windows 11
  * openSUSE Tumbleweed

* Apple M1 | 16GB RAM
  * macOS Monterey 12.3

* 1.7GHz quad-core Intel Core i7, Turbo Boost up to 4.5GHz | 16GB RAM | 128MB of eDRAM
  * macOS BigSur 11.6.5

* Google Colab Pro+ | NVIDIA K80 | 2 x Intel Xeon @ 2.199GHz | 52GB RAM
  * Ubuntu 18.04.5 LTS

## [Report](https://drive.google.com/file/d/16_msAakQK8Gb70fQCHjNNfCA9kkAxgBq/view?usp=sharing)
