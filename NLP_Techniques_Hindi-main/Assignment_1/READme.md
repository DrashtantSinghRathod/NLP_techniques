
Computational Linguistics for Indian Languages
CS689A

Assignment 1:

roll.no-> 22111059(Sudiksha Navik)



Implementation:

We performed unicode correction by having some if else statements on the 
natural unicode.
After each consonant add अ but not for consonant with halant
Halant is added to consonant by adding chr(2381)

Syllable are extracted by  vowel sound ending.

precision=truepositive/(truepositive+falsepositive)

recall=truepositive/(truepositive+falsenegative)

F-score is a harmonic mean of precision and recall.

Q7(b) mark the suffix ones that are correct;
    => from the data of frequency itself we find that the string
     which are not suffix are having very less frequency 
     

Assumptions:

    Code size must be in range 1GB


Limitations:

    Due to large file code may take large time to give output.


Libraries used:
	collections
	Counter
	defaultdict
	matplotlib
	pylot
	re
	string
	io
	open
	conllu
	parse_tree_incr(conllu)

all questions are uploaded in same ipynb notebook.

 
outputs of each question are attached on the given drive:

https://drive.google.com/drive/folders/10UyaMC3-l9cfmJe1r5Go23u4v_f5DARw?usp=sharing
