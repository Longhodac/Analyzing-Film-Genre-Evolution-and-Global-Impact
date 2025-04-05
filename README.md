## COGS 108 final project

Names
-Naomi Crowder
-Linh Dinh
-Long HoDac
-Nathan Nguyen
-Kate Wang

## Abstract

Do the most popular movie genres change according to worldwide, life-changing events, such as the COVID-19 pandemic? This project explores this question, comparing movie genres from top-grossing movies from two time periods: pre-pandemic (2017-2019) and post-pandemic (2022-2024).

We collected data from a large movie database found on Kaggle and cleaned it to include only the years and pertinent column information we would need to carry out the project. Then, we conducted numerous analysis including linear models, text analysis like plot summaries and keyword sentiment, paired t-tests, and a Simpson’s diversity index. Alongside this, we generated both line and bar graphs to visualize the data in tandem with the other analysis.

After conducting our data analysis, we determined the conclusion to be that there wasn't any statistically significant evidence showing movie genres changed drastically between these two time periods, but that there were some small shifts in one or two of the many genres we looked at as a whole.

## Research Question
"How did the COVID-19 pandemic impact the genres of top-grossing films, comparing the genres of the 100 highest-grossing films released post COVID-19 pandemic (2022-2024) compared to pre-pandemic years (2017-2019)?"

Background and Prior Work
Films and movies are powerful tools for reflecting aspects of society and human relationships, conveying various messages to a large audience. The evolution of predominant genres and themes serves a fascinating lens to examine the intersection of cinema and societal change. Themes and genres of films have evolved over time, mostly driven by factors such as audience demand or a desire of innovative concepts.1 Over the past two decades, global events have shaped the continuously growing film industry. In particular, the COVID-19 pandemic, beginning late 2019, has had far-reaching effects. The historic event marked a change in industry trends, production, and audience engagement.2 More importantly, the pandemic has affected every socioeconomic and political aspect of society. These changes have also potentially altered the landscape of popular cinema, affecting the types of narratives that find commercial success and popularity.

There has been many discussions surrounding the cultural and social influences of the COVID-19 pandemic on film genres, reflecting the changing values, fears, and politics of society over time. Most authors focus on the impact of the pandemic on film marketing and production, but they have not explored much on potential shifts in genres. To look a little more closely on this topic overall, we can explore the shifts in trending genres that have been noted after certain major events. For instance, dystopian movies (or movies that focused on the idea of mass extinction/plague) gained traction after the development of the atomic bomb during World War 2 and was popularized by Elia Kazan's "Panic in the Streets" (1950).3 Another example is the development of the horror genre's diversification of storytelling and incorporating modern themes, such as social and racial injustices as seen in Jordan Peele's "Get Out" (2017).4 These examples strengthen the exploration of the reflection of societal events in films. In regards to the pandemic specifically, the topic is still being explored but there are conversations on the event's influence on new horror trends that emphasize isolation and contagion, as seen in films like "Host" (2020) which was shot entirely through a Zoom call.4 It seems to mirror the global shift occurring during that time. One thing that could be explored more in depth is how they both impact the other (how films shape cultural/political/economic landscape?). These examples have us interested in the kind of influence the pandemic might have had on popularized genres.

While these discussions provide valuable insights into industry-wide changes, there is a gap in understanding if the pandemic has actually impacted the themes and genres of top-grossing films. In our research, we aim to bridge that gap by comparing the 100 highest-grossing films released post-pandemic (2022-2024) to those from the pre-pandemic period (2000-2019), offering a more nuanced view of how this global event has influenced storytelling in mainstream cinema. We plan on analyzing box office trends and keywords describing genres to find out if certain genres are popularized from the impact of the pandemic, and seeing if there is a correlation of those popularized genres to the socioeconomic and political implications caused by the COVID-19 pandemic.

^ Rewind Zone (24 Aug 2023) The Evolution of Movie Genres: Examining Shifts in Popularity and Diversity from the 90s to Today. Medium. https://medium.com/%40TheRewindZone/the-evolution-of-movie-genres-examining-shifts-in-popularity-and-diversity-from-the-90s-to-today-ca1ffd1ca445

^ Alanay, D. (3 Mar) COVID's Impact on the Film Industry: "The Biggest Shift in the History of Hollywood". Wharton UME. https://www.whartonume.com/blog/covids-impact-on-the-film-industry-the-biggest-shift-in-the-history-of-hollywood

^ Cardillo, J. (27 Mar 2020) Pandemic and dystopian movies: A brief history, with Tom Doherty. BrandeisNOW. https://www.brandeis.edu/now/2020/march/tom-doherty-dystopian-movies.html

^ Mccluskey, M. (7 Oct 2020) Horror Films Have Always Tapped Into Pop Culture’s Most Urgent Fears. COVID-19 Will Be Their Next Inspiration. TIME. https://time.com/5891305/horror-movies-coronavirus-history-genre/

## Hypothesis
We believe that the predominant genres in the top 100 grossing films over the past two decades have shifted toward action-packed genres such as action, fantasy, and sci-fi, reflecting the COVID-19 pandemic, with films often reflecting the themes of survival or dystopias.

## Data
Data overview
Dataset #1
- Dataset Name: Full TMDB Movies Dataset 2024 (1M Movies)
- Link to the dataset: https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies/versions/491?resource=download
- Number of observations: 1181912
- Number of variables: 24
This dataset is updated daily and is a movie database, sourcing information from the TMDB database. Key variables include 'title' (string) representing the movie's name, 'release_date' (date) indicating when the movie was released, 'genre' (string) denoting the production cost in dollars, and 'revenue' (integer) reflecting the earnings in dollars. These variables serve as proxies for analyzing trends in movie production, release patterns, and financial performance over time.

In order to prepate this dataset to answer our questions, we have to drop the variables we don't need (e.g. IMDB id) as it has a lot of different movie-related topics, we also need to narrow down the amount of observations to just the relevant years since it spans way over what we need, clear null values (since some movies don't have recorded revenue), and then reorder the data to from greatest to lowest revenue values.
