LaTeX paper template
====================

This repository serves as a template for LaTeX papers.
Furthermore, it guides you to the process of writing a scientific paper using LaTeX for a computer science conference or journal.
The repository contains several different paper formats (acmart, llncs, and preprints). The content is explained below in **Repo Content**.

Basic steps are

1.  Set up and rename the repository.

2.  Manage collaborators, permissions and links to the repository

3.  Create a work-plan and distribute tasks

4.  Document your research to allow for greater reproducibility

5.  Select templates and plan paper outline

6.  Write the paper collaboratively on GitHub

7.  Get your paper proofread

8.  Format shorten and submit

9.  Get the preprint

10. submit to arxiv and archive the repo


Repo Content
==================

For writing your paper you only need to consider the files with numbers in front `01-08`. When ever you push your changes to github, it automatically
compiles your files (takes about 3min). You find all important files under [releases](/releases).

If you want to compile your files locally, take one the following files:
* `acm.tex` if you submit to an acm conference with sigconf format
* `llncs.tex` if you submit to a conference with the LLNCS format
* `article_preprint.tex` for a preprint version with the article format (one column)
* `acm_preprint.tex` for the preprint version with the acmart format (two columns)

You do not need to change these files in general! All you need to change to edit the content of your paper, edit the files with numbers in front `01-08`.
If you know you don't need acm, than you can ignore all numbered files followed by `acm`, e.g. `05_acm_authors.tex`. Likewise, if you do not need LLNCS at all,
you can ignore the files with `llncs` in it.

Here is an explaination for each file:
1. `01_title.tex` defines the title and short title of the paper. If you do not have a short (also known as running title), just keep it argument for `shortTitle` empty.
2. `02_abstract.tex` contains the abstract of your paper.
3. `03_mainmatter.tex` contains the entire paper content, with sections, textes, figures, etc.
4. `04_keywords.tex` contains the keywords for your paper. If you don't have any, simply delete the content of this file.
5. `05_[acm|llncs]_authors.tex` defines the authors of your paper. Change the file that fits your conference format. For acm use `05_acm_authors.tex`. Unfortunately, the formats are restrictive how to setup authors. Hence, we recommend you change the authors for both `05_acm_authors.tex` and `05_llncs_authors.tex`. Hence, all generated PDFs show the correct authors, also the preprints.
6. `06_[acm|llncs]_acknowledgments.tex` defines the acknowledgments. If you dont have any, just delete the content of the file.
7. `07_reference.tex` contains the reference to this paper. This is needed once you want to publish your preprint! Here you enter the bib-reference to your paper. 
8. `08_acm_categories.tex` you only need to bother with this file if you submit to an acm conference. In this case, change the categories accordingly.


**Double Blind:** For double-blind proceedings in acm format, simply the first line in `acm.tex` to: 
```
\documentclass[sigconf,natbib=false,anonymous]{acmart}
```

**Packages:** If you require more packages, add them to `header.tex`. Check the [releases](/releases) on GitHub, when you add more packages. Sometimes there are conflicts that appear in different formats.

**Preprints:** The generated preprints are the official preprint layout from ag-gipp. If you publish your preprints on arxiv, you need to upload only either `article-arxiv.tar.gz` or `acm-arxiv.tar.gz`. They contains all files necessary for arxiv to compile your paper. If you want to check how your preprints look like, simply check the preprint pdfs in [releases](/releases): `article_preprint.pdf` and `acm_preprint.pdf`.

**What are the other files in [releases](/releases)?** You will also find `main.docx` which is a word version of your latex llncs-formatted paper (not acm-formatted). You also find `spellcheck.html` which is a spellchecker also based on your llncs-formatted paper.


## 1) Set up and rename the repository

To start a new LaTeX paper project, do the following:

