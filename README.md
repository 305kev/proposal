

Capstone Proposals

Owen Temple, December 7, 2017


1. LINGUISTIC SIGNATURES OF PERSUASIVE TED TALKS 

(Data for all posted talks 2002 through 2017 -- webscraped by me including metadata, transcript). I have done a few preliminary exploratory analyses of word counts and word use by category using LIWC – a Linguistic Inquiry and Word Count package.

FROM JAMES PENNEBAKER’S “THE SECRET LIFE OF PRONOUNS”
Pronouns (such as I, you, they), articles (a, an, the), prepositions (to, of, for), auxiliary verbs (is, am, have), and a handful of other common word categories are called function words. On their own, function words have very little meaning. In English, there are fewer than 500 function words yet they account for more than half of the words we speak, hear, and read every day. By analyzing their use, we begin to learn how speakers are connecting with their audiences, their friends, their conversational topics, and themselves.

Do certain linguistic features predict a talk being classified as “persuasive”, “inspiring,”or “beautiful” by TED.com users?
-	Can we use a classifier to take features in the transcript such as use of “I”, use of “you”, or use of question words or positive or negative sentiment to predict whether a TED talk will be tagged as persuasive?
-	Can we use a regressor to take features in the transcript such as use of “I”, use of “you”, use of question words, positive or negative sentiment to predict number of views (adjusted for the length of time it has been posted)?

Has use of words associated with five different categories of morality (Harm, Fairness, Ingroup, Authority, Purity) changed over time?
-	What weighting of the 5 different moral dimensions characterize TED talks?


I would present the findings with a presentation and slides, and an interactive visualization.
A linguistic signature could be displayed beside each TED Talk on a web app.


Next steps:
Webscrape https://www.ted.com/talks?sort=persuasive, https://www.ted.com/talks?sort=inspiring, etc. to find out which of the talks were tagged by users as “persuasive” or “inspiring” etc.
Produce new features from text content of TED talk transcripts




2. MORALITIES AND LINGUISTIC FEATURES OF THE GREATEST FILMS OF ALL TIME

I compiled, from multiple credible film industry sources, a combined list of the “greatest films of all time.”  I webscraped the metadata for these 1200 films from IMDB.com.  I acquired the subtitles (complete English transcript) of each of these movies and 34,000 other films from a researcher friend (Robert Lewis) and moviesubtitles.org. I have done a few preliminary exploratory analyses of word counts using the LIWC Linguistic Inquiry and Word Count package.

Are there linguistic features of the film’s dialogue that predicts a film being on lists of “greatest films”?
Are there other features of films that predict being deemed a “great film?”
Has the use of words about moral choices changed in movies over time?

Are there linguistic features of the film’s dialogue that are associated with higher ratings from IMDB users?

I would present the findings with a presentation and slides, and an interactive visualization.

The preliminary summary data for the “greatest films” are in this repository. I have metadata for 35,000 films. (The subtitles file is too big to post to GitHub).

Next steps:
Produce new features from text content of movie subtitles



FROM ROBERT LEWIS’ “FILM MORALITY IN LINGUISTIC CONTENT”

There has been a recent acknowledgement in media psychology that morality exists “in the plural,” and is central to how individuals process and understand narratives (Krcmar & Cingel, 2016; Tamborini, 2011, 2013; Weaver & Lewis, 2012; Weber, Popova, & Mangus, 2012). That is, moral judgments are based on a number of different psychological foundations relevant to diverse areas of social life, including issues such as ingroup loyalty, respect for authority, and the idea of purity and sanctity (Haidt & Joseph, 2007).

According to Haidt and Joseph’s (2007) moral foundations theory, judgments are based on five motivational foundations, labeled as follows: Care is concerned with feeling and disliking the pain of others; fairness is related to reciprocity, equality, and proportionality; ingroup loyalty relates to our tribal history as a species, and underlies ingroup biases and feelings of community; authority is about respecting dominance hierarchies, traditions, and high-status individuals; and purity is concerned with contamination—physical and metaphysical—and endeavoring to live in a more noble manner (Graham, Haidt, & Nosek, 2009).



CATEGORIES OF WORDS ASSOCIATED WITH MORAL CHOICES (see dictionary_of_moral_words_by_category in repository for full list)
%		
01                    HarmVirtue - ex. safe*, peace*, compassion*, empath*, sympath*, care		
02                    HarmVice - ex. harm*, suffer*, war
03                    FairnessVirtue - ex. fair, fairness, fairplay, equal*, justice	
04                    FairnessVice - ex. unfair, unequal, bias
05                    IngroupVirtue - ex. together, nation, homeland
06                    IngroupVice - ex. foreign, enem*, betray
07                    AuthorityVirtue - ex. obey, duty, law
08                    AuthorityVice - ex. defian*, rebel, dissent
09                    PurityVirtue - ex. piety, pure, clean, sacred
10                    PurityVice - ex. disgust, deprav*, sin
11                    MoralityGeneral - ex. righteous, moral, ethic*
%		
		



