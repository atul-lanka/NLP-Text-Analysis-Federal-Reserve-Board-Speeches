# NLP-Text-Analysis-Federal-Reserve-Board-Speeches
Using Natural Language Processing (NLP) to analyze Federal Reserve (Fed) Speeches:

- Categorize the Federal Reserve Chairman’s speeches into categories or topics of interest 
- Identify trends in topics that each Chairman has uniquely discussed in their term
- Identify the numerous agencies they've created or supported in order to implement their policies
- Compare quantitative measures and clusters against key economic indicators such as Fed Funds Rate and Unemployment as well as historic events that have impacted our economy in the last two decades (2000 dot com bubble, 9/11, 2008 Housing Crisis, 2020 Covid-19 pandemic)  to determine whether there is any palpable correlation.
- Use sentiment analysis to compare tone and impartiality for each Chair’s addresses over their respective terms. 


## Research Method 

- To identify topics overall and unique to each speaker, the dataset is vectorized using TFIDF, Doc2Vec and Word2Vec as well. K-means clustering is applied on both the TFIDF and Doc2Vec matrices to get an initial idea at how the topics are shaping out. LDA topic modeling will also refine our results of topics and term similarity. This was performed using the TFIDF matrix as well as a bag of words.
- An initial ontology of topics will be created to reflect the overall scope of the Federal Reserve. In order to clean up the vocabulary and accentuate the topic clusters, terms from the TFIDF clusters, output vectors similar_by_word function for Word2Vec and domain knowledge aided in creating equivalence classes. 
- I used Doc2Vec to visualize speech similarity in a 2D space. Using Doc2Vec to reduce the dimensionality of the speech to a 20-dimensional vector, I then used Multi-Dimensional Scaling to plot each speech in two dimensions.
- LDA (Latent Dirichlet Allocation) was used to group speeches together based on probability of a word's frequency in a certain topic vs the frequency in all topics. A web-based interactive visualization of the topics created from the LDA is also generated to corroborate our initial results and understand which topics are most closely related. 
- Sentiment analysis is run on the original text dataset to test the idea that the Federal Reserve meticulously chooses its verbiage in order to abate market fluctuations and overreactions from analysts. These metrics will also be compared to the fluctuations of the Federal interest, unemployment and inflation rates to observe if there is any correlation. 

## Key Results
### WordCloud
<img width="469" alt="image" src="https://user-images.githubusercontent.com/74167574/216733717-95dac3a5-adcb-46ae-a0d0-0d0ae16f4c3d.png">

Janet Yellen
Topic	TFIDF K-means/ LDA Terms
![image](https://user-images.githubusercontent.com/74167574/216733788-fb51a263-ce0a-45c5-a563-aa4df3033d8c.png)

### LDA Model
<img width="586" alt="image" src="https://user-images.githubusercontent.com/74167574/216733993-82960ffb-e1a7-48e3-a138-d094bd6e2cf4.png">


### Sentiment Analysis and Subjectivity
<img width="466" alt="image" src="https://user-images.githubusercontent.com/74167574/216733943-3c6ba2f4-1036-41ea-b2d7-3e126d6d30b1.png">

<img width="458" alt="image" src="https://user-images.githubusercontent.com/74167574/216733947-21bb3188-b432-4ce4-9c46-87aeec4d47d6.png">

### Ontology
<img width="549" alt="image" src="https://user-images.githubusercontent.com/74167574/216733906-907c4b14-6a43-496a-b1f8-e2206f68c275.png">
