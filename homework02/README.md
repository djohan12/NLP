# NLP HW1

Please find the homework assignment instructions [here](https://docs.google.com/document/d/1K8s_Ecms0cIqRO1PKPFs2bfFVFfZpc1nFoEhtxRlCaM/edit?tab=t.5c3153xm9mha).

*Free response answers are in the ipynb file

## Part 1
* Model accuracy: 

Epoch 1/5	Average Loss: 0.6284	Time: 2.27s
Epoch 2/5	Average Loss: 0.2595	Time: 2.20s
Epoch 3/5	Average Loss: 0.1929	Time: 2.04s
Epoch 4/5	Average Loss: 0.1813	Time: 2.15s
Epoch 5/5	Average Loss: 0.1582	Time: 2.01s
Validation Accuracy: 0.9325
Test Accuracy: 0.9353

* Free response:

Sentence 1:
1. the DT DT
1. flight NN NN
1. should MD MD
1. arrive VBP VBP
1. at IN IN
1. eleven CD CD
1. a.m RB RB
1. tomorrow NN NN
1. . PUNC PUNC

Sentence 2:
2. i PRP PRP
2. would MD MD
2. like VB VB
2. to TO TO
2. find VB VB
2. a DT DT
2. flight NN NN
2. that WDT WDT
2. goes VBZ VBZ
2. from IN IN
2. la NNP NNP
2. guardia NNP NNP
2. airport NNP NNP
2. to TO TO
2. san NNP NNP
2. jose NNP NNP
2. . PUNC PUNC

Sentence 3:
3. show VB VB
3. me PRP PRP
3. the DT DT
3. flights NNS NNS
3. from IN IN
3. newark NNP NNP
3. to TO TO
3. los NNP NNP
3. angeles NNP NNP
3. . PUNC PUNC

Sentence 4:
4. what WP WP
4. airline NN NN
4. is VBZ VBZ
4. this DT DT
4. ? PUNC PUNC

Sentence 5:
5. show VB VB
5. me PRP PRP
5. the DT DT
5. t NNP NNP
5. w NNP NNP
5. a DT DT
5. flight NN NN
5. . PUNC PUNC

Sentence 6:
6. i PRP PRP
6. would MD MD
6. like VB VB
6. to TO TO
6. travel VB VB
6. to TO TO
6. westchester NNP NNP
6. . PUNC PUNC

Sentence 7:
7. list VB VB
7. american NNP NNP
7. airlines NNP NNP
7. flights NNS NNS
7. from IN IN
7. new NNP NNP
7. york NNP NNP
7. newark NNP NNP
7. to TO TO
7. nashville NNP NNP
7. . PUNC PUNC

Sentence 8:
8. thanks UH UH
8. . PUNC PUNC

Sentence 9:
9. what WP WP
9. flights NNS NNS
9. are VBP VBP
9. there EX EX
9. from IN IN
9. nashville NNP NNP
9. to TO TO
9. houston NNP NNP
9. tomorrow NN NN
9. evening NN NN
9. that WDT WDT
9. serve VBP VBP
9. dinner NN NN
9. ? PUNC PUNC

Sentence 10:
10. i PRP PRP
10. 'd MD MD
10. like VB VB
10. to TO TO
10. fly VBP VBP
10. next JJ JJ
10. friday NNP NNP
10. . PUNC PUNC

## Part 2
* How many unique rules are there?
    419
* What are the top five most frequent rules, and how many times did each occur?
    1.	IN --> IN_t	(Occurence: 482 times)
    2.	PUNC --> PUNC_t	(Occurence: 469 times)
    3.	NP_NNP --> NNP_t(Occurence: 451 times)
    4.	NNP --> NNP_t	(Occurence: 408 times)
    5.	NN --> NN_t	(Occurence: 281 times)
* What are the top five highest-probability rules with left-hand side NNP, and what are their probabilities?
    1.	NP --> NNP NNP	(Probability: 0.1928)
    2.	NP --> NP NP*	(Probability: 0.1159)
    3.	NP --> DT NN	(Probability: 0.1014)
    4.	NP --> DT NNS	(Probability: 0.0855)
    5.	NP --> DT NP*	(Probability: 0.0841)
* Free Response: Did the most frequent rules surprise you? Why or why not?
    Not really, the most frequent rules would be things like Punctuation, Proper nouns, and other nouns are the most common parts of speech in sentences

## Part 3
* CKY parses using gold POS tags:
    Sentence 1:
    (TOP (S (NP (DT the) (NN flight)) (VP (MD should) (VP (VB arrive) (VP* (PP (IN at) (NP (CD eleven) (RB a.m))) (NP_NN tomorrow))))) (PUNC .))	Probability: -20.432453165513543

    Sentence 2:
    (TOP (S (NP_PRP i) (VP (MD would) (VP (VB like) (S_VP (TO to) (VP (VB find) (NP (NP (DT a) (NN flight)) (SBAR (WHNP_WDT that) (S_VP (VBZ goes) (VP* (PP (IN from) (NP (NNP la) (NP* (NNP guardia) (NN airport)))) (PP (TO to) (NP (NNP san) (NNP jose)))))))))))) (PUNC .))	Probability: -37.07221194904133

    Sentence 3:
    (TOP (S_VP (VB show) (VP* (NP_PRP me) (NP (NP (DT the) (NNS flights)) (NP* (PP (IN from) (NP_NNP newark)) (PP (TO to) (NP (NNP los) (NNP angeles))))))) (PUNC .))	Probability: -14.05035596365033

    Sentence 4:

    Sentence 5:
    (TOP (S_VP (VB show) (VP* (NP_PRP me) (NP (NP (DT the) (NP* (NNP t) (NNP w))) (NP* (NNP a) (NN flight))))) (PUNC .))	Probability: -15.293025795448274

    Sentence 6:
    (TOP (S (NP_PRP i) (VP (MD would) (VP (VB like) (S_VP (TO to) (VP (VB travel) (PP (TO to) (NP_NNP westchester))))))) (PUNC .))	Probability: -13.749954730718668

    Sentence 7:
    (TOP (S_VP (VB list) (NP (NP (NNP american) (NP* (NNP airlines) (NNS flights))) (NP* (PP (IN from) (NP (NNP new) (NP* (NNP york) (NNP newark)))) (PP (TO to) (NP_NNP nashville))))) (PUNC .))	Probability: -23.377904870031664

    Sentence 8:
    (TOP (INTJ_UH thanks) (PUNC .))	Probability: -5.457455587886334

    Sentence 9:
    (TOP (SBARQ (WHNP_WHNP (WDT what) (NNS flights)) (SQ (VBP are) (SQ* (NP_NP_EX there) (SQ* (PP (IN from) (NP_NNP nashville)) (PP (TO to) (NP (NP (NNP houston) (NP* (NN tomorrow) (NN evening))) (SBAR (WHNP_WDT that) (S_VP (VBP serve) (NP_NN dinner))))))))) (PUNC ?))	Probability: -24.920365753804205

    Sentence 10:
    (TOP (S (NP_PRP i) (VP (MD 'd) (VP (VB like) (S_VP (TO to) (VP (VB fly) (NP (JJ next) (NNP friday))))))) (PUNC .))	Probability: -16.968303330244407

* CKY parses using predicted POS tags:
    Sentence 1:
    (TOP (S (NP (DT the) (NN flight)) (VP (MD should) (VP (VBP arrive) (VP* (PP (IN at) (NP (CD eleven) (RB a.m))) (NP_NN tomorrow))))) (PUNC .))	Probability: -22.735038258507586

    Sentence 2:
    (TOP (S (NP_PRP i) (VP (MD would) (VP (VB like) (S_VP (TO to) (VP (VB find) (NP (NP (DT a) (NN flight)) (SBAR (WHNP_WDT that) (S_VP (VBZ goes) (VP* (PP (IN from) (NP (NNP la) (NP* (NNP guardia) (NNP airport)))) (PP (TO to) (NP (NNP san) (NNP jose)))))))))))) (PUNC .))	Probability: -34.87498737170512

    Sentence 3:
    (TOP (S_VP (VB show) (VP* (NP_PRP me) (NP (NP (DT the) (NNS flights)) (NP* (PP (IN from) (NP_NNP newark)) (PP (TO to) (NP (NNP los) (NNP angeles))))))) (PUNC .))	Probability: -14.05035596365033

    Sentence 4:

    Sentence 5:
    (TOP (S_VP (VB show) (VP* (NP_PRP me) (NP (NP (DT the) (NP* (NNP t) (NNP w))) (NP (DT a) (NN flight))))) (PUNC .))	Probability: -16.268394941752202

    Sentence 6:
    (TOP (S (NP_PRP i) (VP (MD would) (VP (VB like) (S_VP (TO to) (VP (VB travel) (PP (TO to) (NP_NNP westchester))))))) (PUNC .))	Probability: -13.749954730718668

    Sentence 7:
    (TOP (S_VP (VB list) (NP (NP (NNP american) (NP* (NNP airlines) (NNS flights))) (NP* (PP (IN from) (NP (NNP new) (NP* (NNP york) (NNP newark)))) (PP (TO to) (NP_NNP nashville))))) (PUNC .))	Probability: -23.377904870031664

    Sentence 8:
    (TOP (INTJ_UH thanks) (PUNC .))	Probability: -5.457455587886334

    Sentence 9:
    (TOP (SBARQ (WHNP_WHNP (WDT what) (NNS flights)) (SQ (VBP are) (SQ* (NP_NP_EX there) (SQ* (PP (IN from) (NP_NNP nashville)) (PP (TO to) (NP (NP (NNP houston) (NP* (NN tomorrow) (NN evening))) (SBAR (WHNP_WDT that) (S_VP (VBP serve) (NP_NN dinner))))))))) (PUNC ?))	Probability: -24.920365753804205

    Sentence 10:
    (TOP (S (NP_PRP i) (VP (MD 'd) (VP (VB like) (S_VP (TO to) (VP (VBP fly) (NP (JJ next) (NNP friday))))))) (PUNC .))	Probability: -16.843140187290402

* Free response:
