

### Capstone Proposals

### Owen Temple, December 7, 2017


## 1. LINGUISTIC SIGNATURES OF PERSUASIVE TED TALKS 

How are peruasive or highly viewed TED Talks different from other TED Talks?
What moral concepts are discussed in TED Talks and have these changed over time?

I webscraped using BeautifulSoup to create a dataset for all posted talks 2002 through 2017 - including metadata, transcript. I have done a few preliminary exploratory analyses of word counts and word use by category using LIWC – a Linguistic Inquiry and Word Count package.


> FROM JAMES PENNEBAKER’S “THE SECRET LIFE OF PRONOUNS”
Pronouns (such as I, you, they), articles (a, an, the), prepositions (to, of, for), auxiliary verbs (is, am, have), and a handful of other common word categories are called function words. On their own, function words have very little meaning. In English, there are fewer than 500 function words yet they account for more than half of the words we speak, hear, and read every day. By analyzing their use, we begin to learn how speakers are connecting with their audiences, their friends, their conversational topics, and themselves.

> FROM ROBERT LEWIS’ “MORALITY IN LINGUISTIC CONTENT”
There has been a recent acknowledgement in media psychology that morality exists “in the plural,” and is central to how individuals process and understand narratives (Krcmar & Cingel, 2016; Tamborini, 2011, 2013; Weaver & Lewis, 2012; Weber, Popova, & Mangus, 2012). That is, moral judgments are based on a number of different psychological foundations relevant to diverse areas of social life, including issues such as ingroup loyalty, respect for authority, and the idea of purity and sanctity (Haidt & Joseph, 2007).

>According to Haidt and Joseph’s (2007) moral foundations theory, judgments are based on five motivational foundations, labeled as follows: Care is concerned with feeling and disliking the pain of others; fairness is related to reciprocity, equality, and proportionality; ingroup loyalty relates to our tribal history as a species, and underlies ingroup biases and feelings of community; authority is about respecting dominance hierarchies, traditions, and high-status individuals; and purity is concerned with contamination—physical and metaphysical—and endeavoring to live in a more noble manner (Graham, Haidt, & Nosek, 2009).


>CATEGORIES OF WORDS ASSOCIATED WITH MORAL CHOICES (see dictionary_of_moral_words_by_category in repository for full list)
- 01                    HarmVirtue - ex. safe*, peace*, compassion*, empath*, sympath*, care		
- 02                    HarmVice - ex. harm*, suffer*, war
- 03                    FairnessVirtue - ex. fair, fairness, fairplay, equal*, justice	
- 04                    FairnessVice - ex. unfair, unequal, bias
- 05                    IngroupVirtue - ex. together, nation, homeland
- 06                    IngroupVice - ex. foreign, enem*, betray
- 07                    AuthorityVirtue - ex. obey, duty, law
- 08                    AuthorityVice - ex. defian*, rebel, dissent
- 09                    PurityVirtue - ex. piety, pure, clean, sacred
- 10                    PurityVice - ex. disgust, deprav*, sin
- 11                    MoralityGeneral - ex. righteous, moral, ethic*		
		
Research Questions
- Do certain linguistic features predict a talk being classified as “persuasive”, “inspiring,”or “beautiful” by TED.com users?
- Can we use a classifier to take features in the transcript such as use of “I”, use of “you”, or use of question words or positive or negative sentiment to predict whether a TED talk will be tagged as persuasive?
- Can we use a regressor to take features in the transcript such as use of “I”, use of “you”, use of question words, positive or negative sentiment to predict number of views (adjusted for the length of time it has been posted)?
- Has use of words associated with five different categories of morality (Harm, Fairness, Ingroup, Authority, Purity) changed over time?
- What weighting of the 5 different moral dimensions characterize TED talks?
- WHat are the most common phrases in highly viewed or persuasive talks verus other talks?



I would present the findings with a presentation and slides, a polished and visual Jupyter Notebook, and perhaps an interactive web ap visualization. (Perhaps a single Talk's linguistic signature could be displayed beside each TED Talk on a web app.)


Next steps:
- Build preliminary classifier and regressor models to predict views and 'persuasiveness' based on data I already have
- Clean transcript text
- Produce new features from text content of TED talk transcripts
- Learn about Natural Language Processing in NLTK and Stanford CoreNLP to explore additional possibilities
 

Data acquired:
- Metadata on TED Talks from 2002 to 2017 with preliminary text analysis of transcript ```TED_Talks_by_ID_plus-transcripts.csv```
- Classification of talks by users as persuasive, inspiring, etc. ('ratings' column in ```ted_main.csv```)
- Transcripts of talks


## 2. CHANGES IN MORAL CONCERNS OVER TIME AND LINGUISTIC FEATURES OF THE GREATEST FILMS OF ALL TIME

How are films that are called "the greatest" different from films in general?

I compiled, from multiple credible film industry sources, a combined list of the “greatest films of all time.”  I webscraped the metadata for these 1200 films from OMDBAPI.com.  I acquired the subtitles (complete English transcript) of each of these movies and 34,000 other films from a researcher friend (Robert Lewis) and moviesubtitles.org. I have done a few preliminary exploratory analyses of word counts using the LIWC Linguistic Inquiry and Word Count package.

Research Questions
- Are there linguistic features of the film’s dialogue that predicts a film being on lists of “greatest films”?
- Are there other features of films that predict being deemed a “great film?”
- Has the use of words about moral choices changed in movies over time?
- Are there linguistic features of the film’s dialogue that are associated with higher ratings from IMDB users?

I would present the findings with a presentation and slides, and an interactive visualization.

The preliminary summary data for the “greatest films” are in this repository. I have metadata for 35,000 films. (The subtitles file is too big to post to GitHub).

Next steps:
Produce new features from text content of movie subtitles

Data acquired:
- list of greatest films with metadata and preliminary text analysis columns (```greatest_films_from_multiple_sources.csv```)
- metadata on larger set of films (```all-films.csv```)
- movie subtitle text files for 35K films (on hard drive)


## 3. DETECTING GENRE AND CHARACTERISTICS OF "GREAT FILMS" FROM MOVIE POSTERS

I webscraped movie posters from OMDBAPI.com and built up a dataset of 1208 movie posters from films on greatest films list.

Research questions:
- How are movie posters for great films different than movie posters for other films?
- Can we use image feature detection, object identification, and a neural network 

Attempt a multi-label classification of a movie poster using object identification.

I read a paper by Chu and Guo ("Movie Genre Classification based on Poster Images with Deep Neural Networks" included in the repository) that said that YOLO object detection performed best to classify movies by genre.

Here are some details on YOLO:
https://github.com/pjreddie/darknet/wiki/YOLO:-Real-Time-Object-Detection and  https://pjreddie.com/darknet/yolo/

> All prior detection systems repurpose classifiers or localizers to perform detection. They apply the model to an image at multiple locations and scales. High scoring regions of the image are considered detections.

> We use a totally different approach. We apply a single neural network to the full image. This network divides the image into regions and predicts bounding boxes and probabilities for each region. These bounding boxes are weighted by the predicted probabilities.

> Finally, we can threshold the detections by some value to only see high scoring detections:

> Our model has several advantages over classifier-based systems. It looks at the whole image at test time so its predictions are informed by global context in the image. It also makes predictions with a single network evaluation unlike systems like R-CNN which require thousands for a single image. This makes it extremely fast, more than 1000x faster than R-CNN and 100x faster than Fast R-CNN. See our paper for more details on the full system.

Research Questions
- Do certain objects on movie posters indicate certain movie genres?
- Do certain objects on movies posters for 'greatest films' differ from objects on other 'non-great' movies

Next steps:
- Use existing list of 30,000 movie poster URLs (example: https://image.tmdb.org/t/p/w440_and_h660_bestv2/6ksm1sjKMFLbO7UY2i6G1ju9SML.jpg) to save to file the jpgs of movie posters (for films not on greatest films list) from https://www.themoviedb.org
- Research YOLO object detection to find the simplest neural network model that gets somewhat accurate classification of genre and or/ prediction of a movie being in the great films list

Data:
- 1200 greatest films movie posters (already scraped and in this repository in ```greatest-films-posters``` directory)
- 30000 movie posters - I have image URLs - need to download to disk (list of URLs in 'poster_path' column of ```movies-metadata.csv```)
- movie metadata, with dummy variables for each genre (genre columns in ```all-films.csv```)
