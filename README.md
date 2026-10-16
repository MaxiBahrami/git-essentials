# The Git Guide

A small website about Git and GitHub, made with HTML, CSS and JavaScript by Maximilian Bahrami (@MaxiBahrami). This repository currently records individual work.

## Submission links

- Repository: https://github.com/MaxiBahrami/git-essentials
- Live website: https://maxibahrami.github.io/git-essentials/

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
- All five published pages were visually checked at desktop width (1348 CSS pixels of content), with no horizontal page overflow. Responsive CSS is present, but phone-width visual checks are still required.
- Live click, clipboard and keyboard checks could not be completed because the test browser restricted interactions after sign-in. The simulated JavaScript checks above do not replace those live checks.
- GitHub and GitHub Docs external links returned HTTP 200. The Git documentation URL returned HTTP 403 from the checking environment, so its availability needs a manual browser check.
- Existing history includes the initial commit and merged PR #1 from `feature/update-about-page`. PR #1 has no submitted review.
- GitHub Pages is enabled using **Deploy from a branch**, `main`, `/(root)`. The [Pages deployment](https://github.com/MaxiBahrami/git-essentials/actions/runs/38930456428) succeeded.
- The live root URL, all five HTML pages, CSS and JavaScript returned HTTP 200 after publication.

## Before submitting

- [x] Enable GitHub Pages from `main` / `/(root)` and confirm the deployment succeeds.
- [x] Check all five published pages at desktop width for layout and horizontal page overflow.
- [ ] Check all five pages at phone widths for layout and horizontal page overflow.
- [ ] Test the mobile menu, keyboard navigation, code copy buttons and all external links in a browser.
- [ ] Check the actual assignment instructions with the teacher: individual work is recorded here. If group participation, individual branches/commits/PRs, reviews by another student, or a demonstrated merge conflict are required, those must be completed genuinely or explicitly waived. A conflict example in a guide is not evidence of resolving a real conflict.
- [ ] Submit the repository link and the working Pages link.

## References

- [Git documentation](https://git-scm.com/docs)
- [GitHub Docs](https://docs.github.com/)
