# diy-gitlab-pages

Un primer, et quelques bonnes recettes gitlab pages


## Back to the present


```bash
export URI_DE_CE_REPO=https://github.com/Jean-Baptiste-Lasselle/diy-gitlab-pages

export COMMIT_MESSAGE=""
export COMMIT_MESSAGE="$COMMIT_MESSAGE Reprise de travail"

git clone "$URI_DE_CE_REPO" .

atom .

# git add --all && git commit -m "$COMMIT_MESSAGE" && git push -u origin master

```

# Primer



## Sources

* https://about.gitlab.com/2016/04/07/gitlab-pages-setup/
* https://docs.gitlab.com/ee/user/project/pages/index.html


# Mdr

* À la page https://about.gitlab.com/2016/04/07/gitlab-pages-setup/#gitlab-ci :

>
> The most important fact is that with GitLab CI, you take control over your builds. They won't be in an invisible black box where you don't know what is going on! You can actually see any build running live
>
> (JBL : mort de rire la "black-box" évoquée ici est évidemment "Github Pages")
>
