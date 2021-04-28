# heinrich-2021a
Resources for Heinrich et al., 2021

The raw imaging data and ground truth data used for machine learning model training can be found in this s3 bucket:  
[`s3://janelia-cosem-publications/heinrich-2021a`](https://open.quiltdata.com/b/janelia-cosem-publications/tree/heinrich-2021a/)  

## Data organization
This directory contains array data stored hierarchically in the [`n5`](https://github.com/saalfeldlab/n5) format. 

- FIB-SEM data used for generating ground truth and predictions is stored as n5 datasets, and can be found at `{dataset_name}.n5/volumes/raw`
- Human-generated annotations ("crops") are stored as a collection of n5 groups in `{dataset_name}.n5/volumes/labels/0003/{crop_name}`. The pixel data for the crop is stored at `{dataset_name}.n5/volumes/labels/0003/{crop_name}/labels/all`

## Data access
Warning: Be advised that copying large amounts of imaging data from cloud storage may use a lot of local storage space and take a long time to complete!  
([`AWS cli`](https://aws.amazon.com/cli/)) Download everything to `local/path`. 
```
aws s3 cp janelia-cosem-publications/heinrich-2021a/ local/path --recursive
```

([`AWS cli`](https://aws.amazon.com/cli/)) Download just data for the `jrc_hela-2` dataset to `local/path/jrc_hela-2.n5`:
```
aws s3 cp janelia-cosem-publications/heinrich-2021a/jrc_hela-2.n5 --recursive
```
## Related repositories: 
- [Training setups](https://github.com/janelia-cosem/training_setups): scripts used for training ML networks on FIB-SEM data
