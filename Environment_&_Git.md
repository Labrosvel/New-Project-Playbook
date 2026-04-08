# ENVIRONMENT
---
## Python environment
1. **python3 -m venv <env_name>**                    *# create env*
2. **source <env_name>/bin/activate**                *# activate it*
3. **deactivate**                                    *# deactivate it*
4. **pip list**                                      *# see what's in the environment*
5. **pip freeze > requirements.txt**                 *# export environment*
6. **source <env_name>/bin/activate**                *# return to venv*
7. **pip install -r requirements.txt**               *# clone to new environment*
8. **rm -rf <env_name>**                             *# remove environment*

## Conda environment
1. **conda env list**                                                    *# conda environment list*
2. **conda create --name myenv python=3.10**                            *# Create new environment*
3. **conda activate myenv**                                             *# Activate it*
4. **conda deactivate**                                                 *# Deactivate it*
5. **conda list**                                                       *# See what's in the base environment*
6. **conda activate base**                                              
7. **conda env export > base_environment.yml**                          *# Export env to a file*
9. **conda env create --name clonedenv --file base_environment.yml**    *# Clone base into a new env*
10. **conda env create -f <file.yml>**                                   *# Create env from file.yml*
12. **conda remove --name myenv --all**                                  *# Remove env*
13. **conda env update --name myenv --file environment.yml --prune**    *# Update env removing packages not in YAML*
15. **conda install -c conda-forge <package_name>**

## Kernel
1. **jupyter kernelspec list**    *# lists all available kernels*
2. **jupyter kernelspec remove <kernel_name>**    *# removes the kernel*
3. **python -m ipykernel install --user --name=<kernel_name> --display-name 'Python (kernel_name)'**    *#(Re-)registers a kernel from inside the current venv*

# GIT
---
## Initiate git
1. mkdir dirname
2. cd dirname
3. git init
4. ls -la .git
5. touch filename

## Link remote repo
1. Create repo in Github
2. git remote add origin url
3. git remote -v (for checking)
4. git push origin branchname
5. git remote rm origin
6. rm -rf .git*
7. git fetch origin branchname
8. git fetch --prune *#Synchronize the local with the remote*
9. git fetch --all --prune *#Synchronize all branches with the remote*
10. git pull --ff-only *#Validate that current branch is synchronized with remote*

## Standard git
- git add filename
- git add *
- git reset *#reverses the git add command*
- git add -u *#only adds files in the not staged status excluding untracked files*
- git commit -m 'message'
- git branch branchname
- git checkout branchname
- git status
- git log
- git branch ( , -a, -r)
- git merge branchname
- git push origin branchname (--force)
- git branch -d branchname
- git checkout -b branchname
- git checkout -b localbranch  origin/remotebranch
- git stash (-k)
- git branch -m newname
- git clone url newname
- git reflog
- git tag \<tagname\>
- git push origin \<tagname\>
- git push origin --tags
- git tag
- git tag -d \<tagname\>
- git push --delete origin \<tagname\>
- git push origin --delete branchname
- git branch -vv
- git branch --set-upstream-to=origin/branchname branchname
- git push -u origin branchname
- git checkout old-branch-name --> git branch -m new-branch-name

## Large files
- cd dirname
- git lfs install
- git lfs track '*filename.ext'
- git add .gitattributes
- git lfs migrate import --include='*file.ext'
- git actions as usual

# Git synchronisation
## 1. Verify branches status
- git status
- git branch
- git branch -r
## 2. Check sync status
- git branch -vv
- git checkout branchname
- git branch --set-upstream-to=origin/branchname branchname
- git branch -vv
- git push origin branchname
- git pull
## 3. Check dev and master are on the same commit
- git checkou branch1
- git log branch2..branch1
- git checkout branch2
- git log branch1..branch2





















