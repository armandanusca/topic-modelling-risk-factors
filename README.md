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
* Burstiness model - utilises Emma Tattershal work to detect bursty terms https://github.com/etattershall/burst-detection
* Regression model - forecast topic evolution
* Classifier model - evaluate the burstiness of a term

