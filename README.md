

Capstone Proposals

Owen Temple, December 7, 2017

2. High level description of the project: what question or problem are you addressing?
3. How are you presenting your work? (web app, visualization, presentation/slides, etc.)
4. What’s your next step?
5. Data
  - link to and description of data source
  - please note that proposals without specific data source cannot be considered



LINGUISTIC SIGNATURES OF PERSUASIVE TED TALKS 

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




MORALITIES AND LINGUISTIC FEATURES OF THE GREATEST FILMS OF ALL TIME

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


CATEGORIES OF WORDS ASSOCIATED WITH MORAL CHOICES
%		
01                    HarmVirtue
02                    HarmVice
03                    FairnessVirtue
04                    FairnessVice
05                    IngroupVirtue
06                    IngroupVice
07                    AuthorityVirtue
08                    AuthorityVice
09                    PurityVirtue
10                    PurityVice
11                    MoralityGeneral
%		
		
safe*			01
peace*			01
compassion*		01	
empath*			01
sympath*		01	
care			01
caring			01
protect*		01	
shield			01
shelter			01
amity			01
secur*			01     
benefit*        	01           
defen*			01 
guard*			01
preserve		01 07 09         
		
harm*			02
suffer*			02
war			02        
wars			02        
warl*			02        
warring			02        
fight*			02
violen*			02
hurt*			02
kill			02
kills			02
killer*			02
killed			02
killing			02
endanger*		02	
cruel*			02
brutal*			02
abuse*			02
damag*			02
ruin*			02 10
ravage			02
detriment*		02            
crush*			02
attack*			02
annihilate*		02
destroy			02
stomp			02
abandon*		02 06
spurn			02
impair			02             
exploit			02 10            
exploits		02 10
exploited		02 10
exploiting		02 10
wound*			02
		
fair			03
fairly			03
fairness		03
fair-*			03
fairmind*		03
fairplay		03
equal*			03
justice			03
justness		03
justifi*		03
reciproc*		03	
impartial*		03	
egalitar*		03	
rights			03         
equity			03
evenness		03
equivalent		03	
unbias*			03
tolerant		03
equable			03
balance*		03           
homologous		03
unprejudice*		03
reasonable		03
constant		03
honest*			03 11
		
unfair*			04
unequal*		04	
bias*			04
unjust*			04
injust*			04
bigot*			04
discriminat*		04
disproportion*		04
inequitable		04
prejud*			04
dishonest		04
unscrupulous		04
dissociate		04
preference		04
favoritism		04
segregat*		04 05
exclusion		04
exclud*			04         
		
together		05	
nation*			05
homeland*		05	
family			05
families		05
familial		05
group			05
loyal*			05 07
patriot*		05	
communal		05
commune*		05
communit*		05
communis*		05
comrad*			05
cadre			05
collectiv*		05
joint			05
unison			05
unite*			05
fellow*			05
guild			05
solidarity		05
devot*			05
member			05
cliqu*			05
cohort			05
ally			05
insider			05
		
foreign*		06	
enem*			06
betray*			06 08
treason*		06 08	
traitor*		06 08	
treacher*		06 08	
disloyal*		06 08	
individual*		06	
apostasy		06 08 10
apostate		06 08 10
deserted		06 08
deserter*		06 08
deserting		06 08
deceiv*			06
jilt*			06
imposter		06
miscreant		06
spy			06
sequester		06
renegade		06
terroris*		06
immigra*		06		


obey*			07
obedien*		07
duty			07
law			07
lawful*			07 11
legal*			07 11
duti*			07
honor*			07
respect			07	
respectful*		07
respected		07
respects		07
order*			07
father*			07
mother			07
motherl*		07
mothering		07
mothers			07
tradition*		07	
hierarch*		07	
authorit*		07	
permit			07
permission		07	
status*			07
rank*			07
leader*			07
class			07
bourgeoisie		07
caste*			07
position		07
complian*		07
command			07
supremacy		07
control			07
submi*			07
allegian*		07
serve			07
abide			07
defere*			07
defer			07
revere*			07
venerat*		07
comply			07
		
defian*			08
rebel*			08
dissent*		08	
subver*			08
disrespect*		08	
disobe*			08
sediti*			08
agitat*			08
insubordinat*		08
illegal*		08
lawless*		08
insurgent		08
mutinous		08
defy*			08
dissident		08
unfaithful		08
alienate		08
defector		08
heretic*		08 10
nonconformist		08
oppose			08
protest			08
refuse			08
denounce		08
remonstrate		08
riot*			08
obstruct		08
		
piety			09 11
pious			09 11
purity			09
pure*			09
clean*			09
steril*			09
sacred*			09
chast*			09
holy			09
holiness		09	
saint*			09
wholesome*		09 11	
celiba*			09
abstention		09
virgin			09
virgins			09
virginity		09
virginal		09
austerity		09
integrity		09 11
modesty			09
abstinen*		09
abstemiousness		09
upright			09 11
limpid			09
unadulterated		09
maiden			09
virtuous		09
refined			09
decen*			09 11
immaculate		09
innocent		09
pristine		09
church*			09
		
disgust*		10	
deprav*			10
disease*		10	
unclean*		10	
contagio*		10
indecen*		10 11	
sin			10
sinful*			10 
sinner*			10
sins			10
sinned			10
sinning			10
slut*			10
whore			10
dirt*			10
impiety			10
impious			10
profan*			10
gross			10
repuls*			10
sick*			10
promiscu*		10
lewd*			10
adulter*		10
debauche* 		10
defile*			10
tramp			10
prostitut*		10
unchaste		10
intemperate		10
wanton			10
profligate		10
filth* 			10
trashy			10
obscen*			10
lax			10
taint*			10
stain*			10
tarnish*		10
debase*			10
desecrat*		10
wicked*			10 11
blemish			10
exploitat*		10
pervert			10
wretched*		10 11
		

righteous*		11
moral*          	11	
ethic*          	11	
value*          	11	
upstanding      	11	
good            	11	
goodness        	11	
principle*      	11	
blameless		11
exemplary		11
lesson			11
canon			11
doctrine		11
noble			11
worth*			11
ideal*			11
praiseworthy		11
commendable		11
character		11
proper			11
laudable		11
correct			11
wrong*			11
evil			11
immoral*		11
bad			11
offend*			11 
offensive*		11
transgress*		11



