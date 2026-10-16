# The Git Guide

A small website about Git and GitHub, made with HTML, CSS and JavaScript by Maximilian Bahrami (@MaxiBahrami). This repository currently records individual work.

## Submission links

- Repository: https://github.com/MaxiBahrami/git-essentials
- Website (available after GitHub Pages is enabled): https://maxibahrami.github.io/git-essentials/

## Pages

- `index.html` – Home
- `project.html` – Starting projects, local and remote repositories
- `changes.html` – Making and sharing changes
- `branching.html` – Branches, pull requests, reviews and merge conflicts
- `about.html` – Project and author

Shared styles are in `assets/style.css`. `assets/script.js` handles the mobile menu and code copy buttons. No dependencies or build step are needed.

## Run locally

```bash
git clone https://github.com/MaxiBahrami/git-essentials.git
cd git-essentials
python3 -m http.server 8000
```

Open http://localhost:8000. Stop the server with Ctrl+C. You can also open `index.html` directly, but clipboard access may be unavailable. If copying is blocked, select the code and copy it manually.

## Publish with GitHub Pages

1. Open https://github.com/MaxiBahrami/git-essentials/settings/pages while signed in as the repository owner.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose `main` and `/(root)`, then save.
4. Wait for the Pages deployment to finish, then open the website link above.
5. Check all five pages on the published site before submitting.

## Make a change

```bash
git switch main
git pull origin main
git switch -c fix/describe-the-change
# Edit and check the affected files
git status
git diff
git add path/to/changed-file
git commit -m "Describe the change"
git push -u origin fix/describe-the-change
```

Open a pull request into `main` and explain the change and checks performed. If the assignment requires collaboration, another real student must review the work using their own account. Do not invent contributors or reviews.

## Verification recorded on 16 October 2026

- All five HTML pages have working local file references and fragment targets, one main heading and the correct active navigation link.
- JavaScript syntax passes. Menu state changes and copy success/failure feedback pass checks with a simulated DOM.
- Responsive CSS is present for mobile and desktop, including scrollable code blocks and tables. Visual browser checks at both sizes are still required; source checks alone do not confirm the layout.
- GitHub and GitHub Docs external links returned HTTP 200. The Git documentation URL returned HTTP 403 from the checking environment, so its availability needs a manual browser check.
- Existing history includes the initial commit and merged PR #1 from `feature/update-about-page`. PR #1 has no submitted review.
- The expected Pages URL returned HTTP 404 at the time of checking. Publication is not yet verified.

## Before submitting

- [ ] Enable GitHub Pages from `main` / `/(root)` and confirm the deployment succeeds.
- [ ] Open every page at desktop and phone widths; check for horizontal page overflow.
- [ ] Test the mobile menu, keyboard navigation, code copy buttons and all external links in a browser.
- [ ] Check the actual assignment instructions with the teacher: individual work is recorded here. If group participation, individual branches/commits/PRs, reviews by another student, or a demonstrated merge conflict are required, those must be completed genuinely or explicitly waived. A conflict example in a guide is not evidence of resolving a real conflict.
- [ ] Submit the repository link and the working Pages link.

## References

- [Git documentation](https://git-scm.com/docs)
- [GitHub Docs](https://docs.github.com/)
