Archived: This pipeline is now maintained as part of https://github.com/databio/bedboss

# bedmaker

Pypiper pipeline to convert supported file types* into BED format and bigBed format

## Before running the pipeline: 

Users will need to format metadata as a Portable Encapsulated Project (PEP). Looper will use the PEP yaml config file to run the pipeline on all the dataset samples.  

### Validate the PEP with [`eido`](https://github.com/pepkit/eido)

The input PEP can be validated against the [JSON schema in this repository](pep_schema.yaml). This ensures the PEP consists of all required attributes to run `bedmaker` pipeline.

```
eido -p <path/to/pep> -s pep_schema.yaml
```

## To run the pipeline:

1. Activate [`bulker`](http://bulker.io/) environment

```
bulker load databio/bedmaker:default
bulker-activate databio/bedmaker:default
``` 

2. Submit the pipeline with [`looper`](https://looper.readthedocs.io/en/latest/)
 
```
looper run example/cfg.yaml
```


----
## Currently supported formats*:

- bedGraph
- bigBed
- bigWig
- wig

