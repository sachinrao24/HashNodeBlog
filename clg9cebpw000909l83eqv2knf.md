---
title: "Bag of Words simplified"
seoTitle: "A simplified explanation of Bag of Words in NLP"
seoDescription: "This articles provides a foundational understanding of the Bag of Words concept in NLP."
datePublished: Sun Apr 09 2023 11:49:42 GMT+0000 (Coordinated Universal Time)
cuid: clg9cebpw000909l83eqv2knf
slug: bag-of-words-simplified
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1681040771398/1f1b1acf-04e8-4d2a-8000-c0212efadc5e.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1681040901146/87c43182-4c84-4bdc-839d-fdad0e2d313c.jpeg
tags: data, data-science, machine-learning, natural-language-processing

---

The Bag of Words (BoW) model in NLP can be referred to as a feature extraction technique where only the frequency of each word is noted. You can think of the BoW model as an actual bag, where you just dump all the words and then count the number of occurrences.

If you are completely new to NLP, you can learn the basics of it within 3 minutes, by reading [this article](https://sachinrao.hashnode.dev/natural-language-processing-an-introduction).

Since NLP models cannot work on raw text, BoW can be used to convert this text into vectors, which are basically a numerical representation of the text. Let's see how this works by taking the following text data-

> Chaos isn't a pit, chaos is a ladder.

This text is first tokenized to extract the individual words, and then stored in the form of a dictionary with the keys being the words and the values being the number of times they occur. After converting all characters to lowercase, the dictionary would look like this-

```python
{
"chaos": 2,
"isn't":1,
"a":2,
"pit":1,
"is":1,
"ladder":1
}
```

Now, if we take another statement-

> Chaos is a ladder.

By referring to our dictionary, the BoW vector for this statement can be represented as-

```python
[1, 0, 1, 0, 1, 1]

#The order of the words in the dictionary are-
#["chaos", "isn't", "a", "pit", "is", "ladder"]

#The 1s imply that the word exists in the given statement, and the 0s imply that it doesn't.
```

It should be noted that this model does have the disadvantage that it completely ignores the order of the words and the context in which they were used, which is crucial in most text-processing applications.

However, it is a very simple and easy-to-use model and can be used to create an initial vector representation before moving on to more complex techniques.

I'll be going into more detail about NLP in my future articles, so make sure to subscribe to my newsletter to be notified. If you found this helpful, consider liking and sharing it, and please feel free to leave your thoughts, questions and ponderings in the comments.

You can also follow me for more data and ML-related content. I focus on demystifying technical jargon and encouraging newcomers in the field by explaining concepts as simply as possible.

This is Sachin being succinct :)