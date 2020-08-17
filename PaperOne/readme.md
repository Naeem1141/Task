# Employing Contribution and Quality Metrics for Quantifying the Software Development Process

**_Authors:_**

*_Themistoklis Diamantopoulos, Michail Papamichail , Thomas Karanikiotis, Kyriakos Chatzidimitriou , Andreas Symeonidis_*

## **When**

    Tue 30 Jun 2020 10:52 - 11:00 at MSR:Zoom - Evolution Chair(s): Jürgen Cito
 [Paper Link]
 ***
https://issel.ee.auth.gr/wp-content/uploads/2020/05/MSR2020.pdf

***_Media Link_*** :
    https://youtu.be/tkC4_FtfWHE

  >## **Description**  
   > The full integration of online repositories in the contemporary software development process promotes remote work and remote collaboration. Apart from the apparent benefits, online repositories offer a deluge of data that can be utilized to monitor and improve the software development process. Towards this direction, we have designed and implemented a platform that analyzes data from GitHub in order to compute a series of metrics that quantify the contributions of project collaborators, both from a development as well as an operations (communication) perspective. We analyze contributions in an evolutionary manner throughout the projects’ lifecycle and track the number of coding violations generated, this way aspiring to identify cases of software development that need closer monitoring and (possibly) further actions to be taken. In this context, we have analyzed the 3000 most popular Java GitHub projects and provide the data to the community.
   
## Introduction
The emergence of the open-source initiative has changed the way
software is developed. Software development is now a collaborative
process, taking place in online code hosting facilities, such as
GitHub, Bitbucket or GitLab. And although software engineering
has always relied on effective teamwork, today more than ever we
are able to observe this process transparently and at such a massive
scale. Indicatively, GitHub at the time of writing hosts more than
100 million repositories from more than 30 million developers1.
Collaboration often expands to multiple axes, including
not only writing code, but also augmenting documentation, proposing
the development of new features, discussing any issues raised
by end-users, resolving bugs, etc. This information, is available in
different formats (i.e. source code, commits, issues, pull requests,
etc.), and tracks the whole timeline of the project.

1. Constatntly evolving open source initiative.
2. Numerous code hosting facilities (Github, Gitlab, BitBucket).
3. Collaboration lies on top of everthing.
Software projects, Development operations, effective monitoring.

## Motivation
 1. Create a dataset to be used.
 2. as dataset for keeping track  of what we call Story of      the development project.
 3. as a benchmark for answering operations related questions .

    > who has worked on what.
    
    > what issues have arisen.

    > who is the most suitable contributor to fix this issue.

    As a benchmark for answering development related questions.

    > what is the evolution of the quality overtime?

    > how does heavy workload affect quality?
      #### ARCHITECTURE AND TOOLS

      architecture of our platform, which comprises
      four modules: the Data Downloader, the MongoDB Management
      System, the Contributions Analyzer, and the Quality Analyzer. These
      modules are presented in detail in the following paragraphs.

      Data Downloader. It is a Python application that uses the GitHub
      API4 in order to retrieve all information offered for a given repository.
      This information includes commits, issues, commit comments,
      issue comments, issue events, contributors information, repository
      information, as well as the source code of the repository. Apart from
      downloading the data as raw .json files, the data downloader offers
      integration capabilities with MongoDB, which can be used for
      storing, retrieving and querying the data.
      
      MongoDB Management System. We use MongoDB
      our database
      management system, which contains all the raw data retrieved
      from GitHub along with the results of the contributions and the
      quality analysis.

      Contributions Analyzer. It uses the information retrieved from
      GitHub in order to compute a series of metrics that quantify the
      activity of each contributor both in terms of development and
      operations. Table 1 presents the calculated metrics along with their
      category (Dev for “development” or Ops for “operations”) and their
      computation interval (Weekly or Full). Weekly denotes that the
      respective metric is computed for every week of the project lifecycle
      (starting from its day one until the present day), while Full refers
      to metrics that are computed aggregatively taking into account all
      project data. The results are stored in the collection “metrics”. Given
      that each contributor may contribute in more than one repositories,
      each document refers to the combination contributor-repository.

      DATASET CONSTRUCTION

      In a development community that is continuously moving towards
      component reuse, online software repositories constitute an integral
      part of the software development process. While this poses a
      series of challenges in terms of managing software development, it
      also provides a series of opportunities. These opportunities originate
      from the deluge of available data that enable quantifying
      the software development process and building effective evaluation
      models. Towards this direction, we extracted data residing in
      GitHub in order to construct a dataset that can be used for these
      purposes.

     > ###  RESEARCH DIRECTIONS
      Our dataset can be used to confront several challenges in current
      research. At first, given that it comprises various software process
      metrics along with the occurrence of multiple violations, it could be
      employed for extracting the behavior of the metrics and studying
      their co-evolution.
      The integration of semantics can also produce interesting findings
      about the expertise of individual developers. Our dataset includes
      source code (e.g. commits), textual (e.g. commit/issue comments),
      and process (e.g. bursts, activity periods) data that can be
      mined to extract the areas of expertise of each developer [9]. This
      information can be then used to construct developer profiles [9]
      or even visual resumes [20] and find the best match for the team.
      In an even more practical context, one can also search within a
      project for “the right developer for the job”. Research in the field of
      automated bug/feature assignment is broad and current methods
      use several metrics found in our dataset, including not only issuerelated
      data (issue text, keywords) [1, 22], but also information
      about the acquaintance of developers with specific components [3]
      or even about their latest activity in the project [7].

     >### CONCLUSIONS
     Mining contribution data from GitHub can offer useful insights on
      the software development process and produce practical results
      that may be used to improve it. In this work, we have pursued this
      research direction by creating a platform that can be employed to
      produce useful metrics. Furthermore, we have proposed a set of
      metrics and built a large dataset that can be used to answer multiple
      research questions. As future work, we plan to augment our dataset,
      by adding more repositories and, most importantly, more metrics
      that can cover additional development scenarios, such as supporting
      various programming languages (e.g. Python, JavaScript). Finally,
      it would be interesting to study the co-evolution of these metrics
      with regard to metrics relevant to the quality of the projects.