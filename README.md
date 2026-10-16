# The Git Guide

A small group website about Git and GitHub, made with HTML, CSS and JavaScript.

## Pages

- `index.html` – Home
- `project.html` – Starting projects, local and remote repositories
- `changes.html` – Making and sharing changes
- `branching.html` – Branches, pull requests, reviews and merge conflicts
- `about.html` – Group members (add your own names and GitHub usernames)

Styles are in `assets/style.css`. The JavaScript in `assets/script.js` handles the mobile menu and copy buttons.

## Open the website

Open `index.html` in a browser. The website does not need any installation or build step.

## Put the website on GitHub

Create an empty repository on GitHub and copy its URL. In the project folder, run:

```bash
git init
git branch -M main
git add .
git commit -m "Add website pages"
git remote add origin https://github.com/USERNAME/git-guide.git
git push -u origin main
```

Replace `USERNAME` with the GitHub account name. If the group already has a shared repository, clone that repository instead of creating a second one.

## Publish with GitHub Pages

1. Open the repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose `main` and `/(root)`, then save.
5. Find the published website address under GitHub Pages. For a project repository it will usually look like `https://USERNAME.github.io/git-guide/`.

## Working as a group

Each member should do the Git tasks themselves so they show up in the GitHub history.

```bash
git clone https://github.com/USERNAME/git-guide.git
cd git-guide
git switch -c feature/my-page
# Make a change to a file
git add .
git commit -m "Update my page"
git push -u origin feature/my-page
```

Open a pull request on GitHub, ask someone else to review it, and merge the branch when the changes are ready. Each member also needs to review another person's pull request and merge a branch. Remember to pull the latest `main` before starting new work.

If two people edit the same part of a file, Git may report a merge conflict. Read both changes, decide what to keep, remove the conflict markers, test the page and commit the resolved file.

## Before submitting

- [ ] Replace the example team members and usernames in `about.html`.
- [ ] Check the five pages on a phone-sized screen and on desktop.
- [ ] Check all links, examples and spelling.
- [ ] Confirm each member has created a branch, commit and pull request, reviewed someone else's code and merged a branch.
- [ ] Confirm the GitHub Pages link is working.
- [ ] One person submits the repository link and live website link.

## References

- [Git documentation](https://git-scm.com/docs)
- [GitHub Docs](https://docs.github.com/)
