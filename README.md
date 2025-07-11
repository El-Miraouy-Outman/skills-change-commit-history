<header>

<!--
  <<< Author notes: Course header >>>
  Read <https://skills.github.com/quickstart> for more information about how to build courses using this template.
  Include a 1280×640 image, course name in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Next to "About", add description & tags; disable releases, packages, & environments.
  Add your open source license, GitHub uses the MIT license.
-->

# Remove commit history

Accidental commits can be tricky to remove with Git. In this GitHub Skills course, you'll use BFG Repo-Cleaner to change the history of a Git repository. You can apply what you learn in this course to fully remove sensitive material from your own repository.

</header>

<!--
  <<< Author notes: Course start >>>
  Include start button, a note about Actions minutes,
  and tell the learner why they should take the course.
-->

## Welcome

A trustworthy commit history is the backbone of version control with Git. As a result, altering commit history is difficult by design. Sometimes, the history needs to be altered to remove credentials or other sensitive data that is mistakenly checked in. In this course, we'll learn how to remove content from repository's complete history and apply best practices for preventing accidental commits in the future.

- **Who is this for**: Intermediate users of Git, organizations
- **What you'll learn**: How to remove a file from Git's entire history
- **What you'll build**: You'll manipulate the history of a Git repository
- **Prerequisites**: We recommend you clone this repository to your machine and use the command line to follow along. You'll also need to install BFG Repo-Cleaner, but the steps will be covered in the course.
- **How long**: This course takes less than 1 hour to complete.

In this course, you will:

1. Remove content from the root directory of a repository
2. Use BFG Repo-Cleaner to remove content from repository history
3. Avoid future accidental commits by adding a pattern to `.gitignore`

### How to start this course

<!-- For start course, run in JavaScript:
'https://github.com/new?' + new URLSearchParams({
  template_owner: 'skills',
  template_name: 'change-commit-history',
  owner: '@me',
  name: 'skills-change-commit-history',
  description: 'My copy of the skills course on changing commit history',
  visibility: 'public',
}).toString()
-->

[![start-course](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=skills&template_name=change-commit-history&owner=%40me&name=skills-change-commit-history&description=My+copy+of+the+skills+course+on+changing+commit+history&visibility=public)

1. Right-click **Start course** and open the link in a new tab.
2. In the new tab, most of the prompts will automatically fill in for you.
   - For owner, choose your personal account or an organization to host the repository.
   - We recommend creating a public repository, as private repositories will [use Actions minutes](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions).
   - Scroll down and click the **Create repository** button at the bottom of the form.
3. After your new repository is created, wait about 20 seconds, then refresh the page. Follow the step-by-step instructions in the new repository's README.
<header>

<!--
  <<< Author notes: Course header >>>
  Read <https://skills.github.com/quickstart> for more information about how to build courses using this template.
  Include a 1280×640 image, course name in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Next to "About", add description & tags; disable releases, packages, & environments.
  Add your open source license, GitHub uses the MIT license.
-->

# Remove commit history

Accidental commits can be tricky to remove with Git. In this GitHub Skills course, you'll use BFG Repo-Cleaner to change the history of a Git repository. You can apply what you learn in this course to fully remove sensitive material from your own repository.

</header>

<!--
  <<< Author notes: Step 1 >>>
  Choose 3-5 steps for your course.
  The first step is always the hardest, so pick something easy!
  Link to docs.github.com for further explanations.
  Encourage users to open new tabs for steps!
-->

## Step 1: Removing sensitive data

_Welcome to "Change commit history"! :wave:_

We'll start by working with `.env` files. These files usually contain sensitive content. For this course, we'll work on removing that file and all traces in the Git history. The first step is to remove the file from repository. We'll alter the history later.

We'll assume you're using the command line, but you can complete the course using your preferred tooling.

**What is _sensitive content_?** Sensitive content is anything that is checked into your repository history that may put you or your organization at risk. This content usually comes in the form of credentials (i.e., passwords, access keys). The best practice for accidentally exposed sensitive content is to invalidate it (i.e., revoke a personal access token), completely remove it from all repository copies, and take measures to prevent future exposure.

See [Deleting a file on GitHub Docs](https://docs.github.com/en/repositories/working-with-files/managing-files/deleting-files-in-a-repository#deleting-a-file) if you need additional help removing a file.

### :keyboard: Activity: Remove `.env` in the project root directory

1. Open your terminal of choice, clone this repository, and switch to your repository directory.
   ```shell
   git clone <your-repository-url>
   cd <your-repository-name>
   ```
2. Delete `.env` from the root directory.
   ```shell
   git rm .env
   ```
3. Commit the removal of `.env`.
   ```shell
   git commit -m "remove .env file"
   ```
4. Push the removal to GitHub:
   ```shell
   git push
   ```
5. Wait about 20 seconds then refresh this page (the one you're following instructions from). [GitHub Actions](https://docs.github.com/en/actions) will automatically update to the next step.

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/change-commit-history) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2024 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/change-commit-history) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2024 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>


<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/change-commit-history) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2024 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>


