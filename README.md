<!-- #region -->
# 601project

Presentation Link
https://docs.google.com/presentation/d/1IWNI1zmTcvfd4WU1S5XwMY2SHHHw9x8D/edit?usp=sharing&ouid=104997931037842592346&rtpof=true&sd=true

Dataset: https://www.kaggle.com/datasets/abcsds/pokemon

Run all cells on Pokemon EDA Final for correct visualisations and data wrangling.

Pokémon – Insights into Game Mechanics 
Team: Pikachu {Alan Cheun, Naz Shalamo, Spandan Biswas} 

Pokémon is a popular Japanese media franchise which was released in 1996 by Nintendo. It takes place in a world  where creatures of various types, strengths, and abilities coexist. The aim of Pokemon is to battle other monsters using unique abilities in order to capture them and become the best trainer in the world. We are focusing specifically on Pokemon Go which is an augmented reality game designed for mobile devices. It currently has about 89 million players and is rising. These Pokémon enthusiasts will find value in understanding the significance of the attributes that define these creatures as it will help choose which monsters will be more successful in battle.
The dataset it is structured tabular data stored as a CSV file obtained from Kaggle which has been collated from other sources. The final form of the dataset will also be stored as a CSV file.


#: ID for each pokemon
Name: Name of each pokemon
Type 1: Each pokemon has a type, this determines weakness/resistance to attacks
Type 2: Some pokemon are dual type and have 2
Total: sum of all stats that come after this, a general guide to how strong a pokemon is
HP: hit points, or health, defines how much damage a pokemon can withstand before fainting
Attack: the base modifier for normal attacks (eg. Scratch, Punch)
Defense: the base damage resistance against normal attacks
SP Atk: special attack, the base modifier for special attacks (e.g. fire blast, bubble beam)
SP Def: the base damage resistance against special attacks
Speed: determines which pokemon attacks first each round
Generation: which generation the pokemon was released in
Legendary: whether the pokemon is rare or not
Guiding Questions 

Are there noticeable patterns or advantages in having dual types compared to single-typed Pokémon? (Alan)

Understanding the strategic advantages of dual-typed Pokémon over single-typed ones can provide insights into team composition and battle dynamics. This question explores whether the complexity of having two types enhances a Pokémon's versatility and effectiveness in battles. 

Are there specific types that are more likely to be associated with legendary Pokémon? (Alan)


Investigating the prevalence of certain types among legendary Pokémon sheds light on potential thematic or design patterns. Recognizing these associations contributes to the lore and strategic considerations in Pokémon battles. 
How have the attributes of Pokémon evolved across different generations? (Alan)


Examining the evolution of Pokémon attributes across generations provides a historical perspective on the franchise's game design. Understanding these changes can offer insights into the developers' approach to balancing and enhancing gameplay over time. 
How do different types of Pokémon correlate with their overall strength, as indicated by the 'Total' attribute?(Spandan)
The total attribute factor is just a simple addition of all of its other attributes. Just by looking at the data there is no way to tell if there is a specific attribute that contributes more to this total value on average and why that might determine if a pokemon is stronger. The addition of the adjacency matrix will show which types are stronger on average and then it can be correlated with the total attribute.
What insights can be gained from analyzing the relationship between specific attributes (e.g., Attack, Defense, Speed) and a Pokémon's effectiveness in battles?(Spandan)
In order to determine this a rating is called the combat power which is used by the game developers of Pokemon Go. It is a value assigned to each pokemon to determine its performance in battle by using the weighted value of its attributes. This will allow us to find a more normalized value for all the pokemon in comparison to its ‘Total Attribute’ value and give us a better understanding as to which pokemon is better.


How do legendary Pokémon compare to non-legendary Pokémon in terms of overall strength and individual attributes?(Naz) 


Comparing legendary and non-legendary Pokémon helps evaluate whether legendary status significantly impacts overall strength or if certain attributes distinguish them from regular Pokémon. This insight is valuable for trainers aiming to include or counter legendary Pokémon in their teams. 
What is the distribution of primary and secondary Pokémon types? (Naz)


Examining the distribution of primary and secondary types helps identify the most common combinations. This information is essential for trainers aiming to build diverse and strategically balanced teams. 
Are certain types more prevalent than others? (Naz)
Understanding the prevalence of Pokémon types provides valuable information for trainers preparing for battles. It helps identify which types are commonly encountered, allowing trainers to tailor their teams for a competitive edge. 

Tasks and Visualization


One of our first tasks is to create an adjacency matrix table which will have the relationships between all the types of pokemon denoted by either a 1 which is effective against that type or a 0 which is non effective. This will allow us to determine the overall effectiveness of a pokemon and observe how it changes based on other attributes. One of the visualizations we will make use of is a graph network as it will clearly show clusters of types which are stronger than the others as it will have more nodes present.


A few of our guiding questions are based on relationships between attributes and other factors such as generation,type,evolution and whether a pokemon is legendary or not. The good way to visualize this are radar charts that can be created with either seaborn  or matplotlib. This is a great visualization as a reader can easily see if certain attributes are favored more than the other.


In order to see the distribution of Pokemons using types,generations and whether they are legendary or not, boxplots and scatterplots will be utilized. The distribution of primary and secondary typing will be effectively portrayed using a stacked bar chart, providing a two-dimensional comparison. For a chronological breakdown of primary to secondary types over time, cascade or waterfall charts are deemed suitable. To highlight the magnitude of different types, a tree map or bubble chart will be employed. Additionally, exploring relationships between types will involve visualizations such as Chord, Network, or Venn Diagrams, offering insights into the interconnectedness and overlaps among various Pokémon types.


Packages: Numpy, Matplotlib, Pandas, Igraph, Seaborn
<!-- #endregion -->
