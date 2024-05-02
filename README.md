# Results

This repository is part of the diploma theses at Charles University. The main repository can be found [here](https://github.com/Erunno/protein-binding-sites).

This repository contains the results measured over the course of model development. It includes two main folders:

- [**netw_runs**](./netw_runs): This folder contains runs from training and hyperparameter tuning. Each file represents one training session. Different "type" of models are distinguished by their specific `tag`. To analyze these results, set the `networks_results_folder` variable to this folder in the [config file in the main repository](https://github.com/Erunno/protein-binding-sites/tree/master/config). You can use scripts in the folder [res_presentation](https://github.com/Erunno/protein-binding-sites/tree/master/res_presentation) to analyze these results.

- [**final_runs**](./final_runs/): This folder contains data from the final evaluations of models. These results are presented in the thesis. To browse them, set the `final_networks_results_folder` variable to this folder in the [config file in the main repository](https://github.com/Erunno/protein-binding-sites/tree/master/config). Scripts in the [res_presentation](https://github.com/Erunno/protein-binding-sites/tree/master/res_presentation) folder can also be used for analysis.

## Tags of Models Explained

The specific tags may be a bit cryptic and most results are from various experiments which were not presented in the thesis. Here we list the relevant tags and explain which model in the thesis they correspond to:

### Reference Models

- `p2rank`: Results from the P2Rank tool.
- `reference`: Results from the article by Hoksza and Hamza (mentioned in the thesis). However they have used different embedders.

### Protrusion Models

- `one_prot_fst_v3_c`: A single *protrusion* value as a hyperparameter in the first layer.
- `protrusion_bypass_v4_c`: A single *protrusion* value as a hyperparameter bypassing hidden layers.
- `prot_all_c`: Multiple *protrusion* values in the first layer.

### SASA Models

- `SASA_fst_v2_c`: *SASA* value as a hyperparameter in the first layer.
- `SASA_bypassed_v2_c`: *SASA* value as a hyperparameter bypassing hidden layers.

### Neighboring Residues Models

- `neighboring_emb_5_v2_c`: Direct input of 5 embeddings (4 neighboring).
- `nei_emb_3_v2_c`: Direct input of 3 embeddings (2 neighboring).
- `nei_emb_5_avrg_v2_c`: 5 averaged embeddings (4 neighboring).
- `nei_emb_3_avrg_v2_c`: 3 averaged embeddings (2 neighboring).
- `nei_5_comprs_v3_cc`: Compression layer of pre-trained models for 5 embeddings (4 neighboring).
- `nei_3_comprs_v3_cc`: Compression layer of pre-trained models for 3 embeddings (2 neighboring).
- `nei_compr_3_small_v4_c`: Compression layer of pre-trained models for 5 embeddings (4 neighboring) - *small trainable network*.
- `nei_compr_5_small_v4_c`: Compression layer of pre-trained models for 3 embeddings (2 neighboring) - *small trainable network*.
