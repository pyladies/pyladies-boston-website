# PyLadies Chapter Website Contributing Guidelines

Thank you for your interest in contributing to the PyLadies Boston website! We welcome contributions from everyone. This guide will help you get started.

## Contribution Workflow

Follow these steps to contribute to the repository:

### Step 1: Forking the Repository

1. **Navigate to the repository** on GitHub: `https://github.com/pyladies/pyladies-boston-website`

2. **Click the "Fork" button** in the top right corner of the repository page

3. **Select your GitHub account** as the destination for the fork (if you have multiple accounts)

4. **Wait for the fork to complete** - GitHub will create a copy of the repository under your account

### Step 2: Cloning your fork to your local machine:

1. **Clone to your computer** On Terminal, run
   ```bash
   git clone https://github.com/YOUR_USERNAME/pyladies-boston-website.git
   cd pyladies-boston-website
   ```

2. **Add the original repository as an upstream remote** (recommended for keeping your fork synchronized):
   ```bash
   git remote add upstream https://github.com/pyladies/pyladies-boston-website.git
   ```

3. **Verify your remotes** are set up correctly:
   ```bash
   git remote -v
   ```
   
   You should see:
   - `origin` pointing to your fork
   - `upstream` pointing to the original repository

### Step 3: Branching

1. **Make sure you're on the default branch** (`gh-pages`):
   ```bash
   git checkout gh-pages
   ```

2. **Update your local default branch** with the latest changes from upstream:
   ```bash
   git fetch upstream
   git pull upstream gh-pages
   ```

3. **Create a new branch** for your changes. Use a descriptive branch name that describes what you're working on:
   ```bash
   git checkout -b feature/your-feature-name
   ```
   
   Branch naming conventions:
   - `feature/` - for new features or enhancements (e.g., `feature/add-event-calendar`)
   - `fix/` - for bug fixes (e.g., `fix/navigation-links`)
   - `update/` - for content updates (e.g., `update/organizer-bios`)
   - `docs/` - for documentation changes (e.g., `docs/update-contributing`)

4. **Verify you're on your new branch**:
   ```bash
   git branch
   ```
   
   The current branch (indicated by `*`) should be your newly created branch.

### Step 4: Making Changes

1. **Make your changes** to the relevant files:
   - `index.html` - Main page content, organizer information, chapter branding
   - `style.css` - Styling and layout
   - `images/` - Images and organizer photos
   - `CONTRIBUTING.md`, `README.md`, etc. - Documentation files

2. **Test your changes locally** by running a local web server:
   ```bash
   python3 -m http.server
   ```
   
   Or specify a port:
   ```bash
   python3 -m http.server 8000
   ```
   
   Then open your browser and navigate to `http://localhost:8000` to view the website.

3. **Verify your changes** look correct before committing.

4. **Stage your changes**:
   ```bash
   git add .
   ```
   
   Or stage specific files:
   ```bash
   git add path/to/file.html
   ```

5. **Commit your changes** with a clear, descriptive commit message:
   ```bash
   git commit -m "Add descriptive commit message about your changes"
   ```
   
   Commit message tips:
   - Use the imperative mood ("Add feature" not "Added feature")
   - Keep it concise but descriptive
   - Reference issue numbers if applicable: "Fix #123: Update navigation links"

6. **Push your branch** to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
   
   If this is the first push for this branch, set the upstream:
   ```bash
   git push -u origin feature/your-feature-name
   ```

### Step 5: Creating a Pull Request

1. **Navigate to your fork** on GitHub: `https://github.com/YOUR_USERNAME/pyladies-boston-website`

2. **You should see a banner** at the top saying "your-feature-name had recent pushes" with a "Compare & pull request" button. Click it.
   
   Alternatively:
   - Click on the "Pull requests" tab
   - Click "New pull request"
   - Select "compare across forks"
   - Set the base repository to `pyladies/pyladies-boston-website` and base branch to `gh-pages`
   - Set the head repository to `YOUR_USERNAME/pyladies-boston-website` and compare branch to `feature/your-feature-name`

3. **Fill out the pull request template** with:
   - **Summary**: A clear description of what your changes do and why
   - **Testing**: Check the box confirming you tested the website locally
   - **Screenshot**: If your changes affect the visual appearance, include a screenshot

4. **Review your changes** in the "Files changed" tab to make sure everything looks correct

5. **Click "Create pull request"** to submit your PR

6. **Wait for review** - Maintainers will review your PR and may request changes or ask questions

7. **Address feedback** if requested:
   - Make additional commits to your branch
   - Push the updates to your fork (the PR will automatically update)
   - Comment on the PR to let reviewers know you've made changes

### Step 6: Merging Changes

Once your pull request is approved:

1. **Maintainers will merge your PR** - You typically don't need to do anything at this point

2. **After merging**, you can clean up your local branch:
   ```bash
   git checkout gh-pages
   git pull upstream gh-pages
   git branch -d feature/your-feature-name
   ```

3. **Update your fork** to keep it in sync:
   ```bash
   git push origin gh-pages
   ```

4. **Delete the branch on GitHub** (if it hasn't been auto-deleted):
   - Go to your fork on GitHub
   - Navigate to the "Branches" page
   - Delete the merged branch

**Note**: If your PR needs to be rebased or updated before merging, maintainers will let you know. You may need to:
```bash
git fetch upstream
git rebase upstream/gh-pages
git push origin feature/your-feature-name --force-with-lease
```

### Pull Request Guidelines

- **Test your changes locally** before submitting a PR
- **Provide a clear description** of what your changes do
- **Include screenshots** if your changes affect the visual appearance
- **Keep PRs focused** - try to limit each PR to one feature or fix
- **Be responsive** to feedback from reviewers

### Types of Contributions

We welcome various types of contributions:

- **Content updates**: Updating organizer information, event listings, chapter details
- **Styling improvements**: CSS enhancements, responsive design improvements
- **Bug fixes**: Fixing broken links, layout issues, or other bugs
- **Accessibility improvements**: Making the site more accessible
- **Documentation**: Improving documentation or adding helpful comments

### Getting Help

If you need help or have questions:

- Ask in the [PyLadies Slack](https://slackin.pyladies.com) in the `#city-boston` channel
- Open an issue on GitHub for bugs or feature requests

Thank you for contributing to PyLadies Boston! 🐍
