# NLP Techniques on Hindi
## Assignment-1
Link to datasets: https://github.com/UniversalDependencies/UD_Hindi-HDTB/tree/master<br>
The corpus files are available from https://indicnlp.ai4bharat.org/corpora/#downloads<br>
+ Performed unicode correction for Hindi
  + The default unicode of Hindi characters are not correct:<br>
    For eg.,
    The unicode bifercation of character in "कल्पना" comes out to be: ['क', 'ल', '्', 'प', 'न', 'ा'] which is wrong.<br>
    Its correct unicode is: ['क्', 'अ', 'ल्', 'प्', 'अ', 'न्', 'आ']<br>
+ Cleaned the corpus, i.e., get rid of non-language characters
    
+ Considering a word as a white-space separated sequence of characters. For each word, found the characters and the syllables. Stored a list of them and the words in descending order of their frequencies.<br>
  + {'करने': [['क्', 'अ', 'र्', 'अ', 'न्', 'ए'], 6, ['क', 'र', 'ने'], 3]}    

+ Found the bi-gram frequencies of syllables and characters
    +  ('आ', 'वे'): 3, ('वे', 'द'): 3
+ Implemented BPE on the corpus with different vocabulary sizes.
  +  For each token thus found, found the characters and the syllables, the unigram and bi-gram frequencies of tokens, syllables and characters
+ For each vocabulary size of BPE, found the precision, recall and F-score of the BPE-output token set as found previously
+ Extracted a list of lemmas and the corresponding surface forms found from the UD- tagged files
+ Drawn the frequency v/s rank plot of whitespace-separated words, BPE tokens, syllables, characters, lemmas and verified if they follow Zipfian law
+ Given a lemma and the corresponding surface form, derived the suffix. Performed an end stripping from the surface form till the lemma or a subset of the lemma is reached (chosen the longer one). Called the stripped part as the suffix. Listed the 50 most common suffixes ordered in this manner.

## Assignment-2
The Python code notebook for BERT MODEL and the respective datasets can be found at: <br>
https://drive.google.com/drive/folders/1VKwQtnSRqWERULev2JwXKj6Y4Ow61EPk?usp=sharing. <br>The BERT models are listed in https://huggingface.co/ai4bharat/indic-bert.
+ In the parse file attached,
Consider a particular sentence S consisting of n words w1 . . . wn.<br>
Corresponding to that are the POS tags t1 . . . tn. <br>
For each word wi, assume the gender, case and number to be gi, ci and bi respectively.<br>
There are also n dependency relations in the sentence (including the one with the root). Assume a dependency relation to be ⟨wi,R,wj⟩ which indicates that the word wi is connected to its head word wj by the relation R. Correspondingly, the POS tag relation is ⟨ti,R,tj⟩.<br>
For each of the questions below, output the list in descending order of frequencies:<br>
  +   Found the frequencies of POS tags of words.<br>
  +  Listed the 50 most frequent words corresponding to each POS tag.<br>
  +  Found the frequencies of gender, case and number of words separately.<br>
  +  Listed the 50 most frequent combinations of gender, case and number as a 3-tuple.<br>
  +  Found the frequencies of POS tags corresponding to only head words.<br>
  +  Found the directed POS tag tuples, i.e., ⟨ti , tj ⟩. For each such 2-tuple, list the frequencies separately for each relation R as well as total.<br>
  +  For each dependency relation R, listed the frequencies separately for each 2-tuple ⟨ti,tj⟩ as well as total.<br>
+  Fine-tuned the pre-trained BERT model for the UPOS prediction task. Recorded precision, recall and F-score
