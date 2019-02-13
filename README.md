# tdi
This contains links to the datasets from
1) USPTO: https://www.uspto.gov/learning-and-resources/electronic-data-products/patent-examination-research-dataset-public-pair [2017 csv dumps for application_data and all_inventors]
2) crunchbase open data map: https://data.crunchbase.com/docs/2013-snapshot
I cannot provide the actual mysqldump from crunchbase here, because the API key is uniquely generated upon request (takes a few minutes to get it).
I used rebasedata.com cloud service to convert sql dumps to csv format. I found that the github python script available for that did not work yielding error messages I did not have the time to iron out just yet. (It may have to do with my UTF code settings.)

UPDATES Feb 13, 2019

Basic assumption made here: patent as prerequisite to a product. This is not always true. 
Several solutions:
1) Stick with the assumption and build a prediction model.
2) Consider including preceding stage of a patent: publications. 
A concrete solution is possible via http://api.semanticscholar.org/
There is also a large data set available for mining (45 million papers, 46GB of data): http://labs.semanticscholar.org/corpus/

Sample output of the semantic scholar engine: https://www.semanticscholar.org/author/Ary-L.-Goldberger/32868771

Key metric of this engine of interest to us are:
- citation velocity
- citation acceleration
- influence score
- highly influential citations

Semantic scholar engine is unique in the ability to conduct a cognitive search (cf. https://www.geekwire.com/2018/ai2-joins-forces-microsoft-upgrade-search-tools-scientific-research/) which creates the foundation for predictive algorithms.

This output gives a clue to what the proposed project can do for patent - product space.

What specific questions should the model answer:
1) Given a desired product XYZ, what are the prerequisites in the idea space? That should give the prediction of how probably such a product is at this time. Such questions come up often in reviewing idea proposals when the reviewers and funding agencies need to judge the feasibility of a proposed outcome/product.
2) Conversely, given the present idea space in the domain XYZ, what are the possible product developments?

