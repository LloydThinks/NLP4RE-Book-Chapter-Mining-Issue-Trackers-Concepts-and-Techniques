## Summary of Artefacts

These artefacts accompany the "Mining Issue Trackers: Concepts and Techniques" chapter within the "Handbook of Natural Language Processing for Requirements Engineering" book. The book chapter includes a "Use Cases" section where natural language processing (NLP) techniques are applied to issue tracker data from Montgomery et al. [1]. The JupyterNotebooks in this replication package can be used to follow along with the use cases in the chapter.

## Author and Article Details

Lloyd Montgomery - lloyd.montgomery@uni-hamburg.de
Dr. Clara Lüders - clara.marie.lueders@gmail.com
Prof. Dr. Walid Maalej - walid.maalej@uni-hamburg.de

All authors are affiliated with the University of Hamburg in Hamburg, Germany.

Please cite this work as:

Montgomery L, Lüders C, Maalej W. of Part, "Mining Issue Trackers: Concepts and Techniques," in "Handbook of Natural Language Processing for Requirements Engineering", 1st Edition, Ferrari A, Deshpande G. Eds. Springer Nature Switzerland AG, Cham, Switzerland, 2024, to appear.

Title of Chapter: "Mining Issue Trackers: Concepts and Techniques"

Abstract of the Chapter: An issue tracker is a software tool used by organisations to interact with users and manage various aspects of the software development lifecycle. With the rise of agile methodologies, issue trackers have become popular in open and closed-source settings alike. Internal and external stakeholders report, manage, and discuss “issues”, which represent different information such as requirements and maintenance tasks. Issue trackers can quickly become complex ecosystems, with dozens of projects, hundreds of users, thousands of issues, and often millions of issue evolutions. Finding and understanding the relevant issues for the task at hand and keeping an overview becomes difficult with time. Moreover, managing issue workflows for diverse projects becomes more difficult as organisations grow, and more stakeholders get involved. To help address these difficulties, software and requirements engineering research have suggested automated techniques based on mining issue tracking data. Given the vast amount of textual data in issue trackers, many of these techniques leverage natural language processing. This chapter discusses four major use cases for algorithmically analysing issue data to assist stakeholders with the complexity and heterogeneity of information in issue trackers. The chapter is accompanied by a follow-along demonstration package with JupyterNotebooks.

## Description of Artefacts

The artefact is split into three use cases, all sharing the same `data` folder.

- `use_case_1.ipynb`: Use Case: "Issue Quality Analysis"
    - "The objective of this use case is to assess the quality of requirements issues, using well-known NLP techniques and algorithms from the requirements quality literature. We will focus on the requirements quality factor 'ambiguity' and work towards detecting the following subtypes of ambiguity: subjective language, coordination, compound nouns, and nominalisations."
- `use_case_2.ipynb`: Use Case: "Evolution Analysis"
    - "Our objective with this use case is to investigate sentiment across evolutions and uncover the dynamics of issue descriptions through time. In particular, we are interested to see if edits to issue descriptions make them more positive in sentiment."
- `use_case_3.ipynb`: Use Case: "Discussion Analysis"
    - "Our objective with this use case is to find situations where specific issue fields are discussed in the comments and attempt to identify situations where information in the comments is not propagated up into the issue itself. For example, are there situations where someone has commented that the status should be updated, but it was not?"
- `data`: This folder contains the data needed for the use cases to run.
    - `jira_issuetype_thematic_analysis.json`: The results of a thematic analysis that unifies the issue types across the different Jiras under a single Thematic Map.
    - `load_evolution_dataframe(sample_data_n=10000).pgzip`: A pickle file (that has also been compressed using gzip) containing a random sample of issues from the original Public Jira Dataset [1].
    - `use_case_1_data.tsv`: A sample of issues for Use Case 1.
- `utils.py`: A small collection of useful functions to perform standard tasks like pickling and unpickling files, among other things.

## Licences

The code is licensed under MIT. The licence is included in this repository and further information can be found here:https://opensource.org/licenses/MIT

The data is licensed under CC BY 4.0. The licence is included in this repository and further information can be found here: https://creativecommons.org/licenses/by/4.0/

## Resources

[1] Montgomery, L., Lüders, C., Maalej, W.: An alternative issue tracking dataset of public jira repositories. In: Proceedings of the 19th International Conference on Mining Software Repositories. pp. 73–77 (2022)
