## Introduction
Language bias is a significant area of discussion when it comes to mass media. Another major area of mass media is sports coverage, and the accompanying commentary of live sporting events. Specifically when considering American football (henceforth “football”), -a sport that regularly draws tens of millions of viewers , studying racial biases in commentary is important. Implicit racial biases in sports commentary have predominantly been studied from a social sciences perspective - on small-scale datasets and subjective annotation of “racial” language. However, more recently, this area of research has garnered attention due to harmful impacts of implicit racial biases including involuntarily profiling and segregating marginalized groups. Iyyer et al conduct a major study into football commentary from 1960-2019, collected from YouTube videos of full games and have produced the dataset titled FOOTBALL [X]. Although their work affirms the conclusions of previous social science analyses (that point to the fact that commentators tend to compliment caucausian players for their strategy and intelligence while providing applause to colored players for their strength and other physical attributes), the simplistic NLP approaches applied lack the sophistication to handle the temporal as well as confounding characteristics of the data. For example, it was hard for their model to identify if a descriptive comment was in reference to a player’s physical characteristics or his position. We seek to apply modern NLP methods to improve upon some of the limitations highlighted by Iyyer et al and hence provide deeper insight into implicit racial bias in sports commentary.

## Motivation and Background
Our main goal is to enhance bias detection capabilities - using sports commentary and the FOOTBALL corpus as our target domain. Previous work largely consists of simplistic models with significant limitations [1]. By employing sophisticated NLP/ML methods, we hope to extract more insights from the corpus and look to answer the following questions:
* What model / term extraction strategy best handles temporal bias and confounding factors in the FOOTBALL corpus? 
* How do perturbations in various model parameters lead to stronger/more robust racial bias detection?
* How much does bias detection depend on the context i.e. if I use the same model on fashion show commentary describing models and not players will the model perform just as well?

## Proposed Approach/Experiments 
Keeping aside fine-tuning models, the three approaches we plan on employing are: 
* Method followed by Iyyer et al - an additive log linear model with potential covariate pairs to account for confounds in the data [1]. While it has limitations, we want to explore  different covariate pairs and vary the number of  tokens extracted per instance to formulate a well-established baseline  
* Neural  attention mechanisms.  These methods have been applied to key term extraction problems before to identify the importance of words in relation to each other in whole sequences. We believe by leveraging word embeddings and context-specific attention strategies we will be able to tackle the confounding factors of whether descriptions are role or character specific.
* Lastly, applying coreference resolution methods also serve as an alternative to tackle the confounding problem stated above. These methods help identify which words or phrases are relative to the entity or the position-specific features of the entity/players. 

We believe the above stated methods would be able to tackle some of the limitations mentioned in the paper by Iyyer et al. By leveraging preliminary insights from their work, we believe our modeling will account for the confounding issues in the corpus and provide more generalizable solutions for bias detection. 

## Project Value
We believe that our experiments will present a significant contribution to the study of language bias within the field of NLP. By extending the work of Iyyer et al, we will represent the first of efforts to apply neural methodologies in sports commentary bias - a crucial part of mass media. Further, our methods would provide a foundation for further research into racial/cultural bias analyses for different domains and across different time periods.

## References
[1]https://www.aclweb.org/anthology/D19-1666.pdf<br>
[2]https://medium.com/better-programming/understanding-racial-bias-in-machine-learning-algorithms-1c5afe76f8b<br>
[3]https://theundefeated.com/features/tony-dungy-some-announcers-biased-language-perpetuates-black-qb-stereotypes/



