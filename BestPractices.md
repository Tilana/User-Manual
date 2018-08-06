##  Best Practices - Machine Learning



#### How to select a good evidence sentence?

- choose a representative sample phrase
- stick to one concept which can be specified as necessary (e.g. religious symbols in public institutions)
- give priority to short, but precise expression (e.g. access to information) as long  sentences and words asscociated with other concepts introduce noise  
- avoid too broad or very frequent terms, e.g. the court, applicant, law, 



#### When to start accepting/rejecting suggestions?

- wait until around 10 suggestions appear before accepting or rejecting them. Stop the running algorithm, press *Retrain* to train the neural network and *Toggle predict* to get suggestions based on the provided sentences.



#### How to train the classifier?
 - balance the number of positive and negative sample sentences
 - choose sample sentences that cover the different facets of a category,
  e.g. to classify documents about discrimination include sentences about racial, gender, religious, etc. discrimination
 - to improve the classifier, accept/reject about 10 suggested sentences, then *Retrain* and afterwards *Toggle predict* the category 


