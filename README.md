# Quality Content for Everyone     
     
<p align="center">
  <a href="https://colab.research.google.com/github/saman-nia/Overtone/blob/main/Technical_Exercises_Overtone.ipynb">
    <img src="https://raw.githubusercontent.com/saman-nia/Overtone/main/colab.svg"
         alt="Run the script in google colb" width="200" height="30">
  </a>
</p>

<!-- About The Task -->
# About The Task
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

* [![Python][Python.com]][Python-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

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
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Optimization -->
# Optimization
In the case of having a large dataset, a similar way to solve this problem would be to use a natural language processing library such as NLTK to tokenize the sentences and then compare the resulting list of words.
Alternatively, using a word embedding model such as word2vec to find semantically similar words and then compare the resulting list of words. Another solution would be to use a pre-trained model for text classification such as BERT, to encode the input sentences and then compare the resulting embeddings using a similarity metric such as cosine similarity.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Note -->
# Note
This script is a basic implementation. It is not optimized for large datasets or real-world use cases.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
