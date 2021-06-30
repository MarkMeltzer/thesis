![Cover image of the thesis](cover_image.png)

# Thesis
Code for my Artificial Intelligence Bachelor Thesis. I will analyse EU public procurement tenders from TED (Tenders Electronic Daily) in the context of the digitalization of borders.

The final thesis document can be found [here](Thesis.pdf) (githubs pdf viewer might not render it properly, it is advised to download and open the file in a different pdf viewer). This document also contains information on how the raw data was retrieved (not all of it is done via python).


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

#### Notebooks

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