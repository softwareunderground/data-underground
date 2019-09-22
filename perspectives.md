# DRAFT

## Introduction

#### What is this file?
This markdown file is something akin to a slack comment in purpose, but way to long for that format, so I'm putting it here. I apologize for the rambling. This is in part an attempt to collect my thoughts.

#### Why I'm writing this?
After I reading the original <a href="https://github.com/softwareunderground/data-underground/blob/master/open-data-guidelines.md">document</a> in this repo titled open-data-guidelines.md, it bugged me a little for reasons I had a hard time narrowing down. After giving it some thought, I realized I felt there were things left out due to the focus on the dataset.

The focus on the dataset makes sense, of course, but I think you get to a better place but not just asking questions about what characteristics the dataset should have but also considering the site that hosts the dataset as well as the different types of members in the community around both the dataset and the site as a hole.

<i>This document is an attempt to suggest other perspectives to consider when creating an open-data site for datasets geared to geoscience + coding beyond what characteristics should the dataset have.</i>

#### Open-data Sites & Constraints On Users
As stated above, a focus on the characteristics datasets should have makes sense, of course. However, I typically find myself less bothered by the characteristics of individual datasets and more by my experiences, or other peoples' experiences, of trying to work with open-datasets in aggregate. Searching through them, evaluating them, organizing them, and aggregating them is often very difficult due to constraints built in place early. Sometimes constraints occur, because certain metadata wasn't encouraged. Other times sites lack certain filtering capability. Other times aspects of the datasets are not programmatically accessible. I less often find myself working with a specific dataset and say "oh it would be great it this particular dataset had blank".

These concerns are less obvious with only 17 datasets on https://dataunderground.org/dataset as of today. These problems appear more as the number of individual datasets grows greater than users' willingess to read through all of them. 

Additionally, these types of issues increase as the percent of datasets that can be aggregated into larger datasets increases. If all the datasets are completely separate or different in domain and,or format, than these issues are less of a problem.

#### Background That Informs My Requirements/Needs
First, I co-lead the houston data visualization meetup, which means I spend some time searching for good datasets people would enjoy visualizing during our datajams over the course of about 4 hours. There's a lot of potential open-data sites out there. Second, I help maintain data.nasa.gov, which has approximately ~40,000 datasets and gets harvested into <a href="https://catalog.data.gov/dataset">data.gov</a>, which has almost a quarter of a million. 

#### Minimizing Time-To-Start is Maximizing Use Rate
A hypothesis I have based on my own experiences and, to be completely honest, not based on any real data whatsoever, is that a lot of the most used open-data is just the easiest to use. 

This is what we see with data.nasa.gov. The most used datasets are typically small ones, in a standard format, that are harvested into sites with great user-interfaces making the evaluation and time to start very minimize. 

A lot of datasets are hard to discover, and "discover" is often a more accurate word than "find" as a significant amount of use of open-data comes from people who didn't already know a dataset existed except through the open-data site or someone else who found it on the open-data site.  

To maximize the rate of discoverability, you need to make the amount of time to get there shorter. This requires the ability to sort and filter datasets in ways the correlate with user needs. 

[STRONGLY HELD OPIONION] The search functionality of some open-data sites is more geared to finding datasets than discovering them, which impacts the user experience.

#### Discoverability Problems That Occur With More Datasets on a Site

##### A. How do you find datasets based on task?
Some users won't care about the dataset content so much as they know it has labels and can be modeled as a time series problem. How do they find all the datasets that meet that definition?

##### B. How do you find datasets based on data format or data structure?
Some people will want LAS 2.0 well logs. Others will absolutely need well with well paths included, which LAS file formats won't have.

##### C. Can you find all the versions of a dataset?
If a user stumbles upon a preprocessed dataset like <a href="https://github.com/JustinGOSSES/McMurray-Wabiskaw-preprocessed-datasets/blob/master/processed_datasets/mcmurray_facies_dataframe.h5.zip">this one</a> will they also see that there is an original dataset <a href="https://dataunderground.org/dataset/athabasca">here</a??

#### D. How do find datasets based on mininum number of instances?
Some users will be interested in calculating petrophysical variables in Python and want to know what curves are available. Others will want to do stratigraphic top prediction and need more than 800 wells at minimum. 

#### Tags and Flexibility and Who Does the Work?
The obvious solution to many of the discoverability problems above is tags. One of the problems with tags is that they're typically applied by humans with differing perspectives on what's important. Sometimes even with the same perspective on what's important, they might phrase things differently. What this often leads to is partial coverage of datasets that could fall under any individual tag being actually tagged with that keyword. 

A few different solutions exist to the tagging issues highlighted above. 

First, there can be a defined list of tags with certain mandatory key-value pairs that dataset suppliers have to fill out. 

Second, there can a heoric website manager, or assigned intern, who goes through and re-tags every dataset. 

Third, if lengthy enough text description of each item exists, automated text tagging of topics can augment human-generated tags. 

Fourth, the community that users the dataset can tag datasets as they evaluate & use them, potentially according to an ontology that develops over time and is maintained in a central location. For example, there might be a characteristic about well logs, like whether they have tops, that is deemed interestingly enough that it is flagged by the group as something all datasets with well logs should be re-tagged with. This requires an active community and may not be possible if the open-data site is harvesting hundreds or thousands of datasets from other open-data sites.

Fifth, there isn't a good way to discovery datasets that meet a range of criteria except through a lot of work reading descriptions and downloading datasets.

#### Comments on the Solutions Listed Above
The first, second, third, and fitch options don't require anyone to have permissions to make edits to datasets except the dataset suppliers and maybe the website managers. The fourth, however, requires everyone to have edit access. This enables a lot of flexibility, especially going into the future after a dataset is initially uploaded, but has the downside of potentially scaring dataset suppliers.

#### A Back-of-napkin ontology just for example sake

[NOTHING STARTED HERE]

## Brainstorming Users, Personas, Use-cases, Potential Addons, and Evolutions of Requirements

### Users
Highest level breakdown of users:
1. Suppliers of the datasets
2. Maintainers of the website (perhaps the most active users!)
3. End-users consuming datasets

#### Builders & Maintainers of the website that hosts and presents that data to end-users
These would be the people with the ability to make changes to https://dataunderground.org/dataset.

Some characteristics one could use to describe them that might matter would be:
1. The amount of time they want to / can contribute.
2. The degree to which they choose to accept edits, code, or other types of control from outside the initial group. 
3. Skills, particularly those that affect tech stack and the time to do different dataset approval, organization, or cleaning tasks. 

#### A few personas of end-users:
1. Curious about what data is available but no end goal, project or datasets in mind. 
  a. Goes to first page and that's it if not interested there.
  b. Spends <4 minutes browsing and then bails if nothing in line with interests.
  c. Will read details of multiple datasets and maybe download 1 or 2 max.
  d. Will read details on every dataset up to first 50 and downloads 4 or 10 to explore in more depth.
2. Geologist with high level of programming skills. Interested in seismic data related to automatic fault picking.
3. Geologist with low level of programming skills. Interested in facies prediction. Wants to move example work from an open-dataset to be applied to their own internal well log data.
4. Geophysicist who wants to try out unsupervised machine-learning package that he's seen used recently on geology data and is curious what open data could used for that sort of approach.

#### End-users Use-cases
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

