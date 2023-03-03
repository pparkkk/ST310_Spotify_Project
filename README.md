# ST310_Spotify_Project

This is a course project for the ST310 Machine Learning module. We attempt to compare the performance of different prediction models in predicting the popularity of a song based on their characteristics.


## Brief description of dataset

This is a dataset of [Spotify tracks](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset) over a range different genres, covering 114000 tracks. Each track has 21 audio features associated with it, ranging from artist name, popularity, duration, genre, ‘acousticness’, and tempo. All measures that can’t be measured directly such as ‘acousticness’, ‘danceability’, ‘instrumentalness’, have been normalised to a scale of 0-1.


## Variables Description

We will predict the popularity of a song given the following characteristics:

1. **popularity**: The popularity of a track is a value between 0 and 100, with 100 being the most popular. The popularity is calculated by algorithm and is based, in the most part, on the total number of plays the track has had and how recent those plays are. Generally speaking, songs that are being played a lot now will have a higher popularity than songs that were played a lot in the past. Duplicate tracks (e.g. the same track from a single and an album) are rated independently. Artist and album popularity is derived mathematically from track popularity.
2. **duration_ms**: The track length in milliseconds
3. **explicit**: Whether or not the track has explicit lyrics (true = yes it does; false = no it does not OR unknown)
4. **danceability**: Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable
5. **energy**: Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale
6. **key**: The key the track is in. Integers map to pitches using standard Pitch Class notation. E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1
7. **loudness**: The overall loudness of a track in decibels (dB)
8. **mode**: Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0
9. **speechiness**: Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks
10. **acousticness**: A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic
11. **instrumentalness**: Predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly "vocal". The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content
12. **liveness**: Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live
13. **valence**: A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry)
14. **tempo**: The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration
15. **time_signature**: An estimated time signature. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure). The time signature ranges from 3 to 7 indicating time signatures of 3/4, to 7/4.
16. **track_genre**: The genre in which the track belongs

*Source*: [Kaggle](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)


## Analysis Stage

Five different machine learning models are used to fit the data and evaluate their performance, according to the following criteria:

1. At least one model must be simple enough to consider as a **baseline** for comparison to the more sophisticated models. Regression models or nearest neighbors methods, based on only a few predictors, are good candidates for baseline methods.

2. At least one model should be fit using your own implementation of **gradient descent**. The only restrictions on this model are that the gradient of the loss function should not be a constant. You are free to use a simple model and a simple loss function to make the derivation and computation manageable.

3. At least one non-baseline model must be (relatively) **interpretable**. For this model you should write a brief sub-section including your interpretation of the results. You could compare to a baseline model on both predictive accuracy and (in)consistency of interpretations.

4. At least one model must be (relatively) **high-dimensional**. If your dataset has many predictors, and the number of observations is not much larger, then for example you could fit a penalized regression model using all the predictors. If your dataset does not have many predictors you could consider models that include non-linear transformations, interaction terms, and/or local smoothing to increase the effective degrees of freedom.

5. At least one model must be (relatively) more focused on **predictive accuracy without interpretability**. Imagine that you would submit this model to a prediction competition where the winner is chosen using a separate set of test data from the same data generating process (in-distribution generalization).
