# Attitudes in replies of downvoted comments in specialized and generalized communities

# Link to the project website

https://mitravasu-cscd25-data-story-site.vercel.app/

# Abstract

Reddit is a social platform that allows users to participate in user-created communities (called subreddits) by creating posts, commenting, and voting. We can loosely categorize these subreddits into two types: generalized and specialized. Generalized subreddits are those that are not centered around a niche subject, and can have discourse about anything. In this report, we will be using comments from r/AskReddit, r/funny and r/todayilearned. Specialized subreddits are those that are centered around a niche subject. In this report, we will be using comments from r/guitars, r/piano, and r/photography. We want to examine the difference in attitude towards negatively voted comments in these communities to uncover what emotions a user feels when they read these comments that diverge from the community's values. We will be using the Reddit text dataset in conjunction with the Reddit API to extract negatively voted comments and their first replies in specialized and generalized communities. We will be using the NRC Emotion Lexicon to conduct our sentiment analysis of the comments. Using this data and tools, we hope to find general trends in the attitudes of users in these communities. In addition, we will also explore the difference in attitudes towards positively voted comments in these communities, and also the how the emotions of the initial comment is related to the emotion of its replies. Finding trends in these interactions could help us understand how what responses we can expect when posting a comment with a certain sentiment.

# Definitions

**Specialized communities**: refers to communities that are centered around a niche subject. Examples: r/guitars, r/piano, r/photography

**Generalized communities**: refers to communities that can have discourse about anything. Examples: r/AskReddit, r/funny, r/todayilearned

# Research Questions

How do replies to negatively voted comments differ in attitude between specialized and generalized communities?

## Sub-questions:

1. How are these attitudes distributed across the two types of communities?
2. How do the attitudes of the replies relate to the attitudes of the initial comment?
3. How do the attitudes differ in replies to positively voted comments?

# Additional Datasets

In addition to the Reddit comments text dataset, we will be using the Reddit API to extract the first replies of the comments in this dataset.

To conduct the sentiment analysis of each comment and reply, we will be using the NRC Emotion Lexicon.

# Methods

We will be using the Reddit comments dataset which includes both metadata and text. As the dataset contains data from the top 5,000 subreddits, we will be reducing our focus to 3 specialized and 3 generalized communities. We will be using the following specialized communities: r/guitars, r/piano, and r/photography. We will be using the following generalized communities: r/AskReddit, r/funny, and r/todayilearned.

From our dataset of Reddit comments, we will be extracting the comments for the above mentioned communities. We will then use the Reddit API to get the first replies to these comments, and store them in a seperate file. We will perform this step for both positively and negatively voted comments.

Next we will use the NRC-Emotion-Lexicon to determine the emotion of the comments and replies. The NRC Emotion Lexicon will represent the sentiment of each comment and reply as an array of 8 emotions: anger, anticipation, disgust, fear, joy, sadness, surprise, and trust and 2 polarities: positive, negative.

To answer our first sub-question, we will aggregate the emotion scores and polarity scores for the comments and replies for the two types of subreddits, and find the distribution of the emotions and polarities.

To answer of second sub-question, we will determine the frequency with which an emotion in the comment text appears with an emotion in the reply text, and the frequency with which each polarity in a comment appears with each polarity in the reply. This will give us a better sense of the relationship between the emotions and polarities of comments and replies.

To answer our third sub-question, we will repeat the steps for the first sub-question, but for positively voted comments.

By answering these three sub-questions, we will be able to determine the difference in attitudes towards negatively voted comments between specialized and generalized communities.
