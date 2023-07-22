  #  
  # Differential Correlations Informed Metabolite Set Enrichment Analysis to Decipher Metabolic Heterogeneity of Disease


## Install   
The projects uses some packages. Go check them out if you don't have them locally installed. Enter the Python terminal interface，

`pip install networkx 2.6.3`

## Usage
### Algorithm of dci-MSEA strategy  
All process in example file：  

`dci_MSEA_for_phenotype_specifc.py`(group),  
`dci_MSEA_for_individual_specific.py`(sample),  



**1.Construct general metabolite network**   
`get_general_metabolite_network.py`  ------  Parameter requirements： Concentration matrix file address for CRC and control, note that The first column is the detected metabolite KEGG id, and each subsequent column is the sample.Please refer to the original file for the specific return of this function.



**2.Screen the significantly differential correlations (DC) and calculate differential expression level (DE) for each detected metabolite of POI group**  

calculate DC for group ------          `get_DC_group.py`   
calculate DE for group  ------          `get_DE_group.py`

**3.Construct the differential correlations-informed metabolite network (dci-net)**   

`get_dci_Net.py`  ------   This function involves three parameters which are graph form of general metabolite network,DC and metabolite list.  

**4.RW-based MSEA**   

`get_MSEA.py`    ------    This function involves five parameters which are row-normalized matrix of dci-Net, metabolite list,DE,KEGGid and pathway filepath
  
