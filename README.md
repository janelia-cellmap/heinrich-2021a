# heinrich-2021a
Resources for Heinrich et al., 2021

The raw imaging data and ground truth data used for machine learning model training can be found in this s3 bucket:  
[`s3://janelia-cosem-publications/heinrich-2021a`](https://open.quiltdata.com/b/janelia-cosem-publications/tree/heinrich-2021a/)  

This directory contains array data stored hierarchically in the [`n5`](https://github.com/saalfeldlab/n5) format. 

- FIB-SEM data can be found at `s3://janelia-cosem-publications/heinrich-2021a/{dataset}.n5/volumes/raw`
- Human-generated annotations are stored as `n5` groups in  be found at `s3://janelia-cosem-publications/heinrich-2021a/{dataset}.n5/volumes/labels/0003/{crop_name}/labels/all`
