---
title: "Natural Language Processing: An introduction"
seoTitle: "Introduction to Natural Language Processing"
seoDescription: "All you need to get started with Natural Language Processing."
datePublished: Sun Mar 12 2023 10:06:43 GMT+0000 (Coordinated Universal Time)
cuid: clf58e1b6000709k02c6phvz7
slug: natural-language-processing-an-introduction
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678615356000/becf70bd-0357-4cf5-9f8a-05b63d1a5681.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1678615527876/5137e2f5-66eb-49de-b184-ae7c2f244889.png
tags: introduction, data-science, machine-learning, nlp, natural-language-processing

---

If you've been interested in Artificial Intelligence and Machine Learning, you may have come across the abbreviation "NLP" before. The expansion of NLP, i.e., Natural Language Processing arouses the question, "What is natural language?". Well, this blog, for example, is a form of natural language. When we speak to our friends (or foes), the act of speaking is a form of natural language. Any form of verbal or written communication among human beings represents natural language.

Let's take an example to understand a basic use case of NLP. If you've used Google Assistant, Siri, Cortana, etc. before, you've already utilized an NLP application. But of course, these chatbots or machines don't understand language the same way you and I do.

To us, "Add an hour of exercise and an hour of meditation to my schedule" seems structured enough and easy to understand. But how can machines understand what we're saying? Well, they convert these words into what is known as vectors, which are just numerical representations of words. We'll discuss the different vectorization techniques in a different blog.

Some tasks that can be performed in NLP are-

1. ### Tokenization
    
    Converting a string of words into smaller chunks is known as tokenization. For example, the sentence, "Add an hour of exercise and an hour of meditation to my schedule" consists of 13 tokens (one word is considered as one token in this case).
    
2. ### Stemming/Lemmatization
    
    Most languages consist of words that are derived from other words. The changes made to the base form of a word to express different grammatical meanings are known as inflections. For example, "found" is an inflection of the word, "find". Both stemming and lemmatization focus on deriving the root form of a word, but they have a major difference.
    
    Stemming removes letters from the end of a word until the stem is identified. Stemming the words, "boats" and "boating", you would get, "boat". The drawback of stemming can be seen by applying it to the word "caring", where you would obtain "car". However, car and caring don't have the same meaning.
    
    Lemmatization, on the other hand, identifies the lemma, or the dictionary form of the base word. Applying it to the word "caring", you would get "care".
    
3. ### Part-of-speech (POS) tagging
    
    POS tagging is the process of labeling each word with its appropriate part of speech. Parts of speech refer to the category of each word in a sentence, such as nouns, pronouns, verbs, adjectives, etc. Identifying the categories of a word helps us to derive the context in which it was used.
    
    For instance, take the sentence- "I can play for hours". Here, the word "play" is a verb denoting the action of playing.
    
    However, when we say, "I'm going to watch a play", the word "play" acts as a noun. Therefore, although the word "play" is the same, the context in which it is used makes a world of difference.
    
    You might even call it a play on words (Ba dum tss!).
    
4. ### Named Entity Recognition (NER)
    
    This is the process of classifying a named entity (a proper noun such as names, geographic locations, etc) into their respective categories. NER helps us classify, "Jeff" as a name and "Tuscany" as a location.
    

I'll be going into more detail about NLP in my future blogs, so make sure to subscribe to my newsletter to be notified. If you found this helpful, consider liking and sharing it, and please feel free to leave your thoughts, questions and ponderings in the comments.

You can also follow me for more data and ML-related content. I focus on demystifying technical jargon and encouraging newcomers in the field by explaining concepts as simply as possible.

This is Sachin being succinct :)
