# tailwind-tutorial
All the course files for the Tailwind CSS tutorial on the Net Ninja YouTube channel.


# ------------------------------------------------
# SETUP
# ------------------------------------------------
# 1.1 - Clones the repo in the local machine.
Git clone https://github.com/iamshaunjp/tailwind-tutorial.git


# 1.2 - Gets all the remote branches.
Git fetch --all


# 1.3 - Start tracking of the branches. The command sets up the branches in the local repository and makes them track their counterparts in the  # remote repository. (Needs to be executed using Git Bash because of the "grep" command)

git branch -r | grep -v '\->' | sed "s,\x1B\[[0-9;]*[a-zA-Z],,g" | while read remote; do git branch --track "${remote#origin/}" "$remote"; done

# 1.4 - Push all local branches to origin and set them all to be tracked.
git push --all origin -u
# ------------------------------------------------




# ------------------------------------------------
# EXTRA NOTES
# ------------------------------------------------
# Adds a specific Remote Origin @ Github
git remote add origin https://github.com/[YOUR_GITHUB_ACCOUNT]/tailwind-tutorial.git


# Removes the Remote Origin
git remote remove origin


# Updates the Remote Origin
git remote set-url <REMOTE-NAME> <NEW-URL>


# Renames the Existing Remote
git remote rename <old-name> <new-name>


# Show the name and path of the Remote
git remote -v


# Pushes all commits of all branches to origin
git push --all origin -u
# To simplify that aswell, you can run 'git push --all origin -u' once and now all you’ll have to do is 'git push'. This will now by default push all branches to the default remote github.


# Pushes all commits of the current local branch (andy) to origin @ remote branch (andy). When pushing for the first time: git push -u origin branch_name, the -u flag tells git to make the local branch track the remote branch.
git push -u origin andy


# Pushes all committed code to the specified branch previously set by 'origin -u'.
git push 


# Pulls commits from the remote branch named 'main' @ github origin
git pull origin main


# Shorthand for pulling commits into local branch that is tracking a remote branch
git pull
# The git pull command is used to fetch and download content from a remote repository and immediately update the local repository to match that content. The git pull command is a combination of git fetch and git merge. git pull will download the content from the remote repository. Once the content is downloaded, git merge will merge the content to your local repository. A new merge commit will be created and HEAD updated to point at the new commit.