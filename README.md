# miniTRASGO Documentation

**Welcome to the miniTRASGO Cosmic Ray Telescope documentation!**  
This repository hosts the documentation and usage guide for the miniTRASGO project. The documentation is built using **mkdocs**, a simple and user-friendly tool that generates a webpage from markdown files. **No specific coding knowledge is required to contribute!**

---

## How to Edit the Documentation

Anyone with a GitHub account can contribute to the documentation by editing markdown files directly on GitHub. Here's how:

### Step 1: Fork the Repository (First-Time Contributors)

1. Go to the [miniTRASGO GitHub repository](https://github.com/cayesoneira/miniTRASGO).
2. Click the **Fork** button in the top-right corner. This creates a copy of the repository under your GitHub account.

### Step 2: Edit Files Online (Preferred Method)

1. In your forked repository, navigate to the `docs/` folder.
2. Find the markdown file you want to edit (e.g., `docs/home/motivation.md`).
3. Click the file to open it, then click the **pencil icon** (✏️) in the top-right corner to start editing.
4. Make your changes using **Markdown syntax** (simple text formatting).  
   - Need help with Markdown? Check out this [Markdown Guide](https://www.markdownguide.org/).

### Step 3: Propose Changes

1. After editing, scroll down to the "Commit changes" section.
2. Add a short description of your changes (e.g., "Fixed typo in motivation section").
3. Select **Create a new branch for this commit and start a pull request**.
4. Click **Propose changes**.

### Step 4: Create a Pull Request

1. Review your changes on the pull request page.
2. Add a title and description explaining your changes.
3. Click **Create pull request**.  
   - Your changes will be reviewed by the repository owners and merged if approved.

---

### Adding a New Page

To add a new page:
1. In your forked repository, click **Add file** in the `docs/` folder and create a new `.md` file (e.g., `docs/help/new-topic.md`).
2. Edit the `mkdocs.yml` file and add the new file under the appropriate section in the `nav` section. For example:
   ```yaml
   nav:
       - Troubleshooting:
           - help/index.md
           - help/new-topic.md
   ```
3. Follow the steps above to propose changes and create a pull request.

---

## Structure of the Documentation

The documentation is organized into folders and markdown files. Below is the hierarchy:

```
miniTRASGO/
│   mkdocs.yml  # Configuration file for mkdocs
│   README.md   # This file
│
├── docs/       # Main documentation directory
│   ├── index.md  # Home page
│   ├── home/
│   │   ├── motivation.md
│   │   ├── about.md
│   │   ├── publications.md
│   │   ├── contact.md
│   ├── design/
│   │   ├── index.md
│   │   ├── hardware.md
│   │   ├── environment.md
│   ├── operation/
│   │   ├── index.md
│   │   ├── configuration.md
│   │   ├── calibration.md
│   │   ├── measuring.md
│   │   ├── monitoring.md
│   ├── data/
│   │   ├── index.md
│   │   ├── shape.md
│   │   ├── dataflow.md
│   ├── tasks/
│   │   ├── index.md
│   │   ├── objectives.md
│   │   ├── to-understand.md
│   │   ├── notes.md
│   ├── help/
│   │   ├── index.md
```

---

## Deployment Process: For Repository Owners Only

The deployment of the documentation is **automatic using GitHub Actions**. Contributors do not need to worry about this step. The documentation is automatically updated with every hour push and hosted at [https://csoneira.github.io/miniTRASGO-documentation/](https://csoneira.github.io/miniTRASGO-documentation/).

---

## Troubleshooting

If you encounter issues while editing:
- Ensure the markdown syntax is correct.
- Verify that new files are referenced in the scheme in `mkdocs.yml`.
- If the online site does not update, contact the repository owners.

---

## Contact

For questions, suggestions, or contributions, feel free to:
- Create an issue in the [GitHub repository](https://github.com/csoneira/miniTRASGO-documentation/issues).
- Contact the repository owners directly.
