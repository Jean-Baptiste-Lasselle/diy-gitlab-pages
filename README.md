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

# Off to the future

Citation très intéressante de la doc :

>
> Additionally, you can have a distinct `./.gitlab-ci.yml` for each repository - even for each branch. This means you can test your script in parallel branches before pushing to your master branch. **If the build succeeds, you merge**.
>
> Source : https://about.gitlab.com/2016/04/07/gitlab-pages-setup/#gitlab-ci
>

https://github.com/Jean-Baptiste-Lasselle/diy-gitlab-pages

### Primer Step by Step

* _Step 1_ : Il faut avoir créé un "projet"( bon, un repo `git`)

* _Step 2_ : Créer son fichier `gitlab-ci.yml`. Quelques exemples :
  * Si l'on ne commit & push que du "statique" : HTML CSS JS MEDIA ASSETS (photo video etc...).
  * Si l'on a un site avec un static generator comme `hugo`, par exemple.

* _Step 3_ : on git commit et on pousse

```bash
git commit & push
```

et le site est disponible à :

* À la page : `https://gitlab.com/<YourUsername>/<your-hugo-site>/pipelines`, on trouvera un statut du build gitlab Pages
* À la page : `https://<YourUsername>.gitlab.io/<your-hugo-site>/`

After the build has passed, your new website is available at https://<YourUsername>.gitlab.io/<your-hugo-site>/.

## Sources

* https://about.gitlab.com/2016/04/07/gitlab-pages-setup/
* https://docs.gitlab.com/ee/user/project/pages/index.html

## ResSources

* http://tachyons.io/docs/themes/skins/

# Mdr

* À la page https://about.gitlab.com/2016/04/07/gitlab-pages-setup/#gitlab-ci :

>
> The most important fact is that with GitLab CI, you take control over your builds. They won't be in an invisible black box where you don't know what is going on! You can actually see any build running live
>
> (JBL : mort de rire la "black-box" évoquée ici est évidemment "Github Pages")
>
