Computational Linguistics for Indian Languages (CS689A)
Assignment 2:
Roll no: 22111059 (Sudiksha Navik)

List of file in zip folder
1.	22111059-Assignment2.ipynb
2. assign_2_cs689a.ipynb
3. Make file
4. READme.md

Q1. Dependency Parsing
parse(): CoNLL-U Parser parses a CoNLL-U formatted string into a nested python dictionary.
POS tags and all the asked features are accessed from the the obtained dictionary.

Libraries used:
	collections
	Counter
	string
	io
	open
	conllu
	parse(conllu)

All questions are uploaded in the .ipynb notebook.

Q2. Fine-tune the pre-trained BERT model for the UPOS prediction task.
Dependencies: numpy, conllu, datasets, transformers, seqeval
Installations:
1. pip install transformers
2. pip install sentencepiece
3. pip install datasets
4. conda install pytorch torchvision -c pytorch
5. pip install seqeval

HyperParameters batch_size, learning_rate, num_train_epochs and weight_decay are tuned in order to improve the accuracy of the model.

For 1 epoch,
Precision: 0.777324
Recall: 0.790884
F1: 0.784045
Accuracy: 0.830763

For 2 epochs,
Precision: 0.804477
Recall: 0.817231
F1: 0.810804
Accuracy: 0.852626

