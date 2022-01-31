# FIFA

## Intro

If there's been one constant in my life, it would be soccer. I not only have fond memories in the form of playing under the floodlights in the rain and cold or waking up at 4 am to watch overseas games with my dad, but also from playing the game virtually on none other than EA Sports' FIFA. I remember at a young age always playing as Argentina in FIFA 2000 scoring goals with Batistuta, and re-inserting the disk multiple times just to watch [the amazing intro](https://www.youtube.com/watch?v=64h4pztcpqE) over and over. From then on I collected every edition, and whether it was playing all night at my friend's house or years later playing in dorm room tournaments in university, my fascination for the game never faded. As I develop my skills in the world of data analytics, I figured that there's no better way to improve than to use what I've learned to run analysis on soccer. In this particular project I wanted to focus on one of my favourite editions of FIFA, FIFA19. 

## Summary

In this Jupyter notebook, I first conducted an exploratory data analysis to get a basic overview of the distribution of players and teams across the game. Before beginning however, it was important to clean the data (such as dealing with null values) to make it suitable for analysis. My EDA involved assessing factors such as top players in each category and position, age distribition, position distribution, and nationalities. Below are some examples of the visualizations. 

![Screen Shot 2022-01-31 at 3 31 41 PM](https://user-images.githubusercontent.com/88220704/151890139-e5b779f6-0212-498f-b486-cad5d97c7b1b.png)

![Screen Shot 2022-01-31 at 3 31 54 PM](https://user-images.githubusercontent.com/88220704/151890163-3607496b-589c-46dd-a08f-4160ef23f5c1.png)

![Screen Shot 2022-01-31 at 3 32 19 PM](https://user-images.githubusercontent.com/88220704/151890207-0d67f928-8ef3-4a7a-9ef7-fee1b611822d.png)

Following the EDA, I decided to fit an unsupervised clustering algorithm on the data to see if it can accurately classify the players into different categories. The specific algorithm I used was K-Means clustering. After using PCA(Principal Component Analysis) to reduce the number of components down to 2 (x and y), the model split the players into 5 different clusters based on their attributes. A snapshot of this classification can see in the list below of the top 5 players in the game. 

![Screen Shot 2022-01-31 at 3 36 42 PM](https://user-images.githubusercontent.com/88220704/151890634-4de4cffe-d852-4eb9-9b24-0b3448e3f7af.png)

It is also worth mentioning that because the dataset is so large, I only used a subset of players in the game: those who are rated 86 overall and above. Finally, I visualized the results on a scatter plot as shown below to get a better idea of how the players were clustered.

![Screen Shot 2022-01-31 at 3 39 35 PM](https://user-images.githubusercontent.com/88220704/151890946-1e20f3d8-a3d1-457f-8e0e-b6eec235c854.png)

As shown in the graph, the players are fairly accurately clustered. The goalkeepers are all clustered to the far right in orange, the defensive players towards the top in green, and the midfielders and attackers distributed across the purple, blue, and red. There does seem to be some overlap between wingers and strikers however, which can be an area that I can work to improve. For example Modric and Harry Kane are in the same cluster (in blue) which is not accurate given that they are different types of players. Regardless, it was a good performance for a first model and I will look to improve the results with further models and trying different unsupervised learning algorithms. 
