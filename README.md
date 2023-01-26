# Overtone
Quality Content for Everyone     
     
<p align="center">
  <a href="https://colab.research.google.com/github/saman-nia/Overtone/blob/main/Technical_Exercises_Overtone.ipynb">
    <img src="https://raw.githubusercontent.com/saman-nia/Overtone/main/colab.svg"
         alt="Run the script in google colb" width="300" height="54">
  </a>
</p>


The first exercise requires me to write a function in Python that takes in a set of synonyms and two sentences and returns a sentence indicating whether the sentences are equivalent according to the given synonyms. The second exercise is similar to the first one, but with the added assumption that (a, b) and (a, c) do imply (b, c). This means that if two words are synonyms, and one of them is synonym with a third word, then the second and the third words are also synonyms.

Below are the steps to solve both problems. By step four, both exercises have the same solution. Only for the second exercise, one more step should be added to the solution.

1- Breaking down text into a list of words.
2- Case-insensitivity: Converting text to lowercase makes it case-insensitive.
3- If one word is in the given set of synonyms, replace each word in the list with its synonym.
4- Finally, compare the final lists of words and if they are the same, the sentences are equivalent.
5- JUST FOR THE SECOND EXERCISE: Repeat steps 3 and 4 for any new synonyms that are found until there is no more synonyms in the lists.

In the script, I've defined a function called ***comparable()*** which accepts four parameters: a set of synonyms, two sentences and an additional parameter implies that is set to False by default. If implies is set to true, the function will solve the second task by using the while loop to replace words with synonyms found in the previous iteration, if not, the function will solve the first task by using the initial way of replacing.

This function compares two sentences and checks if they are equal or not. It first converts the sentences to lowercase and tokenizes them (i.e. breaking them down into individual words). Then, it replaces certain words in the sentences with their synonyms, specified in the input "synonyms" dictionary. Finally, it compares the two lists of words and returns a string indicating whether the sentences are equal or not.

However, in the case of having a large dataset, a similar way to solve this problem would be to use a natural language processing library such as NLTK to tokenize the sentences and then compare the resulting list of words, however as mentioned, it requires having a large dataset to train a model and solve any test sets. So, instead of using a dictionary to replace words with their synonyms, I could also use a word embedding model such as word2vec to find semantically similar words and then compare the resulting list of words. Another solution would be to use a pre-trained model for text classification such as BERT, to encode the input sentences and then compare the resulting embeddings using a similarity metric such as cosine similarity.
