# movie-summary-search
A search engine for movie plots' summaries.

Worked with a dataset of movie plot summaries that is available from the
Carnegie Movie Summary Corpus site. Built a search engine for the plot
summaries that are available in the file “plot summaries.txt” that is available under the Dataset link
of the above page.
Used the tf-idf technique to accomplish the above task.

Steps:

1. Extracted and uploaded the file plot summaries.txt from http://www.cs.cmu.edu/~ark/personas/
data/MovieSummaries.tar.gz to Databricks. Also uploaded a file containing user’s search terms
one per line.

2. Removed stopwords.

3. Created a tf-idf for every term and every document (represented by Wikipedia movie ID)
using the MapReduce method.

4. Read the search terms from the search file and output following:

(a) User enters a single term: You will output the top 10 documents with the highest tf-idf
values for that term.

(b) User enters a query consisting of multiple terms: An example could be “Funny
movie with action scenes”. In this case, you will need to evaluate cosine similarity between
the query and all the documents and return top 10 documents having the highest cosine
similarity values.


You can read more about cosine similarity at the following resources:
- http://text2vec.org/similarity.html : Read the cosine similarity section
- https://janav.wordpress.com/2013/10/27/tf-idf-and-cosine-similarity/
- https://courses.cs.washington.edu/courses/cse573/12sp/lectures/17-ir.pdf


For the search terms entered by the user, returned the list of movie names sorted by
their relevance values in descending order. 
