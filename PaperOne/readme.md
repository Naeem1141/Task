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