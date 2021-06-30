![Cover image of the thesis](cover_image.png)

# Thesis
This repository contains the code for my Artificial Intelligence Bachelor Thesis. For this project I analysed EU public procurement documents from Frontex in the context of datafication of borders.

The final thesis document can be found [here](Thesis.pdf) (githubs pdf viewer might not render it properly, it is advised to download and open the file in a different pdf viewer). This document also contains information on how the raw data was retrieved (not all of it is done via python).


#### Thesis abstract
> Borders in the European Union (EU) are becoming increasingly datafied: that is, more data is collected and processed for migration management. This process is criticized on multiple issues in the social science literature. However, the agency tasked with managing borders in the EU, Frontex, has been criticized for its lack of transparency. Nevertheless, there is some information Frontex is compelled to publish, that being public procurement documents. This paper aims to analyse these documents using Latent Dirichlet Allocation (LDA), a topic modelling method. In this research, LDA is used to analyse datasets made up of contract award notices (CAN) and call for tender (CFT) documents. The resulting topics and timelines of topics give an empirical account of the datafication of borders and support the social science literature on this issue.


# File structure

```
.
├── data
|     ├── CSV        # the CAN and CFT datasets in CSV
|     ├── JSON       # list of section names for the CFT documents
|     ├── PDF        # the original selected CFT documents in PDF format
|     ├── processed  # different versions of the different datasets (serialised with pickle)
|     ├── ZIP        # archives containing all the documents related to each CFT
|     ├── XML        # CAN documents in XML format
│     └── sheets     # sheets listing tender award notices
│     
├── models           # different models for the different datasets (serialised with pickle)
├── visualisations   # visualisations such as plots and pyLDAvis html exports
└── notebooks        # notebooks containing code for analysing the data
      ├── simple_visualisations_CAN         # some simple exploration of the CAN data
      ├── data_extraction_CAN               # extracting data from CANs
      ├── data_extraction_CFT               # retrieving and extracting data from CFTs
      ├── LDA_scikit_CAN                    # producing the LDA models and timeline plots for the CAN dataset
      ├── LDA_scikit_CFT_full_text          # ditto for the full-text variant of the CFT dataset
      └── LDA_scikit_CFT_selected_sections  # ditto for the selected-sections variant of the CFT dataset

```

# Requirements

The following python modules are required to run all of the code in the notebooks:
- pandas
- matplotlib
- nltk
- pdfminer.six
- bs4
- tqdm
- spacey
- pyLDAvis
- tmtoolkit
