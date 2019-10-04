# Tests

## Recommendation requests

This is done in the notebook Get-recommendations.ipynb.

* The most recent events file is loaded
* A number of test users is selected
* Results from three recommender systems are asked for these users
* Recommendations lists are stored on disk



## Evaluation

This is done in the notebook Evaluate.ipynb.

* The recommendations are read from disk
* The next event files are loaded


### Fail rate

The fraction of the recommendation requests that returned no recommendation list.

cpn-hybrid
Fail rate: 0.23011844331641285

cpn-als
Fail rate: 0.23011844331641285

cpn-recent-random
Fail rate: 0.0


### Accuracy

For each user that occurs in both the recommendations and the next events, we check if the item she read in the next event was also in the recommendation list (of each recommender): True/False.  The hit rate is the fraction of the times this was true.

cpn-hybrid
HR: 0.03296703296703297

cpn-als
HR: 0.0
91 post events between 8 and 8915 seconds after recommendation
Recommendations retrieved between 2019-09-09 14:18:27 and 2019-09-09 15:25:47

cpn-recent-random
HR: 0.04854368932038835
103 post events between 4 and 8910 seconds after recommendation
Recommendations retrieved between 2019-09-09 14:18:31 and 2019-09-09 15:25:51




## Speed

The waiting time between the recommendation request and the retrtieval.

Average waiting time: 2.31 seconds
