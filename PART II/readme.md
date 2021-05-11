# Part II

In this part, we firstly did some data cleaning and categorized productes using regex, see [codes](https://github.com/liyue34673/DSO_560_NLP_Project_2021_Black/blob/main/PART%20II/Part%20II_Data%20Cleaning%20and%20Preprocessing.ipynb) here. Then We create functions for searching matched products and give recommendation outfit combinations.

Input: a string of query

Output: Printed sentences indicating search results

## Overall query logic

* If the query is a product ID
 
  * In human domain experts' combinations: print out related experts' combos
  
  * Not In human domain experts' combinations: find the most similar product

* Vectorize query and dataset columns (Here we use name and description!)
  
  * One thing to be attentioned: we weighted name and description, since name matters more and too many noisy words in description

* Using cosing similarity to find the most similar product

  * Similarity should be more than a threshold

  * The most similar product should be a clothing

* Return the most similar product and recommendated outfit combinations

## Our methodology

* Good functions
  * [Unigram & Bigram](https://github.com/liyue34673/DSO_560_NLP_Project_2021_Black/blob/main/PART%20II/PART%20II_Function_Unigram%26Bigram.ipynb)
  * [TF-IDF](https://github.com/liyue34673/DSO_560_NLP_Project_2021_Black/blob/main/PART%20II/Part%20II_Function_TF_IDF.ipynb)
  * [TF-IDF Weighted Word Embedding](https://github.com/liyue34673/DSO_560_NLP_Project_2021_Black/blob/main/PART%20II/Part%20II_Final_Function_TF-IDF%20Weighted%20Word%20Embedding.ipynb)

* Poor function
  * [Doc2vec](https://github.com/liyue34673/DSO_560_NLP_Project_2021_Black/blob/main/PART%20II/Part%20II_Function_Doc2vec.ipynb): might because the sample size is not enough

## Final Function

N-gram, TF-IDF and TF-IDF weighted word embedding all have good performances of our example queries. Considering the advance of algorithm, we decide the TF-IDF weighted word embedding as our final function.
