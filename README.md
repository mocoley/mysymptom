# mysymptom
This is project for MySymptom: Disease Dictionary
What if we could find out symptoms to a given symptom, from a symptom-disease database using Python? This model that I found on github does just that. This model can be used to predict symptoms that are closely related to a given symptom. The idea behind the model is that the user enters a symptom, and a list of similar symptoms will appear which the user selects the one that applies the most to them. The database contains a table of diseases and their associated symptoms. Here is how the model is designed:
1. After preprocessing, make the data into the symptom-disease format from the existing disease-symptom format.
2. Make symptoms the target words and the associated diseases the context words, and use this as the (target word, context word) pair for skip gram generation.
3. After assigning labels of 1 or 0 to the pairs, feed it into the Keras model, which generates new word vectors on top of existing Glove vectors
4. Loop through the set of all symptoms in the data set to find out the cosine similarity between the embeddings of the given symptom and current symptom in the loop, and then print out the symptoms with a high similarity score.
However, what this project does not include is that once the user selects their symptoms they still are not aware of what disease they may have. What I want to do is create an extension of this project that will use the symptoms to predict the disease the person is suffering from and redirect them to the associated specialist. We must keep in mind that this model is not intended to be replacement from visiting and being diagnosed by a doctor. It is more so there to help users learn of possible symptoms and diseases so that once they visit their physician, they can help point them in the right direction.
