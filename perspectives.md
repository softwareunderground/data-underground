# DRAFT


### Purpose of this document:
This markdown file is to certain extent a proposal for what to include in this repository. 

### Introduction
After reading the initial file in this repository called <a href="https://github.com/softwareunderground/data-underground/blob/master/open-data-guidelines.md">"open-data-guidelines.md"</a>, I made some issues <a href="https://github.com/softwareunderground/data-underground/issues/1">here</a> and <a href="https://github.com/softwareunderground/data-underground/issues/2">here</a>.

After further evaluation, the thing that was bugging me was that the <a href="https://github.com/softwareunderground/data-underground/blob/master/open-data-guidelines.md">document</a> was written directed at the supplier of a dataset. While that is the obvious place to start, it is worth thinking about a range of personas, multiple use cases, and different possible future states. 

## Brainstorm of Personas, Use-cases, Users, Evolutions of Requirements

### Builders & Maintainers of the website that hosts and presents that data to end-users
These would be the people with the ability to make changes to https://dataunderground.org/dataset.

Some characteristics one could use to describe them that might matter would be:
1. The amount of time they want to / can contribute.
2. The degree to which they choose to accept edits, code, or other types of control from outside the initial group. 
3. Skills, particularly those that affect tech stack. 

### Users
Highest level breakdown of users:
1. Suppliers of the datasets
2. Maintainers of the website (perhaps the most active users!)
3. End-users consuming datasets

#### A few personas of users:
1. Curious about what data is available but no end goal, project or datasets in mind. 
  a. Goes to first page and that's it if not interested there.
  b. Spends <4 minutes browsing and then bails if nothing in line with interests.
  c. Will read details of multiple datasets and maybe download 1 or 2 max.
  d. Will read details on every dataset up to first 50 and downloads 4 or 10 to explore in more depth.
2. Geologist with high level of programming skills. Interested in seismic data related to automatic fault picking.
3. Geologist with low level of programming skills. Interested in facies prediction. Wants to move example work from an open-dataset to be applied to their own internal well log data.
4. Geophysicist who wants to try out unsupervised machine-learning package that he's seen used recently on geology data and is curious what open data could used for that sort of approach.

#### Use-cases
1. Demo datasets in code packages. 
2. Hackathon datasets.
3. Datasets to go with open-source code. Users then make changes to the code but keep using the dataset.
4. Various type of datascience: visualization, data exploration, sql practice, unsupervized learning, supervised learning, classification, regression prediction, etc.

#### Suppliers of datasets / who might have edit rights in some form?
1. Owners of original datasets who also collected the data. 
2. People who have rights to make the dataset public but didn't collect it originally or prep it. 
3. People who found the dataset with an open-source license elsewhere and want to suggest it for inclusion on data-underground.
4. People who want to add a correction to the already published dataset. 
5. People who want to supply some additional notes to the dataset (for example which logs have bad formatting and won't load easily via LASIO). 
6. People who want to add or link to code to load the dataset or work with the dataset in some way. 
7. People who found a paper that references the dataset but don't own either the dataset or the paper.

#### Level of dataset hosting
here = data-underground
1. This dataset exists only here. 
2. This dataset is uploaded here but originally lived in this other place.
3. This dataset is referenced here but still lives in its originally place here.
4. This dataset is referenced here but has been automatically harvested from this site.
4. This dataset is referenced here but to download it you have to go to this other site.

#### Add-ons
For: 
- Discoverability
- programmatic creation of meta-data from descriptions
- end-user creation of new meta-data
- end-user created code to use with the dataset

