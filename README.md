# Concurrent-implementation-of-J48-via-WEKA
This is a Concurrent Implementation of J48 via WEKA which I have attempted for my MSc project. I have successfully made it much faster than the original version.
If you require more information, such as how fast it runs in comparison to the original, or just techincal information, please view my dissertation.

Not all of the files have been included as github limits the size, this only has the source-code. If you want pre-compiled versions, and an alternative JCSP implementation, please visit my website:
https://www.lysaks.com/deama/Files/trees/index.html

General Information:
-You can run them via the terminal if you want, however you cannot modify the poolsize through an argument, that feature has not been added yet.
Here is a general command line to run via a terminal:
java -cp weka-4.jar weka.classifiers.trees.J48 -C 0.25 -M 2 -t /data/train.arff -no-cv
This will run weka-4.jar with the J48 configuration, with the "train.arff" dataset and without any cross-validation.

-The source code is a netbeans project, however, you may be able to open it via a different IDE. In order to compile a ".jar" file of the project, you will need to include two library files included in the libraries folder under source code.

-In the source code, pruning parallelised v2 is enabled (which is either the same, or slightly better than the original); if you want to disable it, find "firstPrune()" in the "C45PruneableClassifierTree.java" class and change it to "prune()".

-This implementation was made with the explorer GUI version in mind; the terminal version does work fine, and the large amount of tests done proves this to be true, however keep this in mind when browsing through the source code.

-Here is the link to my google-sheets test tables for the various tests I have conducted: https://docs.google.com/spreadsheets/d/1jzmcN_xSdGnoUz2bkDQxRatBBUN5bEabRigjV_chelY/edit?usp=sharing
