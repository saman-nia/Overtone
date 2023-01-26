# Overtone
Quality Content for Everyone

The first exercise requires me to write a function in Python that takes in a set of synonyms and two sentences and returns a Boolean value indicating whether the sentences are equivalent according to the given synonyms. The second exercise is similar to the first one, but with the added assumption that (a, b) and (a, c) do imply (b, c). This means that if two words are synonyms, and one of them is synonym with a third word, then the second and the third words are also synonyms.

Below are the steps to solve both problems. By step four, both exercises have the same solution. Only for the second exercise, one more step should be added to the solution.

- Case-insensitivity: Converting text to lowercase makes it case-insensitive.
- Breaking down text into a list of words.
- Replace each word in the list with its synonym, if one exists in the given set of synonyms.
- Compare the resulting lists of words. If they are the same, the sentences are equivalent.
- JUST FOR THE SECOND EXERCISE: Repeat steps 3 and 4 for any new synonyms that are found until no more synonyms are found in the lists



This function compares two sentences and checks if they are equal or not. It first converts the sentences to lowercase and tokenizes them (i.e. breaking them down into individual words). Then, it replaces certain words in the sentences with their synonyms, specified in the input "synonyms" dictionary. Finally, it compares the two lists of words and returns a string indicating whether the sentences are equal or not.

However, in the case of having a large dataset, a similar way to solve this problem would be to use a natural language processing library such as NLTK to tokenize the sentences and then compare the resulting list of words, however as mentioned, it requires having a large dataset to train a model and solve any test sets. So, instead of using a dictionary to replace words with their synonyms, I could also use a word embedding model such as word2vec to find semantically similar words and then compare the resulting list of words. Another solution would be to use a pre-trained model for text classification such as BERT, to encode the input sentences and then compare the resulting embeddings using a similarity metric such as cosine similarity.



In the script, I've defined the function comparable which accepts four parameters: a set of synonyms, two sentences and an additional parameter implies that is set to False by default. If implies is set to true, the function will solve the second task by using the while loop to replace words with synonyms found in the previous iteration, if not, the function will solve the first task by using the initial way of replacing.
