# Neural-Network-to-Learn-Logical-Semantics
This is the final project for CSE498 at Lehigh University.
 
## Related Papers
[1] RNN can Learn Logical Semantics. \
[2] Tree-Structured Composition in Neural Networks without Tree-Structured Architecture

## Related Repository
[1] https://github.com/sleepinyourhat/vector-entailment

## Dataset
The dataset is downloaded from the vector-entailment repository. \
Each entries are logical predicates, label with its satisfiability. If satisfiable, there has to exist on combination truth values of p and q that makes this predicate true. \

## Task
We make the prediction on satisfiability.

## Methods

#### Baseline: Sum of Vector
The implementation of the same type of baseline discussed in paper [1]. Since this method is lask of explainability, nothing can really be explained here. It reaches to 64.8 accuracy on the test set.

#### RNN: The LSTM
Intuitively, the LSTM layer capture sequencial relationships. But comparing to TreeRNN, it is recieve less amount of help from human knowledge. In this implementation, the parentheses are also encoded as indexes. It is interesting to see whether the LSTM algorithm can learn the semantics of parentheses through out the training. After tuning, it reaches to 72.0% accuracy on the test set.

#### Tree RNN
We implement the TreeRNN discussed in paper [1]. After tuning, it achieves 93.4% accuracy on the test set. In the paper, the TreeRNTN model archieve better accuracy. The implementation of TreeRNTN might be the future's work.

## Contribution
Previous work in repository [1] uses Matlab as parimary language. Our work uses python's pytorch library, and get a decent accuracy with TreeRNN. 
