# ACSAC22-Artifacts
ArchiveSafe LT ACSAC '22 Artifacts

The artifacts are divided into three groups:
 - Experiment Code: Contains the code used to run the evaluation experiment detailed in Section 5. The code is written in Python.
 - Data Results: Contains the data points collected by the evaluation experiment and presented in Section 5.
 - Tamarin Files: Contains the Tamarin theory files modeling the security experiments for the design detailed in Section 4.3. 

Experiment Code:
 - CreateSample.py: A Python program used to generate random data files to be used as sample archive files in the evaluation experiment. It generates groups of files in different data sizes. 
 - RunFileExp.py: A Python program simulating an update of a leaf in the Merkle tree. This event corresponds to an update to the contents of an archive file. The program measures the time needed to update a leaf in a tree using different size trees.
 - RunConfExp.py: A Python program used to measure the time needed to evolve the confidentiality of archives of different sizes. The program uses the sample files created by the CreateSample.py application. It performs the initial creation of the archive followed by three evolution processes. The program measures the time needed for the initial creation of the archive and the subsequent evolution processes.
 - RunIntExp.py: A Python application used to measure the time needed to evolve the integrity of archives of different sizes. The program uses the encrypted files created by the RunConfExp.py application. It measures the time needed to evolve the integrity of archives of different sizes.

Data Results:
 - Archive Confidentiality Exp.xlsx: The data points collected by the RunConfExp.py program.
 - Archive Integrity Exp.xlsx: The data points collected by the RunIntExp.py program.
 - Tree Update:  The data points collected by the RunFileExp.py program.

Tamarin Files:
In order to run these files, Tamarin Automatic Prover must be installed (http://tamarin-prover.github.io/). To run a file, run "tamarin-prover interactive example.spthy" on the comand prompt then go to "http://127.0.0.1:3001" from the browser.
 - archivelt_conf.spthy: A Tamarin theory file simulating the confidentiality experiment.
 - archivelt_forge.spthy: A Tamarin theory file simulating the integrity experiment.
