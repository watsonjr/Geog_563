# Introduction to GitHub for Collaborative Research
This repository is a teaching resource that introduces the basics of using GitHub for collaborative research. 
It is designed for graduate students in ecology, oceanography, and related fields who are beginning to work on 
group projects that require shared code, data, and documentation.

Why GitHub matters in collaborative research
--------------------------------------------
GitHub is a platform that enables researchers to share code and data, collaborate on projects, track changes over time, 
and make research more transparent and reproducible. It mirrors the way modern science is done: collaboratively, openly, 
and with strong attention to detail and version history.

What you will learn
-------------------
By working through this material, you will learn how to:
- Create and manage GitHub repositories
- Make commits, branches, and pull requests
- Use Issues and Discussions to collaborate with others
- Write clear documentation in Markdown
- Apply best practices for reproducibility in research workflows

Getting Started with GitHub
---------------------------
1. Sign up for an account
   - Create a free account at GitHub.com.
   - Use your professional or university email for easy association with your research.

2. Install GitHub Desktop
   - Download GitHub Desktop: https://desktop.github.com/
   - Available for Windows and macOS.

3. Set up GitHub Desktop
   - Log in to GitHub Desktop with your GitHub.com account.
   - Configure your identity (name and email) in the application preferences.
   - Choose a local folder where your cloned repositories will be stored.

Core Concepts
-------------
- Repository (Repo): A folder that contains your project files and the full history of changes.
- Commit: A snapshot of your changes at a given time.
- Branch: A parallel version of your repo where you can safely experiment.
- Pull Request (PR): A request to merge your branch back into the main branch.
- Issue: A place to track tasks, bugs, or suggestions.
- Fork vs Clone:
  * Fork = make a personal copy of a repo under your GitHub account.
  * Clone = download a repo from GitHub to your computer using Desktop.

Basic Workflow
--------------
Typical workflow when collaborating on a project:

1. **Clone a repository**
   - In GitHub Desktop, go to File > Clone Repository.
   - Choose a repo from GitHub or paste the repo URL.
   - Select a local folder where the repo will be stored.

2. **Make changes**
   - Open the local repo folder and edit files (e.g., scripts, README).
   - GitHub Desktop will detect your changes.

3. **Commit changes**
   - In GitHub Desktop, review the changed files.
   - Write a clear commit message describing your changes.
   - Click "Commit to main" (or another branch).

4. **Push changes to GitHub**
   - Click "Push origin" to sync your changes with GitHub.com.

5. **Pull updates from others**
   - Click "Fetch origin" to check for updates.
   - If updates exist, click "Pull origin" to bring them into your local repo.

Collaboration on GitHub
-----------------------
- Branching workflow:
  1. In GitHub Desktop, go to the Current Branch menu > New Branch.
  2. Name your branch (e.g., "feature-plotting").
  3. Make edits locally and commit them to the branch.
  4. Push the branch to GitHub.com.
  5. On GitHub.com, open a Pull Request to merge your branch into main.

- Reviewing and merging pull requests:
  * On GitHub.com, review proposed changes.
  * Add comments, request edits, or approve.
  * Merge when ready.

- Using Issues:
  * Open issues in the GitHub.com repo to suggest changes or report problems.
  * Use labels (e.g., “bug,” “enhancement,” “documentation”).

- Using Discussions (if enabled):
  * Hold broader conversations outside the scope of specific issues or PRs.

Writing Good Documentation
--------------------------
- README.md should explain:
  * What the project is about
  * How to install or use it
  * Where to find more resources

- Good commit messages:
  * GOOD: "Add instructions for cloning repo"
  * BAD: "Fix stuff"

- Markdown basics:
  * # for headers
  * * for bullet lists
  * ``` for code blocks ```
  * [text](url) for links
  * ![](../../Resources/Images/image_1.png) for images

Common Mistakes & How to Fix Them
---------------------------------
- Merge conflicts: Occur when two people edit the same part of a file. GitHub Desktop will highlight conflicts and allow you to open the file in your editor to resolve them before committing.
- Accidentally committed wrong files: Add them to .gitignore to prevent future commits.
- Forgetting to pull before pushing: Always "Fetch origin" and "Pull origin" before pushing new commits.

Best Practices in Research
--------------------------
- Organize repos clearly:
  data/
  scripts/
  results/
  README.md

- Use .gitignore to exclude large files, raw data, or temporary outputs.

- Licensing:
  Add a license (e.g., MIT for code, CC-BY for data/documents).

- Small, frequent commits:
  Easier to review and roll back if necessary.

Further Reading
---------------
- [GitHub's Guide](https://docs.github.com/en/get-started/start-your-journey/hello-world)
- [The Git Book](https://git-scm.com/book/en/v2)
- [John Blischak's paper](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004668)

Other Resources
---------------
- [Code Academy](https://www.codecademy.com/learn/learn-git)
- [Datacamp class](https://www.datacamp.com/courses/introduction-to-github-concepts)
- [Cheatsheets](https://education.github.com/git-cheat-sheet-education.pdf)
- [Youtube](https://www.youtube.com/watch?v=a9u2yZvsqHA)... I linked just one, there are tonnes on there.

Exercises for Students
----------------------
1. Clone this repo using GitHub Desktop and add your name to a CONTRIBUTORS.md file.
2. Open an Issue on GitHub.com suggesting an improvement to this README.
3. Create a branch in GitHub Desktop, edit the README, and submit a Pull Request.

Happy collaborating! 🚀
