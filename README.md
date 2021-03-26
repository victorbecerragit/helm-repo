# helm-repo

*Run in your local chart:

$helm repo index .
$cat index.yaml
 
echo "# helm-repo" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/victorbecerragit/helm-repo.git
git push -u origin main

*Create a new branch to push index.yaml and the new helm packages to github pages.

 git checkout --orphan gh-pages

 git add index.yaml ca-webapp-0.1.0.tgz ca-webapp-0.1.1.tgz ca-webapp-0.1.2.tgz

 git status

 git commit -am "helm packages demo files"

 git push origin gh-pages

 
 *Test that you can read the index.yaml from the gh-repo
 
 curl -i  https://victorbecerragit.github.io/helm-repo/index.yaml
 
 *Add the gh-repo to your local helm repositories
 
 helm repo add helm-gh-repo-demo  https://victorbecerragit.github.io/helm-repo/
 helm repo update
 helm repo list
 helm search repo helm-gh-repo-demo
 
 