<header>

<!--
  <<< Author notes: Course header >>>
  Read <https://skills.github.com/quickstart> for more information about how to build courses using this template.
  Include a 1280×640 image, course name in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Next to "About", add description & tags; disable releases, packages, & environments.
  Add your open source license, GitHub uses the MIT license.
-->

# Remove commit history

Accidental commits can be tricky to remove with Git. In this GitHub Skills course, you'll use BFG Repo-Cleaner to change the history of a Git repository. You can apply what you learn in this course to fully remove sensitive material from your own repository.

</header>

<!--
  <<< Author notes: Step 2 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## Step 2: Removing a file from Git history using BFG Repo-Cleaner

_You removed `.env` from the repository's root directory! :tada:_

Now that we've deleted the file, people that browse the repository on GitHub.com or anyone looking at just the head commit won't see the file. However, due to Git's nature, the file is still present in the history. In this step, we'll work on removing the file from the repository history.

**What is a _head commit_**? In Git, HEAD points to a branch or a commit. When we say [head commit](https://docs.github.com/en/get-started/quickstart/github-glossary#head), we usually mean the most recent commit in the repository's history.

There are multiple tools available for removing Git history, we'll use BFG Repo-Cleaner in this step. You can find additional documentation on [Using the BFG in GitHub Docs](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository#using-the-bfg).

**What is _BFG Repo-Cleaner_**? BFG Repo-Cleaner is software that can help you search through and alter repository history. Git can natively do this using [`git filter-repo`](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository#using-git-filter-repo), but it can be more complex.

### :keyboard: Activity: Use BFG Repo-Cleaner to remove the `.env` file

1. Update the local copy of your repository to ensure you have the most recent version of the course files.
   ```shell
   git pull
   ```
2. Install BFG Repo-Cleaner on your machine. You can follow the [instructions on the web site](https://rtyley.github.io/bfg-repo-cleaner/) to do so or you can use a package manager for your operating system.
3. Confirm the `.env` file is removed from the root directory. The command should return empty.
   ```shell
   find . -name ".env"
   ```
4. Search for .env in the repository's history. The command should return at least 2 commits: the addition of `.env` when you copied this template repository, and the removal of `.env`.
   ```shell
   git log --stat --all -- .env
   ```
5. Use BFG Repo-Cleaner to delete all references to `.env` that exist in the repository.
   ```shell
   
   bfg --delete-files .env 
   ou 
   wget https://repo1.maven.org/maven2/com/madgag/bfg/1.14.0/bfg-1.14.0.jar -O bfg.jar
   java -jar bfg.jar --delete-files '.env'
   git reflog expire --expire=now --all
   git gc --prune=now --aggressive

   ```
6. The tool will run and make some suggestions about some follow-up commands. Run those to get your local repository cleaned up.
7. Repeat the search for `.env` in the repository's history. This time, the command should return empty.
   ```shell
   git log --stat --all -- .env
   ```
8. Push your changes to GitHub. Note we're using the `--force` argument in this step since we're altering Git history.
   ```shell
   git push --force
   ```
9. Wait about 20 seconds then refresh this page (the one you're following instructions from). [GitHub Actions](https://docs.github.com/en/actions) will automatically update to the next step.

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/change-commit-history) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2024 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>

<header>

<!--
  <<< Author notes: Course header >>>
  Read <https://skills.github.com/quickstart> for more information about how to build courses using this template.
  Include a 1280×640 image, course name in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Next to "About", add description & tags; disable releases, packages, & environments.
  Add your open source license, GitHub uses the MIT license.
-->

# Remove commit history

Accidental commits can be tricky to remove with Git. In this GitHub Skills course, you'll use BFG Repo-Cleaner to change the history of a Git repository. You can apply what you learn in this course to fully remove sensitive material from your own repository.

</header>

<!--
  <<< Author notes: Step 3 >>>
  Start this step by acknowledging the previous step.
  Define terms and link to docs.github.com.
-->

## Step 3: Avoiding future commits with `.env`

_Nice work removing the file from entire history of the repository! :sparkles:_

The steps we've taken so far ensure that any _new_ clones of the repository don't contain the sensitive data. But what about collaborators that may already have a copy of the repository? You should ask anyone with a copy of the repository to delete it and clone the repository fresh. In a real-life scenario, you'd also take [additional steps](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository#fully-removing-the-data-from-github) to ensure no sensitive data is cached on GitHub.com.

Now that we've mitigated the risk of exposing sensitive content, we'll be proactive and prevent its addition.

We'll now configure Git so it ignores a future addition of sensitive content by adding `.env` to `.gitignore`. If someone should that file to the local copy of their repository, it will remain only on the contributor's machine and won't be pushed to GitHub.

**What is `.gitignore`?** This special file allows us to tell Git naming patterns to ignore. You can read more about it in [Ignoring files on GitHub Docs](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files).

### :keyboard: Activity: Add `.env` to `.gitignore`

1. Update the local copy of your repository to ensure you have the most recent version of the course files.
   ```shell
   git pull
   ```
2. Locate the file we added to the repository titled `.gitignore`.
3. Add `.env` to the file.
4. Stage, commit the file:
   ```shell
   git add .gitignore
   git commit -m "ignore .env files"
   ```
5. Push the file to GitHub.com
   ```shell
   git push
   ```
6. Wait about 20 seconds then refresh this page (the one you're following instructions from). [GitHub Actions](https://docs.github.com/en/actions) will automatically update to the next step.

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/change-commit-history) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2024 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>

<header>

<!--
  <<< Author notes: Course header >>>
  Read <https://skills.github.com/quickstart> for more information about how to build courses using this template.
  Include a 1280×640 image, course name in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Next to "About", add description & tags; disable releases, packages, & environments.
  Add your open source license, GitHub uses the MIT license.
-->

# Remove commit history

Accidental commits can be tricky to remove with Git. In this GitHub Skills course, you'll use BFG Repo-Cleaner to change the history of a Git repository. You can apply what you learn in this course to fully remove sensitive material from your own repository.

</header>

<!--
  <<< Author notes: Finish >>>
  Review what we learned, ask for feedback, provide next steps.
-->

## Finish

_Congratulations friend, you've completed this course!_

<img src="https://octodex.github.com/images/dinotocat.png" alt=celebrate width=300 align=right>

Here's a recap of all the tasks you've accomplished in your repository:

- Removed a file from the head commit of the repository
- Used BFG Repo-Cleaner to removed a file from all Git history in the repository
- Avoided accidental commits by telling Git to ignore a specific file name

### What's next?

- The Docs on [Removing sensitive data](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository) are comprehensive and recommended reading after this course.
- Try your hand at some of the other features listed in the [BFG Repo-Cleaner documentation](https://rtyley.github.io/bfg-repo-cleaner/).
- [We'd love to hear what you thought of this course](https://github.com/orgs/skills/discussions/categories/change-commit-history).
- [Take another GitHub Skills course](https://github.com/skills).
- [Read the GitHub Getting Started docs](https://docs.github.com/en/get-started).
- To find projects to contribute to, check out [GitHub Explore](https://github.com/explore).

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/change-commit-history) &bull; [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2024 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

</footer>

