# PCFG_ProbabilisticContext-FreeGrammar
Writing a PCFG, a Probabilistic Context-Free Grammar

More formally, a probabilistic context free grammar consists of:  
• A set of non-terminal symbols 
• A set of terminal symbols (which we can call the vocabulary)
• A set of rewrite or derivation rules, each with an associated probability 
• A start symbol 


The grammar rules will be written in two files, one for a grammar called S1 (and whose start symbol is S1) 
and one to assign non-terminal symbols for the words in the vocabulary of this limited language,
where these symbols can be thought of as POS tags, but are not required to be.  

There is a second grammar, S2, which you do not have to write and which will generate all word strings as a 
linear sequence with no structure if there is no rule in S1 that will apply.  This grammar is a convenience 
for the scoring function.  Essentially S2 is a backoff model.Rules will be written in simple text files, 
ending in the file extension “.gr”.  You will have a set of sentences to try to parse, given in a file called dev.sen. 
There is a java program provided that tries to parse these sentences with the PCFG in S1.gr, S2.gr and Vocab.gr.  
It scores the resulting parse trees with a perplexity measure, but in our assignment we are going to ignore these scores. 
(The perplexity measure is lower if your grammar models the sentences well;  that is, it is not surprised/perplexed by the sentences.)  
Instead, your goal is to produce as many parse trees as possible that use your rules from S1, instead of the backoff rules from S2. 
