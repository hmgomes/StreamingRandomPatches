# StreamingRandomPatches
This is the repository for the StreamingRandomPatches (SRP) algorithm implemented (originally) in MOA 2017.10. 
The algorithm has been ported to MOA 2019.04 in this repository. 

The Streaming Random Patches (SRP) algorithm is going to be added to MOA in the near future.
Until that, you may use this repository to have access to its source code. 

For more informations about MOA, check out the official website: 
http://moa.cms.waikato.ac.nz

## Citing StreamingRandomPatches
To cite this SRP in a publication, please cite the following paper: 
> Heitor Murilo Gomes,  Jesse Read, Albert Bifet. 
> Streaming Random Patches for Evolving Data Stream Classification. In IEEE International Conference on Data Mining (ICDM), IEEE, 2019.

## Datasets
The datasets and synthetic data streams are available in the `\dataset` directory.

## How to execute it
To test StreamingRandomPatches you can copy and paste the following command in the interface (right click the configuration text edit and select "Enter configuration”).
Sample command: 

`EvaluateInterleavedTestThenTrain -l (meta.StreamingRandomPatches -l (trees.HoeffdingTree -g 50 -c 0.01) -s 100 -o (Percentage (M * (m / 100))) -c 60 -a 6) -i 100000000 -f 100000000 -s (ArffFileStream -f elecNormNew.arff)`

Explanation: this command executes a interleaved test then train evaluation on SRP with 100 classifiers (-s 100) using 60% of the features to build each subspace (-c 60 and -o (Percentage (M * (m / 100))))
on the ELEC dataset (-f elecNormNew.arff). 
**Make sure to extract the elecNormNew.arff dataset, and setting -f to its location, before executing the command.**
