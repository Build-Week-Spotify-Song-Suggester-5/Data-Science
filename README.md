# Data-Science

#### General Guide
- [Lambda School Project Explanation, Guidelines, and Team Roles](https://airtable.com/shrtA1m4LFJAnjvqS/tblI02wuarVEYWVSv/viw2L09271lKsRt5x/recsd9pTmzGNlk2re?blocks=hide)
- [Song Suggester Architecture](https://www.notion.so/Spotify-Song-Suggester-0fd8e64d69c54e03a7884eec81885dbc)
- [Team Github](https://trello.com/c/i2p8e44L/5-ml-engineers)
- [A Guide to what other roles within our team are doing](https://www.notion.so/Working-Effectively-Across-Tracks-7be8d0eb25a14418b1e2a93ddde1d561)

#### Machine Learning Engineer Links

- [Kaggle Set](https://www.kaggle.com/tomigelo/spotify-audio-features)
- [Data Science Rubric](https://www.notion.so/Data-Science-Unit-4-814c17e421334cd8b3d2867d1d49f541)

### Project Details

 #### *Background*

> Create an algorithm to recommend songs based on user input songs. In production, Spotify uses a mixture of Deep Learning, Collaborative Filtering, persistent user 'taste profiles', frequent itemset mining, and some sort of neighbors algorithm based on
taste profiles, time listened, etc. Competitor Pandora has hired musiciologists to work on their 'music genome project' which
is probably more of a feature engineering thing using domain experts.

#### *We chose this model because:*

We ended up using only Nearest Neighbors. Couldn't find a data set to do CF on. Feature engineering included scraping genres,
predicting languages of the track_names, and sentiment analysis of the track names. While we found several research papers on using
Neural Networks, LSTMs on Nearest Neighbors, we were unable to find source code or pre-trained models or create one in the time alotted.

Research into siamese network matching algorithms looks more promising as they train much faster but we were also unable
to create or find a ready to use model in the time alotted. Also Siamese networks scale much better than Nearest Neighbors as the
dataset increases in size.


Read more [here: K-Nearest Neighbors](https://towardsdatascience.com/machine-learning-basics-with-the-k-nearest-neighbors-algorithm-6a6e71d01761) &  [here: K-Nearest Neighbors Documentation](https://scikit-learn.org/stable/modules/neighbors.html)


#### *Our Goal:*

> **Pitch**: Build an app to enable users to browse and visualize audio features of over 116k spotify songs.

MVP: User can search for a specific song and see its audio features displayed in a visually appealing way. The app also identifies songs with similar audio features.
DS:
1. Build a model to recommend songs based on similarity to user input (I like song x, here are n songs like it based on these similar features)
2. Create visualizations using song data to highlight similarities and differences between recommendations.

#### Further Reading & Resources:

https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/

https://www.reddit.com/r/MachineLearning/comments/2f8jff/using_neural_networks_for_nearest_neighbor/

https://towardsdatascience.com/how-to-build-a-simple-song-recommender-296fcbc8c85

https://medium.com/hulu-tech-blog/applying-deep-learning-to-collaborative-filtering-how-hulu-builds-its-industry-leading-3b10a4ed7470

https://arxiv.org/pdf/1605.09477.pdf

https://medium.com/@b.terryjack/nlp-pre-trained-sentiment-analysis-1eb52a9d742c

https://arxiv.org/pdf/1810.12575.pdf

https://blogs.cornell.edu/info4220/2016/03/18/spotify-recommendation-matching-algorithm/

http://www.mmds.org/

Future Teams are welcome to build upon our data set which includes genres, predicted track languages here:
https://raw.githubusercontent.com/Build-Week-Spotify-Song-Suggester-5/Data-Science/master/spotify_unique_track_id_lang.csv

The script to predict sentiment is still running and will be done soon(TM) but maybe your machines are faster and you can run it here:
https://github.com/Build-Week-Spotify-Song-Suggester-5/Data-Science/blob/master/Sentiment_Feature_Script.ipynb

Note that it only runs sentiment analysis on the top 75000 songs by popularity because of database size constraints for Flask.
