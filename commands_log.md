## Process
This file helps keep track of commands used to edit the README file in this repository.

### Phase 1 - Setup
Initial Git setup was completed, and a new repository named "intern manifesto was created through GitHub. To clone the repository to the local machine, the following command was used:

``` git clone https://github.com/tarakeshwari-sn/intern-manifesto.git ```

After this, to create a new README.md file, the following command was used:

``` touch README.md ```

This created an empty README.md file in the local repository. Here, the title of the document was added using VS Code, and the changes were saved by committing the changes using the following commands:

``` git add . ```

``` git commit -m "Added title to README.md" ```

Finally, to push the changes to the remote repository, the following command was used:

``` git push origin main ```

### Phase 2 - Parallel Timelines
To create 3 parallel timelines in the README.md file, the following commands were used:

``` git checkout -b feature/expectations ```

``` git checkout -b feature/contributions ```

``` git checkout -b feature/day1-log ```

Each branch was used to add a specific section to the README.md file. After adding the content in each branch, the changes were committed and pushed to the remote repository using the following commands:

``` git add . ```

``` git commit -m "Added [section no] to README.md" ```

``` git push origin [branch name] ```

### Phase 3- Merging Branches
After completing the changes in each branch, the branches were merged into the main branch using pull requests on GitHub. The following steps were followed for each branch:

First, a pull request was created using Git CLI using the following command:

``` gh pr create --title "Adds [branch name] " --body "Adds [branch name] section." ```

After creating the pull request, to find out the PR number, the following command was used:

``` gh pr list ```

Finally, to merge the pull request, the following command was used:

``` gh pr merge [PR number] --merge ```

For the first branch, feature/expectations, the merge did not have any conflicts and merged smoothly. However,the second and third branch had conflicts while merging as they were modifying the same section of the README.md file. To resolve the conflicts, the following steps were followed:

I switched to the PR branch using the following command:

``` git checkout [branch name] ```

Then, I pulled the latest changes from the main branch using the following command:

``` git pull origin main ```

The main content was added tot he branch and commited using the following commands:

``` git add . ```

``` git commit -m "Resolved merge conflicts in [branch name]" ```

Finally, the changes were pushed to the remote repository using the following command:

``` git push origin [branch name] ```

After this,the pull request was squashed and merged  using the command:

``` gh pr merge [PR Number] --squash --delete-branch ```

This was repeated for both the branches with conflicts.

Finally, to ensure that the local main branch was up to date with the remote repository, the following commands were used:

``` git checkout main ```

``` git pull origin main ```

This completed the process of editing the README.md file with multiple branches and merging them into the main branch. Finally,this file was created to log the commands used in the process.
