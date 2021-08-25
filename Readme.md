# PeopleSansPeople: A Synthetic Data Generator for Human-Centric Computer Vision

> **Authors:** Salehe Erfanian Ebadi, You-Cyuan Jhang, Alex Zook, Saurav Dhakad, Adam Crespi, Pete Parisi, Steven Borkman, Jonathan Hogins, Sujoy Ganguly
> <br />
> **Authors' affiliation:** Unity Technologies
> <br />
> **Submitted to:** NeurIPS 2021 Track Datasets and Benchmarks Round2
> <br />
> **Paper ID:** 54


## IMPORTANT NOTICE:

**All the files provided are intended only for the NeurIPS 2021 Track Datasets and Benchmarks Round2 review process.**
<br />
**Distribution, making additional copies, or usage for purposes other than reviewing for the NeurIPS conference is strictly prohibited.**
<br />
**All rights reserved for Unity Technologies.**

## Dataset Generation Instructions

We provide two binary files for Linux and MacOS. The binary file will generate the synthetic dataset and corresponding labels from the provided `scenarioConfiguration.json` file.
It is possible to vary the randomizer parameters in `scenarioConfiguration.json` to generate different datasets. 
For example `totalIterations` is the number of frames generated and `randomSeed` is the generation seed.
Under the `randomizers` you will find different randomizers and their exposed parameters and ranges. We ship the configutarion file with the same randomizer configurations that were used to generate the data on our paper.

## Running the Mac Binary

1. Unzip `neurips_bin` file.
2. Run the script `run.sh`. See usage of the script for more details on how to run this script:

```
$ bash run.sh -h
```
For example:
```
bash run.sh run -t Darwin -d /Users/<USERNAME>/neurips_bin/mac_0.1.0 -f /Users/<USERNAME>/neurips_bin/scenarioConfiguration.json -l
```

3. On MacOS the dataset will be written to 
```
/Users/<USERNAME>/Library/Application Support/com.DefaultCompany.HDRPRenderPeople2020.1.17f1/<UUID>
```
where `<USERNAME>` is your user name and `<UUID>` is the folder where the generated dataset from the last simulation is saved.
The dataset output folder will also be shown in the logs in the terminal.
