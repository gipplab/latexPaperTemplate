# LaTeX paper template
This repository serves as a template for LaTeX papers. And guides you to the process of writing a scientific paper using LaTeX for a computer science conference or journal. Basic steps are

1) Set up and rename the repository.
1) Manage collaborators, permissions and links to the repository
1) Create a work-plan and distribute tasks
1) Document your research to allow for greater reproducibility
1) Select templates and plan paper outline
1) Write the paper collaboratively on GitHub
1) Get your paper proofread
1) Format shorten and submit
1) Get the preprint
1) submit to arxiv and archive the repo

## Set up and rename the repository

To start a new LaTeX paper project do the following.
1) Consider starting with Word. Writing in LaTeX comes with some overhead.
If you are unsure, if your paper project will mature and be eventually submitted start with a word document.
Also consult the corresponding [wiki page.](https://isgroup.atlassian.net/wiki/spaces/ISG/pages/16613454/Write+the+Paper)
If you just created this repository please consider [deleting it.](https://help.github.com/en/github/administering-a-repository/deleting-a-repository)
1) [Rename the github repository](https://help.github.com/en/github/administering-a-repository/renaming-a-repository) according to the following naming convention `YYConfTopic.`
Here `YY` is the year of the publication, `Conf` is the Camel-case acronym of the confierence, e.g, `Jcdl,` `Sigir,` or `Neurips.`
`Topic` is a descriptive word for your paper projekt to distinguish it from other papers from the group submitted to the same conference.
You can update the name later, especially if you decide to change the conference.
1) Generate a [github token](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line#creating-a-token) and check the repo permissions (the first group). This enables automated features of this repository, like the creation of PDF, spellchecking or conversion to a word document.
1) Set up the `GITHUB_TOKEN` on [travis.](travis-ci.com) Log in to travis and identify the newly created repository. From the repository go to `More options` -> `Settings`. Eventually you should end up at the following URL `https://travis-ci.com/ag-gipp/YYConfTopic/settings,` where `YYConfTopic` is your repo name as described above. In the section `Environment Variables` create a new variable and past the token you generated in the last step.

## Get the preprint

After your paper was accepted, the first author should carefully review the step-by-step instrunctions in the [wiki](https://isgroup.atlassian.net/wiki/spaces/ISG/pages/2818051/After+your+Paper+was+Accepted+Publishing+a+Paper+on+our+Website)
