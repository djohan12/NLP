# NLP HW1

Please find the homework assignment instructions [here](https://docs.google.com/document/d/1K8s_Ecms0cIqRO1PKPFs2bfFVFfZpc1nFoEhtxRlCaM/edit?tab=t.0).

## Part 1
* Unigram accuracy: 
    - Validation: 17.345%
    - Tesing:     17.464%
* 5-gram accuracy:
    - Validation: 57.943%
    - Testing:    57.285% 
* Free response:
    - 1 Gram: 
        <BOS>"I'm not ready to go," said                                                                                                    
        <BOS>Lily and Max were best friends. One day                                                                                                    
        <BOS>He picked up the juice and                                                                                                    
        <BOS>It was raining, so                                                                                                    
        <BOS>The end of the story was

    - 5 Gram:
        <BOS>"I'm not ready to go," said, "i wanted to the boy who listen the boy who listen the boy who listen the boy who listen the boy w
        <BOS>Lily and Max were best friends. One day, the boy who listen the boy who listen the boy who listen the boy who listen the boy who listen the
        <BOS>He picked up the juice and said, "i wanted to the boy who listen the boy who listen the boy who listen the boy who listen the 
        <BOS>It was raining, so happy and said, "i wanted to the boy who listen the boy who listen the boy who listen the boy who l
        <BOS>The end of the story was a little girl named lily was a little girl named lily was a little girl named lily was a little gir

    The 5 gram is significantly better because it takes in more context in order to determine what the next word will be. However, they are both lacking because they only take in the frequency of words without any regard for grammar or sentence structure.


## Part 2
* RNN accuracy:
    - Validation: 59.409%
    - Testing:    58.908%
* Link to saved model: https://github.com/djohan12/NLP/blob/main/homework01/rnn_model.pth
  
## Part 3
* LSTM accuracy: 
    - Validation: 62.010%
    - Testing:    61.149%
* Link to saved model: https://github.com/djohan12/NLP/blob/main/homework01/lstm_model.pth
  
* Free response:
    - RNN:
        
        <BOS>"I'm not ready to go," said's and the boy named tim.<EOS>" the boy named tim.<EOS>" the boy named tim.<EOS>" the boy named tim.<EOS>" the boy n
        <BOS>Lily and Max were best friends. One day with her happy and said, "i'm some and happy and said, "i'm some and happy and said, "i'm some and 
        <BOS>He picked up the juice andy, he was so happy and said, "i'm some and happy and said, "i'm some and happy and said, "i'm some a
        <BOS>It was raining, son and said, "i'm some and happy and said, "i'm some and happy and said, "i'm some and happy and said
        <BOS>The end of the story was and said, "i'm some and happy and said, "i'm some and happy and said, "i'm some and happy and said,

    - LSTM:

        <BOS>"I'm not ready to go," saidy.<EOS>.<EOS> the said, "i'm sorry, so she was so happy and said, "i'm sorry, so she was so happy and said, 
        <BOS>Lily and Max were best friends. One day and said, "i'm sorry, so she was so happy and said, "i'm sorry, so she was so happy and said, "i'm 
        <BOS>He picked up the juice andy said, "i'm sorry, so she was so happy and said, "i'm sorry, so she was so happy and said, "i'm sor
        <BOS>It was raining, son the store.<EOS> and said, "i'm sorry, so she was so happy and said, "i'm sorry, so she was so happy an
        <BOS>The end of the story was a big brown and said, "i'm sorry, so she was so happy and said, "i'm sorry, so she was so happy and

    a. The RNN handles short-term dependencies whereas the LSTM is able to handle longer streams of text, which has more contextual consistency, but loses grammatical structure over time.

    b. The Neural networks are much better than the N-gram models. They are able to understand more context and generate longer consistent text. The N-gram is only able to remember the nth previous words, so the context preservation is much worse.

    c. Like I mentioned earlier, the N-gram model suffers from only generating based off the previous n words and doesn't have any grammatical structure. The Neural model also suffers from the grammatical issues, but usually to a lesser extent. Another issue they both share is that for these smaller data sets, they tend to get repetitive. A couple possible solutions include adding more training data, or adding more layers to the models so that they can better interpret dependencies and context.
