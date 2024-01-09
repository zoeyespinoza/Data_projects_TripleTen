# Basic-Python-Yandex.Music

## Introduction <a id='intro'></a>

In this project, we compare the music preferences of the cities of Springfield and Shelbyville by studying Yandex.Music data to test the hypotheses and compare user behavior for these two cities.

### Goal: 
Test three hypotheses:
1. User activity differs depending on the day of the week and from city to city. 
2. On Monday mornings, Springfield and Shelbyville residents listen to different genres. This is also true for Friday evenings. 
3. Springfield and Shelbyville listeners have different preferences. In Springfield, they prefer pop, while Shelbyville has more rap fans.

### Stages 
Data on user behavior is stored in the file `/datasets/music_project_en.csv`.

 
The project will consist of three stages:
 1. Data overview
 2. Data preprocessing
 3. Testing the hypotheses

We have tested the following three hypotheses:

1. User activity differs depending on the day of the week and from city to city. 
2. On Monday mornings, Springfield and Shelbyville residents listen to different genres. This is also true for Friday evenings. 
3. Springfield and Shelbyville listeners have different preferences. In both Springfield and Shelbyville, they prefer pop.

After analyzing the data, we concluded:

1. User activity in Springfield and Shelbyville depends on the day of the week, though the cities vary in different ways. 

The first hypothesis is fully accepted.

2. Musical preferences do not vary significantly over the course of the week in both Springfield and Shelbyville. We can see small differences in order on Mondays, but:
* In Springfield and Shelbyville, people listen to pop music most.

So we can't accept this hypothesis. We must also keep in mind that the result could have been different if not for the missing values.

3. It turns out that the musical preferences of users from Springfield and Shelbyville are quite similar.

The third hypothesis is rejected. If there is any difference in preferences, it cannot be seen from this data.


