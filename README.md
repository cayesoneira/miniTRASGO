# miniTRASGO Documentation

This repository hosts the documentation and usage guide for the miniTRASGO Cosmic Ray telescope. The documentation is deployed using `mkdocs`, a Python-based tool that generates HTML pages from a structured set of markdown files.

## Structure of the Documentation

The documentation follows a hierarchical structure as defined in the `mkdocs.yml` file. Below is an overview of the file structure:

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
│
├── assets/
│   ├── trasgo_logo.png  # Project logo
```

## How to Edit the Documentation

### Editing Directly on GitHub (Preferred Method)

Anyone with a GitHub account can propose changes to the documentation by following these steps:

1. **Navigate to the repository:** Go to [GitHub repository](https://github.com/cayesoneira/miniTRASGO).
2. **Locate the file:** In the `docs/` folder, find the markdown file you want to edit or add a new one.
3. **Edit the file:** Click the pencil icon on the top right to make modifications.
4. **Propose changes:** After editing, describe your changes and click **Propose Changes**.
5. **Create a Pull Request:** Click **Create Pull Request** so the changes can be reviewed and merged.

**To add a new page:**

- Create a new markdown file inside the `docs/` folder.
- Edit `mkdocs.yml` and add an entry in the `nav` section with the correct path.
- Follow steps 3-5 above to submit your changes.

### Editing Locally and Deploying

If you prefer working locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/cayesoneira/miniTRASGO.git
   cd miniTRASGO/
   ```
2. Install dependencies:
   ```bash
   pip install mkdocs mkdocs-material
   ```
3. Edit or create markdown files in the `docs/` folder.
4. Preview the site locally:
   ```bash
   mkdocs serve
   ```
   This will start a local server at `http://127.0.0.1:8000/` where you can preview changes.
5. Deploy using GitHub Pages:

   &#x20;
   ```bash
   mkdocs gh-deploy
   ```
   This will update the online documentation (if using GitHub Pages as a deployment method).

## Deploying to a Custom URL (Preferred Method)

The documentation is hosted at [http://nuc1.fis.ucm.es/minitrasgo](http://nuc1.fis.ucm.es/minitrasgo) and is updated automatically every hour. However, manual updates can be performed with the following steps:

### Connecting to the Deployment Server

1. **Configure SSH:**
   Add the following lines to your `~/.ssh/config` file:

   ```bash
   Host nuclab2
       HostName nuclab2.fis.ucm.es
       User petgfn
       PubkeyAcceptedAlgorithms +ssh-rsa
       HostkeyAlgorithms +ssh-rsa
       KexAlgorithms +diffie-hellman-group1-sha1

   Host nuc1
       Hostname nuc1.fis.ucm.es
       User petgfn
   ```

2. **Connect to ****`nuc1`**** through ****`nuclab2`**** as a tunnel:**

   ```bash
   ssh -J nuclab2 nuc1
   ```

3. **Deploy the updated site:**

   ```bash
   sudo /home/www/html/update-minitrasgo.sh
   ```

## Troubleshooting

If you encounter issues with the documentation, check the following:

- Ensure that markdown syntax is correctly formatted.
- Verify that new files are referenced in `mkdocs.yml`.
- Use `mkdocs serve` to test locally before deploying.
- If the online site does not update, manually execute the update script as described above.

## Contact

For any questions, suggestions, or contributions, feel free to contact us or create an issue in the [GitHub repository](https://github.com/cayesoneira/miniTRASGO/issues).