1) Consider starting with Word:
Writing in LaTeX comes with some overhead.
If you are unsure if your paper project will mature and be eventually submitted start with a word document.
Also, consult the corresponding
[wikipage.](https://isgroup.atlassian.net/wiki/spaces/ISG/pages/16613454/Write+the+Paper)
If you just created this repository, please consider 
[deleting it.](https://help.github.com/en/github/administering-a-repository/deleting-a-repository)
1) [Rename the GitHub repository](https://help.github.com/en/github/administering-a-repository/renaming-a-repository)
according to the following naming convention `YYConfTopic.` 
Here `YY` is the year of the publication, 
`Conf` is the Camel-case acronym of the conference,
e.g, `Jcdl, Sigir,` or `Neurips.
Topic` is a descriptive word for your paper projekt to distinguish it from other papers from the group submitted to the same conference.
You can update the name later, especially if you decide to change the conference. 
1) Generate a
[GitHub token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line#creating-a-token)
and check the repo permissions (the first group).
This enables automated features of this repository, like the creation of PDF, spellchecking or
conversion to a word document. 
1) Set up the `GITHUB_TOKEN` on
[travis.](travis-ci.com)
Log in to travis and identify the newly created repository.
From the repository go to `More options` -\> `Settings`.
Eventually, you should end up at the following URL
`https://travis-ci.com/ag-gipp/YYConfTopic/settings,`
where `YYConfTopic` is your repo name as described above.
In the section `Environment Variables,`
create a new variable and pass the token you generated in the last step. 1)
Change the title of the paper in the file
[header.tex](/header.tex).
If you set up the environment variables correctly, the PDF, Word and Spellcheck document should appear in about 5 minutes after the change as
[release](https://help.github.com/en/github/administering-a-repository/viewing-your-repositorys-tags).
1) Retrigger the initial build and ensure that the build passes. You should see the first release in the releases section.
## 2) Manage collaborators, permissions and links to the repository

Take a moment to review the permissions and settings of your new repo.
Invite collaborators that are on GitHub.
Contact other collaborators and ask for their GitHub account names.
Also, link the newly created repository from the corresponding issue in
[JIRA](https://isgroup.atlassian.net/secure/RapidBoard.jspa?rapidView=53&projectKey=MPE&view=planning.nodetail&issueLimit=100)
and to the [Confluence page.](https://isgroup.atlassian.net/wiki/spaces/ISG/pages/54912991)

## 3) Create a work-plan and distribute tasks

After having invited all collaborators to the repository make a work plan, e.g.
using Github issues.
Make sure to schedule the work ahead.
Discuss with your collaborators the distribution of the workload.
Only a significant contribution warrants the co-authorship on the paper.
It is the job of the first author to manage all coauthors and to ensure that everyone contributes their fair share to the project.

## 4) Document your research to allow for greater reproducibility

You can use this GitHub Repository to document your daily progress on the
research project. For example, create a folder called _log_ and create a plaintext or
markdown file. Before you stop working on the project, document the most
critical steps you did. Copy and paste locations and commands you used during
your research including links to help pages and screenshots. Spending 5 minutes
before leaving might save 1 hour the next day.

## 5) Select templates and plan paper outline

Consult the conference website on the requirements regarding formatting. Decide
if you are heading for a long or a short paper. Plan the length of the sections
individually

## 6) Write the paper collaboratively on GitHub


If multiple co-authors are contributing to the document text it might be most
convenient to split the paper into different files so that each coauthor works
on its own file. Otherwise, only the first author should do changes to the
repository. Other co-authors should use pull-request to submit changes.

## 7) Get your paper proofread

Be sure to get your paper proofread at least one week prior to the submission
deadline. See the hints in the wiki.

## 8) Format shorten and submit

Plan one day to format and shorten the paper. Be sure to commit regularly so
that you can revert changes if something goes wrong. After you are done with
reformatting, ensure that all your coauthors review the paper before
submission.

## 9) Get the preprint

After your paper was accepted, the first author should carefully review the
step-by-step instructions in the
[wiki](https://isgroup.atlassian.net/wiki/spaces/ISG/pages/2818051/After+your+Paper+was+Accepted+Publishing+a+Paper+on+our+Website)

## 10) submit to arxiv and archive the repo

