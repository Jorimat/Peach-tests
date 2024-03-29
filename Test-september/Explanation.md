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



| Recommender        | Fail rate            |
| ------------- |:-------------:|
| cpn-hybrid     | 0.23  |
| cpn-als      | 0.23      |
| cpn-recent-random | 0.0     |


### Accuracy

For each user that occurs in both the recommendations and the next events, we check if the item she read in the next event was also in the recommendation list (of each recommender): True/False.  The hit rate is the fraction of the times this was true.



| Recommender        | Hit rate            |
| ------------- |:-------------:|
| cpn-hybrid     | 0.033  |
| cpn-als      | 0.0      |
| cpn-recent-random | 0.049     |




## Speed

The waiting time between the recommendation request and the retrtieval.

Average waiting time: 2.31 seconds
