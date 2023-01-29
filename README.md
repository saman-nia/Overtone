# Quality Content for Everyone     
     
<p align="center">
  <a href="https://colab.research.google.com/github/saman-nia/Overtone/blob/main/Technical_Exercises_Overtone.ipynb">
    <img src="https://raw.githubusercontent.com/saman-nia/Overtone/main/colab.svg"
         alt="Run the script in google colb" width="200" height="40">
  </a>
</p>

<!-- About The Project -->
# About The Project
The function first converts the sentences to lowercase and tokenizes them into individual words. Then, it replaces certain words in the sentences with their synonyms, specified in the input "synonyms" dictionary. Finally, it compares the two lists of words and returns a string indicating whether the sentences are equal or not. Below are the steps to solve both problems. By step four, both exercises have the same solution. Only for the second exercise, one more step should be added to the solution.

- Breaking down text into a list of words.
- Case-insensitivity: Converting text to lowercase makes it case-insensitive.
- If one word is in the given set of synonyms, replace each word in the list with its synonym.
- Finally, compare the final lists of words and if they are the same, the sentences are equivalent.
- JUST FOR THE SECOND EXERCISE: Repeat steps 3 and 4 for any new synonyms that are found until there is no more synonyms in the lists.


<!-- Built With -->
# Built With
This repository contains a Python script that implements a function for comparing two sentences and determining whether they are equivalent according to a given set of synonyms. The function, called comparable(), has the following parameters:

- synonyms: a set of synonyms in the form of a dictionary
- sentence1: the first sentence to be compared
- sentence2: the second sentence to be compared
- implies (optional, default=False): a boolean value indicating whether the additional assumption (a, b) and (a, c) do imply (b, c) should be used

<!-- Usage -->
# Usage
To use the function, simply import the script and call the comparable() function with the desired parameters. For example:

```python
     from synonym_comparator import comparable

     synonyms = {"happy": "content", "sad": "unhappy"}
     sentence1 = "I am happy"
     sentence2 = "I am content"

     print(comparable(synonyms, sentence1, sentence2)) # Output: "The sentences are equivalent"

   ```

The function accepts four parameters: a set of synonyms, two sentences and an additional parameter implies that is set to False by default. If implies is set to true, the function will solve the second task by using the while loop to replace words with synonyms found in the previous iteration, if not, the function will solve the first task by using the initial way of replacing.

This function compares two sentences and checks if they are equal or not. It first converts the sentences to lowercase and tokenizes them (i.e. breaking them down into individual words). Then, it replaces certain words in the sentences with their synonyms, specified in the input "synonyms" dictionary. Finally, it compares the two lists of words and returns a string indicating whether the sentences are equal or not.

However, in the case of having a large dataset, a similar way to solve this problem would be to use a natural language processing library such as NLTK to tokenize the sentences and then compare the resulting list of words, however as mentioned, it requires having a large dataset to train a model and solve any test sets. So, instead of using a dictionary to replace words with their synonyms, I could also use a word embedding model such as word2vec to find semantically similar words and then compare the resulting list of words. Another solution would be to use a pre-trained model for text classification such as BERT, to encode the input sentences and then compare the resulting embeddings using a similarity metric such as cosine similarity.
