# Overtone
Quality Content for Everyone

The first exercise requires me to write a function in Python that takes in a set of synonyms and two sentences and returns a Boolean value indicating whether the sentences are equivalent according to the given synonyms. The second exercise is similar to the first one, but with the added assumption that (a, b) and (a, c) do imply (b, c). This means that if two words are synonyms, and one of them is synonym with a third word, then the second and the third words are also synonyms.

Below are the steps to solve both problems. By step four, both exercises have the same solution. Only for the second exercise, one more step should be added to the solution.

- Case-insensitivity: Converting text to lowercase makes it case-insensitive.
- Breaking down text into a list of words.
- Replace each word in the list with its synonym, if one exists in the given set of synonyms.
- Compare the resulting lists of words. If they are the same, the sentences are equivalent.
- JUST FOR THE SECOND EXERCISE: Repeat steps 3 and 4 for any new synonyms that are found until no more synonyms are found in the lists
