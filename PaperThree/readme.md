# Need for Tweet: How Open Source Developers Talk About Their GitHubWork on Twitter
## Authors
    Hongbo Fang, Daniel Klug, Hemank Lamba, James Herbsleb, Bogdan Vasilescu
## When
    Tue 30 Jun 2020 16:00 - 16:10 at MSR:Zoom - Developer Collaboration Chair(s): Bogdan Vasilescu

## Description
Social media, especially Twitter, has always been a part of the professional lives of software developers, with prior work reporting on a diversity of usage scenarios, including sharing information, staying current, and promoting one’s work. However, previous studies of Twitter use by software developers are generally restricted to surveys or small samples, and typically lack information about activities of the study subjects (and their outcomes) on other platforms. To enable such future research, in this paper we propose a computational approach to cross-linking users on Twitter and GitHub, the dominant platform for hosting open-source development, revealing 70,428 users active on both. As a preliminary analysis of this dataset, we report on a case study of 800 tweets by open-source developers about GitHub work, combining precise automatic characterization of tweet authors in terms of their relationship to the GitHub items linked in their tweets with a deep qualitative analysis of the tweet contents. We find that developers have very distinct behavioral patterns when including GitHub links in their tweets and these patterns are correlated with the relationship between the tweet author and the repository they link to. Based on this analysis, we hypothesize about what might explain such behavioral differences and what the implications of different tweeting patterns could be for the sustainability of GitHub projects.

## Book Link
>https://cmustrudel.github.io/papers/msr20tweets.pdf

>## Introduction
General social media platforms like Twitter, Facebook, and LinkedIn
are impacting the professional lives of many software developers,
facilitating communication and coordination, learning and knowledge
sharing, or recruiting and hiring just name a few.
Among these platforms, Twitter is especially popular with software
developers [4] and actively studied by software engineering
researchers (Sec. 2). Prior work has been exploring, e.g., how developers
use Twitter and what they talk about [15, 18], and has
been theorizing about Twitter’s effects on individual developers or
software development practices and outcomes.

### CROSS-LINKING GITHUB AND TWITTER

This section presents our heuristic approach to cross-link GitHub
and Twitter user accounts, based on mining GitHub user profile
pages and personal blogs for explicit URLs pointing to Twitter.

### CASE STUDY: HOWGITHUB DEVELOPERS TALK ABOUT THEIRWORK ON TWITTER
As a preliminary analysis of our dataset, we perform an exploratory
case study of the content of a sample of tweets by GitHub users in
our dataset, that contain links to GitHub artifacts. As a key contribution
compared to prior work, we use the cross-links between the
two platforms to automatically characterize the relationship of the
tweet authors to the GitHub artifacts their tweets point to, and use
this information as part of our analysis.

Sample Selection. To create our case study sample, we first collected
all the tweets returned by the Twitter API for each of the
70,427 users in our dataset (max 3,200 most recent per person),
and kept the recent ones, posted between January 1, 2018 and July
1, 2019. Among these tweets, we then identified those with URLs
containing the substring /github.com/, for a total of 131,217 tweets.
For each GitHub URL (repositories, issues, pull requests, comments,
etc), we recorded the repository the URL points to. After we filtered
out tweets containing two or more distinct GitHub URLs, to simplify
the subsequent qualitative analysis, 129,843 tweets remained.
### DISCUSSION
Implications. We found that among the tweets whose authors
have an identifiable relationship to the repository (i.e., non-Other),
most are posted by the repository owner and only a few are posted
by followers. This suggests that people engaged in the development
of the repository post most of the tweets linking back to GitHub.
On the other hand, around 40 % of all tweets with a GitHub link
are authored by people with no identifiable relationship to the
linked repository. We hypothesize that people knew about those
repositories from other places, and posted about them on Twitter
to further inform others. This suggests that there are channels
where people can learn about repositories without engaging in
their development or actively following their developers.

## Research
Cross-linking data across online platforms where open source developers
participate (in this paper GitHub and Twitter) is feasible
and it can help provide deeper insights into how the activities of
developers on one platform are moderated by the roles they play
on the other. The social media activities of developers may also
have direct impact on software development outcomes, including
open-source project success. We provide a large dataset mapping
70,427 open-source developer GitHub and Twitter accounts, as basis
for future (quantitative) empirical research in these directions.