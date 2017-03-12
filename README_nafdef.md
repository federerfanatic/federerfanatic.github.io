# References:
# 1. http://stackoverflow.com/questions/2003505/how-to-delete-a-git-branch-both-locally-and-remotely
# 2. https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches
# Create a new branch locally:
git checkout -b "bleedingedge"
 # At which point one can add files and commit
git add && git commit 
 # As this git repository is on github one can make the
 # new branch the primary one on github
git branch --set-upstream-to=origin/bleedingedge

 # Make the remote the master again
git branch --set-upstream-to=origin/master
 # The the files that are not locally but remotely and put them in locally
git pull
 # GET rid of the 'bleedingedge' branch on github:`
git push origin --delete bleedingedge
 # So we force the issue with -D option:
git branch -D bleedingedge

# We want to push local changes to remote see reference 2:
git push origin [name of branch]
