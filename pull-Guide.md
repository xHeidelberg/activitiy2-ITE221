### Step 1: Clone the repository
First, you need to have a local copy of the repository you intend to contribute to. Use the git clone command to clone the repository:<br>

<code>git clone https://github.com/xHeidelberg/activitiy2-ITE221.git </code> <br>
<code>cd activity2-ITE221</code>

### Step 2: Step 2: Create a new branch
Creating a branch in Git allows you to work on new features or fixes without affecting the main codebase. Use the git checkout command to create and switch to a new branch: <br>

<code>git checkout -b (Branch Name) </code>

### Step 3: Make changes and commit them
After creating your branch, make your code changes. Once you're done, use the <code>git add .</code> command to stage your changes and <code>git commit</code> to commit them: <br>

<code>git add .<br></code>
<code>git commit -m "Add a detailed commit message describing your changes" </code> <br>

### Step 4: Push your branch to GitHub
To make your branch available on GitHub, use the git push command. Since this branch doesn’t exist on GitHub yet, you need to set the <a target="_blank" href="https://graphite.com/guides/git-set-upstream">upstream branch</a>: <br>

<code>git push --set-upstream origin (Branch Name)
</code>

### Step 5: Create the pull request
Now that your branch is on GitHub, you can use the GitHub CLI to create a pull request. Run the following command: <br>

<code>gh pr create --base main --head (Branch Name) --title "Your PR title" --body "Detailed description of the changes"</code> <br>

### Step 6: Monitor and modify the pull request

Once your pull request is created, you may need to monitor its status or make additional modifications based on feedback from reviewers. Use the following commands to manage your pull request:
<ul>

<li>List pull requests: <code>gh pr list</code> — shows a list of pull requests in the repository.</li>

<li>Check out pull requests locally:<code> gh pr checkout PR_NUMBER </code>— allows you to checkout a particular pull request locally.</li>

<li>View pull request in the browser:<code> gh pr view --web </code>— opens the pull request in your web browser.</li>
<ul>
<br>
As an example here’s what you might see in your terminal when pushing a branch and creating a pull request:

<code>
$ git push --set-upstream origin feature-branch
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 362 bytes | 362.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote: Resolving deltas: 100% (0/0), completed with 0 local objects.
To https://github.com/xHeidelberg/activitiy2-ITE221.git
 * [new branch]      feature-branch -> feature-branch
Branch 'feature-branch' set up to track remote branch 'feature-branch' from 'origin'.
<
$ gh pr create --base main --head feature-branch --title "New feature" --body "Adding a new feature"
Creating pull request for feature-branch into main in username/repository
https://github.com/xHeidelberg/activitiy2-ITE221.git


</code>
