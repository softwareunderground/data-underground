# Open data for machine learning

Thinking about taking some open data and making it "machine learning ready"? Awesome! We need more open datasets and benchmarked machine learning tasks.

Here are some recommendations:

**It must address at least one clear machine learning task.** The more obviously useful the task, the more useful (and important) the benchmark. The benchmark dataset should be well suited to the task (but does not have to be comprehensive or definitive). 

**It must be open.** That means explicitly licensed with an open, and preferably permissive, license. I think we need to avoid non-permissive (so-called ‘copyleft’) licenses, because it’s not clear how the ‘sharealike’ clause would affect works that depended on the dataset. And we definitely need to avoid restrictive non-commercial clauses.

**It must be discoverable and accessible.** In other words, it needs to be easy to find, and anyone should be able to get it, without registering on a website or waiting for an email or doing anything else that slows down the pace of their research. A properly open dataset can be replicated anywhere, so openness should take care of this.

**It must have enough features to be interesting.** This might mean different things for different tasks, but in general we’d like to see a few physical measurements (e.g. seismic, well logs, RockEval, core photos, field observations, flow rates, and so on). The features should be independent — we can always generate derivatives.

**It must have labels.** As well as some interesting features, the dataset must have some interpretive information with high information value (e.g. seismic facies, lithologies, deposotional environment, sequence boundaries, EURs, and so on). Usually, these are expensive to acquire (which is partly why we’d like to be able to predct them).

**Explicit labels are better than implicit.** For example, to label seismic facies in a 3D seismic volume, provide (inline, crossline, TWT) locations of labels, not subimages of the facies. Apart from being more flexible (e.g. I get to decide on the size of the subimages myself, should I wish to extract them), it requires much less space.

**It should name suitable prediction error evaluation methods,** with reference implementations, for the intended task. If people are to use it as a score benchmark, they need to know how to score their own implementations of the task.

**It can be de-localized, but not completely.** We don’t need to know the exact whereabouts of the dataset, but if we remove the relative spatial relationships between wells, say, or don’t know which basin we’re in, then the questions we can ask about the data get a lot less interesting, and the whole situation gets much less realistic.

**Make everything downloadable in a single large file.** If the single large file is really big, greater than about 100GB, then offer sensible subsets of the data (e.g. split by data type, or geographical area) as well as the complete dataset. If the dataset is intended as a benchmark, consider its size: more than about 1GB means it may be unwieldy for beginners, and may be difficult to download for some users.

**Enable selective downloads of arbitrary size limit or filtered.** Even if the dataset is not very large, it helps to be able to interrogate the data in different ways. Ideally, this is accomplished via an API, so that users may access the data from code.

**Provide very small example files.** Even if subsets are available, consider offering one or more small example files, or (better) one-click examples using the API, so that a person can quickly inspect the data structure without having to download a large file or learn how to use an API.

**It should be clean, but not too clean.** No-one wants to spend hours processing a dataset before it can be used, or — worse — be bitten by some esoteric data problem only a domain expert would spot. But, on the other hand, a dataset with no issues at all might be a bit boring. And, in subsurface at least, completely unrepresentative!

**It should be well documented.** The dataset needs to be described to non-technical people, who know little or nothing about the subsurface. Remember that many users will not be proficient programmers either (see also the point about a demonstration.) Be sure to also describe the data format (especially if non-standard), data structure, column types and units, missing data flags, etc. 

**It should have an accompanying demonstration.** For example, a script or notebook, preferably in at least a couple of languages, that shows how to load and inspect the data (e.g. for Python programmers, into NumPy or Pandas). Ideally this would include a demonstration of how to pose, and answer, a straightforward question as a machine learning task.

These won't all necessarily make sense for the dataset you have in mind, but perhaps you can take the principles underlying these ideas and figure out what does make sense. By all means, adjust this document accordingly so others can learn from what you did.
