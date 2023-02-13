# Eager vs Lazy Learning

There are essentially two approaches in machine learning by which models learn and perform predictions. On a broad level, they can be classified as eager and lazy learning.

To understand these methods, let's take an example. Let's say there are two students A and B who go to the library and borrow textbooks relevant to their coursework. A, being very studious, completes the entire textbook within a week and returns it to the library. B on the other hand is more interested in playing Valorant and doesn't even bother opening the book.

Now, if you ask A any question related to the subject, you get your answer instantly. But when you question B, he has to open the book, search for the answer to your question and then reply. In this case, A represents eager learning, B represents lazy learning and the textbook represents the training data.

Eager learning involves training the model on the dataset and inferring rules and discovering patterns, whereas no training takes place in lazy learning and pattern discovery is postponed until the model is asked to make a prediction.

So eager learning is obviously the better option, right? Well, it depends. Both these methods have their merits and demerits, as listed below-

### Lazy Learning

Merits-

* No need to train the model.
    
* Target function is approximated locally(we only need to refer to the data that is similar to the new instance, i.e., the data point being queried for prediction, instead of the entire dataset).
    
* Adapting to new and constantly changing data is easy.
    

To understand the second point, let's go back to our example. When we ask B a question, he need not look through the entire textbook for the answer, just the chapters relevant to the question.

Demerits-

* Training data needs to be stored at all times.
    
* Slow to evaluate as execution begins after a query is received.
    

Examples-

* K-Nearest Neighbors (KNN)
    
* Locally Weighted Learning (LWL)
    
* Case-Based Reasoning
    

### Eager Learning

Merits-

* Training data can be discarded after model is trained, i.e., lesser storage space is required.
    
* Evaluation is fast since pattern discovery has already been done.
    

Demerits-

* Model needs to be trained on the entire dataset, which can be computationally expensive if the dataset is large.
    
* Generally fails to provide good local approximations for the target function.
    

Examples-

* Bayesian classification
    
* Decision trees
    
* Support Vector Machines (SVM)
    

If you found this helpful, consider liking and sharing it, and subscribing to my newsletter. Feel free to leave your thoughts, questions and ponderings in the comments.

You can also follow me for more data and ML-related content. I focus on demystifying technical jargon and encouraging newcomers in the field by explaining concepts as simply as possible.

This is Sachin being succinct :)
