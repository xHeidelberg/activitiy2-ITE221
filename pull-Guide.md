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
<ol>

<li>List pull requests: gh pr list — shows a list of pull requests in the repository.</li>

<li>Check out pull requests locally: gh pr checkout PR_NUMBER — allows you to checkout a particular pull request locally.</li>

<li>View pull request in the browser: gh pr view --web — opens the pull request in your web browser.</li>
<ol>
As an example here’s what you might see in your terminal when pushing a branch and creating a pull request:


