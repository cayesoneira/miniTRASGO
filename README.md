# miniTRASGO Documentation

**This documentation is designed to be edited easily by anyone. No coding skills or prior technical knowledge are required!**

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

---

## Deployment Process: You Don't Have to Worry About It!

The deployment of the documentation is **handled exclusively by the repository owners**. If you contribute by editing files or submitting pull requests, you **do not need to worry about the deployment process**.

Once your edits are approved and merged into the repository, the documentation will be updated automatically by the maintainers. You can focus **only on contributing edits** and leave the deployment process to us!

---

## Deployment Details (For Reference Only)

The documentation is hosted at [http://nuc1.fis.ucm.es/minitrasgo](http://nuc1.fis.ucm.es/minitrasgo) and is updated automatically every hour. However, manual updates can be performed with the following steps:

### Connecting to the Deployment Server

1. **Configure SSH:** Add the following lines to your `~/.ssh/config` file:

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

2. **Connect to **``** through **``** as a tunnel:**

   ```bash
   ssh -J nuclab2 nuc1
   ```

3. **Deploy the updated site:**

   ```bash
   sudo /home/www/html/update-minitrasgo.sh
   ```

---

## Troubleshooting

If you encounter issues with the documentation, check the following:

- Ensure that markdown syntax is correctly formatted.
- Verify that new files are referenced in `mkdocs.yml`.
- Use `mkdocs serve` to test locally before submitting a pull request.

## Contact

For any questions, suggestions, or contributions, feel free to contact us or create an issue in the [GitHub repository](https://github.com/cayesoneira/miniTRASGO/issues).
