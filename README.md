# eDNA_spatial_temporal_variation
Code and datasets from "Investigating temporal and spatial variation of eDNA in a nearshore rocky reef environment" by Taylor Ely, Paul H. Barber, and Zachary Gold. Decontamination code was written by Zack Gold and can also be found on his page  https://github.com/zjgold/gruinard_decon

# Decontamination: 

Decontamination was conducted using the gruinard_decon scripts modified to handle the presence of 2 separate sequencing projects. Negative and positive controls as well as all samples were included across both projects during the entire decontamination process. Data outputs from the MPA project were then separate post decontamination.

Inputs
Inputs are located in the data directory

Raw Anacapa Output - fishcard_12S_all_ASV_raw_taxonomy_60_edited.txt This file is a standard Anacapa output community-site table with columns of samples and rows of ASVs. See the Anacapa Github page linked above for a more detailed description of the bioinformatic processing.

Metadata File - mpa_metadata_02042020.txt This file provides detailed information associated with each sample.

Hash File This file links the updated taxonomy to each ASV. Taxonomic assignment was assigned to each ASV twice. First, using a reference database of only California fishes, FishCARD. Second, using a global reference database of all MiFish 12S reference barcodes including marine mammals and birds. This updated taxonomy incorporates the marine mammal and bird assignments from the second round of taxonomic assignment to the first round of assignments. The first round of taxonomic assignments have empty strings given the lack of mammalian and avian reference barcodes in the fish only database. This 2 step taxonomic assignment procedure was done because previous work (See FishCARD) demonstrated that local reference databases provide higher accuracy in taxonomic assignments.

Outputs

Outputs include the ASV.nested file which includes the raw ASV and read counts kept through each decontamination step, the ASV.Summary file which includes the counts of samples, ASVs, and reads retained at each step, the summarized .RDS and .CSV community-site tables, and general summary plots from the decontamination steps.

# Analysis: 

Inputs

taylor_pre_occupancy_results_sum.taxonomy_bio_reps_separate_eDNA_index.RDS - This file is a community-site table with columns as samples and rows as species. ASVs assigned to the same taxonomic rank had reads summed together prior to eDNA index calculations. 

taylor_pre_occupancy_results_sum.taxonomy_bio_reps_separate_read_counts.RDS - This file is a community-site table with columns as samples and rows as species. ASVs assigned to the same taxonomic rank had reads summed together. 

metadata - MetaData_eDNA_degradation2020.txt

Monitored_Species_list_20201204.txt - This is a file of species monitored by agencies in southern California. Common name and scientific name are included. Which of the three agencies (National Park Service Kelp Forest Monitoring Program, Reef Check California, and PISCO) monitors each species is indicated by an "X"
