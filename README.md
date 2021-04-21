# AND-Task

This dataset consists of two parts: Devlopement.csv and Testing.csv.

Authors may use the developement part to design their model and they may split it (i.e. Training, validation and testing sets) in anyway they find appropriate. The Testing part will be split such that each target author is present in all sets: Training, validation and testing. If the target author did not publish enough papers to fulfill this condition, the priority is in this order: training, then validation then testing. This means if an author has authored only 2 papers, one will be in the training set and the other in the validation set. In the testing part, the labels will be provided for the training and testing parts only. 

## Devlopment part: 
This part contains 38215 paper records authored by authors whose full names are abbreviated as "Y Wang". Each record is present with two samples in the dataset; 1) with full names and 2) with abbreviated names. Note that when splitting the dataset, make sure that both samples of a unique record are in the same set (i.e. training, validation or testing). Consequently, the file Devlopement.csv contains 76430 samples (lines). Each line is in the following format:

#1;\t #2;\t #3;\t [#c1;\t; #c2;\t ... #cN];\t #4;\t #5;\t #6\n

Where: 
#1: Record index (a unique index for each paper record) 
#2: Target author index (a unique index for each author)
#3: First name and last name of the target author separated by a blank space. This name combination is very likely to be shared by other authors in this dataset.
#4: The title of the paper
#5: The source of the paper (e.g. journal or booktitle)
#6: Year of publication
#c1: First name and last name of the first coauthor separated by a blank space
#c2: First name and last name of the second coauthor separated by a blank space
#cN: First name and last name of the Nth coauthor separated by a blank space

Note that the target author is also present in the list of co-authors.
We use ;\t as a separator/delimiter to seperate these elements.
