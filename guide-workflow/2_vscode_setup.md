# VS Code Setup

### Step 1 — Workspace

If you don't already have VS Code, you can [download](https://code.visualstudio.com/) it here. Create a new project on local drive and duplicate a folder template. Next, open up the folder in VS Code and save it as a workspace file in the root of the project folder.

  

### Step 2 — Extensions

Here's a list of all the extension that I use:

1. Python Extension Pack
2. Path Intellisense
3. Black Formatter
4. Juypter
5. GitHub Pull Requests
6. GitHub Actions
7. GitHub Copilot
8. GitHub Copilot Chat
9. Better Comments
10. Atom One Dark Theme
11. Material Icon Theme
12. (Lots of Azure Extensions)

  

### Step 3 — Styling

*   Lower left corner → ⚙️ Gear Icon → Themes
*   Color Theme: Atom One Dark Theme
*   File Icon Theme: Material Icon Theme

  

### Step 4 — Settings

*   You can tweak settings at the `User` of `Workspace` level
*   Workspace settings are unique to the current project and overwrite user settings.
*   Jupyter → Interactive Window → Text Editor → Execute Selection → Checked
*   Formatter → `@id:editor.defaultFormatter @lang:python python format` → Default Formatter → Black Formatter

  

### Step 5 — Running Notebooks

You can run Jupyter notebook in VS Code similar to how you would normally run notebooks.

  

### Step 6 — Running Python Code

When I am developing, I always run my Python code via interactive sessions to speed up my workflow. Please note that this does not work async functions or running servers (e.g., Flask or FastAPI)