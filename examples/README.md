
# Utilities to manipulate files generated by ANGSD.

These example haven't been fully tested and should be considered as an indication.

### Merge genotype posterior probabilities files

    % ../GetMergedGeno -infiles testA.geno testA.geno -nind 24 24 -nsites 10000 -outfile testA.geno -verbose 0

Please note -nsites must be a unique value, and thus sites must correspond between files.

---

### Select a subset of sites of genotype posterior probabilities files

From an index file with sites to keep:

    % ../GetSubGeno -infile testA.geno -posfile pos_file.txt -nind 24 -nsites 10000 -len 5000 -outfile testA.sub.geno -verbose 0

-nsites refers to the original file, while -len is the number of sites to keep.

---

[]: # "### Select a subset of of individuals and sites from simulated data files"

[]: # "    % ../GetSubSim -infile testA.glf.gz -nind 24 -nsites 10000 -outfile testA.sim.glf.gz -nind_new 10 -nsites_new 500 -check 0"

[]: # "---"

### Switch major/minor or ancestral/derived in genotype posterior probabilities files

    % ../GetSwitchedGeno -infile testA.geno -posfile pos_file.txt -nind 24 -nsites 10000 -len 5000 -outfile testA.switched.geno -verbose 0
