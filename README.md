# ctg-containers
- Singularity containers for ctg NGS data processing

### Containers
- [ sc-rna-10x ]: For 10x single cell mRNA-seq. Based on cellranger
- [ ngs-tools ] : Misc tools for ngs data processing
- More to come

### HOWTO:
#### Build containers from recipes
```
sudo -E singularity build <container.sif> <container-build> 
```

E.g to build sc-rna-10x container:
```
sudo -E singularity build sc-rna-10x.v6.sif sc-rna-10x.v6-build
```

#### Run command with container
```
singularity exec --bind /fs1 sc-rna-10x.v6.sif cellranger count (..arguments..)
```
