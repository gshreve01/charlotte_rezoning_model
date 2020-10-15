# <div style="text-align: center;">Can I change that?</div>
## Predicting Outcomes of Charlotte, NC, Rezoning Requests

For this project we used the Charlotte Rezoning Data and Charlote Quality Of Life Data points
* Gather Data
    * Charlotte Zoning Request Feed
    * Charlotte Quality Of Life Excel Datasets
    * Clean and Merge different data sets
* Predict Zoning Request Outcome
    * Clasify, Encode, Transform and Scale
    * MLM: K Nearest Neighbor
    * Unbalanced Data
    * MLM: Logistic Regression + SMOTE Method
* Visualize
    * Tableau
    * Household Income VS Confirmed Cases

![alt text](Readme.png "Charlotte Zoning NPA")

# Implementation Approach
## Merging the Data
The only pieces of shared information was geographical location.  Both were represented by geo polygons, so using the NPA as the boundary, it was determined by calculating a central geo point of the request which NPA with which it was associated.

## Running the Model
A review of all the available data points was done, and those deemed most appropriate were used.  After some closer analysis of the data, it was determined that almost all requests were approved.  The initial model run of K-Nearest Neighbors accuracy fell within indicating approval of all requests.  The data was unbalanced, so a new model was used which included SMOTE modeling to try to overcome the unbalanced data, but we were not successful.

# Conclusion
The current state of data would not allow for a predictive model.  We could change the focus of the analysis on the few that were declined, and possibly pull in text information about the request and use natural language processing to determine sentiment that may help.