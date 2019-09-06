# Kezako

Le Dockerfile doit être utilisé comme indique ici (accès restreint): https://gitlab.com/second-bureau/omega/blob/master/operations.sh

Notre objectif : transformer le dockerfile, en un `.gitlab-ci.yml`.


## Travaux préliminaires


* Initialisation du site à partir d'un template :

```bash
# Gitlab veut partir d'une image Docker hugo "toute faite"
# On est à la racine du repo

export HUGO_THEME_GIT_REPO_URI=https://github.com/budparr/gohugo-theme-ananke.git
export NOM_COMMERCIAL_SITE=wiki.nso.io
export HUGO_STARTER_LOCAL_ID=starter-wiki-nso

hugo new site $NOM_COMMERCIAL_SITE

ls -allh ./$NOM_COMMERCIAL_SITE

cd ./$NOM_COMMERCIAL_SITE && git submodule add $HUGO_THEME_GIT_REPO_URI themes/$HUGO_STARTER_LOCAL_ID

sed -i 's#HUGO_STARTER_LOCAL_ID_JINJA2_VAR#$HUGO_STARTER_LOCAL_ID#g' ./config.toml

cp -Rf ./$NOM_COMMERCIAL_SITE/themes/starter-wiki-nso/layouts/* ./$NOM_COMMERCIAL_SITE/layouts/

# puis on peut ajouter du contenu ensuite

hugo new posts/premier-article.md

```

* Ajout d'un post :

```bash
# Gitlab veut partir d'une image Docker hugo "toute faite"
# On est à la racine du repo

export HUGO_THEME_GIT_REPO_URI=https://github.com/budparr/gohugo-theme-ananke.git
export NOM_COMMERCIAL_SITE=wiki.nso.io
export HUGO_STARTER_LOCAL_ID=starter-wiki-nso

hugo new site $NOM_COMMERCIAL_SITE

ls -allh ./$NOM_COMMERCIAL_SITE

cd ./$NOM_COMMERCIAL_SITE && git submodule add $HUGO_THEME_GIT_REPO_URI themes/$HUGO_STARTER_LOCAL_ID

sed -i 's#HUGO_STARTER_LOCAL_ID_JINJA2_VAR#$HUGO_STARTER_LOCAL_ID#g' ./config.toml

cp -Rf ./$NOM_COMMERCIAL_SITE/themes/starter-wiki-nso/layouts/* ./$NOM_COMMERCIAL_SITE/layouts/

# puis on peut ajouter du contenu ensuite

```
