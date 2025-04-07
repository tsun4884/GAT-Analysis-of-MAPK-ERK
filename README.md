## Project Summary
This project applies Graph Attention Networks (GAT) to analyze bulk RNA-seq data from 19 cancer types, with a focus on MAPK/ERK and JAK/STAT signaling pathway activity. 
Gene expression and mutation data were obtained from OncoDB, covering both normal and tumor samples. A curated gene interaction network from STRINGdb was used to define the relevant signaling pathways.
The analysis is implemented in the notebook BMCS4480_Sundar_Final_Code.ipynb. 
Before running the code, users should download the appropriate datasets from OncoDB and update the file paths in the notebook accordingly.
The project was developed in Python and is best run in Jupyter Lab with packages such as PyTorch, PyTorch Geometric, Scanpy, Pandas, NumPy, and Matplotlib.

## Results
The GAT model achieved an R² of 0.69 on normal pathway data and 0.49 on cancer data, showing it effectively modeled baseline activity while revealing decreased activity in key genes like GRB2 and MAP2K2 in cancer. A mutation-based GAT model yielded an R² of 0.45, highlighting several upregulated genes (RASGRP2,RASGRF1) and downregulated ones (PRKACA).
To explore pathway crosstalk, an SVR model was used to predict JAK/STAT activity based on MAPK/ERK mutation outputs, achieving an R² of 0.67. SHAP analysis identified mutation activity scores and betweenness centrality as key drivers of JAK/STAT pathway changes.

